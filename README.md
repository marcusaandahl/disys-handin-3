# disys-handin-3 (Chitty Chat)

## _Team Bastian_

The handin should be ready-to-run without altering any code. However do note that the username for the client is retrived by the local system. Therefore if you initialize multiple clients from the same machine, they will join with a single username.

## Starting the program
1. Run the server from server folder: go run server/server.go
2. Run a client: go run client/client.go

_Note: the server runs on localhost port 5400. This can result in issues if something is already occupying this port. Therefore it can be necessary to manually kill any process that is occupying this port. This can happen if the program is re-run and has not closed appropriatly._
1. If you want to kill the process you can use command: _"lsof -Pn -i4"_
2. Locate the process that is occupying port 5400 (can be seen in the name column if it is using 5400)
3. Kill the process by command: _"kill -9 PID"_ where PID is switched with the process ID found in previous step.

## Client CLI-usage
1. The user can simply type a message in the terminal and hit the return command. This will send the message to the server if it obides by the length restrictions (128 characters). If not an error prompt is returned. 