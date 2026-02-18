# IPv4 vs IPv6 Latency & Traceroute Comparison

## Objective
Compare IPv4 and IPv6 performance using:
- DNS resolution (A vs AAAA)
- ICMP latency testing (ping)
- PowerShell statistical measurement
- Traceroute path analysis

## Environment
- Windows 11
- PowerShell
- Target: cloudflare.com
- Dual-stack internet connection

## Methodology
1. Resolve A and AAAA records
2. Run ping -4 and ping -6 (20 packets)
3. Run Test-Connection (30 probes)
4. Perform tracert for IPv4 and IPv6
5. Save raw outputs for documentation

## Key Findings
- Both protocols reached destination successfully
- No packet loss observed
- IPv4 showed lower average latency in statistical testing
- IPv6 showed higher variance in max latency
- Traceroute revealed similar hop counts with some ICMP timeouts (rate limiting)

## Analyst Interpretation
Latency differences are influenced by routing policy, ISP peering, and path congestion.
IPv6 is not inherently slower; performance depends on network topology.

## SOC Relevance
ICMP testing helps with:
- Reachability validation
- Latency spike investigation
- Routing anomaly detection
- ISP path comparison

## Ethical Considerations
All testing used standard ICMP diagnostics against a public domain.
No intrusive scanning or exploitation was performed.

## Measured Results (Actual Lab Data)

### Ping (20 packets)

| Metric | IPv4 | IPv6 |
|--------|------|------|
| Minimum | 7 ms | 9 ms |
| Maximum | 73 ms | 37 ms |
| Average | 19 ms | 16 ms |
| Packet Loss | 0% | 0% |

### Test-Connection (30 probes)

| Metric | IPv4 | IPv6 |
|--------|------|------|
| Minimum | 6 ms | 7 ms |
| Maximum | 39 ms | 125 ms |
| Average | 13.8 ms | 33.97 ms |

