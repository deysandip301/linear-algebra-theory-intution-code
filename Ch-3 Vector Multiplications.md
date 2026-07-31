
# Vector dot Product : Algebra
- inner product (or) scalar product.
- multiply the corresponding elements and then sum them up.
- $\alpha = a.b = <a,b> = a^Tb = \sum_{i=1}^Na_ib_i$ 
-  You can compute the dot product between a vector and itself, that works out to be sum of squared elements, and is denoted by $|| a||^2$ . The term ||a|| is called *magnitude*, *length* or *norm* of vector **a**. $a^Ta = ||a|| = \sum_{i-1}^na_ia_i = \sum_{i=1}^na_i^2$ 
- Properties of dot product : 
	- Associative property : 
		- $\gamma(u^Tv) = (\gamma u^T)v = u^T(\gamma v) = (u^Tv)\gamma$  {$\gamma$ is a scalar}
		- vector dot product does not obey the associative property.
	- Commutative property :  
		- $a^Tb = b^Ta$ 
	- Distributive property : 
		- $w^T(u+v) = w^Tu + w^Tv$
	- Cauchy-Schwarz inequality : 
		- $|v^Tw| \le ||v||\ ||w||$ 

# Vector dot product : Geometry
- Geometrically, the dot product is the cosine of the angle between the two vectors, times the lengths of the two vectors.
- $a^Tb = ||a||\ ||b||\ cos(\theta_{ab})$ 
- Signs of the dot product is determined exclusively by the angle between the two vectors.

# Linear weighted combination
- It simply means scalar-vector multiplication and addition : Take some set of vectors, multiply each vector by any scalar, and add then to produce a single vector.
- $w = \lambda_1 v_1 + \lambda_2 v_2 + ... + \lambda_n v_n$ {assumed all vectors have same dimensionality}

# The outer product 
- outer product : $vw^T(m \times n)$ where v = M-element column vector and w is and N-element column vector.
- The outer product : $(vw^T)_{i,j} = v_iw_j$ 

# Element-wise (Hadamard) vector product
- It involves multiplying each corresponding element in the two vectors. 
- The resulting product vector is the same size as the two multiplying vectors. and thus, Hadamard multiplication is defined only for two vectors that have the same number of elements.
- $c = a \cdot b = [a_1b_1\ \ a_2b_2\ ...\ a_nb_n]$ 

# Cross product 
- $||a \times b|| = ||a||\ ||b||\ sin(\theta_{ab})$ 
- The result of the cross product of two vectors is orthogonal to the plane spanned by the two vectors.

# Unit vectors
- || v || = 1
- $\hat{v} = \frac{1}{||v||}v = \frac{1}{\sum_{i=1}^nv_i^2}v$ 