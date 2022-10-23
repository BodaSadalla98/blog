# Python


## Inheritance

- If you have inherited from parent class then you should call the parent class constructor if you overload it, or simply doesn't overload it

Ex:

```python
class parent:
    def __init__:

class child:
    def __init__:
        super().__init__()

class child2:
    ## or simply don't override the constructor and use the parent one


```

### Multiple Inheritance

- when we inherit from two or more classes, whatever class we inherited first(typed first in the list), would be the one to have pariority

  - if the two parent classes have the same function, then Method Resolution Orded (MRO) makes the fist class method to be the one called

- if we override a function from the parent class in the child class, the cild class has the pariority

- to call the both finctions, then we can call the parent class from the child class directly
  - ex: in the child class we can do: `parent.method()`

## Underscore

- single underscore (Before): used for internal variables
- double undescore (After): used also for internal scopes only, and also tells python to change the variable name(mangling)
- underscore (After): helps avoid conflicts with key words ex(class*, int*, etc)

- underscore (Before and Afer): used for thing like \_\_init**, \_\_main**, etc

## Decorators

```python
def function(func):
    def inner():
        print(1)
        func()
        print(3)
    return inner

@function
def print_name():
    print(2)


print_name()
```

    1
    2
    3

- so in this example we decorated a function (print_name), which means we gonna pass the deocared function as a paramemter to the decorator
- so with decorator, we call our function in the inner function, the decorate it, then return the decorated function
- used when u wanna decorate a multiple function with the same, suppose you have an add and multiply function, and you want to print something at the beginig of them, so you crate a decorator that does that, and decorate the two functions with that.

## Operators

- for custom classes, or structures, you can do operators overloads
- but there's also reversed operators when python can't handle operations
  - ex: class.\_\_rmul()

