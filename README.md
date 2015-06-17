# portforward
A portforwarding service, support both local port forwarding and remote port forwarding

## Install  
`npm install -g portforward`  


## Usage  

### Mode1: Local port-forwarding  
`portforward <from> <to>`  

For example, if you want to forward port 5566(For external) to port 80(For internal)  
`portforward 5566 80` 
So `http://localhost:5566` will forward to `http://localhost:80`  

### Mode2: Remote port-forwarding  
`portforward <from> <to> <remoteHost>`  

Example1: if you want to forward local port 5566 to remote host `whatismyip.org` port 80
`portforward 5566 80 whatismyip.org`  
So `http://localhost:5566` will forward to `http://whatismyip.org:80`  
  
Example2: if you want to forward local port 7788 to remote host `ptt.cc` port 22  
`portforward 5566 22 ptt.cc`  
So `ssh localhost -p 5566` will act like `ssh ptt.cc`

Example3: Act as relay server  
You can use this service to turn your host into relay server  

