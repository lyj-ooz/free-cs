# lecture 3 (control)

[lecture](https://www.youtube.com/watch?v=8UwtX-HLo30&list=PLx38hZJ5RLZc2lUzubnMKpnniy8cHjD3T&index=4)

## print & None

-   Python uses None to notate that 'print' returns nothing
    -   ex) x = print(2)
    -   print(x) # None
-   None indicates that nothing is returned

## conditional statements (if statements)

## boolean context

-   any place where an expression is evaluated to check if it is a true value or a false value
-   boolean expressions: and, or, not

## iteration

-   repeatedly execute the same line of code
-   while, for
-   fibonacci sequence with while statement

```python
def fib(n):
    cur, nxt = 0, 1
    count = 0

    while count < n:
        count += 1
        nxt_nxt = cur + nxt
        cur, nxt = nxt, nxt_nxt

    return cur
```
