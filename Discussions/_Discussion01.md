--Discussion 01

--C#

--Name: Xavier Kleiber

 - 1. List two reasons for multitasking, and explain the rationale for them.
	- 1. Improve responsiveness.
	- 2. Improve scalability.

	- A long-running operation may involve tasks that do not require processor time.
You can improve scalability by using the processing resources available to reduce the time required to do the task.

 - 2. Explain Moore's law. What does Moore's law have to do with multitasking?
	- Moore's law was an observation by Gordon Moore that simply stated that the number of componenets per integrated circuit would double every two years(originally forecast to every single year, but was revised to be more acurate). More components mean that data is able to be transfered faster.

 - 3. In UWP, what namespace is used as the containter for the multitasking methods?
	- System.Threading.Tasks

 - 4. What is the difference between tasks and threads? Explain.
	- Tasks represent asynchronous operations. Threads are used to complete that operation by breaking the work up into chunks and assigning to separate threads.

 - 5. What is the ThreadPool?
	- The threadpool takes task and schedules them. It takes into account the available processors.

 - 6. What parameters does the Task() constructor take?
	- Action parameters.

 - 7. How do you start a thread?
	- The Start() method.

 - 8. What is the difference between the Start() and Run() methods?
	- Run() starts a task as soon as it's created and Start() is used with a task object.

 - 9. What is the difference between creating independent tasks with Tasks and parallelization with Parallel? Explain.
	- Task parallelization takes multiple tasks and spreads them accross different processor cores. You have less controll over the individual tasks, but it is faster, simpler, and less likely to get errors.

 - 10. Explain how manual cancellation works using a cancellation token.
	- A cancellation token is a request to cancel any number of tasks. It sets the boolean IsCancellationRequest to true to terminate the tasks.