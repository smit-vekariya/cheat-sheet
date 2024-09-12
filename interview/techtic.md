> 1. What is constructor in python.

A constuctor is special method that is automatically called when object of class is created.\
It is used to initialize the object's attributes or perform other setup tasks

- Method Name: The constructor method in Pthon is named `__init__()`.
- Purpose: Constructors are used to set the initial state of an object by assigning values to its data members (attributes).
- Automatic Execution: When you create an object of a class, the constructor is called automatically. 
- self Parameter: The first parameter of the constructor is always self, which refers to the instance of the class being created.
- Parameters: Constructors can take additional parameters to customize the initialization process

```
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age
```

> 2. What is self in python.

`self` refers to the current instance of a class. It is used to access instance variables and methods within the class.

`self` is the first parameter of any instance method in a class. It represents the object itself on which the method is called. Without self, Python wouldn’t know which instance of the class you are referring to when you access variables or methods.

> 3. What is diffrent between 'git fetch' and 'git pull'.

1. git fetch
- it fetch new data (commits, branch, tags) from the remote repository but does not update your working directory or not automatically mearge these change into your local branches.
- After feching, you can manually review and merge the changes as needed using `git merge`.

2. git pull
- It combines two operations: `git fetch` followed by `git merge`.
- First, it fetches the changes from the remote repository, then automatically attempts to merge them into your current branch.
- This means your working directory will be updated and merged with the fetched changes immediately.

> 4. What is diffent between list and array.

1. type
 - list : python built in data-structure 
 - array : requires imorting array from import array
2. data type
 - list : a list can contain element of diffrent data type (integer, float, string, object)
 - array : An array can only store elements of the same type (e.g., only integers, only floats).
3. syntax
 - list : Defined using square brackets [], e.g., my_list = [1, "hello", 3.14].
 - array : Arrays are defined using the array() function, e.g., my_array = array.array('i', [1, 2, 3]), where 'i' specifies the type of elements (e.g., 'i' for integers).
4. Usage
 - list : General-purpose container that is very flexible.
 - array : Arrays are more memory efficient for handling large amounts of data of a single type, particularly in numeric applications.
5. Performance
- list : Lists are not optimized for numerical calculations but are excellent for generic storage and manipulation of elements.
- array : Arrays are faster and use less memory when working with large collections of numeric data compared to lists.

> 5. What is redis and why we use that in django.

Redis is an in-memory data store, often used as a cache or message broker.
- Caching: To store frequently accessed data (like query results) to improve performance and reduce database load.
- Session Management: Storing session data for faster retrieval.
- Task Queues: Along with tools like Celery, Redis is used to handle background tasks like sending emails or processing long-running tasks.
- Real-time Features: Used for real-time updates, such as WebSockets for chat applications or live notifications.
- It's chosen for its speed, simplicity, and scalability in handling large amounts of data.

> 6. diffrent between list and tuple:
1. Mutability
- list : Mutable, meaning you can modify (add, remove, change) the elements after the list is created.
- tuple : Immutable, meaning once a tuple is created, its elements cannot be changed.
2. Syntax
- list : Defined using square brackets [].
- tuple : Defined using parentheses ().
3. Performance
- list : Slower in terms of performance compared to tuples due to their mutability.
- tuple : faster because they are immutable and use less memory.
4. Use Cases
- list : Used when you need a collection of items that can change over time, such as dynamic data like a to-do list or a collection of user inputs.
- tuple : Used when you want to ensure the collection of items remains unchanged, such as representing fixed data like a person's date of birth or the coordinates of a location.
5. Methods
- list : Supports a wide range of methods like append(), remove(), pop(), sort(), etc.
- tuple : Limited methods, mainly count() and index() (since they are immutable).
6.  Memory Usage
- list : Generally uses more memory since it is mutable and has overhead for supporting dynamic resizing.
- tuple : Uses less memory because it is immutable and doesn’t need additional overhead for resizing.

> 7. What is interface in python

