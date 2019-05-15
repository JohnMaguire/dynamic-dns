# DigitalOcean Dynamic DNS Updater
A quick script for updating DNS.

## Instructions

Clone the repository, and create a `.env` with the following content:

```
API_TOKEN="API token retrieved from DigitalOcean"
DOMAINS_DIR="Path to a directory of config files"
```

`DOMAINS_DIR` should point to a directory (e.g. `/opt/dynamic-dns/domains.d`) with files that look like this:

```
DOMAIN="johnmaguire.me"
SUBDOMAIN="home"
```

Finally, configure a cron job or systemd unit to periodically call the script.
