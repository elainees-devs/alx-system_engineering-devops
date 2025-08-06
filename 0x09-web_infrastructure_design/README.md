# 0x09. Web Infrastructure Design

This project covers basic web infrastructure concepts using a one-server setup.

## Task 0: Simple Web Stack

Design of a basic LAMP-like stack using:
- **1 Server** at IP `8.8.8.8`
- **Nginx** as the Web Server
- **Application Server** for backend logic
- **MySQL Database** for persistent storage
- **Domain** `foobar.com` configured with a **www A record**

### Diagram:
![Simple Web Stack] https://imgur.com/a/cljuNXi

### Key Concepts Explained:
- **Server**: Physical/virtual computer hosting the stack.
- **Domain Name**: Human-readable address pointing to server IP and is used to identify a website on the internet.
- **A Record**: DNS record mapping `www.foobar.com` to `8.8.8.8`. It maps domain names to IP Addresses (version4).
- **Web Server (Nginx)**: Serves static content and proxies dynamic requests.
- **Application Server**: Handles business logic, processes dynamic requests and, handles the backend code e.g. Node.js, python, PHP etc
- **Database (MySQL)**: Stores structured application data.
- **Communication**: Client Web Server via HTTP or HTTPS

### Infrastructure Issues:
- **SPOF**: Single server; if it fails, everything goes down.
- **Downtime for maintenance**: Updating server affects availability.
- **Scalability**: Cannot handle high traffic on a single node.

