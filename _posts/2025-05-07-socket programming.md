---
title: "Socket Programming(1)"
date: 2025-05-02 10:00:00 +0900
layout: post
categories:
  - Socket Programming
tags:
  - Socket
  - Programming
  - Python
---

##What is Socket Programming?

- Socket Programming is an interface between the application layer and the transport layer (TCP/UDP).
- It is a programming interface provided by the operation system (OS) to enable communication networked processes. 
- It allows developers to implement client-server communication models over networks. 


##Socket Key Concepts
- A spcket acts as an endpoint for sending and receiving data across a network.
- The OS provides socket API, which allows applications to interact with lower-layer protocols like TCP or UDP.
- Socket programming is essential for build networked applications, such as servers, chat programs, and file transfer tools.

##Common Operations in Socket Programming.
 
| **Function**     | **Description**                                 |
|------------------|--------------------------------------------------|
| `socket()`       | Create a new socket                              |
| `bind()`         | Bind the socket to an IP address and port        |
| `listen()`       | Listen for incoming connections (server-side)    |
| `accept()`       | Accept a connection request                      |
| `connect()`      | Connect to a remote server (client-side)         |
| `send()` / `recv()` | Send or receive data                         |
| `close()`        | Close the socket                                 |


##Create Socket 
- use the socket() function to create a new socket  
``` socket(int domain, int type, int protocol); ```
domain : address family (e.g. IPv4 : AFINET, IPv6 : AF_INET6)
type :  Communication type (e.g. TCP : SOCK_STREAM, UDP: SOCK_DGRAM)
protocol : Usually set to 0 to automatically select the appropriate protocol 
 

##Bind the Socket 
- use the bind() function to associate the socket with a specific IP address and port number.
``` int bind (int sockfd, const struct sockaddr *addr, socklen_t addrlen); ```
sockfd : The socket file descriptor returned by socket()
addr : A pointer to a sockaddr structure containing the desired IP address and port
addrlen : The size of the sockaddr structure 

- bind() assigns a local address(IP+port) to the socket, so it can receive incoming connections or data.

https://seolin.tistory.com/97