In Python, an interface is a way to define a set of methods that a class must implement. While Python doesn't have a built-in interface keyword like some other languages (e.g., Java), it achieves the same functionality through abstract base classes (ABCs)

- in short interface is a set of method definitions that a class must implement. 
```
from abc import ABC, abstractmethod

class Shape(ABC):
    @abstractmethod
    def area(self):
        pass

    @abstractmethod
    def perimeter(self):
        pass
```
- ABC: Import the ABC class (Abstract Base Class) from the abc module.
- abstractmethod: The @abstractmethod decorator marks a method as abstract, meaning it must be implemented by any concrete class that inherits from this ABC.
```
class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return 3.14 * self.radius ** 2

    def perimeter(self):
        return 2 * 3.14 * self.radius

class Square(Shape):
    def __init__(self, side):
        self.side = side

    def area(self):
        return self.side ** 2

    def perimeter(self):
        return 4 * self.side
```
- Circle and Square classes inherit from the Shape interface (ABC).Both classes provide concrete implementations for the area and perimeter methods, fulfilling the interface contract.

Benefits of Using Interfaces:
- Enforcing a contract : Interfaces ensure that classes adhering to them provide specific methods, promoting consistency and structure.
- Polymorphism : You can treat objects of different classes that implement the same interface in a uniform way.
- Decoupling : Interfaces allow you to write code that depends on the interface rather than the concrete implementation, promoting flexibility and maintainability.

> 8. What is diffrent between await and promise in javascript.

1. promise
- Promise handles asynchronous operations that still need to be completed, and their results may be available after a period of time. It is essential for handling AJAX requests, timeouts, and other asynchronous operations.
- Promises have three states: pending, fulfilled, and rejected. It always starts in the pending state when it is created. When the asynchronous operation completes successfully, the Promise transitions to the fulfilled state and passes the resulting value to the success callback function. If the process fails, the Promise transitions to the rejected state and passes an error object to the error callback function.
- A Promise can only change from the pending state to either the fulfilled or rejected state. Once it has transitioned to either of these states, it cannot change to any other state
```
const ninjaPromise = new Promise((resolve, reject) => {
	// Do some asynchronous operation
  	if (/* operation is successful */) {
 		resolve('Here comes the success!');
  	} 
  	else {
 		reject('Oops we have an Error!');
  	}
});

ninjaPromise.then(result => {
	console.log(result);  // Output: Here comes the success!
}).catch(error => {
	console.error(error);  // Output: Oops we have an Error!
});
```
2. Async/Await
-  It makes the asynchronous code easier to read, write, and maintain asynchronous code. Instead of chaining Promises together, Async Await allows developers to write code that looks like synchronous code.
- Async Await uses only two keywords: async and await. The async keyword is used to declare that a particular function is asynchronous. The await keyword waits for the execution of the async function’s code block until a promise is fulfilled or rejected.

```
const fetchData = async () => {
	try {
		const response = await fetch('https://api.ninjaimages.com/data');
		const data = await response.json();
		return data;  // Output: returns the fetched data
	} 
	catch (error) {
		console.log(error);  // Output: returns the error message
	}
}
```

- `Promise`: Represents an asynchronous operation and its result, typically handled using .then() and .catch().
- `await`: Pauses the execution of an async function until a promise is resolved, making code look synchronous and easier to read.

> 9. Synchronous vs asynchronous in django

1. Synchronous
- Execution : Tasks are executed sequentially, one after the other. A task must complete before the next one begins.
- Blocking: When scyncronous operation, like reading from the database and calling external app, is process, the entire thread is block untill the operation complete.
- Simplicity : Synchronous code is generally easier to write, read, and debug due to its linear flow.  

2. Asynchronous
- Execution : Tasks can be executed concurrently, allowing multiple operations to progress simultaneously.
- Non-Blocking : Async does not block the thread, When an operation is initiated, the thread can continue to execute other tasks while waiting for the operation to finish.
- Complexity: Asynchronous code can be more challenging to write, read, and debug due to the non-linear execution flow and the use of constructs like async/await.
- Efficiency : Asynchronous code is generally more efficient for I/O-bound tasks, like making network requests or interacting with databases, as it minimizes waiting time.

