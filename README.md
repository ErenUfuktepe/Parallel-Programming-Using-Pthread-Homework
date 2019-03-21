# Parallel-Programming-Using-Pthread-Homework

The main thread begins by starting a user-specified number of threads that immediately go to sleep
in a condition wait (the worker threads are idle at first).
The main thread generates tasks to be carried out by the other threads. A task is either an insert, a
delete, or a search a value in a sorted list (in ascending order) with no duplicates. Each time the
main thread generates a new task by adding it to a task queue, it awakens a thread with a condition
signal. When a thread is awakened, it pulls a task from the queue and processes it. When a thread
finishes executing its task, it should return to a condition wait. When the main thread completes
generating tasks, it sets a global variable indicating that there will be no more tasks, and awakens all
the threads with a condition broadcast.

Compile : gcc taskqueue.c -o out -lpthread
