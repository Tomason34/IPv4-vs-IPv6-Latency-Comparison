# IPv4 vs IPv6 Latency Comparison (Ping)

**Target:** cloudflare.com

## Summary Table

| Metric | IPv4 | IPv6 |
|---|---:|---:|
| Samples (replies) | 20 | 20 |
| Packet loss (%) | 0 | 0 |
| Min RTT (ms) | 6 | 7 |
| Avg RTT (ms) | 18.5 | 50.3 |
| Max RTT (ms) | 60 | 247 |
| Jitter (StdDev, ms) | 14.44 | 66.2 |
| TTL observed | 59 | N/A (Windows ping -6 doesn't show TTL) |

**Quick call:** IPv4 (lower average RTT)

## Notes
- *Jitter* here is calculated as the standard deviation of RTT samples (higher = less stable latency).
- IPv4 ping shows TTL= in replies; Windows ping -6 typically does not display hop-limit/TTL, so TTL is recorded as N/A for IPv6.

