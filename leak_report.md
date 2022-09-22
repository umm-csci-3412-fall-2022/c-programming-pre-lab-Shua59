# Leak report

There are two leaks in check_whitespace:
 - The 'strip' function creates a constant 'result' that never gets free of its assingnment, but is also returned by the function. 
 - The 'is_clean' function creates a constant 'cleaned' that never gets free of its assignment.

With respect to the 'strip' function, the result cannot get rid of it's assignment in it's own function, because it is returned to 
wherever the strip fuction is called. Therefore, to fix this leak, we need to free the result variable after the 'strip' function is
called. It is called in testing, so after each test with 'strip', we need to free the 'result' constant of its assignment.

With the 'is_clean' function, the 'cleaned' constat is not returned, so it can be freed inside of the 'is_clean" function.
