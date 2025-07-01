# Elevate-Labs-Task-5

# Wireshark Protocol Analysis Report

**System**: Kali Linux VM  
**Capture Duration**: ~30 seconds  
**Interface**: eth0  
**Protocols Identified**:
- **ICMP** – Ping traffic to public IP (Echo request/reply)
- **DNS** – Domain name lookups (e.g., google.com)
- **UDP** – Transport for DNS queries

---

## Protocol Details

### ICMP:
- **Source**: 10.0.2.16
- **Destination**: 142.251.222.142
- **Type**: Echo (ping) requests and replies
- **Tool Used**: `ping google.com`

### DNS:
- **Query**: google.com (A and AAAA records)
- **Response**: IPs returned – `142.251.222.142`, `2404:6800:...`
- **Server IP**: 183.82.243.66
- **Transport Protocol**: UDP, Port 53

### UDP:
- **Used by DNS** for queries and responses
- **Random source port** (e.g., 50736)
- **Destination port**: 53 (standard DNS port)

---

## Conclusion:
Captured network traffic clearly shows multiple protocol types (ICMP, DNS, UDP). Filters were used effectively to isolate protocol behaviors. The `.pcap` file contains structured and timestamped evidence of each protocol in action.
