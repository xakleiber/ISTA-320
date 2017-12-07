--Discussion 06

--C#

--Name: Xavier Kleiber

 - 1. Can a UWP app directly access a relational database by using technologies provided by Microsoft? Why or why not?
	- No, it eliminates dependencies that a UWP app might have on external resources.

 - 2. Describe how the Entity Framework works.
	- It creates a model between a relational database and your app.

 - 3. What is the difference between the code-first and the database-first approaches to developing UWP apps?
	- In the database-first approach, the Entity Framework generates classes based on the definitions of tables in the database. The Entity Framework also provides a code-first approach; that strategy can generate a set of tables in a database based on classes that you have implemented in your app.

 - 4. What is a partial class? Why would we want to create partial casses?
	- A partial class is a class in which the code is split across one or more source files. This approach is useful for tools such as the Entity Framework because it enables you to add your own code without the risk of having it accidentally overwritten if the Entity Framework code is regenerated at some point in the future.

 - 5. Describe a RESTful web api. (Not in book.) Write a brief description of Representational State Transer. What problem was it designed to solve?
	- REST stands for ‘Representational State Transfer’ and it is an architectural pattern for creating an API that uses HTTP as its underlying communication method.

 - 6. Give a brief description of the functionalities of these HTTP commands: GET, POST, PUT, DELETE.
	- GET retrieves, POST creates, PUT modifies, DELETE removes.