
# Lamports Mutual Exclusion Algorithm

Design and implement a distributed system which consists of three server processes and five client processes. Assume that each file is replicated on all the servers, and all replicas of a file are consistent in the beginning. A client can perform a READ or WRITE operation on the files. READ operation involves only one server that has the target file and the server is chosen randomly by a client. WRITE involves all servers that have a copy of the target file and all of them should be updated in order to keep the replicas consistent. READ/WRITE on a file can be performed by only one client at a time. However, different clients are allowed to concurrently perform a READ/WRITE on different files. In order to ensure this, implement Lamport’s mutual exclusion algorithm among clients so that no READ/WRITE violation could occur. The operations on files (hosted by servers) can be seen as critical section executions.
To host files, create separate directory for each server. The servers must support following operations and reply to the clients with appropriate messages –
1. ENQUIRY : A request from a client for information about the list of hosted files. 2. READ: A request to read last line from a given file.
3. WRITE: A request to append a string to a given file.
The set of files does not change during your program’s execution. Also, assume that there is no server failure during your program’s execution.


## Getting Started
1. Copy Server.java, Client.java to FolderPath.
2. Compile and run Server.java on machines dc09, dc10 and dc11 using below commands
   javac Server.java 	(for compiling)
   java Server <Node_Number>	(Node_Numbers: 1 for dc09, 2 for dc10, 3 for dc11) 
3. Compile and run Client.java on machines dc12, dc13, dc14, dc15 and dc16 using below commands
   javac Client.java 	(for compiling)
   java Client <Node_Number>	(Node_Numbers: 1 for dc12, 2 for dc13, 3 for dc14, 4 for dc15, 5 for dc16) 
4. Each of the 5 clients performs 10 random Read/Write operations and prints the output


### Prerequisites

Language used: Java
Version: Java 9.0.1

## Config
FolderPath = "/home/013/n/nx/nxk174230/AOSProject1/"
Server1FolderPath = "/home/013/n/nx/nxk174230/AOSProject1/Server1"
Server2FolderPath = "/home/013/n/nx/nxk174230/AOSProject1/Server2"
Server3FolderPath = "/home/013/n/nx/nxk174230/AOSProject1/Server3"

Machines used for server processes:  "dc09.utdallas.edu",
				     "dc10.utdallas.edu",
				     "dc11.utdallas.edu"

Machines used for client processes:  "dc12.utdallas.edu",
				     "dc13.utdallas.edu",
				     "dc14.utdallas.edu"
				     "dc15.utdallas.edu"
				     "dc16.utdallas.edu"

