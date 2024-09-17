# Reference Python-Django
> 1. For CBV : https://ccbv.co.uk/
> 2. For DRF : https://www.cdrf.co/
> 3. For all type of decorator : https://www.w3resource.com/python-exercises/decorator/index.php
> 4. DRF cheet sheet:\
    1. https://github.com/Nifled/drf-cheat-sheet?tab=readme-ov-file \
    2. https://djangocentral.com/django-rest-framework-cheat-sheet/
> 5. Django interview questions:\
    1. https://codersdaily.in/courses/django-rest-framework-tutorial/introduction-to-django-rest-framework
> 6. Django celery with redis:\
    1. https://docs.celeryq.dev/en/stable/django/first-steps-with-django.html\
    2. https://youtu.be/kmyOgB4h5uk?si=CgEYKs8m5UBwV9rr
> 7. IDX related:\
    Youtube Channel: https://www.youtube.com/@EverythingIDX


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
Method overriding is an example of run time polymorphism. In this, the specific implementation of the method that is already provided by the parent class is provided by the child class. It is used to change the behavior of existing methods and there is a need for at least two classes for method overriding. In method overriding, inheritance always required as it is done between parent class and child class methods.

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

It hides unnecessary code details from the user. Also,  when we do not want to give out sensitive parts of our code implementation and this is where data abstraction came.\

Diffrent betweeen Abstaction and Encapsulation:

Abstraction

is the process of hiding the how, and only showing the what\
the purpose is to simplify information and hide unnecessary details from the user\
Using only relevant details and hiding unnecessary data at Design Level is called Abstraction. (Like selecting only relevant properties for a class 'Car' to make it more abstract or general.)

Encapsulation

is the process of wrapping data and functionality into a single unit\
the purpose is to protect data, by preventing direct access and only providing a safer and indirect way\
Encapsulation is the hiding of data at Implementation Level. Like how to actually hide data from direct/external access. This is done by binding data and methods to a single entity/unit to prevent external access. Thus, encapsulation is also known as data hiding at implementation level.

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

https://www.geeksforgeeks.org/celery-integration-with-django/ \
https://awstip.com/do-background-job-using-django-celery-5aae1b3e8a3a

 ```python
 => start worker:
 celery -A backend worker --loglevel=INFO --pool=solo

=> start redis:
 redis-cli -p 6379
 
=> start beat:
 celery -A backend beat -l INFO --scheduler django_celery_beat.schedulers:DatabaseScheduler
 ```

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
Use the Django cache framework to store and retrieve data from Redis.

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

> 7. What is AsyncIO.

AsyncIO is a Python library that allows you to write asynchronous code. Asynchronous code is code that can run concurrently, meaning that multiple tasks can be executed at the same time. This can be useful for tasks that take a long time to complete, such as database queries or network requests.

> 8. What is asgi.py and wsgi.py in djnago and what is diffrent between them?

WSGI (web server gateway interface):

1. `Purpose` : define commmunication standard between web server and python web framework like django.
2. `Functionality` : Handles the request synchronosuly, meaning it processed one request at a time and wait for it to finish before moving on to the next.
3. `Concurrency`: Achives concurrency (handlng multiple request simultaneously) using multiple processes or threds. However, this can lead to inefficeencies and limitations, especially for long-running tasks or real time application.
4. `Supported protocols` : Primarlity HTTP,  not ideal for Websocket or other non-Http protocol.
5. `Django usage` : the traditional way to configure a django application fro deployment eith Wsgi server like Gunicorn or u Wsgi, you'll typically find wsgi.py file in your django project like define the WSGI application obejct.

ASGI (Asynchronous server gateway interface):

1. `Purpose` :  A newer standard that builds upon WSGI, enabling asynchronous programming in Python web applications.
2. `Functionality` : Handles requests asynchronously, meaning it can initiate multiple requests concurrently without blocking the main thread. This allows for more efficient handling of long-running tasks or real-time communication.
3. `Concurrency` : Efficiently handles concurrency, making it well-suited for applications with many clients or long-lived connections.
4. `Supported Protocols` : Supports both HTTP and WebSockets, providing a flexible foundation for various communication needs.
5. `Django Usage` : Since Django 3.0, Django projects can leverage ASGI for improved performance and real-time features. You might encounter an asgi.py file that defines the ASGI application object. However, Django can usually still function with a wsgi.py file for backwards compatibility with WSGI servers.

> 9. CPU-bound task vs I/O-bound task:

