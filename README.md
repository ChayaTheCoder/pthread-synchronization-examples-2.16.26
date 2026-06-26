# pthread-synchronization-examples-2.16.26
## Overview
This collection of C++ programs demonstrates **thread synchronization techniques** using the POSIX `pthread` library. Each example explores a different approach to managing concurrent access to shared data. Each file focuses on a different mutual‑exclusion strategy, showing how threads safely share data and avoid race conditions. These examples reflect core Operating Systems concepts such as critical sections, busy waiting, mutex locks, and software‑based synchronization algorithms.

File Breakdown
1. pthread-data-sharing-mutex.cpp
Concept: Hardware‑supported mutual exclusion using a pthread_mutex_t
What it demonstrates:
Protecting a shared variable (count) using a mutex

Locking before entering a critical section

Unlocking after leaving the critical section

Preventing race conditions in a multi‑threaded environment


2. pthread-data-sharing-mutex-peterson.cpp
Concept: Peterson’s Algorithm — a classic software‑only mutual exclusion solution
What it demonstrates:
Two‑thread synchronization without hardware support

Use of interested[] flags

Use of a shared turn variable

Busy waiting (spinlock behavior)


3. pthread-data-sharing-mutex-strict-alternation.cpp
Concept: Strict Alternation — the simplest (but flawed) synchronization method
What it demonstrates:
Threads take turns entering the critical section

Uses a shared turn variable

No fairness or performance guarantees


4. pthread-data-sharing-mutex-os-call.cpp
Concept: Using OS‑level mutex calls to protect shared data
What it demonstrates:
Real‑world use of pthread_mutex_lock() and pthread_mutex_unlock()

Thread creation with pthread_create()

Thread joining with pthread_join()

Safe incrementing of shared variables



