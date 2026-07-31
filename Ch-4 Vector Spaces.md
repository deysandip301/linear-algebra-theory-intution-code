# Dimensions and fields in linear algebra
- **Dimension** : 
	- Algebraically, the dimensionality of a vector is simply the number of elements in the vector.
	- Geometrically, the dimensionality of a vector is the number of coordinate axes in which that vector exists.
- Fields : 
	- A field in mathematics is a set of numbers for which the basic arithmetic operations (addition, subtraction, multiplication, division) are defined.
	- Examples : R (real numbers), C (Complex numbers) , Q (rational numbers), Z (integers).

# Vector spaces 
- A vector space refers to any set of objects for which addition and scalar multiplication are defined.
- the following requirements : 
	- Additive inverse : $v + (-v) = 0$
	- Associativity : $(v+w)+u = v +(w+u)$
	- Commutativity : $v + w = w + v$
	- Additive identity : $v + 0 = v$
	- Multiplicative identity : $v1 = v$
	- Distributivity : $(\alpha + \beta)(v+w) = \alpha v + \alpha w + \beta v + \beta w$

# Subspaces and ambient spaces
- Geometry : 
	- A subspace is the set of all points that you can reach by stretching and combining a collection of vectors(not necessarily basis vectors) (that is addition and scalar multiplication).
- Ambient dimensionality : 
	- ambient space : the main surrounding vector space that contains a smaller subset of subspace of interest.
	- There could be infinite subspaces within an ambient space with dimensionality more than 1.
	- There is only N+1 subspace dimensionalities are possible with an N-dimensional ambient space.
- Algebra
	- A subspace is the set of all points that can be created by all possible linear combinations of vector-scalar multiplication for a given set of vectors in $R^N$ and all scalars in R.
	- In words, a subspace is the set of all points that satisfies the following conditions : 
		- Closed under addition and scalar multiplication.
		- Contains the zeros vector $0$.
	- $\forall\ v,w\ \in\ V,\ \forall\ \lambda,\ \alpha\ \in\ R;\ \lambda v + \alpha w\ \in\ V$ 

# Subsets
- A subset, in contrast to a subspace, is a region in space that can have boundaries instead of extending to infinity, and it need not include the origin.

# Span
- Geometry 
	- Span is the total space that can be reached by any linear combination of a some vectors.
- Algebra
	- The span of a set of vectors is the set of all points that can be obtained by any linear weighted combination of those vectors.
	- $span(\{v_1,....,v_n\}) = \{\alpha_1v_1+...+\alpha_nv_n, \alpha \in R\}$ 

# Linear independence
- It is defined for a set of vectors. Neither a single vector, nor a vector within a set, is independent.
- Geometry : 
	- A set of vectors is independent if the dimensionality of the subspace spanned by that set of vectors is equal to the number of vectors in that set.
- Algebra : 
	- A set of vectors is dependent if at least one vector in the set can be expressed as a linear weighted combination of the other vectors in that set.
	- Linear dependence : $0 = \lambda_1v_1 + \lambda_2v_2 +....+\lambda_nv_n,\ \ \ \lambda\ \in\ R$  
- Any set of M > N vectors in $R^N$ is necessarily linearly dependent.
- Any set of $M \le N$ vectors in $R^N$ could be linearly independent. 

# Basis
- A basis is the combination of span and independence : A set of vectors {$v_1,v_2,...,v_n$} forms a basis for some subspace of $R^N$ if it (1) spans the subspace and (2) is an independent set of vectors.
- There could be infinitely many bases for a subspace.