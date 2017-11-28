---
title: CFP
---

## Call for Papers

Consistency is one of the fundamental issues of distributed computing.
There are many competing consistency models, with subtly different power
in principle.
In practice, the well-known Consistency-Availability-Partition
Tolerance trade-off translates to difficult choices between fault
tolerance, performance, and programmability.
The issues and trade-offs are particularly vexing at scale, with a large number of
processes or a large shared database, and in the presence of high
latency and failure-prone networks.
It is clear that there is not one universally best solution.

Possible approaches cover the whole spectrum between strong and eventual
consistency.
Strong consistency (linearizability or serializability, achieved via total ordering) provides familiar and intuitive semantics but requires slow and fragile synchronisation and coordination overheads.
The unlimited parallelism allowed by weaker models such as eventual consistency promises high performance, but divergence and conflicts make it difficult to ensure useful application invariants, and meta-data is hard to keep in check.
The research and development communities are actively exploring intermediate models (replicated data types, monotonic programming, CRDTs, LVars, causal consistency, red-blue consistency, invariant- and proof-based systems, etc.), designed to improve efficiency, programmability, and overall operation without negatively impacting scalability.

This workshop aims to investigate the principles and practice of consistency models for large-scale, fault-tolerant, distributed shared data systems. It will bring together theoreticians and practitioners from different horizons: system development, distributed algorithms, concurrency, fault tolerance, databases, language and verification, including both academia and industry.

Relevant discussion topics include:
 * Design principles, correctness conditions, and programming patterns for scalable distributed data systems.
 * Techniques for weak consistency: session guarantees, causal consistency, operational transformation, conflict-free replicated data types, monotonic programming, state merge, commutativity, etc.
 * Techniques for scaling and improving the performance of strongly consistent systems (e.g., Paxos-based, state machine replication, shared-log consensus, blockchain).
 * How to expose consistency vs. performance and scalability trade-offs in the programming model, and how to help developers choose.
 * How to support composed operations spanning multiple objects (transactions, workflows).
 * Reasoning, analysis and verification of weakly consistent application programs.
 * How to strengthen the guarantees beyond consistency: fault tolerance, security, ensuring invariants, bounding metadata size, and controlling divergence.
 

### Important Dates

|Submission deadline: | February 07, 2018 |
|--------------|--------------------------|
|Notiﬁcation date: | February 19, 2018|
|Camera-Ready: | March 8, 2018|
|Workshop: | April 23, 2018|

