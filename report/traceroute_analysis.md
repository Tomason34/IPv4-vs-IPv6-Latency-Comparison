# Traceroute Comparison (IPv4 vs IPv6)

| Metric | IPv4 | IPv6 |
|---|---:|---:|
| Total Hops | 7 | 7 |
| Timeouts | 1 | 1 |
| Final Hop | 7    71 ms    98 ms    16 ms  104.16.132.229 | 7    24 ms    12 ms     7 ms  2606:4700::6810:84e5 |

## Analyst Interpretation

- Equal hop counts suggest similar path length.
- Timeouts mid-path are typically ICMP rate limiting, not packet loss.
- Differences in intermediate routers indicate distinct BGP routing policies.
- Even with equal hop count, latency may differ due to peering congestion.

