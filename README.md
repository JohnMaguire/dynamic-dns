# Dynamic DNS Updater
A simple Bash script for updating DNS records in Cloudflare and DigitalOcean.

## Instructions

1. Clone the repository somewhere accessible: `git clone git@github.com:JohnMaguire/dynamic-dns.git /opt/dynamic-dns/`
2. Copy the example .env file into place: `cp /opt/dynamic-dns/examples/env /opt/dynamic-dns/.env`
3. Copy the example domain file into place: `cp /opt/dynamic-dns/examples/domain.example.com /opt/dynamic-dns/domains.d/domain.example.com`
4. Edit both files from the above steps with your desired values.
5. Finally, configure a cron job or systemd unit to periodically call the script. (See examples directory for systemd service and timer.)