```
# views.py (synchronous)

import time
from django.http import JsonResponse

def sync_task_view(request):
    # Simulate a blocking I/O-bound task (e.g., an external API call)
    time.sleep(5)  # This simulates a delay of 5 seconds
    data = {'message': 'This is a synchronous task'}
    return JsonResponse(data)

```
- This example shows how to handle a typical I/O-bound operation synchronously. The task (e.g., fetching data from an external API) blocks until the data is fully retrieved.
- In the example above, the sync_task_view simulates a blocking operation using time.sleep(5), which means the server will wait for 5 seconds before responding. During this time, the thread handling the request is blocked.

```
# views.py (asynchronous)

import asyncio
from django.http import JsonResponse

async def async_task_view(request):
    # Simulate a non-blocking I/O-bound task (e.g., an external API call)
    await asyncio.sleep(5)  # This simulates a delay of 5 seconds asynchronously
    data = {'message': 'This is an asynchronous task'}
    return JsonResponse(data)

```
- Here’s the same task but handled asynchronously, which means that while the task waits (e.g., an API call), other tasks can be processed without blocking.
- In this case, the async_task_view uses await asyncio.sleep(5) to simulate the same 5-second delay, but this delay is non-blocking. While waiting for the 5 seconds to pass, the server can handle other requests.

> 10. What is self join in SQL

- A self-join in SQL allows you to join a table to itself.
- This enables you to compare rows within the same table as though you were joining two different tables. Self-joins are useful for comparing values in a hierarchical table, finding duplicate values, or comparing rows with other rows in the same table.
```
select a.id, a.first_name, a.email, b.email  
from auth_user as a
join auth_user as b
on a.first_name = b.first_name and a.email != b.email
```
> 11. What is diffrent between having and where in SQL

-  both WHERE and HAVING clauses are used to filter results, but they are applied at different stages of query execution and serve different purposes.

1. WHERE 
- Applied before the data is grouped.
- Can be used with regular columns, but cannot be used with aggregate functions (like COUNT, SUM, AVG, etc.).

2. HAVING 
- Applied after the data is grouped using GROUP BY.
- Filters the aggregated results (e.g., groups of rows) after aggregation.
- Typically used with aggregate functions but can also filter by regular columns, especially in conjunction with GROUP BY.

`WHERE` : Used to filter individual rows before grouping or aggregation.
```
SELECT department, COUNT(*) AS employee_count
FROM employees
WHERE salary > 50000  -- Filters employees with salary greater than 50000
GROUP BY department;
```
`HAVING` : Used to filter groups of rows after aggregation.
```
SELECT department, COUNT(*) AS employee_count
FROM employees
GROUP BY department
HAVING COUNT(*) > 5;  -- Filters departments with more than 5 employees
```

> 12. What is lambda function in python.

- A lambda function in Python is a small, anonymous function defined using the lambda keyword. It is typically used for simple, short operations that you don't need to reuse elsewhere. Unlike regular functions defined with the def keyword, lambda functions can only contain a single expression, and the result of this expression is automatically returned.

When to use:
- When you need a small, simple function for a short period of time.
- When the function logic can be expressed in one line.

```lambda arguments: expression```

arguments: A comma-separated list of arguments.\
expression: An expression executed and returned.

```
add = lambda x, y: x + y
print(add(2, 3))  # Output: 5

        like 

def add(x, y):
    return x + y
```
Example:
```
numbers = [1, 2, 3, 4]
squared = map(lambda x: x**2, numbers)
print(list(squared))  # Output: [1, 4, 9, 16]

numbers = [1, 2, 3, 4, 5, 6]
evens = filter(lambda x: x % 2 == 0, numbers)
print(list(evens))  # Output: [2, 4, 6]

pairs = [(1, 'one'), (2, 'two'), (3, 'three')]
sorted_pairs = sorted(pairs, key=lambda x: x[1])
print(sorted_pairs)  # Output: [(1, 'one'), (3, 'three'), (2, 'two')]
```