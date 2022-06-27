---
jupyter:
  kernelspec:
    display_name: Python 3 (ipykernel)
    language: python
    name: python3
  language_info:
    codemirror_mode:
      name: ipython
      version: 3
    file_extension: .py
    mimetype: text/x-python
    name: python
    nbconvert_exporter: python
    pygments_lexer: ipython3
    version: 3.10.1
  nbformat: 4
  nbformat_minor: 2
---

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 1
:::

::: {.cell .code}
``` {.python}
x = [1, 2, 3, 4, 5, 6, 7]

xpop = x.pop
print(type(xpop))

xpop(3)

print(x)
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 2

**A)**
:::

::: {.cell .code}
``` {.python}
print(0.6+0.3 == 0.9)
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

**B)**
:::

::: {.cell .code}
``` {.python}
print(0.0 == 0)
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 3
:::

::: {.cell .code}
``` {.python}
x = {None: None}
if x[None]:
    print("a")
else:
    print("b")
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 4
:::

::: {.cell .code scrolled="true"}
``` {.python}
x = 40
y = int(x >= x)

print(y)
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 5
:::

::: {.cell .code}
``` {.python}
x = (1, 2, 3, 4)

y = x.sort()

print(y)
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 6
:::

::: {.cell .code}
``` {.python}
x = (1, 2, 3, 4)

y = x.pop(-2)

print(y)
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 7
:::

::: {.cell .code}
``` {.python}
x = (1, 2, 3, 4)

x += (5, 6, 7)

print(x)
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 8
:::

::: {.cell .code scrolled="true"}
``` {.python}
print('' in 'python') 
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 9
:::

::: {.cell .code}
``` {.python}
print('Python'.replace('', ' '))
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 10
:::

::: {.cell .code}
``` {.python}
a = 13
b = 11

--a
++b
-++b
print(a+b)
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

# Functions

## Problem 11
:::

::: {.cell .code}
``` {.python}
a = 5

def x():
    a = 3
    print("1) a =", a)

x()
print("2) a =", a)
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 12
:::

::: {.cell .code scrolled="true"}
``` {.python}
def x():
    return x

try:
    print(type(
                x()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()()
              )
         ) 
except:
    print("wtf are you even trying to do")
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 13

**A)**
:::

::: {.cell .code}
``` {.python}
def add(a, b):
    return a + b

def sub(a, b):
    return a - b

def mul(a, b):
    return a * b


dic = {'+': add, '-': sub, '*': mul}

print(dic['+'](4, 2))
print(dic['-'](4, 2))
print(dic['*'](4, 2))
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

**B)**
:::

::: {.cell .code}
``` {.python}
dic = {'+': (lambda a, b: a+b), 
       '-': (lambda a, b: a-b),
       '*': (lambda a, b: a*b),
}

print(dic['+'](4, 2))
print(dic['-'](4, 2))
print(dic['*'](4, 2))
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

**C)**
:::

::: {.cell .code}
``` {.python}
def add():
    return (lambda a, b: a + b)

def sub():
    return (lambda a, b: a - b)

def mul():
    return (lambda a, b: a * b)


dic = {'+': add, '-': sub, '*': mul}

print(dic['+']()(4, 2)) 
print(dic['-']()(4, 2))
print(dic['*'](4, 2))
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 14
:::

::: {.cell .code}
``` {.python}
def add(a, b):
    return a+b

def sub(a, b):
    return a-b

x = 5
y = 13

print((add if x < y else sub)(x, y))
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 15
:::

::: {.cell .code}
``` {.python}
def add(a, b):
    return a + b

def sub(a, b):
    return a - b

def mul(a, b):
    return a * b

def div(a, b):
    return a // b

def mod(a, b):
    return a % b


try:
    funcs = [add, sub, mul, div, mod]
except:
    print("This is not how you use a function.")
    quit(0)  # Quit the program so the program wouldn't continue.

for i in range(len(funcs)):
    f = funcs[i]
    print(f(10, 5))
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 16
:::

::: {.cell .code}
``` {.python}
def remove_odds(arr):
    return list(filter(lambda x: x%2==0, arr))

try:
    print(remove_odds([1,2,3,4,5,6,7,8]))
except:
    print("Nah")
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 17
:::

::: {.cell .code}
``` {.python}
def f(a, b, c, d):
    return [a], [b], [c], [d]

