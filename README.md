# Elevate-Labs-Tasks-5

Task 5

# Capture and Analyze Network Traffic Using Wireshark.

## Objective
Capture live network packets and identify basic protocols and traffic types.

### Tools Used

- **Wireshark (free).** Wireshark is a network protocol analyzer (or packet sniffer). It is used to capture, view, and analyze network traffic in real time or from saved capture files.
## Steps

Below are the key steps taken in this process:

### 1. Install Wireshark.

download wireshark here
- https://www.wireshark.org/download.html

![](https://github.com/Abhijithprashanth/Elevate-Labs-Tasks-5/blob/main/Download%20wireshark.png)

### 2. Start capturing on your active network interface.

Captured the packets in wireshark


![]([https://github.com/Abhijithprashanth/Elevate-Labs-Tasks-4/blob/main/Screenshot%202025-09-28%20192320.png](https://github.com/Abhijithprashanth/Elevate-Labs-Tasks-5/blob/main/Capturing%20Packets.png))




### 3. Browse a website or ping a server to generate traffic.


### 4. Stop capture after a minute.

 

### 5. Filter captured packets by protocol (e.g., HTTP, DNS, TCP)

In the filter panel we can Type protocol name


![](https://github.com/Abhijithprashanth/Elevate-Labs-Tasks-5/blob/main/http.png)
HTTP
![](https://github.com/Abhijithprashanth/Elevate-Labs-Tasks-5/blob/main/dns.png)
DNS
![](https://github.com/Abhijithprashanth/Elevate-Labs-Tasks-5/blob/main/tcp.png)
TCP

### 5. Identify at least 3 different protocols in the capture.


DNS: Queries to resolve domain names (A, AAAA records).

HTTP: GET requests to websites, status codes (200 OK).

TCP: Three-way handshake (SYN, SYN/ACK, ACK).

ICMP: Ping echo request/reply.


### 6. Export the capture as a .pcap file.

File → Save As → capture.pcapng

### 7. Summarize your findings and packet details.

Protocols Observed

- TCP → Used for reliable communication between hosts. Observed SYN, ACK, RST flags showing connection establishment and termination.

- HTTP → Application-layer traffic, showing web requests/responses over TCP port 80.

- TLSv1.2 → Encrypted traffic over HTTPS (port 443), securing web sessions.

- DNS → Queries and responses resolving domains like gstatic.com and google.com.

- ICMP (Ping) → Echo requests and replies confirming network connectivity.
  

Example Packet Details : 


- TCP Handshake:

SYN → SYN/ACK → ACK observed between 192.168.0.113 and external IPs.

Sequence and acknowledgment numbers incremented as expected.

- HTTP Traffic:

Large continuation packets (1494 bytes) containing HTTP payload.

ACKs confirming reliable delivery.

- TLS Traffic:

Encrypted application data exchanged with Google servers (142.250.x.x).

TLS handshake and subsequent encrypted communication noted.



Observations

TCP ensures reliable delivery, retransmitting when needed.

HTTP traffic is human-readable (GET, POST), while HTTPS appears encrypted under TLS.

DNS is crucial for resolving hostnames before connections.

RST (Reset) packets indicate some closed/denied connections.


### 5. Conclusion

The Wireshark capture successfully demonstrated multiple protocols (TCP, HTTP, TLS, DNS, ICMP) in action. I observed how connections are established and terminated, how DNS queries resolve domains, and how HTTP vs HTTPS differ (plaintext vs encrypted). This provided hands-on packet analysis skills and protocol awareness, fulfilling the task objective.
