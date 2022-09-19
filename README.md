# MiniMon

Minimal Monitoring

## Features
* multiple machines
* minimal dependencies
* easily extendable : the sky is the limit

## Installation
Both the client and server have the following dependencies:
* JQ
* socat

### MiniMon Server
To install the server download the minimon-server script and run it
see [usage](#Usage)

### MiniMon Client
To install the server download the minimon-server script and run it
see [usage](#Usage)

## Usage
to start the server use the following command
```bash
./minimon-server -p <port> -c <path/to/cert.pem> -t <path/to/taskfolder> -m <path/to/monitorfolder> -v <0/1> 
```

to start the client use the following command
```bash
./minimon-client -i <ip> -p <port> -c <path/to/cert.pem> -t <path/to/taskfolder> -v <0/1> -d <seconds>
```

## Extending 
Extending minimon is possible by writing custom scripts and place it in your tasks folder.
The client will find the task and add it to the json.
see [sysinfo](./Example-Tasks/Client/sysinfo)

The server also needs a custom script to parse the new data.
see [sysinfo](./Example-Tasks/Server/sysinfo)

The server can also be extended by the creation of monitors:
Monitors are server sided tasks to check if the required service/host is reachable.
see [ping](./Monitors/ping)


