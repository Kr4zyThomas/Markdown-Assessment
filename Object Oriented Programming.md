# Object Oriented Programming
## Day 1 - Object & Class
### What is a Class?
A [class](https://techtarget.com/whatis/definition/class#:~:text=In%20object-oriented%20programming%2C%20a,ideas%20of%20object-oriented%20programming.) is a description of all objects that can be made from a class to be initialized from. It is a definition of the methods and variables in a kind of object. A class contains attributes.

```
#example of a class definition in python

class Person:
    def__init__(self,name):
        self.name = name
    
    def__str__(self):
        return f" Person object called: {self.name}"

class |keyword| <-- Keyword that allows us to create our own classes.
```

### What are attributes?

[Attributes](https://www.freecodecamp.org/news/python-attributes-class-and-instance-attribute-examples/#:~:text=To%20give%20a%20basic%20definition,same%20for%20every%20new%20object.) are an objects accessible tools and has two main Ideas:

1. Fields: Variables that belong to an object or a class which belongs to the instance of the class or to the class itself.

2. Methods: Functions that the object can call.

### What is an Object

A [Object](https://www.javatpoint.com/what-is-an-object-in-python) can either be a variable, data structure, a function or a method. An object in Object Oriented Programming is an instance of a class where this object can be a combination of a variable, data structure, or a function.

- The Properties of an Object Contains:

1. State: Attributes of ebjects represent the state.

2. Behaviour: The method of objects represents Behaviour.

3. Identity: Objects are Uniquely identified  and allow interacting with other objects.


