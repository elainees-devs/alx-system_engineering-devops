# 0x09. Web Infrastructure Design

This project covers basic and distributed web infrastructure concepts using visual diagrams and real-world server setups.

---

## ✅ Task 0: Simple Web Stack

Design of a basic LAMP-like stack using:

- **1 Server** at IP `8.8.8.8`
- **Nginx** as the Web Server
- **Application Server** for backend logic
- **MySQL Database** for persistent storage
- **Domain** `foobar.com` configured with a **www A record**

### 📊 Diagram:
![Simple Web Stack](https://imgur.com/a/cljuNXi)

### 🧠 Key Concepts Explained:
- **Server**: A physical or virtual machine that hosts the full web stack.
- **Domain Name**: Human-readable address (e.g. `foobar.com`) that maps to a server's IP.
- **A Record**: DNS record mapping `www.foobar.com` to `8.8.8.8`.
- **Web Server (Nginx)**: Handles static content and reverse proxies dynamic requests.
- **Application Server**: Processes backend logic using PHP.
- **MySQL Database**: Stores user and application data persistently.
- **Communication**: Client sends requests via HTTP/HTTPS to the Web Server.

### ⚠️ Infrastructure Issues:
- **SPOF (Single Point of Failure)**: If the server fails, the entire site is down.
- **Downtime for Maintenance**: One server must be taken offline to upgrade or fix.
- **Scalability**: One server can't efficiently handle high loads or traffic spikes.

---

## ✅ Task 1: Distributed Web Infrastructure

A high-availability, distributed setup to improve redundancy and scalability for `www.foobar.com`.

### 🧱 Components:
- **1 Load Balancer**: HAProxy using **Round Robin** algorithm.
- **1 Web Server**: Nginx for serving static files.
- **1 Application Server**: Handles backend logic using PHP and connects to MySQL database.
- **1 MySQL Database**: Primary (Master) node for data storage.
- **Application Codebase**: Hosted on the app server.
- **Domain Name**: `www.foobar.com` maps to load balancer.

### 🔁 Load Balancer (HAProxy):
- **Algorithm**: Round Robin — distributes client requests evenly to backend servers.
- **Setup**: Active-Passive (one app server active; one standby)
- **Benefit**: Prevents overloading and improves uptime.

### 🗃️ Database Architecture:
- **Primary Node**: Accepts both reads and writes.
- **Replica Node** *(not shown but recommended)*: Accepts reads only, synced from the primary.
- **Application View**:
  - **Primary**: Write-heavy queries (e.g., registration, posting data)
  - **Replica**: Read-heavy queries (e.g., viewing pages)

### 🔐 Security & Monitoring Considerations:
- No **firewall** – system exposed to potential attacks.
- No **HTTPS** – data in transit is unencrypted and vulnerable.
- No **monitoring** – no insights into system health or alerts on failure.

### ⚠️ Infrastructure Risks:
- **SPOF**:
  - Load balancer (without redundancy)
  - Single MySQL server (no replication or failover)
- **Security**:
  - No firewall or SSL/TLS encryption
- **Scalability**:
  - No autoscaling, no CDN for assets

---

### 📁 Directory Structure:
```bash
alx-system_engineering-devops/
└── 0x09-web_infrastructure_design/
    ├── 0-simple_web_stack
    ├── 1-distributed_web_infrastructure
    └── README.md
