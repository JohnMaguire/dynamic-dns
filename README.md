# Dynamic DNS Updater
A simple Bash script for updating DNS records in Cloudflare and DigitalOcean.

## Instructions

Clone the repository, and create a `.env` with the following content:

```
DOMAINS_DIR="Path to a directory of config files"
# Uncomment the below lines as needed
#DIGITALOCEAN_API_TOKEN="API token retrieved from DigitalOcean (needs read and write scopes)"
#CLOUDFLARE_API_TOKEN="API token retrieved from Cloudflare (needs 'Edit zone DNS' / Zone.DNS permission for all zones)"
```

`DOMAINS_DIR` should point to a directory (e.g. `/opt/dynamic-dns/domains.d`) with files that look like this:

```
DOMAIN="johnmaguire.me"
SUBDOMAIN="home"
# PROVIDER defaults to digitalocean for backwards compatibility
#PROVIDER="cloudflare"
```

Finally, configure a cron job or systemd unit to periodically call the script.
