# NAT and Firewall Performance

## Tests Included

### 1. High-volume TCP throughput (iperf3)

- 50 parallel streams  for 20s for 5 runs.
- Measures aggregate **Mbit/sec** between PC1 and server.

### 2. HTTP Requests (Stress Test)

- 200 requests per run
- Measures **total time**, **header size**, **body size**, and calculates:
  - **Header throughput (B/s, Mbps)**
  - **Body throughput (B/s, Mbps)**
  - **Total throughput (B/s, Mbps)**
- Captures both connection setup and payload transfer performance.

### 3. Rapid ping test

- 50 ICMP requests to measure **latency (ms)**.
- Calculates approximate **throughput (B/s)** from packet size / RTT.

### 4. Rapid short-lived TCP connections

- 50 connections
- Designed to stress **PAT NAT translation tables** by creating many short connections in parallel.
- Helps expose translation and firewall overhead not visible in long HTTP sessions.
