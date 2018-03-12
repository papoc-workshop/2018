---
title: Program
---


The program schedule has not been determined yet.

The list of accepted papers is:

## Ensuring referential integrity under causal consistency
by Marc Shapiro, Annette Bieniusa, Peter Zeller and Gustavo Petri.

Referential integrity (RI) is an important correctness property of a
shared, distributed object storage system. It is sometimes thought
that enforcing RI requires a strong form of consistency. In this
paper, we argue that causal consistency suffices to maintain RI. We
support this argument with pseudocode for a reference CRDT data
type that maintains RI under causal consistency. QuickCheck has
not found any errors in the model.

## Constraining the Eventual in Eventual Consistency
by Jim Bauwens, Florian Myter and Elisa Gonzalez Boix. 

CRDTs are highly available replicated data structures which offer
strong eventual consistency in the face of concurrent operations. 
By their definition, CRDTs eventually converge to a consistent
state given enough time. However, this is not strict enough
for some distributed applications. Current state-of-the-art CRDT
implementations fail to provide programmers with the means to
specify these constraints. As a result, programmers need to write
application-level code which ignores stale or timed-out operations.
In this paper, we introduce a leasing model which allows programmers
to declaratively specify timing constraints for CRDTs. In short,
programmers are able to attach leases to operations on a CRDT
instance. When such a lease expires the underlying implementation
ensures that the operation is eventually canceled for all replicas.

## Towards Affordable Externally Consistent Guarantees for Geo-Replicated Systems
by Manuel Bravo and Luis Rodrigues. 

We propose a novel consistency model called external causality,
which aims at making external consistency affordable for georeplicated
systems. In this short paper, we (i) outline this idea—
informally defining external causality, and (ii) motivate it with two
simple examples that illustrate how developers of cloud services
may benefit from it.

## A Modular Design for Geo-Distributed Querying
by Dimitrios Vasilas, Marc Shapiro and Bradley King.

Most distributed storage systems provide limited abilities for querying data by attributes other than their primary keys. Supporting efficient search on secondary attributes is challenging as applications pose varying requirements to query processing systems, and no single system design can be suitable for all needs. In this paper, we show how to overcome these challenges in order to extend distributed data stores to support queries on secondary attributes. We propose a modular architecture that is flexible and allows query processing systems to make trade-offs according to different use case requirements. We describe adaptive mechanisms that make use of this flexibility to enable query processing systems to dynamically adjust to query and write operation workloads.

## The Pitfalls in Achieving Tagged Causal Delivery
by Georges Younes, Paulo Sérgio Almeida and Carlos Baquero. 

Causal delivery middleware respect causality when delivering messages, but do not provide information about it to the client process. When two messages, m1 and m2 are delivered in sequence to a given process, either they are concurrent or m1 happens-before m2, but the client application is not told which is the case. In some domains, like operation-based CRDTs, this information is useful, and previously we have proposed exposing it in the API of a Tagged Causal Delivery middleware. One could think this would be just a matter of taking some current middleware and exposing the vector-clocks which are internally kept. In this paper we identify some obstacles in doing so, and describe how to overcome them. The essence lies in the role of current middleware, allowing it to tag as ordered some messages that are concurrent, and we describe how it can happen in several interaction models between middleware and client code, either callback-based or with independent threads/processes. This means that vector-clocks in current middleware are not precise to describe happens-before, and cannot be simply exposed in the API.

## Fine-grained Distributed Consistency Guarantees with Effect Orchestration
by Kiarash Rahmani, Gowtham Kaki and Suresh Jagannathan. 

Highly-available distributed applications typically require data to
be replicated over geo-distributed stores that offer weak consistency
guarantees by default. Unfortunately, undesirable behaviors
may arise under weak consistency that can violate application correctness,
forcing designers to either implement complex ad-hoc
mechanisms to avoid these anomalies or by sacrificing performance,
choose to run applications using stronger levels of consistency. In
this paper, we describe a lightweight runtime system that relieves
developers from having to make such tradeoffs. Instead, our approach
leverages declarative axiomatic specifications that reflect
the necessary constraints any correct implementation must satisfy
to guide a runtime consistency enforcement and monitoring
mechanism. Experimental results show that the performance of
our (provably optimal and safe) automatically derived fine-grained
consistency enforcement mechanisms is better than common storeoffered
consistency guarantees.

## Making Consistency More Consistent: A Unified Model for Coherence, Consistency and Isolation
by Adriana Szekeres and Irene Zhang. 

Ordering guarantees are often defined using abstract execution
models. Unfortunately, these models are complex and make different assumptions
about system semantics. As a result, researchers find
it impossible to compare the ordering guarantees of coherence,
consistency and isolation. This paper presents
a simple, unified model for defining ordering guarantees
that is sufficiently general to model a wide range of
systems, including processor memory, distributed storage,
and databases. We define a new single constraint
relationship, result visibility, which formalizes the “appears
to execute before” relationship between operations.
Using only result visibility, we define more than 20 ordering
guarantees from different research areas, including
PRAM, snapshot isolation and eventual consistency
session guarantees. To our knowledge, these
definitions form the broadest survey of ordering guarantees
using a single constraint in the current literature.

## Towards Causal Datacenter Networks
by Ellis Michael and Dan R. K. Ports. 

Traditionally, distributed systems conservatively assume an
asynchronous network. However, recent work on the codesign
of networks and distributed systems has shown that
stronger ordering properties are achievable in datacenter networks
and yield performance improvements for the distributed
systems they support. We build on that trend and ask whether
it is possible for the datacenter network to order all messages
in a protocol-agnostic way. This approach, which we call omnisequencing,
would ensure causal delivery of all messages,
making consistency a network-level guarantee.
