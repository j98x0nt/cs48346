java c
CS 4470 Programming Assignment 1
A Chat Application for Remote Message Exchange
1. Objective
Getting Started: Familiarize yourself with socket programming.
Implement: Develop a simple chat application for message exchange among remote peers.
2. Getting Started
Socket Programming: Beej Socket Guide:http://beej.us/guide/bgnet
3. Implement
3.1 Programming environment
You will write C/C++, Java or Python code that compiles in Linux (e.g., Ubuntu) or Windows systemNOTE: You should (1) use TCP Sockets in your peer connection implementation; (2) use the select() API or multi-threads for handling multiple socket connections; (3) integrate both client-side and server side code into one program and run on each peer.
3.2 Running your programYour process (your program when it is running in memory) will take one command line parameters. The parameter indicates the port on which your process will listen for the incoming connections. For example, if your program is called chat, then you can run it like this:  ./chat 4545, where 4545 is the listening port. Run your program on three computers and perform. message exchange.
3.3 Functionality of your programWhen launched, your process should work like a UNIX shell. It should accept incoming connections and at the same time provide a user interface that will offer the following command options: (Note that specific examples are used for clarity.)
1. help Display information about the available user interface options or command manual.
2. myip Display the IP address of this process.
Note: The IP should not be your “Local” address ( 127.0.0.1). It should be the actual IP of the computer.
3. myport Display the port on which this process is listening for incoming connections.
4. connect   : This command establishes a new TCP connection to the specified  at the specified < port no>. The  is the IP address of the computer. Any attempt to connect to an invalid IP should be rejected and suitable error message should be displayed. Success or failure in connections between two peers should be indicated by both the peers using suitable messages. Self-connections and duplicate connections should be flagged with suitable error messages.5. list Display a numbered list of all the connections this process is part of. This numbered list will include connections  initiated by  this process  and  connections  initiated  by  other  processes.  The  output  should display the IP address and the listening port of all the peers the process is connected to.
E.g.,
id: IP address
1: 192.168.21.21
2: 192.168.21.22
3: 192.168.21.23
4: 192.168.21.24Port No.4545
54545000
50006. terminate  This command will terminate the connection listed under the specified number when LIST is used to display all connections. E.g., terminate 2. In this example, the connection with  192.168.21.22  should  end. An error message is displayed if a valid connection does not exist as number 2. If a remote machine terminates one of your connections, you should also display a message.7. send   (For example, send 3 Oh! This project is a piece of cake). This will send the message to the host on the connection that is designated by the number 3 when command “list” is used. The message to be sent can be up-to 100 characters 代 写CS 4470 Programming Assignment 1C/C++
代做程序编程语言long, including blank spaces. On successfully executing the command, the sender should display “Message sent to ” on the screen. On receiving any message from the peer, the receiver should display the received message along with the sender information.
(Eg. If a process on  192.168.21.21  sends a message to a process on  192.168.21.22 then the  output on 192.168.21.22 when receiving a message should display as shown:
Message received from 192.168.21.21
Sender’s Port: 
Message: “”
8. exit Close all connections and terminate this process. The other peers should also update their connection list by removing the peer that exits.
4. Submission and Grading
4.1 What to Submit
Your submission should contain a zip file – Name it as < your cin_name>.zip:
•    All  source  files  (.h  and  .c  or  .cc  or  .java or  .py files), including Makefile. Note: name your main program as chat.c or chat.cc or chat.java or chat.py.
4.2 How to submit
Make submission on Canvas.
4.3 Grading Criteria
•    Each group needs to show a demo AFTER the due date. All the members should attend the demo, and describe their coding contribution in this project.
•    Correctness of output. Please refer to the grading guidelines for more details.
•    Organization and documentation of your code.
4.4 Important Key Points:
•    There is just one program. DON’T submit separate programs for client and server.
•    Error Handling is very important – Appropriate messages should be displayed when something goes bad.
•    DON’T ASSUME. If you have any doubts in project description, please come to my office hour.
•     Submission deadline is hard. No extension. Any submission after 23:59pm of Nov. 12th  201 will be considered as late submission.
•    Please do not submit any binaries or object files or any test files.
4.5 Grading Guidelines
For programming assignment 1, we will grade your submission following the below guidelines:
[+10] Codes should be compiled successfully.
[+10] The program should start successfully. To Start: ./chat 
Note: Please handle erroneous input appropriately.
[+5] help command: should display the command manual or user interface options.
[+10] myip command - show the IP address of the laptop that runs the program. Note: 127.0.0.1 is NOT correct and get 0 score for this command.
[+5] myport command: should display the port # that the program is running on.
[+10] connect command: should connect to a max of 3 peers and success message should be displayed.
[+10] list command: should list all the connected peers with relevant details.
[+10] terminate command: should terminate a connection. (To test: terminate a peer, connect to another peer and list, and then connect to 2 more peers and list.)[+15] send command: should send the exact message as typed by the user to another peer as specified in the send command. The received message should be displayed with relevant information as specified.
[+10] exit command: should quit the program. On exiting, the user terminates all the connections. The other peers update their connection list by removing the exit peer.
[+5] Check code documentation.
Note: Please use three different laptops to test your program.





         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
