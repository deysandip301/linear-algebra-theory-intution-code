
# Six things to know about matrix rank
1. The rank of the matrix is indicated by the letter r or by rank(A), and is a non-negative integer. Only zeros matrix can have rank = 0.
2. The maximum possible rank of an M x N matrix is the smaller of M or N.
3. Rank is a property of the entire matrix; it doesn't make sense to talk about the rank of the columns of the matrix, or the rank of the rows of the matrix.
4. terminology for full rank matrices : 
	1. square : rank(MxM) = M --> Full rank
	2. vertical : rank(M > N) = N --> Full column rank
	3. horizontal : rank (M < N) --> Full row rank
5. The rank indicates the number of dimensions of *information* contained in the matrix.
6. **rank of a matrix is the largest number of columns that can form a linearly independent set.** This is exactly the same as **the largest number of rows that can form a linearly independent set.**

# Interpretations of matrix rank
- Algebraic interpretation : 
	- If you think of a matrix as comprising a set of vectors, then the rank of the matrix corresponds to the largest number of vectors that can form a linearly independent set.
- Geometric interpretation : 
	- Rank is the dimensionality of the subspace spanned by the columns (or the rows) of the matrix. This is not necessarily the same as the ambient dimensionality of the space containing the matrix.

# Computing matrix rank 
1. Count the largest number of columns (or rows) that can form a linearly independent set. This involves a bit of trial-and-error and a bit of educated guessing. (can follow the same tips for determining linear independence in Chapter 4)
2. Count the number of pivots in the echelon or row-reduced echelon form of the matrix.
3. Count the number of nonzero singular values from a singular value decomposition of the matrix.

# Rank and scalar multiplication
- scalar multiplication has no effect on the rank of a matrix, with one exception when the scalar is 0.

# Rank of added matrices 
- $rank(A+B) \le rank(A) + rank(B)$ 

# Rank of multiplied matrices
- $rank(AB) \le min\{rank(A),rank(B)\}$ 

# Rank of $A,\ A^T,\ A^TA,\ and\ AA^T$ 
- all these four matrices have the same rank.

# Rank of random matrices
- *Almost* every random matrices have maximum possible rank. because it's very unlikely to have linear dependency in random numbers.

# Full-rank matrices via "shifting"
- add a multiple of the identity matrix ($A +\lambda I = \tilde{A}$), which adds a small quantity to the diagonal elements without changing the off-diagonal elements.
- In context of statistics and machine learning, "shifting" is also called *regularization* or *matrix smoothing*.

# Rank and span
- How to find if a vector is in the span of a set of vectors.
	1. Put the vectors from the set S into a matrix S.
	2. Compute the rank of S. call that rank $r_1$.
	3. Augment S by v, thus creating $S_v = S | v$.
	4. Compute the rank of $S_v$. Call that rank $r_2$
		1. if $r_2 > r_1$ : then v is not in the span of S.
		2. if $r_1 = r_2$ : then v is in the span of S.
		3. else check your math or code for a mistake : (

