# Stack Overflow in F# Recursive Function

This example demonstrates a potential stack overflow error in F# when using mutable variables within a recursive function. The `loop` function increments two mutable variables (`x` and `y`) recursively.  If the recursion depth exceeds the stack limit, a stack overflow will occur.

**How to reproduce:** Run the code in a F# compiler. The error might not show up immediately depending on your system and compiler settings, however, a very large number for the limit may cause the error.

**Solution:** The solution involves using tail recursion to avoid stack overflow. Tail recursive calls are optimized by the compiler, effectively turning the recursion into a loop.