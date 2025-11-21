# Prerender IP Ranges

This repository contains the official IP ranges that clients will see making HTTP requests to their websites when using Prerender.io services. **Use these ranges for firewall whitelisting to allow Prerender access to your website.**

**⚠️ Important:** These ranges only include client-facing services (proxy networks and rendering servers). Internal infrastructure IPs (databases, monitoring, load balancers) are excluded.

**Last Updated:** 2025-11-21

### Core IP Range Files

- **`ipranges.txt`** - Plain text format with one IP range per line (324 ranges)
- **`ipranges.json`** - JSON array format of the same ranges for programmatic access

### Geographic Data

- **`geofeed.csv`** - Geographic location data for IP ranges in RFC 8805 format
- **`CNAME`** - DNS CNAME configuration file

## IP Range Categories

The IP ranges are organized by infrastructure provider and purpose:

### Global Proxy Networks (3 ranges)
- `103.207.40.0/22` - Frankfurt, Germany (GlobalSecureLayer)
- `103.207.42.0/22` - Amsterdam, Netherlands (TeraSwitch) 
- `104.224.12.0/22` - United States (GlobalSecureLayer)

### US Rendering Servers (83 ranges)
- `104.224.13.x/25` - NOCix Kansas City (82 ranges)
- `104.224.14.0/24` - WebNX Ogden, Utah (1 consolidated range)

### Individual Rendering Servers (90 ranges)
- NOCix dedicated servers (`63.141.x.x/32`, `69.x.x.x/32`)
- WebNX dedicated servers (`173.231.x.x/32`, `216.x.x.x/32`, `107.182.x.x/32`, `108.171.x.x/32`, etc.)
- Individual /32 ranges for servers that make direct requests to client websites

### IPv6 Ranges (148 ranges)
- `2602:2dd::/36` - Global proxy IPv6 ranges
- `2a01:4f8::/32` - Hetzner IPv6 ranges (primary)
- `2a01:4f9::/32` - Hetzner IPv6 ranges (secondary)
- Used by servers with IPv6 connectivity when making requests to client websites

### Validation
All IP ranges are validated for:
- Geographic accuracy  
- Infrastructure presence
