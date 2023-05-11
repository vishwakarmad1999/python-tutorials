# Notes

## Functions in Python

A function in any programming language is meant to perform a specific set of operations.

For example, `sqrt()` function from `math` package returns the square root of a number passed to it.

```python
from math import sqrt

sqrt(5) # 2.23606797749979
```

Likewise, there’s a built in function available called `len` . It’s job is to calculate the length of any sequence you pass to it as an argument.

```python
arr = [1, 2, 3, 4]
print(len(arr)) # 4

batch_name = "BCA-4"
print(len(batch_name)) # 5
```

These are some of the functions which are available to you one way or another. But how do you create your own function?

Let me first show you how a function looks in Python and later we will break it down into pieces.

```python
def add(n1, n2):
  print(n1 + n2)

a = 4
b = 5
add(a, b) # 9
```

Let me also create the same function in C.

```c
void add(int n1, int n2) {
  printf("%d", n1 + n2);
}

int a = 4, b = 5;
add(4, 5); // 9
```

Using the above two examples, you can surely point the familiarities in them.

To create a function we need to have the following pices:

1. It’s _signature_, `def add(n1, n2)`
   - Here `def` is a keyword which is primarliy used to declare a function.
   - `add` is the name of the function
   - `a` and `b` are called as the formal arguments.
2. It’s _body_

   - To specify the body of any statement in Python, you use colon `:` and then indent the statements towards the right by hitting the `tab` key.
   - In our case the function body is `print(n1 + n2)`

The above two steps are enough to **create** a function in Python.

To call a function, you need to do the perform the following steps:

1. Pass the arguments as mentioned in the function’s signature `def add(n1, n2)`
   - `add(a, b)` where a and b have 4 and 5 respectively.

That’s it. You can now create a function on your own 🎉

Let’s create one more function of our own. This time we'll create a function to check whether the passed number is even or odd. I know you already know the logic, but how do we do that same thing inside a function is pretty straightforward.

```py
def check_even_or_odd(n):
  if n % 2 == 0:
    print(f"{n} is even")
  else:
    print(f"{n} is odd")

check_even_or_odd(5) # 5 is odd
check_even_or_odd(8) # 8 is even
```

## The Return Statement

I ask you to create a function which takes a positive integer as an input which gives me back the sum from 1 till that number. How would you do that?
That's where the **return** statement comes into the picture.

Remember this basic rule: Whenever you want your function to give something back, you use the `return` statement.

Let's look at that same `add` function example, but this time with a return statement:

```py
def add(n1, n2):
    return n1 + n2

res = add(4, 5)
print(res) # 9
```

Let's delve into the code. Whenever a `return` statement is encountered, the execution returns to the point where the function was called at the first place along with the value you specify.

So as soon as the `return n1 + n2` is encoutered, the sum is returned to the `res` and hence it contains 9

Let's look at the even odd example again, but this time with return statements.

```py
def check_even_or_odd(n):
  if n % 2 == 0:
    return True
  else:
    return False

res = check_even_or_odd(5) # res will have False
res = check_even_or_odd(8) # res will have True this time
```
