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

## 1. What is Socket Programming?

- Socket Programming is an interface between the application layer and the transport layer (TCP/UDP).
- It is a programming interface provided by the operation system (OS) to enable communication between networked processes. 
- It allows developers to implement client-server communication models over networks. 


## 2. Socket Key Concepts

- A socket acts as an endpoint for sending and receiving data across a network.
- The OS provides socket API, which allows applications to interact with lower-layer protocols like TCP or UDP.
- Socket programming is essential for building networked applications, such as servers, chat programs, and file transfer tools.


## 3. Common Operations in Socket Programming

| **Function**         | **Description**                                 |
|----------------------|--------------------------------------------------|
| `socket()`           | Create a new socket                              |
| `bind()`             | Bind the socket to an IP address and port        |
| `listen()`           | Listen for incoming connections (server-side)    |
| `accept()`           | Accept a connection request                      |
| `connect()`          | Connect to a remote server (client-side)         |
| `send()` / `recv()`  | Send or receive data                             |
| `close()`            | Close the socket                                 |


## 4. Create Socket

Use the `socket()` function to create a new socket.

```c
int socket(int domain, int type, int protocol);
```

| Parameter  | Description                                                         |
|------------|-------------|
| `domain`   | Address family (e.g., IPv4: `AF_INET`, IPv6: `AF_INET6`) |
| `type`     | Communication type (e.g., TCP: `SOCK_STREAM`, UDP: `SOCK_DGRAM`) |
| `protocol` | Usually set to `0` to automatically select the appropriate protocol |


## 5. Bind the Socket

Use the `bind()` function to associate the socket with a specific IP address and port number.  
`bind()` assigns a local address (IP + port) to the socket so it can receive incoming connections or data.

```cㅌ
int bind(int sockfd, const struct sockaddr *addr, socklen_t addrlen);
```

| Parameter  | Description |
|------------|-------------|
| `sockfd`   | The socket file descriptor returned by `socket()` |
| `addr`     | A pointer to a `sockaddr` structure containing the desired IP address and port |
| `addrlen`  | The size of the `sockaddr` structure |



https://seolin.tistory.com/97