try:
    x = [lambda x: x*3,(), f, lambda y: y//2]
    print(f(x(5))) 
except:
    print("wat")
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 18
:::

::: {.cell .code scrolled="true"}
``` {.python}
def func(a=None, b=None, c=None, d=None):
    if a and b and (c is d is None):
        print("ONLY a and b were given.")
    
    elif b and c and (a is d is None):
        print("ONLY b and c were given.")

func(a=5, b=3)
func(b=5, c=3)
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 19

**A)** Hint:

``` {.python}
print(1,2,3,4,5, sep=", ")

# Output: 1, 2, 3, 4, 5
```
:::

::: {.cell .code}
``` {.python}
x = ['a', 'b', 'c', 'd', 'e', 'f', 'g']
print(*x, sep="\n") 
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

**B)**
:::

::: {.cell .code scrolled="true"}
``` {.python}
def func(a, b, c, d, e, f):
    print(a, b, c, d, e, f)

x = [6,5,4,3,2,1]
func(*x) 
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

**C)**
:::

::: {.cell .code}
``` {.python}
print(*["*"*i for i in range(1, 5)], sep="\n") 
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 20
:::

::: {.cell .code}
``` {.python}
type(
    (lambda a: a**2)()
) 
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 21
:::

::: {.cell .code}
``` {.python}
a = [1, 2, 3, 4, 5, 6]

b = a
b[1] = 13

print(a)
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 22
:::

::: {.cell .code}
``` {.python}
a = "abc"
b = a*0
print(type(b))
print(b)
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 23
:::

::: {.cell .code}
``` {.python}
x = 5
y = 10//2
z = 100**0.5/2.0

if x == y == z:
    print("They are all the same!")
elif x == y != z:
    print("X and Y are equal, both aren't z tho")
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 24
:::

::: {.cell .code}
``` {.python}
a = 5
b = 7
c = 13
d = 10
e = 8
f = 17
g = 17

if a < b < c > d >= e < f == g == 17:
    print("damn")
else:
    print("nmad")
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 25
:::

::: {.cell .code}
``` {.python}
arr = ["ABC", "DEF", "XYZ"]
for elem in arr:
    elem.lower() 
print(arr) 
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 26
:::

::: {.cell .code}
``` {.python}
arr = ["ABC", "DEF", "XYZ"]
for elem in arr:
    arr.append(elem)
print(arr) 
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 27
:::

::: {.cell .code}
``` {.python}
string = "Guess the output!!"

i = "i"
while i in string:
    print(i, end='')
print(i)
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 28
:::

::: {.cell .code}
``` {.python}
print(bool([]), bool(()), bool({}), bool(set()), bool(0), bool(''), bool(None), bool()) 
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 29
:::

::: {.cell .code}
``` {.python}
try:
    print(1/0)
except ArithmeticError:
    print("Caught the exception")
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 30

### A)
:::

::: {.cell .code}
``` {.python}
x = [-1, 1, 2, 6, 4, 5, 8]
y = x[x[0]]
print(y) 
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

### B)
:::

::: {.cell .code}
``` {.python}
x = [-1, 1, 2, 8, 4, 5, 3]
y = x[x[x[x[0]]]]
print(y) 
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

### C)
:::

::: {.cell .code}
``` {.python}
x = [0, 1, 2, 6, 4, 5, 8]
y = x[x[x[x[x[x[x[x[x[x[x[x[x[x[x[x[x[x[x[x[x[x[0]]]]]]]]]]]]]]]]]]]]]]

print(y)
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 31

FYI:

``` {.python}
try:
    1/0
except NameError:
    print("its name")
except ZeroDivisionError:
    print("no its me")

#  Output: no its me
```
:::

::: {.cell .code}
``` {.python}
try:
    π = 3.14159265358  # pi
    γ = 0.57721566490  # Euler's mascheroni constant
    φ = 1.61803398875  # Golden ration
    
    print(π)
    print(γ)
    print(φ)

except SyntaxError:
    print("Not a thing.")

except NameError:
    print("Not a thing.")
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 32
:::

::: {.cell .code}
``` {.python}
x = [1,2,3]
y = x
y += [4, 5, 6]

print(x)
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 33
:::

::: {.cell .code}
``` {.python}
try:
    try:
        1/0
        print("1")
    except:
        print("2")
