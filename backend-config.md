# Reference Python-Django
> 1. For CBV : https://ccbv.co.uk/
> 2. For DRF : https://www.cdrf.co/
> 3. For all type of decorator : https://www.w3resource.com/python-exercises/decorator/index.php
> 4. DRF cheet sheet:\
    1. https://github.com/Nifled/drf-cheat-sheet?tab=readme-ov-file \
    2. https://djangocentral.com/django-rest-framework-cheat-sheet/ 


# Revision Questions
> 1. OOPs in python:

https://www.programiz.com/python-programming/object-oriented-programming

In Python object-oriented Programming (OOPs) is a programming paradigm that uses objects and classes in programming. It aims to implement real-world entities like inheritance, polymorphisms, encapsulation, etc. in the programming. The main concept of object-oriented Programming (OOPs) or oops concepts in Python is to bind the data and the functions that work together as a single unit so that no other part of the code can access this data.

1. Class and object
2. Polymorphism
3. Encapsulation
4. Inheritance
5. Data Abstraction

```1. Class and object```

A class is a collection of objects. A class contains the blueprints or the prototype from which the objects are being created. It is a logical entity that contains some attributes and methods. 

In object oriented programming Python, The object is an entity that has a state and behavior associated with it. It may be any real-world object like a mouse, keyboard, chair, table, pen, etc. Integers, strings, floating-point numbers, even arrays, and dictionaries, are all objects. More specifically, any single integer or any single string is an object. The number 12 is an object, the string “Hello, world” is an object, a list is an object that can hold other objects, and so on. You’ve been using objects all along and may not even realize it.

```2. Polymorphism```

Polymorphism is an ability of an object to take on many forms. In object oriented Programming Python, Polymorphism simply means having many forms. For example, we need to determine if the given species of birds fly or not, using polymorphism we can do this using a single function.

Other word:
The word polymorphism means having many forms. In programming, polymorphism means the same function name (but different signatures) being used for different types. The key difference is the data types and number of arguments used in function.

Method Overloading: 
Method Overloading is an example of Compile time polymorphism. In this, more than one method of the same class shares the same method name having different signatures. Method overloading is used to add more to the behavior of methods and there is no need of more than one class for method overloading.
Note: Python does not support method overloading. We may overload the methods but can only use the latest defined method.

Method Overriding: 
Method overriding is an example of run time polymorphism. In this, the specific implementation of the method that is already provided by the parent class is provided by the child class. It is used to change the behavior of existing methods and there is a need for at least two classes for method overriding. In method overriding, inheritance always required as it is done between parent class(superclass) and child class(child class) methods.

```3. Encapsulation```

https://www.geeksforgeeks.org/encapsulation-in-python/

In Python object oriented programming, Encapsulation is one of the fundamental concepts in object-oriented programming (OOP). It describes the idea of wrapping data and the methods that work on data within one unit. This puts restrictions on accessing variables and methods directly and can prevent the accidental modification of data. To prevent accidental change, an object’s variable can only be changed by an object’s method. Those types of variables are known as private variables.

A class is an example of encapsulation as it encapsulates all the data that is member functions, variables, etc. The goal of information hiding is to ensure that an object’s state is always valid by controlling access to attributes that are hidden from the outside world.

```4. Inheritance```

In Python object oriented Programming, Inheritance is the capability of one class to derive or inherit the properties from another class. The class that derives 	properties is called the derived class or child class and the class from which the properties are being derived is called the base class or parent class. The benefits of inheritance are:

It represents real-world relationships well.
It provides the reusability of a code. We don’t have to write the same code again and again. Also, it allows us to add more features to a class without modifying it.
It is transitive in nature, which means that if class B inherits from another class A, then all the subclasses of B would automatically inherit from class A.

Types of Inheritance

Single Inheritance: Single-level inheritance enables a derived class to inherit characteristics from a single-parent class.

Multilevel Inheritance: Multi-level inheritance enables a derived class to inherit properties from an immediate parent class which in turn inherits properties from his parent class. 

Hierarchical Inheritance: Hierarchical-level inheritance enables more than one derived class to inherit properties from a parent class.

Multiple Inheritance: Multiple-level inheritance enables one derived class to inherit properties from more than one base class.


```5. Data Abstraction```

https://www.geeksforgeeks.org/object-oriented-programming-in-python-set-2-data-hiding-and-object-printing/

It hides unnecessary code details from the user. Also,  when we do not want to give out sensitive parts of our code implementation and this is where data abstraction came.

> 2. API vs REST API vs RESTful API

API (Application Programming Interface)

An API is a general term for a way two pieces of software communicate with each other. It acts as a messenger between applications, allowing them to request and receive data.
APIs can be designed in many ways, using different protocols and formats.

REST API (Representational State Transfer API)

REST API is a specific type of API that follows a set of architectural guidelines called REST (Representational State Transfer).\
REST APIs typically use HTTP verbs (GET, POST, PUT, DELETE) for different actions on data.\
They also use data formats like JSON or XML to exchange information.\
REST APIs are popular because they are:\
Lightweight and flexible\
Easy to implement\
Widely supported across different programming languages and frameworks

RESTful API

A RESTful API is an API that strictly adheres to all the principles of REST architecture.\
This includes characteristics like:\
Statelessness (each request contains all necessary information)\
Client-server architecture\
Uniform interface (consistent way to interact with resources)\
RESTful APIs are considered more reliable and predictable compared to regular REST APIs, making them ideal for complex, large-scale systems.\

In short:\
All RESTful APIs are REST APIs, but not all REST APIs are strictly RESTful.\
REST APIs offer flexibility, while RESTful APIs provide more standardization and predictability.

Here's an analogy:\
Think of an API as a language for two programs to talk to each other.\
REST API is like a specific dialect of that language, with some basic rules.\
RESTful API is like following all the grammatical rules perfectly within that dialect.\