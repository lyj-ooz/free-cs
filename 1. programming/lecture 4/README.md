# lecture 4 (environmental diagram)

[lecture](https://www.youtube.com/watch?v=fGF1fpLMX4k&list=PLx38hZJ5RLZc2lUzubnMKpnniy8cHjD3T&index=4)

## environmental diagram

-   a visual tool to keep track of bindings(assignments) and state of a computer program
-   why use it?
    -   to understand why programs behave the way they do
    -   helpful for debugging

## 'frame'

-   every function call expressions has a corresponding frame
    -   global frame: the starting frame
    -   parent frame: wherever the function defined. Every function has its parent frame. If you can't find a variable in the current frame, you can check its parent from and so on...
-   only call expressions create new frames
-   examples..

    ```python
    y = 10
    def broken_square(x):
        return x + y

    broken_square(4)
    ```

    [ed1](https://github.com/lyj-ooz/free-cs/blob/1-programming/1.%20programming/lecture%204/ed1.jpg)

    ```python
    def square(x):
        return x * x
    def sum_of_squares(x, y):
        return square(x) + square(y)

    sum_of_squares(3)
    ```

    [ed2](https://github.com/lyj-ooz/free-cs/blob/1-programming/1.%20programming/lecture%204/ed2.jpg)

## Lambda Expressions

-   a way that you can write a whole function in one line of code
-   example

    ```python
    square = lambda x: x * x

    def square(x):
        return x * x
    ```

-   exercise (higher-order functions)
    ```python
    def make_greeter(name):
        return lambda greeting: print(greeting, name)

    greeter_function = make_greeter(“Tiffany”)
    greeter_function(“Hey what’s up!”)
    ```
-   higher-order functions (next lecture)
