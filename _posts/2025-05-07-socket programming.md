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


```

