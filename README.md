# Prerender IP Ranges

This repository contains the official IP ranges that clients will see making HTTP requests to their websites when using Prerender.io services. **Use these ranges for firewall whitelisting to allow Prerender access to your website.**

**⚠️ Important:** These ranges only include client-facing services (proxy networks, rendering servers, and the sitemap crawler). Internal infrastructure IPs (databases, monitoring, load balancers) are excluded.

**Last Updated:** 2026-08-11

### Core IP Range Files

- **`ipranges.txt`** - Plain text format with one IP range per line (9 ranges)
- **`ipranges-all.txt`** - Same content as `ipranges.txt`, kept for backwards compatibility
- **`ipranges.json`** - JSON array format of the same ranges for programmatic access

### Geographic Data

- **`geofeed.csv`** - Geographic location data for IP ranges in RFC 8805 format
- **`CNAME`** - DNS CNAME configuration file

## IP Ranges

### Proxy networks and rendering servers (8 ranges)
- `103.207.40.0/24` … `103.207.43.0/24` - EU (Frankfurt, Amsterdam)
- `104.224.12.0/24` … `104.224.15.0/24` - US

### Sitemap crawler (1 range)
- `5.161.0.0/16` - Hetzner US; crawler runs on VMs without static addresses within this range
