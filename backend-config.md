# Reference Python-Django
> 1. For CBV : https://ccbv.co.uk/
> 2. For DRF : https://www.cdrf.co/
> 3. For all type of decorator : https://www.w3resource.com/python-exercises/decorator/index.php
> 4. DRF cheet sheet:\
    1. https://github.com/Nifled/drf-cheat-sheet?tab=readme-ov-file \
    2. https://djangocentral.com/django-rest-framework-cheat-sheet/
> 5. Django interview questions:\
    1. https://codersdaily.in/courses/django-rest-framework-tutorial/introduction-to-django-rest-framework


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
RESTful APIs are considered more reliable and predictable compared to regular REST APIs, making them ideal for complex, large-scale systems.

In short:\
All RESTful APIs are REST APIs, but not all REST APIs are strictly RESTful.\
REST APIs offer flexibility, while RESTful APIs provide more standardization and predictability.

Here's an analogy:\
Think of an API as a language for two programs to talk to each other.\
REST API is like a specific dialect of that language, with some basic rules.\
RESTful API is like following all the grammatical rules perfectly within that dialect.

> 3. what is celery.

https://www.geeksforgeeks.org/celery-integration-with-django/

Celery is an asynchronous task queue or job queue based on distributed message passing. It is used in Python to execute tasks asynchronously. Celery is used to offload long-running tasks from the main request/response cycle within Django. Using Celery becomes critical when your app starts to scale or you need better performance out of Django.
Celery works by sending messages between Django applications and worker processes through a message broker, such as RabbitMQ or Redis. The message broker is responsible for delivering messages to the worker processes. The worker processes then execute the tasks that are contained in the messages.

Here are some of the benefits of using Celery in Django:

Improved performance:\
Celery can improve the performance of your Django application by offloading long-running tasks to worker processes. This allows your Django application to continue to respond quickly to users while the worker processes complete the long-running tasks in the background.

Increased scalability:\
Celery can help you to scale your Django application by distributing the workload across multiple worker processes. This allows you to handle more traffic and process more requests without having to add more servers.

Enhanced reliability:\
Celery can help to improve the reliability of your Django application by providing fault tolerance. If a worker process fails, Celery will automatically reschedule the task to another worker process.\
Overall, Celery is a powerful tool that can help you to improve the performance, scalability, and reliability of your Django application.

> 4. what is redis.

https://stackabuse.com/working-with-redis-in-python-with-django/

Redis is an open-source, in-memory data structure store, used as a database, cache and message broker. It is known for its high performance and scalability. Redis is often used as a cache in Django applications to improve performance by storing frequently accessed data in memory.
Django is a Python web framework that follows the model-template-views (MTV) architectural pattern. It is used to build and maintain complex database-driven websites. Django includes a built-in cache framework that can be used with Redis.

To use Redis with Django, you need to:

Install Redis on your server:\
Install the redis-py Python package.\
Configure your Django settings to connect to the Redis server.\
Use the Django cache framework to store and retrieve data from Redis.\

Here are some of the benefits of using Redis with Django:

Improved performance:\
Redis can store data in memory, which makes it much faster than accessing data from a database.

Reduced load on the database:\
By storing frequently accessed data in Redis, you can reduce the load on your database server.

Scalability:\
Redis is a scalable solution that can handle large amounts of data and traffic.

Versatility:\
Redis can be used for a variety of tasks, including caching, session storage, real-time messaging, and rate limiting.\
Overall, Redis is a powerful tool that can be used to improve the performance, scalability, and versatility of Django applications.

> 5. what is ElasticSearch  and how to use.

https://medium.com/geekculture/how-to-use-elasticsearch-with-django-ff49fe02b58d#:~:text=Elasticsearch%20is%20a%20search%20engine,Elasticsearch%20is%20developed%20in%20Java.

Elasticsearch is a search engine based on the Lucene library. It provides a distributed, multitenant-capable full-text search engine with an HTTP web interface and schema-free JSON documents. Elasticsearch is developed in Java.

Elasticsearch allows you to store, search, and analyze huge volumes of data quickly and in near real-time and give back answers in milliseconds. It’s able to achieve fast search responses because instead of searching the text directly, it searches an index.

> 6. what is docker and how that work with django.

https://chatgpt.com/share/ea69a00d-bfe4-49ec-a02d-3d22764fc50b


Docker is an open-source platform that enables developers to automate the deployment, scaling, and management of applications using containerization. Containers are lightweight, standalone, executable software packages that include everything needed to run an application: code, runtime, libraries, and system tools. Docker ensures that the application runs uniformly across different environments, whether it’s development, testing, or production.

Key Concepts of Docker:

Image: A read-only template with instructions for creating a container. Images are built from a set of instructions written in a Dockerfile.\
Container: A runnable instance of an image. Containers can be started, stopped, moved, and deleted. Each container is isolated but can communicate with other containers.\
Dockerfile: A text file that contains a set of instructions to build a Docker image. It specifies the base image, application code, dependencies, and commands to run the application.\
Docker Hub: A cloud-based repository where Docker users can create, test, store, and distribute Docker images.

Benefits of Using Docker with Django:

Consistency: Docker ensures that your application runs the same in development, testing, and production environments.\
Isolation: Each container is isolated, meaning dependencies and configurations in one container do not affect others.\
Scalability: Docker makes it easy to scale your application by adding more containers.\
Simplified Deployment: With Docker, you can deploy your application as a container on any system that supports Docker.