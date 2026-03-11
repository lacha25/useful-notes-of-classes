# Concurrency

## Core Idea

- Concurrency means doing something else while waiting for a task.
- Parallelism and concurrency can improve throughput and reduce latency.

## Shared-State Risks

- A data race happens when two threads access the same mutable variable without proper synchronization.
- A critical section is code that accesses shared memory where only one thread should operate at a time.

## Mutual Exclusion

- Mutual exclusion means only one thread can execute a critical section at once.
- A lock protects the critical section.
- Typical lock usage:
  - `lock(&mutex)`
  - `unlock(&mutex)`

## Locking Approaches

- Interrupt lock:
  - Disables interrupts during the lock
  - Can be dangerous because of context switching issues
- Software lock:
  - Uses a shared variable such as `locked = true`
  - Can fail if a thread is interrupted before updating the flag correctly
- Test-and-set:
  - Updates the lock state as one atomic instruction
- Mutex:
  - Waiting threads go to sleep instead of spinning
  - Lock holders wake them up later
  - Common API family: `pthread_mutex_*`

## Deadlock and Starvation

- Deadlock happens when each process waits for another to release what it needs.
- Example:
  - Process A has resource 1 and needs resource 2
  - Process B has resource 2 and needs resource 1
- Common mitigations:
  - Use timeouts
  - Acquire locks in the same order
  - Avoid unsafe wait patterns
- Starvation happens when a thread keeps getting denied access.

## Semaphores

- A semaphore acts like a bouncer controlling how many threads can proceed at the same time.
