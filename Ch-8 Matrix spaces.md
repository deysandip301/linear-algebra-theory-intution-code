
# Column space of a matrix
- The *column space* of a matrix is the subspace spanned by all columns of that matrix.
- It is indicated by C(A.
- $C(A) = \{\beta_1a_1 + ...\beta_na_n,\ \ \beta \in R\}$
- $C(A) = span(a_1,...,a_n)$ 
- If the dimensionality of the column space is same as the number of columns, then then columns forms a basis.

# The column space of A and $AA^T$ 
- A and $AA^T$ has the same column space.

# Determining whether v $\in$ C(A)
- we can solve a formula Ax = v, where x is the weight vectors.

# Row space of a matrix
- Indicated by R(A).
- same concept as column space, except it refers to the subspace spanned by the rows.
- R(A) = $C(A^T)$ 
- here we do $x^TA = v^T$

# Row space of A and $A^TA$
- R(A) = R($A^TA$)

# Null space of a matrix
- Indicated by N(A) and is defined as the subspace containing all of the vectors that satisfy the equation : Ay = 0
- This means that there is a linear combination of the columns in matrix A that produces a column vector of zeros, and the elements of vector y specify those weightings.
- two cases : 
	1. when y = 0
	2. when not all elements in y are zero, and the specific numbers in y and A align in just the right way that the matrix-vector product is the zeros vector. This is the non-trivial case.
- N(A) = $\{\lambda y\ |\ Ay=0,\ \ lambda\ \in\ R\}\ -\ \{y=0\}$ 
- Sometimes a matrix can have no null space : example -> [ [ 1, 2], [ 4, 7] ]
- full-rank square matrices and full-column-rank matrices necessarily have an empty null space, whereas reduced-rank and reduced-column-rank matrices necessarily have a non-empty null space.

## Left-null space 
- There is a complementary space to the null, called the left-null space, which is the same concept but with a row vector on the left of the matrix instead of a column vector on the right of the matrix. The resulting zeros vector is also a row vector. 
- $y^TA = 0^T$
- it can be thought as the "regular" null space of the matrix transpose.

# Geometric interpretation of the null space
- It squishes the ambient-spaced vector to a lower dimension. (transformation)
- Ay = 0 -> y is in the null space of A.

# Orthogonal subspaces, orthogonal complements
- If a pair of vectors is orthogonal, then any scalar-vector multiplication will also be orthogonal.
- $v \perp w\ =>\ \sigma v\ \perp \ \lambda w,\ \ \sigma, \lambda\ \in\ R$ 
- Subspaces S and M are orthogonal subspaces if $\forall v \in S\ and\ \forall w\ \in \ M, \ \  v\ \perp\ w$ 

## Orthogonal complements
- The idea is that any ambient space $R^N$ can be decomposed into two subspaces W and V such that $W \bigcup V$ spans all of $R^N$ and $W\ \perp \ V$ .
# Orthogonality of the matrix spaces
- Orthogonality of the column space and the left-null space : 
	- column space and the left-null space are orthogonal.
	- C(A) $\bigcup$ N($A^T$)   <=>   $R^M$ 
	- For a given M x N matrix, every vector in $R^M$ is either in the column space or in the left-null space. No vector can be in both except for the trivial zeros vector.
- Orthogonality of the row space and the null space :
	- As with the column and left-null spaces, the row space and null space are orthogonal complements that together span all of $R^N$.

# Dimensionalities of matrix spaces 
- The row space lives in ambient $R^N$ but can span a lower-dimensional subspace depending on the elements in the matrix. The orthogonal complement--the null space--fills up whatever directions in $R^N$ are not already spanned by the row space. If the matrix is full-row rank, then the row space already spans all of $R^N$ and therefore the null space must be empty.
- $C(A) \cup N(A^T)$ => $R^M$
- $R(A) \cup N(A)$ => $R^N$
- $dim(C(A)) + dim(N(A^T)) = M$
- $dim(R(A))+dim(N(A))=N$
- $rank(A) = dim(C(A))+dim(R(A))$ 

# More on Ax = b and Ay = 0
- Ax = b
	- **does it have a solution ?** --> The equation has an exact solution when b is in the column space of A. In that case, the coefficients in vector x tell you that weightings of the columns in A in order to produce vector b. If vector b is not in the column space of matrix A, then that leads to the second question:
	- **What is the closest approximation to an exact solution ?** --> This changes the equation to $Ax = \hat{b}$ , where x and $\hat{b}$ are selected such that (1) $\hat{b}$ is in the column space of A and x are the coefficients, and (2) $\hat{b}$ is as close as possible to the original **b** . This is obtained through the "least squares solution," which is the backbone of statistics, model fitting, machine learning, and many other areas of applied mathematics.
- Ay = 0
	- people are more interested in the shifted version of this matrix, expressed as ($A-\lambda I)y = 0$.
	- The solution to this equation (vector y) is called an eigenvector of the matrix, and $\lambda$ is its associated eigenvalue. Eigenvectors reveal directions in the matrix that have special properties, such as robustness to geometric transformations or maximizing covariance in a dataset.
	- In different contexts, the solution to $Ay = 0$ is called Principal Components Analysis, generalized eigendecomposition, singular value decomposition, Fisher linear discriminant analysis, Rayleigh quotient, and many other names.