# Ognjen Bobic — Portfolio

Personal portfolio site: networking and security projects, built as a static site with no framework or build step.

**Live:** https://ogi-cyber.github.io

## Projects documented here

**Network-wide DNS filtering and monitoring** — A Raspberry Pi 4 running Pi-hole as the DHCP server, DNS resolver and sinkhole for a 32-device home network. Roughly 76,000 lookups a day checked against 2.6M ad, tracker, malware and phishing domains, with ~23.8% blocked. Tailscale (WireGuard) extends the same filtering off-network.

**Two-site enterprise network** — A hospital network built in Cisco Packet Tracer: 5 subnets across 3 VLANs, 802.1Q trunking with router-on-a-stick inter-VLAN routing, centralized DHCP with relay, OSPF failover across redundant WAN links (~1s), and guest isolation enforced by an extended ACL.

## Structure

```
index.html        home — about, projects, skills, contact
pihole.html       Pi-hole project write-up
enterprise.html   Packet Tracer project write-up
style.css         all styles; design tokens in :root, light and dark themes
img/              screenshots and photos
favicon.svg
.nojekyll         serve files as-is, skip Jekyll processing
```

## Notes

- No build step. Edit the HTML and CSS, commit, and GitHub Pages republishes.
- Theme follows the visitor's system preference; every colour is a token redefined under `prefers-color-scheme: dark`.
- Layout is a single centred column; figures and tables break out to full width, and everything collapses to one column at phone width.
- The Pi-hole architecture diagram is inline SVG and themed from the same tokens, so it works in both light and dark.
