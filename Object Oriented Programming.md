# Object Oriented Programming
---

### What is a class?

A [class](https://techtarget.com/whatis/definition/class#:~:text=In%20object-oriented%20programming%2C%20a,ideas%20of%20object-oriented%20programming.) is a description of all objects that can be made from a class to be initialized from. It is a definition of the methods and variables in a kind of object. A class contains attributes.
    

---

---
```python
#example of a class definition in python

class Person:
    def__init__(self,name):
        self.name = name
    
    def__str__(self): <-- Allows us to convert our object to string
        return f" Person object called: {self.name}"
    
    def __repr__(self): <-- Allows us to present a printable version of our object
        return __str__()

class |keyword| <-- Keyword that allows us to create our own classes.
```
---
---
### What are attributes?

[Attributes](https://www.freecodecamp.org/news/python-attributes-class-and-instance-attribute-examples/#:~:text=To%20give%20a%20basic%20definition,same%20for%20every%20new%20object.) are an objects accessible tools and has two main Ideas:

1. Fields: Variables that belong to an object or a class which belongs to the instance of the class or to the class itself.

2. Methods: Functions that the object can call.
---
---
### What is an Object?

A [Object](https://www.javatpoint.com/what-is-an-object-in-python) can either be a variable, data structure, a function or a method. An object in Object Oriented Programming is an instance of a class where this object can be a combination of a variable, data structure, or a function.

- The Properties of an Object Contains:

1. State: Attributes of ebjects represent the state.

2. Behaviour: The method of objects represents Behaviour.

3. Identity: Objects are Uniquely identified  and allow interacting with other objects.
---
---

### What is Encapsulation?

[Encapsulation](https://www.sumologic.com/glossary/encapsulation/#:~:text=Encapsulation%20is%20a%20way%20to,an%20instantiated%20class%20or%20object.), also known as  Information hiding Restricts the acces to class/objects containing certain attributes and methods. We use Encapsulation for Data Protection and to restrict certain methods to be callable. For python, Encapsulation uses a special system, We hide attributes and methods by using a Double underscore ( __ ) as a prefix.

Encapsulation Example:

```python
class Student:
    def __init__(self, nameF, nameL, num):
        self.firstName = nameF
        self.lastName = nameL
        self.__studentNumber = num
       
    def __getStudentNumber(self):
        return self.__studentNumber
       
#end of Student

s1 = Student("Thomas", "Petkovic", 335714598)
print(s1.firstName)

#Another Better option/ Common Practice

    def setFirstName(self, newName): <-- setter
        self.__firstName = newName
    
    def getFirstName(self): <-- getter
        return self.__firstName
    
```
---
---

### What is Overloading & Overriding

[Overloading](https://www.scaler.com/topics/function-overloading-in-python/) is defined when two methods in one class have the same method name but different parameters. **There is no Overloading in Python 3**


Example of Overloading:

```python

class Calculator:
    def add(self, x, y):
        return x + y
    
    def add(self, x, y, z):
        return x + y + z
        
# same method name but different parameters
```

[Overriding](https://www.upgrad.com/blog/method-overriding-in-python/#:~:text=called%20multilevel%20inheritance.-,What%20is%20Method%20Overriding%20in%20Python%3F,the%20parent%20class%20or%20superclass.) is defined when two methods have the same name and have the same parameters.

Example of Overriding:

```python

class Animal:    
    def make_sound(self):
        print("Animal makes a sound")

class Cat(Animal):
    def make_sound(self):
        print("Meow")
        
# Cat inherits from Animal and overrides the make_sound method to prints "Meow" instead of "Animal makes a sound"

```
---
---
### What is Polymorphism?

[Polymorphism](https://www.edureka.co/blog/polymorphism-in-python/#:~:text=Polymorphism%20in%20python%20defines%20methods,inherited%20from%20the%20parent%20class.) is a method that can be used across different class and is dependent on the parameters

#### Overriding and Polymorphism.

The two Fundamental concepts of overriding and polymorphism in python are:
- Two classes can have the same attributes and methods
- A child of a parent can have an overrided method

If we overide a built-in method that we use in python called "magic methods"

For example:

```python

class Dog:
    def __init__(self, name):
        self.__name = name
        
    def __str__(self):
        return "Woof, I'm %s." % self.__name
lab = Dog("Luna")
print(lab) <-- "Woof, I'm Luna."
```

Why do we Override built in methods/operators?

- We can complete mathematical operations on objects
- We can compare equality between objects

We can therefore manipulate how the object behanve when met with a built in method
---
---
### What is Inheritance

[Inheritance](https://www.w3schools.com/python/python_inheritance.asp) is when an object or class is based on another class and its features (**parent class**)



Types:
- Single Inheritance: A > B
- Multiple Inheritance: A > C < B or A > B > C or a mixture of the two
- Multilevel Inheritance: A > B > C


Types of Multiple Inheritances

Inhertance types can mix creating a Hybrid.

A child will receive all attributes and methods from parent
A child can create new attributes and methods
A child can Override attributes and methods

**Important:**
- The child does not need a now Initialization method unless new attributes are needed
- The child does not need to reinstate parents methods unless overriden

```python

class Person:
    def __init__(self, name):
        self.__name = name
        
    def getName(self):
        return self.__name
        
class Student(Person):
    def __init__(self, name, num):
        Person.__init__(self, name)
        self.__sNum = num
        
    def getStudentName(self):
        return("%s: %s" % (self.__sNum, self.getName()))
        
```
#### What is Super()

[Super()](https://www.programiz.com/python-programming/methods/built-in/super) is a built-in method for classes to refer to their parent class

prevents ParentClass.method(self)

Example with super():

```python
class Person:
    def __init__(self, name):
        self.__name = name
        
    def getName(self):
        return self.__name
        
class Student(Person):
    def __init__(self, name, num):
       super().__init__(name)
        self.__sNum = num
        
    def getStudentName(self):
        return("%s: %s" % (self.__sNum, self.getName()))
        
```
---
---

### Polymorphism in Inherited Classes!

Inherited classes modifying Inheroted Methods (Overriding) --> polymorphism in python

```python
class Parent:
    def method(self):
        pass
class Child(Parent):
    def method(self):
        # something different
        # Polymorphed into something else
        # same method name
        pass

```

---
---

### What are Iterable Objects?

[Iterable objects](https://www.w3schools.com/python/python_iterators.asp#:~:text=An%20iterator%20is%20an%20object) are objects that we can interate through like a sequence.
Ex: Strings, Lists, Sets, Dictionaries etc.)

Interable does not always mean indexable

_ _ iter _ _() allows our object to be iterable when usedm it will call the method by returning itself
 
_ _ next _ _() allows us to get to the next value when interating. 
 
When the end of the sequence is reached use **raise StopIteration**


---
---

 








