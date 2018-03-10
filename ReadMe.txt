Language used: Java
Version: Java 9.0.1
Contributor: Nandita Koppisetty (Net Id: nxk174230)

Instructions:
1. Copy Server.java, Client.java to FolderPath.
2. Compile and run Server.java on machines dc09, dc10 and dc11 using below commands
   javac Server.java 	(for compiling)
   java Server <Node_Number>	(Node_Numbers: 1 for dc09, 2 for dc10, 3 for dc11) 
3. Compile and run Client.java on machines dc12, dc13, dc14, dc15 and dc16 using below commands
   javac Client.java 	(for compiling)
   java Client <Node_Number>	(Node_Numbers: 1 for dc12, 2 for dc13, 3 for dc14, 4 for dc15, 5 for dc16) 
4. Each of the 5 clients performs 10 random Read/Write operations and prints the output



Information:
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
