# "Standard" matrix multiplication
- Matrix multiplication is not commutative.
- Matrix multiplication is valid only when the two "inner dimensions" match, and the size of the resulting product matrix is given by the "outer dimensions"
- **The "element perspective"
	- Each element $c_{i,j}$ in AB = C is dot product between the $i^{th}$ row in A and $j^{th}$ column in B.
- **The "layer perspective"**
	- It involves conceptualizing the product matrix as a series of layers, or "sheets", that are summed together. This is implemented by creating outer products from the columns of A and the rows of B, and then summing those outer products together.
- **The "column" perspective**
	- All matrices are thought of as sets of column vectors. Then the product matrix is created one column at a time.
	- The first column in the product matrix is a linear weighted combination of all columns in the left matrix, where the weights are defined by the elements in the first column of the right matrix. Similar for all the columns in the product matrix.
- **The "row" perspective**
	- It is the same concept as the column perspective but here we take rows instead of columns.
	- Each row in the product matrix is the weighted sum of all rows in the right matrix, where the weights are given by the elements in each row of the left matrix. The top row of the product matrix is created by summing together the two rows of the right matrix , but each row is weighted according to the corresponding element of the top row of the left matrix. Similar for all the other rows.

# Multiplication and equations
- keep in mind that matrix multiplication is not commutative while simplifying equations.

# Matrix multiplication with a diagonal matrix
- There is a special property of multiplication when one matrix is a diagonal matrix and the other is a dense matrix : 
	- Pre-multiplication by a diagonal matrix scales the rows of the right matrix by the diagonal elements.
	- Post-multiplication by a diagonal matrix scales the columns of the left matrix by the diagonal elements.

# LIVE EVIL (a.k.a. order of operations)
- An operation applied to multiplied matrices gets applied to each matrix individually but in reverse order.
- $(A...B)^T = B^T....A^T$ 
- LIVE EVIL rule applies to other operations as well, such as the matrix inverse.

# Matrix-vector multiplication
- Three observations : 
	1. bA is not defined (assuming b is a column vector) 
	2. If A is rectangular, then either $b^TA$ or AB is undefined (depending on the sizes, but they can't both be valid).
	3. Ab $\ne$ $b^TA$ even when both are valid operations.
- symmetric matrix times a vector 
	- if $A=A^T$ then $Ab = (b^TA)^T$ 

# Creating symmetric matrices
- Additive : 
	- $C = \frac{1}{2}(A^T + A)$ 
	- This method is valid only for square matrices.
- Multiplicative method : 
	- This involves multiplying a matrix by its transpose.
	- $A^TA$ is square as well as symmetric matrix.

# Multiplication of two symmetric matrices
- In general, the product of two symmetric matrices is not a symmetric matrix. There are exceptions to this rule, like 2x2 case with constant diagonals, or if one of the matrices is the identity or zeros matrix.

# Element-wise (Hadamard) multiplication
- Hadamard multiplication involves multiplying each element of one matrix by the corresponding element in the other matrix.

# Frobenius dot product
- To compute the Frobenius dot product, you first vectorize the two matrices and then compute their dot product as you would for regular vectors.
- Vectorizing a matrix means concatenating all of the columns in a matrix to product a single column vector.
- Frobenius dot product can also be written as : $<A,B>_F = tr(A^TB)$ 

# Matrix norms
- Frobenius matrix norm (l2 norm) : $||A||_F = \sqrt{\sum_{i=1}^m \sum_{j=1}^n(a_{i,j})^2}$ 
- Euclidian distance between two matrices : $||A-B||_F = \sqrt{\sum_{i,j}(a_{i,j}-b_{i,j})^2}$
- matrix p-norm : $||A||_p = (\sum_{i=1}^M \sum_{j=1}^N |a_{ij}|^p)^{\frac{1}{p}}$ 

# Matrix division
- $\frac{A}{B}$ is equivalent to $AB^{-1}$ 