except:
    print("3")
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 34
:::

::: {.cell .code}
``` {.python}
a = "Python"
b = "is"
c = "excellent"

d = a[0] + c[0] + a[-1] + b
print(d)
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 35

**A)**
:::

::: {.cell .code}
``` {.python}
x = 5;
x += 3;

print(x)
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

**B)**
:::

::: {.cell .code}
``` {.python}
x = 5; x += 3;

print(x)
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 36

**A)**
:::

::: {.cell .code}
``` {.python}
x = [0] * 5
print(x) 
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

**B)**
:::

::: {.cell .code}
``` {.python}
x = [[]] * 5

print(x) 
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

**C)**
:::

::: {.cell .code scrolled="true"}
``` {.python}
x = [[]] * 5
x[0].append("Hello!")

print(x)
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

**D)**
:::

::: {.cell .code}
``` {.python}
x = [[]] * 5

print(x[0] is x[1] is x[2] is x[3] is x[4])
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 37
:::

::: {.cell .code}
``` {.python}
for i in range(100):
    for j in range(100):
        if i == j == False:
            print(i, j)
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 38
:::

::: {.cell .code}
``` {.python}
try:
    True, False = False, True
    print("Yope")
except SyntaxError:
    print("Nope")
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 39
:::

::: {.cell .code}
``` {.python}
arr = [1, 2, 3, 4, 5, 6, 7, 8]

print(list(filter(
                    lambda x: int(x%1 == 0) +1, arr
                 )
          )
     ) 
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 40

Hint: `<br>`{=html} \\n is a line break character (new line)
:::

::: {.cell .code}
``` {.python}
print("New\\nLine")
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 41
:::

::: {.cell .code}
``` {.python}
x = [[0,1,2]]
y = x[:] 
y[0][0] = 5

print(x)
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 42
:::

::: {.cell .code}
``` {.python}
x, y = "10"
y, x = x + y

print(x, y)
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 43
:::

::: {.cell .code}
``` {.python}
x = 0

if False:
    x += 1

if [False]:
    x += 1

if (False):
    x += 1

print(x)
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 44
:::

::: {.cell .code}
``` {.python}
def func(n):
    1 == 1

arr = [i for i in range(1000)]

x = 0
for n in arr:
    if func(n):
        x += 1
print(x)
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 45
:::

::: {.cell .code}
``` {.python}
def get_linear_equation(m, b):
    def f(x):
        return x*m+b
    return f

print(
    get_linear_equation(2, 3)
) 
```
:::

::: {.cell .markdown}
## Problem 46
:::

::: {.cell .code scrolled="true"}
``` {.python}
def print2():
    return print

print2()("hello2") 
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 47
:::

::: {.cell .code}
``` {.python}
try:
    print("Yah")
except UrMomError:
    print("Nah")
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 48
:::

::: {.cell .code}
``` {.python}
def foo():
    print("hello")
    return
    print(text)

try:
    foo()
except:
    print("I think you forgot to define text")
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 49
:::

::: {.cell .code}
``` {.python}
x = [0, 1, 2, 3, 4, 5, 6, 7]

if x.pop(0) and x.pop(0):
    print("IN") 
else:
    print("OUT")
print(x) 
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 50
:::

::: {.cell .code}
``` {.python}
for = 5
print(for) 
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 51

**A)**
:::

::: {.cell .code}
``` {.python}
print(type(range)) 
```
:::

::: {.cell .markdown}
**B)**
:::

::: {.cell .code}
``` {.python}
print(type(range(4)))
```
:::

::: {.cell .markdown}
**C)**
:::

::: {.cell .code}
``` {.python}
print(range(4) == [0, 1, 2, 3]) 
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 52
:::

::: {.cell .code}
``` {.python}
print(
    True, True, True == (True, True, True)
) 
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 53 - What is the recursion limit?
:::

::: {.cell .code}
``` {.python}
def x(c):
    global cnt
    cnt = c
    return x(c+1)

try:
    x(2)
except RecursionError:
    print("Recursion Limit Is", cnt)
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 54
:::

::: {.cell .code}
``` {.python}
def oops():
    print(1/0)

x = 3
if x % 2 == 1 or oops():
    print("yay no error")
else:
    print("1/0...?") 
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 55
:::

