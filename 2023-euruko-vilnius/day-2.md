# Matz - In Defense of GVL - Keynote

Python Global Interpreter Lock (GIL)
Concurrency (or thread safety)

Thread Safety
Shared data can cause clashes.
Every Read/Write should be protected.

Global VM Lock (GVML)

The issue is multi-core. Ruby was born in 1993 (30 years ago).
30 yeards passed since single-core machines 30 years ago.

Moore's Law

Parallelism means Physical Concurrency.
Speed improvements comes from
GIL prevents Parallelism.
Kill the GIL.
The alternative approach.
Fine Grain Lock (Lock/Unlock around all data acess)

2 problems with the FGL:
1. If you forget to protect any access, you'll get bugs
2. It makes VM more complex, consumer more memory and makes software slower.

They tried to implement it (Python 1.4/Ruby 1.9).

Memory usage/Significant slower performance.
Because of that, the idea was abandoned.

PEP703: Remove the GIL for Python VM, that removes the GIL.

- Reference Counting
- Gine Grained Locks
- Other improvements

- Immortalization
- Biased Reference Counting
- Delayed Reference Counting

Immortalization
They abandon object counting for some objects. Classes or type objects, they remain valid until the end of the programme.

Biased Reference Counting
Reference counts from the same threads.
Reference counts from other threads.

Python used Optimistic Locks.
Container Locks.
Python estimated changes would take 5+ years of implementation.
THey need to change the C API.
They suffered from Python3 - community split into those using Python 2 vs Python 3.

What should Ruby do?
Ruby is used for web apps, and conceptually is single thread (HTTP request)

Web apps are I/O bound. The bottlenec occurs in:
- Network Connection
- DB access
- ...

Removing GVL only works for CPU applications.

We have less motivation for Removing GVL.
GVL is simples/safer/less error prome/less memory/faster.

GVL is bad for CPU bound apps. To address that, Ractor was provided.
GVL -> Per Ractor Lock





# Scott Chacon  - Ask your code
product design for version control

### First principles
Ask why enough times to get to the bottom of things, to the first principles.

- we all use git
- we need version control
- to collaborate and save our work
- our computer doesn't save history of our files or let other peoples to edit

What does version control do?
- backing up / experimenting / collaborating and reviewing / moving bits / archaeology

### Archeology
"what question does this answer?" - to understand what are you building a feature for.

"what are the last commits made?
"what is the last person who touched this line of code?" - question

Who should I talk to.

#### Uncommon questions
"What commits are no this branch that are not yet merged into this other branch?"
`git log main..self-hosted` - to compare branches
`git log self-hosted ^main` - to "exclude" main branch

`git log -S <file> -p` - to see differences

"Where this method was moved from"
`git blame -w -C -C -C -L 15,26 path/to/file`
-w ignore whitespace
-C if I copy a section of file and move it
second -C - in one commit
third -C - in between commits

"What files are most closely related to this file?"

`rugged` - gem to write a script

#### The impossible question
"What PR contributed to this file?"
"What code in other repositories are related to this code?"
"What were the converstaions (in chat/GitHub) my team had around this code before it was merged?"
"What did the author/s reference when writing this?"
"What specifications was this based on?"
"What errors or are commonly created by this code or code related to it?"

What do you want to ask your code?

# Hiroshi Shibata - How resolve Gem dependencies in your code?

## Learning concurrency?
Concurrency is not dark magic.

## Concurrency in Ruby
- Processes
- Ractors
- Threads
- Fibers

Process -> Ractor -> Thread -> Fiber

Threads vs Processes

Lower memory usage / Share JIT / Easy cooperation, communication

Threads Isolation, latency impact

Threads vs Ractos
- Not experimental
- Share mutable objects


- Share mutable objects/Isolation/Share global VM (GVL/GIL)

Theads vs Fibes

Preemptive scheduling (vs cooperative)
Latency impact
- Preemptive scheduling
- More expensive to create
- Require more memory

Gotchas of using threads
Threads in Ruby are concurrent but they are not parallel.

Code execution doesn't go faster with multiple threads.
`gvl-tracing` or `gvltools` to investigate internals of Ruby.

Threads in JRuby and TruffleRuby are parallel.

Thread:Queue to signal.
`done_queue = Queue.new`



