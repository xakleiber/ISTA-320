--Discussion 02

--C#

--Name: Xavier Kleiber

 - 1. What is an asynchronous method? When the book talks about a contract, what is the contract and who is it with?
	- A method that does not block the current thread on which it starts to run. A contract expects the method to return control to the calling environment quite quickly and to perform its work on a separate thread

 - 2. What can be the problem with decomposing a series of discrete method calls into a set of tasks, such as we saw in chapter 23?
	- UI can become unresponsive.

 - 3. What can be the problem with decomposing a series of discrete method calls into a set of continuations? When does the last continuation "complete" as compared to the previous continuations? What problem might this cause?
	- The signatures of the methods have to change to accommodate the requirements of continuations. The last continuation completes after the previous continuations. Any following methods do not wait for the continuations to complete.

 - 4. What might be the problem with implementing the previous solution as a continuation passing a delegate? What would be your interpretation with this error message: "The application called an interface that was marshaled for a different thread."?
	- It can happen if you attempt to get information from a different thread.

 - 5. The book suggests a solution using a continuation delegate calling another continuation delgate via an anonymous function. What does the book identify as a problem with this suggested solution?
	- This works, but it is messy and difficult to maintain.

 - 6. What does the async modifier do? What does the await operator do?
	- The async modifier indicates that a method contains functionality that can be run asynchronously. The await operator specifies the points at which this asynchronous functionality should be performed.

 - 7. What is an awaitable object? Be specific.
	- -The await operator specifies the points at which this asynchronous functionality should be performed. It specifies a point at which the C# compiler can split the code into a continuation.

 - 8. In a method defintion, how do you create and run a Task and return a reference to the Task? What is the type of such a method? What does the method return?
	- 

 - 9. How do you define method calls in the implementation of an asunc method? Specifically, you must define a task, you must run the task, you must implement the task, and you must await the task. What is the syntax for doing this?

 - 10. What is the difference between decomposing a series of method calls that do not return values, and a series of method calls that return values? What is the Result property of a method that returns a value? How do you use the await operator in this circumstance?

 - 11. What is the difference between the await operator and the Wiat method?