# Fault Tolerant RAFT
By request of MIT's 6.824 Distributed Systems' instructors, I have chosen to keep the code private as current students are not permitted to view the codes of others. Please request to see the source code and I will make it available, thank you for your understanding.

## Motivation for project:
I am interested in algorithmic, optimization, and concurrency projects as I like to think myself foremost a computer scientist since I was a mathematics major that turned to philosophy. This project involved using locks and semaphores, condition variables to prevent unnecessary CPU utilization, go threads which are multiplexed and act as pools, and zero-copy for greater performance in real-time settings.
  
## Background Context:
A replicated service like raft achieves fault tolerance by storing complete copies of its state (i.e., data) on multiple replica servers. Replication allows the service to continue operating even if some of its servers experience failures (crashes or a broken or flaky network, simulated by labrpc and enforced via test cases). The challenge is that failures may cause the replicas to hold differing copies of the data. Raft organizes client requests into a sequence, called the log, and ensures that all the replica servers see the same log. Each replica executes client requests in log order, applying them to its local copy of the service's state. Since all the live replicas see the same log contents, they all execute the same requests in the same order, and thus continue to have identical service state. If a server fails but later recovers, Raft takes care of bringing its log up to date (optimized via binary search). Raft will continue to operate as long as at least a majority of the servers are alive and can talk to each other. If there is no such majority, Raft will make no progress, but will pick up where it left off as soon as a majority can communicate again.

### Thank you for visiting my project. 