::: {.cell .code}
``` {.python}
x = [(i for i in range(1000)), 5]
print(x[0][0]) 
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 56
:::

::: {.cell .code}
``` {.python}
s = [10, 20]
try:
    for s[0] in range(5):
        print(s)
except SyntaxError:
    print("tf?")
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 57
:::

::: {.cell .code}
``` {.python}
try:
    (lambda x=13: print(x))()
except:
    print("<lambda>() missing 1 required positional argument: 'x'")
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 58
:::

::: {.cell .code}
``` {.python}
def f(m, x, b):
    return m*x + b

try:
    if f:
        print("1")
    else:
        print("2")
except:
    print("3")
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 59

\"Why would a function return a function?\"
:::

::: {.cell .code}
``` {.python}
def myCache(func):
    cache = {}

    def inner(*args, **kwargs):
        arguments = f"{args}{kwargs}"
        if arguments in cache:
            return cache[arguments]
        val = func(*args, **kwargs)
        cache[arguments] = val
        return val
    return inner
```
:::

::: {.cell .code}
``` {.python}
def fib(n):
    if n <= 1:
        return n
    return fib(n-1) + fib(n-2)

fib = myCache(fib)
print((fib(800) ^ 0b10101011101) % 1)
```
:::

::: {.cell .markdown}
# Problem 60
:::

::: {.cell .markdown}
## A) {#a}
:::

::: {.cell .code}
``` {.python}
print(1/0)
```
:::

::: {.cell .markdown}
## B) {#b}
:::

::: {.cell .code}
``` {.python}
try:
    print(1/0)
except ValueError:
    print("Dont div by 0")
```
:::

::: {.cell .markdown}
## C) {#c}
:::

::: {.cell .code}
``` {.python}
try:
    print(1/0)
except ArithmeticError:
    print("Dont div by 0")
```
:::

::: {.cell .markdown}
## D)
:::

::: {.cell .code scrolled="true"}
``` {.python}
try:
    print(1/0)
except BaseException:
    print("Don't div by 0")
```
:::

::: {.cell .markdown}
## Problem 61

**A)**
:::

::: {.cell .code}
``` {.python}
class A:
    pass

a = A()
print(type(a))
```
:::

::: {.cell .markdown}
#### B) {#b}
:::

::: {.cell .code}
``` {.python}
print(a.__class__)
```
:::

::: {.cell .code}
``` {.python}
b = a.__class__.__class__
print(b)
print(b.__class__)
```
:::

::: {.cell .code}
``` {.python}
print(a.__class__.__class__.__class__.__class__.__class__.__class__.__class__.__class__.__class__.__class__)
```
:::

::: {.cell .markdown}
## Problem 62

**Which takes more time?**
:::

::: {.cell .code}
``` {.python}
print(5 in range(-500, 500))
```
:::

::: {.cell .code}
``` {.python}
print(5 in range(-1000000, 1000000000))
```
:::

::: {.cell .markdown}
## Problem 63
:::

::: {.cell .code}
``` {.python}
arr = [[1, 2], 5]
[a, b], c = arr
print(a, b, c)
```
:::

::: {.cell .markdown}
# Object Oriented Programming in Python
:::

::: {.cell .markdown}
## Problem 64
:::

::: {.cell .code scrolled="true"}
``` {.python}
class XX:
    a = 3
    _b = 13
    __c = 15
    def __init__(self):
        pass
x = XX()
print(x.a)
```
:::

::: {.cell .code}
``` {.python}
class Mother():
    __x = 13.5
    def __init__(self):
        pass

class Daughter(Mother):
    __x = 3
    def __init__(self):
        pass
    
obj = Daughter()
```
:::

::: {.cell .markdown}
### A) {#a}
:::

::: {.cell .code}
``` {.python}
print(obj.__x) 
```
:::

::: {.cell .markdown}
### B) {#b}
:::

::: {.cell .code}
``` {.python}
print(obj._Daughter__x)
```
:::

::: {.cell .markdown}
### C) {#c}
:::

::: {.cell .code}
``` {.python}
print(obj._Mother__x)
```
:::

::: {.cell .markdown}
## Problem 65 - Everything is an Object
:::

::: {.cell .code}
``` {.python}
class A:
    pass

def func():
    pass

x = isinstance(func, object)
print(x)

x = isinstance(A(), object)
y = isinstance(A, object)
print(x)
print(y, '\n')

print(isinstance(type, object))
```
:::

