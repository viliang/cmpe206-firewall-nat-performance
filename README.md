# NAT and Firewall Performance

## Tests Included

### 1. High-volume TCP throughput (iperf3)

- 50 parallel streams  for 20s for 5 runs.

### 2. HTTP Requests (Stress Test)

- 200 requests per run

### 3. Rapid ping test

- 50 ICMP requests

### 4. Rapid short-lived TCP connections

- 50 connections

| Test                  | Protocol | Focus                       | Highlights                                       |
| --------------------- | -------- | --------------------------- | ------------------------------------------------ |
| iperf3                | TCP      | Sustained bulk throughput   | NAT/firewall overhead for large flows           |
| HTTP requests         | TCP      | Frequent short/medium flows | Connection setup + payload, NAT/firewall latency|
| Rapid ping            | ICMP     | Latency                     | Basic reachability and per-packet processing    |
| Rapid short-lived TCP | TCP      | Many quick connections      | PAT translation load, small-flow stress         |

