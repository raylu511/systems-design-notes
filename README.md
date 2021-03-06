# Systems Design 

## What is a distributed system? 

A distributed system is a computing enviornment in which many components are spread across multiple computers on a network. 

In other words, a distributed system is a bunch of computers on a network that coordinate with each other to complete tasks more efficiently. 
When a user requests some data, the thousands of servers/computers have to communicate with each other to locate that information and then returns it as a response. 

## Networks aren't reliable

When you have thousands of servers communicating with each other, networks will often break.

## Latency

There's going to be some latency/delay when servers communicate with each other.

## Low bandwidth

Bandwidth refers to the amount of data that can be transfered between severs in bits per sec (Bps).
Moving a bunch of data between servers will become an issue because of low bandwidth.

## Data transport cost

Moving data across servers can be expensive. 


## Common distributed system characteristics

### No shared clock

Different computers will run on different times. This leads to a common issue called Clock Drift which refers to timers on computers to be out of sync which will lead to ordering of events. Clock drifts can move negatively or positively affecting timestamps of requests and responses. This is a big issue for stock exchanges or bidding websites like Ebay. 
Google handles this issue by using a combination of GPS receivers and the atomic clock, and they call this True time.

### No shared memory

Each computer will have their own hardware (ram, storage).
If some computer needs information from another computer on the same network, it needs to request that data from that computer.

### Shared resources

Kind of goes hand and hand with no shared memory. 
Computers on the same network should be able to share hardware, software or data efficiently.

### Concurrency and consistency

Computers on the same network should be able to work together and simultaneously.
Multi-threading is a technique that allows concurrency and consistency among servers.

### Needs to be able to communicate

Computers on the same network will often share information and they will need to communicate for this to happen. 
There's often some type of protocol or format the distributed systems uses to handle this. 

### Benefits

More reliable.
Scalability.
Lower latency, increased performance
Cost effective
