# Leak report

_Use this document to describe whatever memory leaks
you find in `clean_whitespace.c` and how you might fix
them. You should also probably remove this explanatory
text._

There are two leaks in check_whitespace:
 - The 'strip' function creates a constant 'result' that never gets free of its assingnment, but is also returned by the function. 
 - The 'is_clean' function creates a constant 'cleaned' that never gets free of its assignment.


