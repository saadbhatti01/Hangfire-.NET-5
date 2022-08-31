# Hangfire-.NET5
Hangfire is an open-source and well-documented task scheduler for ASP.NET and ASP.NET Core. It’s multi-threaded, easily scalable, and offers a variety of job types. It’s well structured, simple to use, and gives a powerful performance.

#Most Notable Hangfire Features
Comparing to other available schedulers, Hangfire offers a lot of advantages. Among other things, it’s notably easy to install and configure, it uses persistent storage and it has a nice UI dashboard to check up on our jobs at any time. It supports multiple queue processing and we can also explicitly choose which queue we want to use for a specific job.
Because the persistent storage saves the job state, we also have a great bonus – job retries. This feature helps make sure our jobs finish executing even if they run into a transient exception or if the dedicated application pool crashes. If a job fails, Hangfire will try to run it again as soon as possible.
