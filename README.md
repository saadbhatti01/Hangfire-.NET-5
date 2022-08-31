# Hangfire-.NET5
Hangfire is an open-source and well-documented task scheduler for ASP.NET and ASP.NET Core. It’s multi-threaded, easily scalable, and offers a variety of job types. It’s well structured, simple to use, and gives a powerful performance.

#Most Notable Hangfire Features
Comparing to other available schedulers, Hangfire offers a lot of advantages. Among other things, it’s notably easy to install and configure, it uses persistent storage and it has a nice UI dashboard to check up on our jobs at any time. It supports multiple queue processing and we can also explicitly choose which queue we want to use for a specific job.
Because the persistent storage saves the job state, we also have a great bonus – job retries. This feature helps make sure our jobs finish executing even if they run into a transient exception or if the dedicated application pool crashes. If a job fails, Hangfire will try to run it again as soon as possible.

How Hangfire Works?
There are three main components of Hangfire architecture – the client, the server, and the storage. They are closely intertwined in the whole process and depend on each other.

The Role of Each Component
Let’s see what each component is responsible for:

Hangfire client – These are the actual libraries inside our application. The client creates the job, serializes its definition, and makes sure to store it into our persistent storage.
Hangfire storage – This is our database. It uses a couple of designated tables that Hangfire creates for us. It stores all the information about our jobs – definitions, execution status, etc. Hangfire supports both RDBMS and NoSQL options, so we can choose which one works for our project. By default, it uses SQL Server, but any other supported option is also easy to configure.
Hangfire server – The server has the task of picking up job definitions from the storage and executing them. It’s also responsible for keeping our job storage clean from any data that we don’t use anymore. The server can live within our application, or it can be on another server. It always points to the database storage so its location doesn’t play a role, but this diversity can be very useful.
Since Hangfire is built as generic as possible, we can also extend some of its parts like storage implementation, job creation, or job activation processes manually to fit specific needs.

The Hangfire Workflow
The workflow between components is pretty simple:

After we specify our task in the code and call the appropriate Hangfire method to create it, the Hangfire client creates the job and stores it in the database. The control then returns to the application so the main thread can continue with its work.
When a job is in the storage, the server picks it up and creates a background thread to process the fetched job.






###Copied from internet#####