::: {.cell .markdown}
## Problem 66 - Not everything is A Type
:::

::: {.cell .code}
``` {.python}
class A:
    pass

class B(A):
    pass

class C(B):
    pass

x = isinstance(C, type)
y = isinstance(C(), type)
print(x)
print(y, '\n')

print(isinstance(object, type), '\n')

print(isinstance(A, type))
print(isinstance(B, type))
print(isinstance(C, type))
```
:::

::: {.cell .markdown}
`<br>`{=html} `<br>`{=html}

## Problem 67
:::

::: {.cell .code}
``` {.python}
import builtins
class MyPrinter:
    def __call__(self, *args, **kwargs):
        original_print = builtins.print
        original_print(*args, **kwargs)
    
    __sub__ = __call__
    __add__ = __call__
    __mul__ = __call__
    __floordiv__ = __call__
    __truediv__ = __call__
    __pow__ = __call__
    __mod__ = __call__
    __and__ = __call__
    __or__ = __call__
    __xor__ = __call__
    __gt__ = __call__
    __lt__ = __call__
    __ge__ = __call__
    __le__ = __call__
    __eq__ = __call__
    __ne__ = __call__
    
print2 = MyPrinter()
print2 / "h"
print2 + "e"
print2 - "l"
print2 * "l"
print2 ** "o"
print2 // ","
print2 & " "
print2 | "w"
print2 ^ "o"
print2 > "r"
print2 < "l"
print2 == "d"
print2 != "!"
```
:::

::: {.cell .markdown}
## Problem 68
:::

::: {.cell .code}
``` {.python}
def DataClass(cls):
    for k, v in cls.__annotations__.items():
        setattr(cls, k, v())
    return cls

@DataClass
class A:
    x: int
    y: float
    z: str
        
a = A()
a.x = 3
a.y = 5.3
a.z = 'abc'

print(a.x)
```
:::

::: {.cell .markdown}
# Easter eggs
:::

::: {.cell .code}
``` {.python}
from __future__ import barry_as_FLUFL
```
:::

::: {.cell .code}
``` {.python}
print(1 <> 2)
```
:::

::: {.cell .markdown}
TL; DR\
While wondering how many permutations are there to fit *n* characters in
3,4,5,6,\...,x characters words (Like in the game \[Word
Cookies\]\[1\]), dividing by *n!* give *e* `<br>`{=html} This:

$\displaystyle\frac{\displaystyle\sum_{x=3}^n{\frac{n!}{(n-x)!}}}{n!}$
as n \--\> $\infty$

Gives *e* (*2.718281828*) somehow.\
`<br>`{=html} `<br>`{=html} Here is the full
story:`<br>`{=html}`<br>`{=html} I was playing \[Word Cookies\]\[1\] (I
suggest looking at the image for better understanding of the
game)`<br>`{=html} and while programming a bot that would play the game
for me, `<br>`{=html} I was wondering how many possible permutations are
there for *n* characters`<br>`{=html} that need to fit inside words with
3-*x* characters (depends on the word, as shown in the
picture).`<br>`{=html} At first, my friend came up with this (wrong)
formula (trust me its relevant):`<br>`{=html}`<br>`{=html}
$\displaystyle\sum_{x=3}^n{n!}$ `<br>`{=html} `<br>`{=html} As you see,
this is not the right formula. Later I found out this formula
(right):`<br>`{=html}`<br>`{=html}
$\displaystyle\sum_{x=3}^n{\frac{n!}{(n-x)!}}$

Then he said that he was surprised the right formula is bigger than the
wrong (with factorial).`<br>`{=html}

So I decided to check how much is it bigger (the ratio) so, I wrote in
my calculator:`<br>`{=html}`<br>`{=html}
$\frac{\displaystyle\sum_{x=3}^8{\frac{8!}{(8-x)!}}}{8!}$
(n=8)`<br>`{=html}`<br>`{=html} And got the result:
*2.716666*`<br>`{=html} Immediately I thought of the golden ratio. So I
checked bigger numbers seeing of I can get closer to *e*.`<br>`{=html}
When n=15, the result is *2.718281828*`<br>`{=html} \[1\]:
<https://i.stack.imgur.com/nRZL9.png>
:::
