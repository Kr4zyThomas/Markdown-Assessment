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
    
    def__str__(self):
        return f" Person object called: {self.name}"

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

[Overriding](https://www.upgrad.com/blog/method-overriding-in-python/#:~:text=called%20multilevel%20inheritance.-,What%20is%20Method%20Overriding%20in%20Python%3F,the%20parent%20class%20or%20superclass.) is defined when two methods have the same name and have the same parameters.

FOr example





