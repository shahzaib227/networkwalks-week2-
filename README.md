# Networkwalks Week 2: Footprinting & Network Scanning

This is my Week 2 submission for the Cybersecurity & Ethical Hacking program at Networkwalks (Batch B082).

In this week I did two practical tasks:

1. **W2-PM1, Footprinting:** I collected public information about the `networkwalks.com` domain with different Kali Linux tools. I had written permission for this target.
2. **W2-PM5, Network scanning:** I used Zenmap to run a ping scan on my own lab network and saved the topology.

## What is in this repo

```
.
├── W2-PM-FINAL_Pentest_Report.docx   <- the full report
├── outputs/                          <- raw output of each command
│   ├── task1_whois.txt
│   ├── task2_whatweb.txt
│   ├── task3_nslookup.txt
│   ├── task4_curl.txt
│   └── task5_wafw00f.txt
└── screenshots/
    ├── ip_a.png                      <- my IP address on Kali
    ├── zenmap_ping_scan.png          <- Zenmap ping scan result
    └── zenmap_topology.pdf           <- topology saved from Zenmap
```

## Tools I used

| Tool | What I used it for |
|---|---|
| whois | Domain registration details |
| whatweb | Website technologies |
| nslookup | Finding the IP address |
| curl -I | HTTP response headers |
| wafw00f | Checking for a web application firewall |
| Zenmap (Nmap) | Finding live hosts on the local network |
| ip a | Checking my own IP and MAC address |

## Main things I found

- The website runs on **WordPress 7.1.5** with the **WordPress Download Manager 3.3.79** plugin.
- The domain resolves to **192.232.216.135**.
- The site is protected by **ModSecurity (SpiderLabs)**.
- The domain is registered with GoDaddy and uses HostGator name servers. DNSSEC is not signed.
- The Zenmap ping scan said that all 256 addresses of `10.0.0.0/24` were up. My lab is a virtual network, so I do not think all of them are real devices.

More detail, the risk table and my recommendations are in the report.

## Disclaimer

I only tested systems where I had written permission or devices that I own. This work is for education only and no exploitation was done.

**Author:** Shahzaib Memon
