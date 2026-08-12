
# Complex numbers and C
- solution to the equation $x^2+1=0$ => x = $\pm \sqrt{-1}$ 
- There are two parts of a complex number => "real" and "imaginary"
- We can get complex-valued eigenvalues from real-valued matrices sometimes.

# What are complex numbers ?
- Can be represented in two-dimensional plane where there are two axis, the horizontal axis is often called the *real axis* (often abbreviated Re) and the vertical axis is called the *imaginary axis* (often abbreviated Im).
- **Complex vectors and complex matrices** are just vectors and matrices that contain some non-zero imaginary values for some entries.

# The complex conjugate
- The *conjugate* of a complex number is simply that number with the sign of the imaginary part flipped. 
- It is indicated using ($\bar{z}$) or using a superscripted asterisk (z*).
- **Complex conjugate pairs** : A complex conjugate pair is a complex number and its conjugate, together forever, just like penguins.

# The Hermitian and complex dot products
- The Hermitian transpose, often called simply the Hermitian, is a fancy term for a conjugate-and-transpose operation.
- It is indicated with a superscripted H instead of a T ($v^H$).
- **Dot product with complex vectors** is exactly the same as the dot product with real-valued vectors: element-wise multiply and sum. However, in nearly all cases, the "regular" dot product is replaced with the Hermitian dot product, which simply means to implement the dot product as $z^Hw$ instead of $z^Tw$.

# Special complex matrices
- **Hermitian matrices** : 
	- A Hermitian matrix is the complex-valued equivalent of something between a symmetric matrix ($A=A^T$) and a skew-symmetric matrix ($A=-A^T$). A Hermitian matrix is defined as $A=A^H$ . Thus, the magnitudes of the real and imaginary parts are the same, but the signs of the imaginary parts are swapped.
- **Unitary matrix :**
	- For real-valued matrices, and "orthogonal matrix" is one for which its transpose is its inverse; thus, multiplying the matrix by its transpose gives the identity matrix ($QQ^T=I$). Another way to phrase this is that each column in an orthogonal matrix is orthogonal with each other column, and that each columns has unit magnitude.
	- A complex-valued matrix that has such properties is called a unitary matrix.