* Multiprocessing and multithreading both are used to achieve multitasking
* threads are light weight VS process
* context switching is fast for thread
* use shared memory area

## concurrency vs parallelism
* concurrency is the task of running and managing multiple computation at the same time. it can be done on single processing unit
* parallelism:is the task of running multiple computation simultaneously

## how to create a thread
1. By extending thread class
2. implement runnable interface

## life cycle
1. New stage: instance of thread is create but not started by invoking the start method
2. Runnable: after invoking the start method & before selected by schedular to run
3. Running: after selected by schedular
4. Non Runnable: Thread alive, not eligible to run
5. Terminate:run() method has exited
