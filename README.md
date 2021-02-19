# AKKA LIBRARY USING SCALA !!!

## Day-1

* **@ AKKA, What it is ?** 
>A toolkit, integrate it without having to follow a source code layout. Akka helps us to focus on meeting business needs.  Akka provides Concurrency, Distribution, Fault tolerance out of the box Many programming models do not resolve the major problems associated with designing systems For modern computer architecture. Programming models must be fully distributed. Akka deals with many realities like Components get crashed without responding, messages get lost without a trace on the wire, and network latency fluctuates. So, Akka provides Multithreading, Transparent remote communication between systems and their components, A clustered, high-availability architecture that is elastic. It uses the actor model also gives you a vast set of tools that resolve the distributed/parallel system issues and provide everything where blends tightly and effectively together.


* **@ Why modern systems need a new approach of programming?**
> Earlier, Many Organization developing  the distributed system with the day to day challenges which can not be completely tackle by conventional object-oriented programming(OOPs) that’s why Actor model came into the existence which was proposed by the Carl Hewitt. “A way to manage the parallel processing in a high-performance Network”. Actor model is the reality of modern multi-threaded, multi-CPU architectures.
Actor model focus on the main issues like:
a.	The  Encapsulation Challenge
b.	An  illusion of shared memory on modern computer architectures
c.	The Illusion of a Stack of Call


* **@ The Actor Model Meets New, Distributed Systems Needs. How ?**
 Many programming models or practices do not fulfill the need of the modern distributed System. The actor model focuses on communication, not just the exchange of code that occurs between the organization. The Actor model crux on the supreme points which allow the structure to act in a manner that better suits our model best.

=> Actor fundamental unit of computation that embodies:
1. Processing
2.	Storage
3.	Communication


=> Advantage of Actor model as it allows to:

1.	Enforce encapsulation without resorting to locks.
2.	Use the cooperative entity model that responds to signals, changes state, and sends signals to each other to forward the entire application.
3.	Stop worrying about an executing mechanism that is a mismatch to our world view.


## Day-2

### @ Mechanism OF an ACTOR MODEL !!!

Actors send messages to each other instead of calling methods directly. Actors don’t contain the execution of the thread they just delegate the message from the sender to the destination without blocking and complete more at the same time.
The actor responds to the message and returns the execution when the current message is processed.
The actor acts as an object. Object invokes the method while the actor invokes the messages. Actors execute independently and also react to the incoming messages sequentially but actor different actors currently processing the messages work concurrently with each other which helps not to drive multiple threads into the actor or causing any destruction.
Here, Simply we can say the actor adds the messages in queue form, and the actor is scheduled and marks it to a ready state. The actor picks the message from the front of the queue and modifies it like an internal state and sends it to the other actors available and the actor gets unscheduled. This happens when the actor receives any message. After these messages go into the actor mailbox and the behavior of the actor is a  description of how the actor reacts to messages.
Actor states are immutable and non-shareable, data propagate through messages this is how modern memory hierarchy works. Also, message data is stored on a cached line while keeping the local state and data cached at the original core.

### @ Actor handling the error !!!

Since there is not a call stack in the actor model due to which we need to handle the error in a different way.
The first error, if the actor delegates the task to the other actor i.e delegate actor and it gets failed which may be because of validation issues or user-id didn’t exist etc. Here, the message is not damaged, the actor is the one containing the error. The actor reply to the messages to the sender of the message.
Second, when encountering any internal fault. The actor in the system is organized in a tree-like structure.
When the actor creates another actor became the parent actor of the new actor and if any actor fails or stopped the parent actor decide how  to act. Also if the parent actor stopped all the child actor present also get stopped.

## Day-3

### @ Akka modules and libraries overview 
* Remoting 
* Cluster 
* Cluster Sharding
* Cluster Singleton
* Persistence
* Distributed Data
* Streams 
* HTTP


