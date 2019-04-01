# lambdapy
#### Untyped Lambda Calculus in python

> Lambda calculus (also written as λ-calculus) is a formal system in mathematical logic for expressing computation based on function abstraction and application using variable binding and substitution. It is a universal model of computation that can be used to simulate any Turing machine. It was first introduced by mathematician Alonzo Church in the 1930s as part of his research of the foundations of mathematics...

LambdaPy is an "interpreter" for untyped lambda calculus

## Installation

```
pip install lambdapy
```

## Usage

### From python

```python
from lambdapy import *

# you could use the pylambda function instead of the l function  
# you could also use the unicode lambda symbol (λ) instead of a backslash
identity = l(r"(\x.x)")

# this assigns the identity lambda term to the variable "id" in the lambdapy internal namespace, which can be accessed from within lambda expressions
assign("id", identity)

# this is a lambda term applying the identity function to (\y.(y y)). it should be (\y.(y y))
identity_usage = l(r"(id (\y.(y y)))")

# this just pretty-prints the expression, here you can test if it really is (\y.(y y))
identity_usage.display()
```

### From the command line

```
lambda
```
^ This launches the lambdapy REPL, here you can enter commands like this:
```
 __ 
 \ \      LambdaPy Interactive shell 
  ⟩ \      type .help for help
 / ^ \      type .quit to exit
/_/ \_\

>>> (\y.y)
(λy.y)
>>> a = (\x.x)
(λx.x)
>>> a
(λx.x)
>>> (a a)
(λx.x)
```
