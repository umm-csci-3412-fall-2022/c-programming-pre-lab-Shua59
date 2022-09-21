# Leak report

_Use this document to describe whatever memory leaks
you find in `clean_whitespace.c` and how you might fix
them. You should also probably remove this explanatory
text._

There are a couple of string that are not clean (have unecessary spaces at the beginning and end of them)
 - The string '  stuff' is not clean because it has two extra blank spaces before the letters
 - The string 'nonsense  ' is not clean because it has two extra blank spaces after the letters
 - The string '   ' is because it is a string only containing blank spaces
 - The string '     silliness    ' is not clean because it has five extra blank spaces before and four extra blank spaces after the letters

