🚦 IPv4 vs IPv6 Latency Test (Windows 11 + PowerShell)

I ran a small network-analysis style experiment comparing IPv4 vs IPv6 performance to a real-world target (cloudflare.com).

✅ What I measured:
- DNS A vs AAAA resolution
- ICMP latency + jitter + loss (ping)
- Routing behavior & hop visibility (tracert)

📌 Results (Ping):
- IPv4 avg ~19ms (min 7ms / max 73ms), 0% loss
- IPv6 avg ~16ms (min 9ms / max 37ms), 0% loss

📌 Results (Test-Connection):
- IPv4 avg 13.8ms (min 6ms / max 39ms)
- IPv6 avg 33.97ms (min 7ms / max 125ms)

🧠 Analyst takeaway:
IPv6 can be faster *or* slower depending on ISP peering, routing policy, congestion, and ICMP handling. Traceroute timeouts usually indicate ICMP rate-limiting—not necessarily real packet loss.

🔐 SOC relevance:
Ping/traceroute are fast triage tools to validate reachability and spot routing vs endpoint issues during incidents.

🗂️ I documented the raw outputs + analysis in a GitHub-ready format.

#PowerShell #Windows11 #Networking #IPv6 #Cybersecurity #SOC #ITSupport
