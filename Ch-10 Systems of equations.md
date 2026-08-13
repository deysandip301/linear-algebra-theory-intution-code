
# Matrices representing systems of equations
1. **Variables :** These are the unknowns that you want to solve for. They are typically labeled x,y,...,or $x_1$, $x_2$,, ...
2. **Coefficients :** These are the numbers that multiply the variables. There is one coefficient per variable. If the variable is sitting by itself, then the coefficient is 1; if the variable is not present, then the coefficient is 0.
3. **Constants :** These are the numbers that do not multiply variables. Every equation has one constant (which might be 0).

###  Components to matrices
1. The coefficients go into the coefficients matrix, with columns corresponding to variables and with rows corresponding to equations.
2. The variables go into a column vector that right-multiplies the coefficients matrix. Importantly, the order of variables in this vector must match the order of variables in the columns of the matrix.
3. The coefficients matrix and variables vector are on the left-hand side of the equation. The constants go into a column vector on the right-hand side of the equation, with the number of elements of the vector corresponding to the number of equations. Of courses, the $n^{th}$ element in the constants vector must correspond to the $n^{th}$ equation in the coefficients matrix.
4. Often represented as Ax = b.

# Row reduction, echelon form, and pivots
- **Echelon form :** A matrix is in its echelon form when the following two criteria are satisfied:
	1. The first non-zero number in each row is to the right of the first non-zero numbers in the rows above.
	2. Rows of all zeros are below rows with at least one non-zero element.
-  **Row reduction :** The process of applying linear transformation to the rows to reduce it to echelon form. Below are few tips.
	1. Divide an entire row by a scalar to make the left-most non-zero number equal 1.
	2. Multiply a row by a scalar to facilitate eliminating elements.
	3. Multiply a row by a scalar to get rid of difficult fractions.
- **Keeping track of row reduction :** 
	- If we do some row reduction in a matrix A, it is same as doing the same row reduction in an identity matrix and multiplying it with the actual matrix.
	- E = RA => where E : the row-reduced matrix ; A : the row-reduced identity matrix.
- **Exchanging rows in a matrix :**
	- It is also known as permutation.
	- Sometimes needed in row-reduction to convert to echelon form.
- **Pivots :**
	- After putting the matrix into echelon form, the pivots are the left-most non-zero elements in each row.
- **Pivot-counting and rank :**
	- The rank of a matrix is the number of pivots in the echelon form of that matrix.
	- row-reduction reveals a basis set for the row space. You simply take all the non-zeros rows.
- **Non-uniqueness of the echelon form :**
	- The echelon form of a matrix is non-unique.

# Gaussian elimination
1. Augment the coefficients matrix by the constants vector.
2. Row reduce to echelon form.
3. Apply back-substitution to solve the system.

# Row-reduced echelon form
- The goal here is to continue with row reduction after converting a matrix to its echelon form, until it becomes a matrix where all pivots have a value of 1, and each pivot is the only non-zero element in its column.
- Below is the procedure to do this : 
	1. Transform a matrix into its echelon form as described earlier.
	2. For each row that contains a pivot:
		1. Divide that row by its pivot, which converts the pivot into the number 1.
		2. Apply row-reduction but work upwards instead of downwards. That is, use row-reduction to produce zeros in the elements above the pivot. Continue "upwards row-reduction" until the pivot is the only non-zero element in its column.
- Each matrix has a unique RREF.

# Gauss-Jordan elimination
1. Augment the coefficients matrix by the constants vector.
2. Row reduce to row-reduced echelon form.
3. You have the solution now bro.

# Possibilities of solution
- There are three possibilities :
	1. the system has no solutions.
	2. The system has exactly one unique solution.
	3. The system has an infinite number of solutions.
- **No solution :**
	- There are some mathematical impossibility.
- **Unique solution :**
	- Just use Gaussian elimination.
- **Infinite solutions :**
	- There is some zeros column.
	- The variables are dependent.

# Matrix spaces after row reduction
- Row space does not change by row reduction but column space may changes.
- dimensionality of row space or column space remains same.
- The column space can change. This can happen when the column space occupies a lower-dimensional subspace of the ambient space in which the columns live. The reason is that row reduction involves changing entire rows at a time; individual elements of a column will change while other elements in the same column stay the same.