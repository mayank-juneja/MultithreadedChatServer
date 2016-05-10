Peer to Peer Chat Service Program Version 1.0 12/07/2014
author: Mayank Juneja

OBJECTIVE
------------------
- Build a peer-to-peer chat and file sharing service, where multiple clients will be able to log into a central server,and subsequently share files with each other directly.

GENERAL USAGE NOTES
--------------------------------------
- Navigate to file location in command prompt.
- Run the server python file.
- Run Client python file in format: "python client.py hostname port" where host name is localhost and port number is 9090 (as server.py runs on this port)
- After client is connected to server you can either connect multiple clients by repeating the above step in new command prompt.
- Chat service usage description is as follows:
	- Enter "GET_CLIENT_LIST" to request list of active clients.
	- Enter "GET_CLIENT_INFO <username>", with username of a client to connect to
	- CLIENT_LIST<name1, name2, ... > tells names of active clients'
	- Enter "SEND_FILE<file path>" to send any file from respective path'
	- Enter "CLOSE_SESSION" to stop communicating with any client'
	- Enter "DISCONNECT_CLIENT" to disconnect from chat service'
	- Enter "#HELP" anytime to read instructions again'

FRAMEWORK DESIGN
----------------------------------
- Initially when client program is run, it is connected to server by default.
- Server asks if it is new or returning user and server authenticates if it is a returning user.
- User can ask list of connected clients.
- User can connect to clients using "GET_CLIENT_INFO<another user name>".
- After connection is done, user can chat or send files to other user.
- All the recieved files are stored in the home location of the program.
- Server keeps listening to all the connected users. Whenever any user closes its chat session using "CLOSE_SESSION", it by default connect sends all the further request to server.
- User can leave the service when not in chat session by entering  "DISCONNECT_CLIENT".

VERSION INFORMATION
-------------------------------------
- This Version of Web Server is developed using Python 2.7 on Linux VM.
- This version includes a basic file sending functionality whoch will nnot work on big sized files.

References
-----------------
- http://www.w3.org/Protocols/rfc1945/rfc1945
- http://www.pythonforbeginners.com/
- https://wiki.python.org/
- http://stackoverflow.com/questions/20242434/how-to-run-python-scripts-on-a-web-servere-g-localhost
- http://ilab.cs.byu.edu/python/socket/echoserver.html

----------------------------------------------------------------------------------------------------------------------------
Mayank Juneja can be reached at:

Voice:	530-820-2311
E-mail:	mayank.juneja@colorado.edu
