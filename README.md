# taylor-polynomial-of-sine-function
Find and classify the real roots of a Taylor polynomial of sine function

In the first section, we’re trying to find all roots of the Taylor Polynomials. With an input n, we create a 1 x n matrix “a” that consists of zero terms. The matrix then is filled by the terms that are computed by the formula of Taylor Polynomials. Flipping the updated matrix “a” in the left-right direction, we have matrix “p”. Next, we create a new matrix “A” that has one more column than “p” and copy the elements in matrix “p” into new matrix “A” completely corresponding to same row and same column for every element. Then, in order to satisfy the coefficients of every Taylor Polynomials and to satisfy the rule of command “roots”, let the last second column’s element to be 1 for matrix “A”. Now, the matrix “A” presents all possible coefficients of the Taylor Polynomials of sin(x). 

In the second section, we decide to process the imaginary roots first. The size of the matrix “A” is displayed as [x, y]. Next, we take the roots of “A” as a matrix called “solution_temp” and choose only the imaginary value of roots to be a matrix “imaginary” in the size of [x1, y1]. In this matrix, if there is any element that’s not equal to 0, then the corresponding element in the matrix called “solution_temp” would be 0 (do not consider real value solution 0 now). After putting on the display, all imaginary roots are cleared and become one single, zero root. And we continued coding for nonzero roots in the next section. Attention: In order to avoid the all 0 roots and avoid error command, we use “if” command to divided into two situations.

In the third section, we’re attempting to process the real roots. For the valid real roots existing in matrix “solution_temp”, we locate the nonzero roots and put their number of position row into the matrix “v”. Then, we utilize the matrix “v” to stand the non-zero roots out of the original roots, naming the matrix of real roots as “solution” (including real root 0). Now, we get the size of matrix “solution” in [x2, y2], later starting the “RE” (numbers of regular roots) and “IRRE” (number of irregular roots) as 0s and two values “r” and “s” as 1. By applying the mathematical observation | sin(x) | <= sin d (0.1), we find the valid (regular) roots that lie within the distance 0.1 of sin(x) = 0. Thereby, the roots are divided into either regular roots or irregular roots. And the outcomes are preserved in the matrix “regular”, “irregular”. 

In the final section, we display the final version of output. We apply “num2str”, which converts numbers to the string representations. When the numbers of irregular roots and regular roots are not equal to 0, both outcomes are displayed, including how many and what values. We dp this so as to avoid an error output when the matrix of irregular roots disappears. Otherwise, having 0 irregular root would be shown and the certain number(s) and the corresponding value(s) of regular root(s) still present. A key fact to mention is that no matter what value of n is, there is always a regular root that’s 0 as found above.

Conclusively, the output for n=4 is shown (TEST):
The number of irregular roots is 2, the irregular roots are -4.9632      4.9632.
The number of regular roots is 3, the irregular roots are -3.1487      3.14870.      
