# Reasons for concurrency and parallelism


To complete this exercise you will have to use git. Create one or several commits that adds answers to the following questions and push it to your groups repository to complete the task.

When answering the questions, remember to use all the resources at your disposal. Asking the internet isn't a form of "cheating", it's a way of learning.

 ### What is concurrency? What is parallelism? What's the difference?
 > Concurrency is when things appear to be run at the same time, but they are actually not, it is just that we can not tell by looking at it. Parallelism is when things are really running at the same time, for example with multicores.

 ### Why have machines become increasingly multicore in the past decade?
 > Because the rate of clock speed improvements slowed, so for improving overall processing performance it is important to use multicores.

 ### What kinds of problems motivates the need for concurrent execution?
 (Or phrased differently: What problems do concurrency help in solving?)
 > When it requires that different tasks to be run at the same time independently.

 ### Does creating concurrent programs make the programmer's life easier? Harder? Maybe both?
 (Come back to this after you have worked on part 4 of this exercise)
 > *Your answer here*

 ### What are the differences between processes, threads, green threads, and coroutines?
 > processes: OS-managed concurrent, exist within their own address space.
 threads: OS-managed, a form of concurrent processing.
 green threads: user-space projections of the same concept as threads, but not OS-managed.
 coroutines: a form of sequential processing.

 ### Which one of these do `pthread_create()` (C/POSIX), `threading.Thread()` (Python), `go` (Go) create?
 > They all create threads.

 ### How does pythons Global Interpreter Lock (GIL) influence the way a python Thread behaves?
 > GIL is a mutex, that prevents multiple threads from executing phthon bytecodes at once. So only one thread can be in a state of execution.

 ### With this in mind: What is the workaround for the GIL (Hint: it's another module)?
 > By using the multiprocessing module. It creates another process.

 ### What does `func GOMAXPROCS(n int) int` change?
 > It sets the maximum number of CPUs that can be executing simultaneously.
