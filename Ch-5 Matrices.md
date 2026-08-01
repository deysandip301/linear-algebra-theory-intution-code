
# Interpretations and uses of matrices
- set of column vectors standing next to each other (or) set of row vectors stacked on top of each other.

# Matrix dimensionalities
- Matrix can have different interpretations of dimensionality, depending on the application and the information stored in the matrix .The possible dimensionalities of an M x N matrix containing real-valued numbers include:
	- $R^{M\times N}$ 
	- $R^{MN}$ , if each matrix element is its own dimension.
	- $R^M$ , if the matrix is conceptualized as a series of column vectors.
	- $R^N$, if the matrix is conceptualized as a stack of row vectors.


# Matrix zoology
- **Square or rectangular** 
	- A square matrix is a matrix that has the same number of rows as columns, thus an N x N matrix or M x N if M = N.
	- A non-square matrix is called rectangular matrix.
- **Symmetric**
	- A matrix is symmetric if it is "mirrored" across the diagonal, meaning the upper-right of the matrix is a flipped version of the lower-left of the matrix. Formally, matrix A is symmetric if it equals its transpose 
- **Skew-symmetric**
	- A skew-symmetric matrix is a matrix where the lower-triangle is the sign-flipped version of the upper-triangle. the diagonal elements should be zero.
- **Identity**
	- The identity matrix is the matrix equivalent of the number 1, all the diagonal elements are 1 and all other elements are 0. It must be square matrix. (more appropriate term would be "multiplicative identity matrix")
- **zeros**
	- All the elements of the matrix are 0.
- **$A^TA$**
	- It is a square matrix, even if A is rectangular.
	- It is symmetric, even if A isn't.
	- It is full-rank if A is full column-rank.
	- It is invertible if A is full column-rank.
	- It has the same row space as A.
	- It has orthogonal eigenvectors.
	- It is positive (semi)definite.
	- It has non-negative, real-valued eigenvalues.
	- It is called a "covariance matrix" if A is a data matrix.
	- It often looks pretty : )
	- These same properties hold for **$AA^T$** as well.
- **Diagonal**
	- values are only present in diagonals.
	- Diagonal matrices can be rectangular.
	- The opposite of diagonal matrix is called hollow matrix. A hollow matrix has all zeros on the diagonal, while the off-diagonal elements may be non-zero.
- **Augmented**
	- An augmented matrix is the result of concatenating two or more matrices column-wise. Two matrices can be augmented only if they have the same number of rows;
- **Triangular**
	- Triangular matrices are half-way between a diagonal matrix and a full matrix. It comes in two form upper-triangular and lower-triangular.
- **Dense and sparse**
	- A matrix in which most or all matrix elements are non-zero is called a dense matrix (sometimes also called a "full matrix").
	- A sparse matrix is one that contains mostly zeros and a relatively small number of non-zero elements. They are very computationally efficient.
- **Orthogonal**
	- A matrix is called orthogonal if it satisfies the following two criteria : 
		1. All of its columns are pairwise orthogonal. That means the dot product between any two columns is exactly 0.
		2. Each column i has $||\ Q_i\ ||\ =\ 1$ , in other words, each column is unit magnitude. 
	- dot product of $Q_i,Q_j$ = 1 if i=j, and dot product of $Q_i, Q_j$ = 0 if i $\ne$ j.
	- A more compact way of writing this is : $Q^TQ = I$
- **Toeplitz**
	- Toeplitz and Hankel matrices are closely related to each other. Both involve creating new rows of a matrix as systematic rearrangements of elements in previous rows. One of the remarkable properties of Toeplitz and Hankel matrices is that they can have rank $r > 1$ even if they are created from a rank r = 1 vector.
	- In a Toeplitz matrix, all diagonals contain the same element. 
- **Hankel**
	- A Hankel matrix is kind of like a rotated Toeplitz matrix.
	- Creating a Hankel matrix from a vector : $Y_{i,j} = x_{i+j-1}$ 

# Matrix addition and Subtraction
- size of both matrices should be same.
- element wise addition and subtraction.
- Matrix addition is Commutative.

# Scalar-matrix multiplication
- multiplying each of the elements by the scalar

#  "Shifting" a matrix
- To "shift" a matrix means to add to the matrix a multiple of the identity matrix. 
- $\tilde{A} = A + \lambda I\ ,\ \ A\ \in \ R^{M \times M},\ \lambda\ \in\ R$
- Shifting is applied only to square matrices.
- Only the diagonal elements are affected.
- When $\lambda$ is close to zero, then $\tilde{A}$ is really similar to A. Indeed, when $\lambda = 0$, then $\tilde{A} = A$. In practical applications, $\lambda$ is often selected to be as small as possible while large enough to satisfy other constraints.

# Diagonal and trace
- The diagonal elements of a matrix can be extracted and placed into a vector.
- **Trace :**
	- The trace is an operation that produces a single number from a square matrix. It is indicated as tr(A) and is defined as the sum of all diagonal elements of a matrix.
	- $tr(A) = \sum_{i=1}^Ma_{i,j}$ 
	- The trace is defined only for square matrices.