# Networking

## Client-Server Basics

- In client-server architecture, the client sends HTTP requests to the server.
- Common web server ports:
  - `80`, `8080` for HTTP
  - `443`, `8443` for HTTPS
- `DNS` means Domain Name System.

## Sockets

- A server uses a socket to open a connection.
- A client also uses a socket to connect.
- Typical calls:
  - `bind(s, [8.8.8.8, 53])` sets the IP address and port on the server side
  - `sendto(s, request, [8.8.8.8, 53])` sends data
  - `recvfrom(s, ...)` is used by the server to receive data

## Delivery and Performance

- Off-net caches can help reduce latency.
- Important network link properties:
  - Transmission rate
  - Length
  - Propagation speed
- Key network issues to monitor:
  - Packet loss
  - Packet delay

## UDP and TCP

- `UDP` does not provide confirmation.
- `TCP` uses a three-way handshake.

## Flow and Congestion Control

- Flow control prevents the receiver window from being overwhelmed.
- The congestion window helps avoid network congestion.