1. CPU-bound
- Definition: Tasks that require significant computation and are limited by CPU processing power.
- Example: Performing complex data analysis or generating large amounts of statistical reports within a Django view.
```python
# CPU-bound task example in a Django view
from django.http import HttpResponse
import math

def compute_heavy_task(request):
    # Example of a CPU-bound task
    result = sum(math.factorial(x) for x in range(1000))
    return HttpResponse(f"Result: {result}")

```
2. I/O-bound
- Definition: Tasks that are limited by input/output operations rather than CPU processing power.
- Example: Reading or writing files, or making network requests within a Django view.
```python
# I/O-bound task example in a Django view
from django.http import HttpResponse
import requests

def fetch_data_from_api(request):
    # Example of an I/O-bound task
    response = requests.get('https://api.example.com/data')
    data = response.json()
    return HttpResponse(f"Data: {data}")
```

> 10. What is GIL and muti-threading and how they work.

1. Global Interpreter Lock (GIL):
- What is it?: The GIL is a mutex (a type of lock) used in CPython (the standard implementation of Python). It ensures that only one thread can execute Python bytecode at a time.
- Why is it used?: The GIL simplifies the implementation of memory management and makes sure that Python’s internal data structures are accessed in a thread-safe manner. Without the GIL, managing concurrency in Python's memory management system would be much more complex.
2. Multi-threading in Python:
- What is it?: Multi-threading involves running multiple threads concurrently within the same process. Threads can perform tasks simultaneously and share data with each other.
- How is it implemented?: Python’s threading module provides a way to create and manage threads.
3. Interaction Between GIL and Multi-threading:
- CPU-bound tasks: For tasks that require a lot of computation (e.g., heavy mathematical calculations), the GIL can be a limitation. Since only one thread can execute Python bytecode at a time, Python threads don’t get true parallel execution on multiple CPU cores. This means that multi-threading may not speed up CPU-bound tasks in Python.
- I/O-bound tasks: For tasks that involve waiting for external resources (like network communication or file I/O, calling ecternal api), the GIL is less of a problem. While one thread is waiting for I/O operations to complete, the GIL is released, allowing other threads to run. Thus, Python threads can be effective for handling I/O-bound operations concurrently.
4. Effect on Multi-threading:
- With GIL: Multi-threading can be used in Python, but its effectiveness depends on the type of task. For CPU-bound tasks, multi-threading may not improve performance due to the GIL. For I/O-bound tasks, it can still be useful as threads can handle multiple I/O operations concurrently.\
`Alternatives:`
    - Multiprocessing: For CPU-bound tasks, the multiprocessing module can be used to create separate processes, each with its own Python interpreter and memory space. This bypasses the GIL, allowing true parallel execution.
    - Asyncio: For I/O-bound tasks, asynchronous programming with the asyncio module can handle many tasks concurrently without using traditional multi-threading.

`summery`
- Python does support multi-threading.
- GIL: In CPython, the GIL limits true parallelism for CPU-bound tasks, as only one thread can execute Python code at a time.
- Effective Use: Multi-threading is still useful for I/O-bound tasks, where threads can work concurrently on tasks that spend time waiting for external resources.
- Alternatives: Use multiprocessing for CPU-bound tasks to achieve parallelism or asyncio for concurrent I/O operations.

> 11. annotate() vs aggregate()

1. annotate:
- It computes values per object in the queryset, meaning that it adds calculated fields to each record in the queryset.
-  is for per-object calculations and adds the result as a field to each individual object in the queryset.
- If we want to calculate the sum of total_amount for each order, or an additional calculated field, we can use annotate(). For example, calculating a field total_price_per_order by multiplying total_amount by quantity for each order
```python
orders = Order.objects.annotate(total_price_per_order=F('total_amount') * F('quantity'))

for order in orders:
    print(order.total_price_per_order)
```

2. aggregate:
- It computes a single value (or multiple values) for the entire queryset and returns a dictionary with the computed values. It is typically used when you need summary values like sum, average, or count for the whole dataset.
- is for summary calculations across all rows and returns a dictionary.
```python
# Aggregate example: calculate the total amount for all orders
result = Order.objects.aggregate(total_sum=Sum('total_amount'))
print(result)  # {'total_sum': 1234.56}
```

> 12. What is signals.

- Signals in Django allow you to execute certain code when specific actions or events occur, without modifying the core logic of your app.
- They are highly useful for actions like sending emails, logging, modifying data before save, or any background task you need to perform when certain events happen.
- Commonly Used Signals:
pre_save, post_save, pre_delete, post_delete, request_started, request_finished
```python
@receiver(post_save, sender=User)
def send_welcome_email(sender, instance, created, **kwargs):
```
> 13. Nginx, Supervisor, gunicorn

`Nginx`
- Type: Web server and reverse proxy.
- Purpose: Serves static files, handles incoming HTTP requests, and forwards them to an application server like Gunicorn.
- Role: Nginx excels at handling high concurrency, load balancing, SSL termination, caching, and serving static assets (CSS, JavaScript, images) directly to the client. It acts as a reverse proxy, meaning it routes requests to the backend application server (Gunicorn) and then forwards the response back to the client.
- Concurrency: Designed to handle a large number of connections simultaneously and is very efficient in doing so using event-driven architecture.
- Usage: Often deployed in front of application servers to offload tasks that aren't directly related to application logic (e.g., serving static files or dealing with slow client connections).

