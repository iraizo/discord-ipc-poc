# discord-ipc-poc
Reading out sensitive account data from IPC socket

### How does it work?
Discord opens an local websocket that exists for the RPC also called RPCServer (which we are gonna exploit)
if you send an packet  with the cmd `OVERLAY` and some args (read source code hint: L59) it will give you back an packet
with the cmd `DISPATCH` and the `PID` you gave in `args`, that packet will give you the whole user object and token, this only works on windows
as of right now since its the only OS where the overlay works, i do not know how to get it working on linux yet.

<img src="http://pays.host/uploads/68e43db6-db36-46c3-b69e-540a857770cf/1BCQ8TOn.png">
