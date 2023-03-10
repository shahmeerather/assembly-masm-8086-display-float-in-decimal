# assembly-masm-8086-display-float-in-decimal

This code displays float values in decimal notation.

One of the problems of 8086 masm assembly is that, the call writefloat function only displays in the scientific/exponential notation. Here I have written a code which can display float values upto three decimal places.

the code can be modified to display to more decimal places. for example if we need to display upwards of 4 decimal places, we can change the procedure so that instead of multiplying and dividing by 1000 we could use 10000 and give ecx(loop counter) value of 4 instead of 3.

---- How does this code work ?----

The displayfloat procedure takes a floating-point number and displays it on the screen in decimal notation.

To do this, it first calculates the integer part of the floating-point number and displays it on the screen using the writeint procedure. Then it multiplies the floating-point number by 1000 and converts it to an integer, which gives the number of thousandths in the decimal part. It then displays a dot '.' on the screen.

Next, the procedure subtracts the integer part and the thousandths from the floating-point number to get the remaining decimal part. It then extracts the digits of the decimal part, starting from the tenths place and moving to the right, using repeated divisions by 10.

For each digit, the procedure pushes it onto a stack and continues to the next digit until it has extracted all three decimal digits. Finally, it pops each digit off the stack one by one and displays it on the screen using the writedec procedure.

So, in simpler terms, the procedure takes a number and separates it into an integer part and a decimal part. It displays the integer part on the screen, followed by a dot, and then displays the decimal part digit by digit.