`Gunicorn`
- Type: Python WSGI application server.
- Purpose: Handles the execution of Python web applications and passes requests from Nginx (or directly if no reverse proxy is used) to the application (like a Django app).
- Role: Gunicorn is designed to run Python web applications using the WSGI interface. It handles request processing by distributing incoming requests to a pool of worker processes that serve the app. It doesn't serve static files and is generally only responsible for dynamic content.
- Concurrency: Uses a pre-fork worker model, where each worker handles one or more requests depending on configuration. Gunicorn is good for managing concurrent requests but doesn't scale as well as Nginx for high volumes of static content or slow clients.

Together:
- Nginx + Gunicorn: Nginx is often used as a reverse proxy in front of Gunicorn. Nginx handles static files, slow client connections, and forwards dynamic requests to Gunicorn. Gunicorn then processes these requests using your Python app (e.g., Django) and returns the response to Nginx, which then forwards it to the client.

Summary:
- Nginx: Web server, reverse proxy, handles static files and client connections, suitable for high concurrency.
- Gunicorn: WSGI application server that runs Python web applications and processes dynamic requests.

`Supervisor`
- Type: Process control system.
- Purpose: It ensures that critical processes like Gunicorn (and sometimes Nginx) stay running, automatically restarting them if they crash or fail.
- Role: Supervisor is primarily used to manage long-running processes like Gunicorn. It starts, stops, and restarts the application server, ensuring high availability and monitoring process health.

- Starts and stops processes: Supervisor ensures your Django application and other background tasks are running continuously during server uptimes. You can easily start, stop, restart, or reload these processes through Supervisor commands.
- Monitors processes: Supervisor keeps an eye on your processes, detecting crashes or failures. It automatically restarts them based on defined rules, ensuring your application stays online.
- Error logging and reporting: Supervisor captures logs and error messages from your processes, simplifying troubleshooting and alerting you to potential issues.

Example Flow:
- Nginx handles incoming HTTP requests and forwards dynamic requests to Gunicorn.Gunicorn processes the requests using your Python application.
Supervisor ensures Gunicorn is always running, restarts it if it crashes, and provides process monitoring and control capabilities.

Summary:
- Supervisor ensures the Gunicorn process remains up and running, automatically restarting it in case of failure and allowing for easy process control. It acts as a "guardian" for Gunicorn in the deployment stack.

> 14. What is diffrent between @classmethod, @staticmethos, @abstractmethod in django

In Django (and Python in general), the decorators `@classmethod`, `@staticmethod`, and `@abstractmethod` serve different purposes in defining methods in a class. Here's a breakdown of their differences:

1. `@classmethod`
- A `@classmethod` defines a method that is bound to the **class**, not the instance of the class.
- It receives the class (`cls`) as its first argument instead of the instance (`self`).
- You can call class methods on the class itself or on an instance of the class.
- **Use Case in Django**: A class method is typically used to create factory methods or alter class-wide properties.

```python
class MyModel(models.Model):
    name = models.CharField(max_length=100)

    @classmethod
    def create_with_default(cls):
        return cls.objects.create(name="Default Name")
```

 2. `@staticmethod`
- A `@staticmethod` defines a method that neither depends on the instance (`self`) nor the class (`cls`). It behaves just like a normal function, but it belongs to the class' namespace.
- It doesn’t access or modify class state, making it useful for utility functions.
- **Use Case in Django**: Static methods are used when the method doesn’t need to access or modify any class or instance data.

```python
class MyModel(models.Model):
    name = models.CharField(max_length=100)

    @staticmethod
    def is_valid_name(name):
        return len(name) > 0
```

3. `@abstractmethod`
- `@abstractmethod` is used in **abstract base classes (ABC)**, which are classes meant to be subclassed. It defines a method that must be implemented in any subclass of the abstract class.
- You cannot instantiate a class with an abstract method unless you provide implementations for those methods in a subclass.
- In Django, this is useful when creating custom model classes or other base classes that require subclasses to implement certain methods.

```python
from abc import ABC, abstractmethod

class BaseModel(ABC):
    
    @abstractmethod
    def save_model(self):
        """This method must be implemented by subclasses"""
        pass

class MyModel(BaseModel):
    
    def save_model(self):
        print("Model saved!")
```

Key Differences:
- **`@classmethod`**: Method operates on the class itself (uses `cls`).
- **`@staticmethod`**: Method is independent of class and instance (doesn’t use `self` or `cls`).
- **`@abstractmethod`**: Declares methods in abstract base classes that must be overridden in subclasses.
