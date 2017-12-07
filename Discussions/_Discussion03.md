--Discussion 03

--C#

--Name: Xavier Kleiber

 - 1. What are the two scenarios in which you can use PLINQ to speed up operations? Why does using PLINQ in these scenarios speed up processing?
	- Parallelization & Sequential modes. It executes the queries in parallel.

 - 2. How does AsParallel qualify as an extension method? First, explain what an extension method is and how you define extenssion methods, and then explain why AsParallel qualifies as an extension method.
	- An extension method is a method added to an object after the original object was compiled. The modified object is often a class, a prototype, or a type. The AsParallel method returns a ParallelQuery object that acts in a similar manner to the original enumerable object, except that it provides parallel implementations of many of the LINQ operators, such as join and where.

 - 3. How do you cancel a PLINQ query before it finishes? Be specific with respect to the variables and methods used for the cancellation operation, and how the variables and methods are used.
	- You specify a CancellationToken object from a CancellationTokenSource and use the WithCancellation extension method of the ParallelQuery.

 - 4. Why is it important to synchronize concurrent access to a server? Give an example of a specific condition that will cause an error in you application if concurrent acces is not synchronized.
	- Attempts to obtain a mutual-exclusion lock over the specified object, and it blocks if this same object is currently locked by another thread.

 - 5. What does the lock statement do?
	- Attempts to obtain a mutual-exclusion lock over the specified object, and it blocks if this same object is currently locked by another thread.

 - 6. This is not in the book. Define mutex, define semaphore, and explain the difference between them.

 - 7. What does it mean to say that some collection classes are not thread safe? Explain how not being thread safe may lead one of these collection classes to produce a malfunction in the program.
	- If a piece of code fails to function correctly during simultaneous execution by multiple threads./ It must satisfy the need for multiple threads to access the same shared data, and the need for a shared piece of data to be accessed by only one thread at any given time.

 - 8. Explain how thread safe collection classes are made thread safe.
	- A piece of code is thread-safe if it functions correctly during simultaneous execution by multiple threads.

 - 9. Why are thread safe classes slower than non-thread safe classes? Be specific.
	- Locking and unlocking data to guarantee thread safety adds to the overhead of the calling methods.