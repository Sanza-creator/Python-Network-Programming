# Python Network Programming — AgriHealth Rural Operations Platform

### Scenario
AgriHealth Rural Operations supports mobile healthcare and agricultural teams across remote South African farming communities, coordinating medicine deliveries, field reports, and service requests between rural service points and a central office. Communication was slow, service requests were poorly tracked, and sensitive record transfers weren't secure. I built a set of Python networking applications to address this, progressing from basic sockets to secure multi-client services.

### What I did

**1. Client-Server Communication**
- Built a socket-based Python server that receives an item request (e.g. vaccine stock, animal feed, water testing kits) from a client and checks it against a predefined availability list
- Built a matching client that prompts the user for an item, sends the request, and displays the server's availability response

**2. File Storage & Service Data Processing**
- Built a Python application to capture and persist rural service requests (requester name, service type, number of units) to a file, supporting repeated data entry
- Built a second program that reads stored requests, calculates each request's value (units × R50), and outputs them ranked from highest to lowest value — supporting prioritisation of service delivery

**3. Secure & Multi-Client Network Services**
- Developed a secure client-server application using SSL/TLS to ensure only authenticated clients could access server data, with clear failure handling on connection/authentication errors
- Set up a certificate-based trust configuration using OpenSSL to support the secure connection
- Built a multithreaded TCP server capable of handling multiple simultaneous client connections, supporting file upload and file download between clients and the server — for secure transfer of records such as patient referrals and livestock disease reports

### Skills demonstrated
`Python socket programming` · `Client-server architecture` · `File I/O & data persistence` · `SSL/TLS secure sockets` · `Multithreading` · `Multi-client TCP services
