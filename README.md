# Network-packet-analysis-using-Wireshark

## Capture and Analyze Network Traffic Using Wireshark

1. Start the Wireshark and capture packets from the eth0 interface.

![image](https://github.com/user-attachments/assets/0a21e784-01b8-41b4-9daf-5415fa8fd6a0)

2. Surf the Internet.
- Visit http://testphp.vulnweb.com/login.php and enter some random credentials.

3. Let us filter HTTP traffic.

- The random credentials entered in the HTTP login page is captured in plaintext.

![image](https://github.com/user-attachments/assets/970469b0-9457-484a-837f-c7ab94717067)

4. Go to Statistics --> Protocol Hierarchy
- It displays the protocols present, their packet and byte counts, and their bandwidth usage, allowing users to quickly understand the distribution of traffic across different layers.

![image](https://github.com/user-attachments/assets/fb39a991-65eb-4978-873e-6a388374c90a)

### Some Protocols

**1. TCP - Transmission Control Protocol**
- TCP uses IP as its underlying protocol.
- It is a connection-oriented protocol for communications.
- It operates at the transport layer(Layer 4).
- TCP establishes a reliable connection between sender and receiver using the three-way handshake (SYN, SYN-ACK, ACK) and it uses a four-step handshake (FIN, ACK, FIN, ACK) to close connections properly.

**2. UDP - User Datagram Protocol**
- User Datagram Protocol (UDP) is a Transport Layer protocol.
- UDP uses IP as its underlying protocol.
- Unlike TCP, it is an unreliable and connectionless protocol.

**3. OUIC - Quick UDP Internet Connections**
- QUIC Protocol is running on the top of UDP.
- QUIC just extends the UDP as reliable connection provider here with some advanced techniques.
- In QUIC, it doesn't do this round trips to each SYN, SYNACK, ACK, and SSL Verification in separate requests to the server.
- Instead of in the first request itself, it gets to know about the Server Security Information & as it is using UDP in its transport layer.

**4. DNS - Domain Name System**
- DNS protocol allows internet users to navigate the internet using hostnames instead of numeric IP addresses.
- A browser will first check its cache for the record.
- If the requested record is not cached at the local level, DNS queries are then directed through a series of external DNS servers that help resolve the request.
