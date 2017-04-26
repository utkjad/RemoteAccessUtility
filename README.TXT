Aim - 
Remote exec utility implementation
In a programming language of your choice, write a client and server program that allows selected users to remotely execute selected programs on a server:
Server machine: ./server config-file
config-file allows an Admin to specify users, their passwords, and the programs they are allowed to execute.
Client machine: ./client --server <server ip> --user <username> --password <password> --exec <program to execute>

Requirements -
json
sys
socket
thread
collections
NOte make sure you have you have dependencies. 
#TODO requirement.txt and pip

How to Use -
A. Config-file
The utility makes use of config-file as a collection of json objs.
The structure of the config-file is list of dictionaries.
Exmaple -

```
[
{"username": "Mangesh", "password":"1010", "allowed_programs":["ls"]},
{"username": "Utk", "password":"1010", "allowed_programs": ["ls"]}
]
```
Note - Make sure you have correct key names

1. To run server -
./server config-file
Note - tested on localhost only. Did not test on remote devices. Should work with port forward.

2. from client side -
./client --server <server ip> --user <username> --password <password> --exec <program to execute>
 example 
 ./client --server 127.0.0.1 --user Mangesh --password 1010 --exec 'ls -l'

Note - the exec param should be in string.






