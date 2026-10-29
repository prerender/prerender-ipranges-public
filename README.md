# Prerender IP Ranges

This repository contains the official IP ranges that clients will see making HTTP requests to their websites when using Prerender.io services. **Use these ranges for firewall whitelisting to allow Prerender access to your website.**

**⚠️ Important:** These ranges only include client-facing services (proxy networks, rendering servers, the sitemap crawler and the integration check). Internal infrastructure IPs (databases, monitoring, load balancers) are excluded.

**Last Updated:** 2026-10-29

### Core IP Range Files

- **`ipranges.txt`** - Plain text format with one IP range per line (8 ranges)
- **`ipranges-all.txt`** - Same content as `ipranges.txt`, kept for backwards compatibility
- **`ipranges.json`** - JSON array format of the same ranges for programmatic access

### Geographic Data

- **`geofeed.csv`** - Geographic location data for IP ranges in RFC 8805 format
- **`CNAME`** - DNS CNAME configuration file

## IP Ranges

### Proxy networks, rendering servers, sitemap crawler and integration check (8 ranges)
- `103.207.40.0/24` … `103.207.43.0/24` - EU (Frankfurt, Amsterdam)
- `104.224.12.0/24` … `104.224.15.0/24` - US

The sitemap crawler and the integration check fetch from `104.224.14.0/24` (US, New York). The former sitemap crawler range, `5.161.0.0/16` (Hetzner US), is no longer used.
