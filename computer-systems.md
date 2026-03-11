# Computer Systems

## Memory Layout

- Disk and memory notes mentioned:
  - Test data / global variables / static data
  - Heap for persisting dynamically allocated data
  - Stack for local variables, function arguments, and pointers

## Processes and Threads

- A process can contain several threads.
- Common thread roles include manager threads and worker threads.
- CPU virtualization makes each thread behave as if it were running alone.
- Threads in the same process share:
  - Text segment
  - Data segment
  - Heap
- Each thread has its own stack.

## Process States

- `Running`
- `Ready`
- `Blocked`

## Filesystems

- Mount points connect filesystems into the directory tree.

## CPU Scheduling

- `SJF`: Shortest Job First
- `STCF`: Shortest Time to Completion First
- `RR`: Round Robin, using a fixed time interval
- `MLFQ`: Multi-Level Feedback Queue
