# Lamports Mutual Exclusion Algorithm

## Distributed System: <br />
5 Client processes and 3 Server processes consisting a set of files on which a client can perfom READ/WRITE operations.

## Assumptions: <br />
- Each file is replicated on all the 3 servers and all replicas of a file are consistent in the beginning.
- The set of files does not change during program’s execution. 
- There is no server failure during the program’s execution.

## Lamports Mutual Exclusion Algorithm
A client can perform a READ or WRITE operation on the files. READ operation involves only one server that has the target file and the server is chosen randomly by a client. Whereas WRITE involves all servers that have a copy of the target file and all of them will be updated in order to keep the replicas consistent. Hence, the critical section will be READ/WRITE operation on files.

Lamport's Mutual Exclusion algorithm is implemented among the clients to avoid READ/WRITE violations on the files. This algorithm ensures that READ/WRITE on a file is performed by only one client at a time. But different clients are allowed to concurrently perform a READ/WRITE on different files. 

The Server processes support the following operations:
1. ENQUIRY : A request to return the list of hosted files.
2. READ: A request to read last line from a given file.
3. WRITE: A request to append a string to a given file.


## Getting Started
Step 1: Copy Server.java to 3 different machines and Client.java to 5 different machines <br />

Step 2: Compile and run Server.java on all server machines using below commands <br />

   ```
   javac Server.java 	
   ```
   ```
   java Server <Node_Number>	
   ```
   Node_Numbers: 1 for Server1, 2 for Server2, 3 for Server3 <br />
   
Step 3: Compile and run Client.java on all client machines using below commands <br />
   ```
   javac Client.java 	
   ```
   ```
   java Client <Node_Number>	
   ```
   Node_Numbers: 1 for Client1, 2 for Client2, 3 for Client3, 4 for Client3, 5 for Client5 <br />
   
Step 4: Each of the 5 clients performs 10 random Read/Write operations and prints the output <br />

### Prerequisites
8 different machines to serve as 3 server processes and 5 client processes <br />
Java 9.0.1
