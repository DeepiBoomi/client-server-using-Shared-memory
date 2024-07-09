This project consists of a client-server application implemented in C. The server can handle multiple clients concurrently using threads, and clients can send messages to the server. The server uses shared memory to store the messages received from clients, and a semaphore for synchronization.

Features
      1.Multithreaded server capable of handling multiple clients.
      2.Shared memory for inter-process communication.
      3.Semaphore for synchronizing access to shared memory.
      4.Clients can send messages to the server, which are echoed back.
Prerequisites
      1.GCC (GNU Compiler Collection)
      2.POSIX thread library
      3.Socket programming libraries
      4.Linux-based operating system (recommended)
Files
      1.server.c: Contains the server-side code.
      2.client.c: Contains the client-side code.
Compilation
      To compile the server and client code, use the following commands:

                 gcc -o server server.c -lpthread -lrt
                 gcc -o client client.c
Usage:
     1.Running the Server:
           Start the server by executing the following command:
                    ./server
           The server will start listening on port 9090.
    2.Running the Client
            Start the client by executing the following command:
                    ./client
            The client will attempt to connect to the server running on 127.0.0.1 (localhost). If your server is running on a different IP, change the SERVER_IP macro in client.c.
            Enter messages to send to the server. The server will echo the messages back to the client.
            To quit the client, enter Q or q.
