# assembly-masm-8086-display-float-in-decimal

This code displays float values in decimal notation.

One of the problems of 8086 masm assembly is that, the call writefloat function only displays in the scientific/exponential notation. Here I have written a code which can display float values upto three decimal places.

the code can be modified to display to more decimal places. for example if we need to display upwards of 4 decimal places, we can change the procedure so that instead of multiplying and dividing by 1000 we could use 10000 and give ecx(loop counter) value of 4 instead of 3.
