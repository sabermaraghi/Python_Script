DNS Updater

A Python script to monitor and update DNS servers on Ubuntu systems, ensuring optimal network performance by selecting the fastest available DNS server from a predefined list. The script supports automatic setup, logging, and scheduling via cron, making it suitable for DevOps and system administration tasks.

Features





Tests latency of multiple DNS servers (e.g., Cloudflare, Shatel, Shecan).



Automatically updates DNS settings for active network interfaces if latency exceeds a threshold (default: 100ms).



Logs all actions to /var/log/dns-update.log.



Sets up a cron job to run every 30 minutes.



Falls back to a default DNS server (Cloudflare: 1.1.1.1) if no servers are reachable.



Supports Docker and non-Docker interfaces.

Requirements





OS: Ubuntu 22.04 or later.



Python: 3.6+.



Dependencies: None (uses standard library).



Permissions: Root access (sudo) for setup and DNS updates.



Tools: ping, resolvectl, systemd-resolved, crontab.

Installation





Clone the repository:

git clone https://github.com/your-username/dns-updater.git
cd dns-updater



Run the setup script as root:

sudo python3 setup_and_update_dns.py --setup



Verify the cron job:

crontab -l

Usage





Setup Mode: Configures the script, logging, and cron job.

sudo python3 setup_and_update_dns.py --setup



Run Mode: Checks and updates DNS servers.

sudo python3 setup_and_update_dns.py --run



Logs are written to /var/log/dns-update.log.

Configuration

Edit the following variables in setup_and_update_dns.py:





LATENCY_THRESHOLD: Maximum acceptable DNS latency (default: 100ms).



DNS_SERVERS: List of DNS servers to test.



FALLBACK_DNS: Default DNS server if none are reachable (default: 1.1.1.1).



LOG_FILE: Path to the log file (default: /var/log/dns-update.log).



MAX_INTERVAL_MINUTES: Maximum interval between runs to detect scheduling issues (default: 40 minutes).

Contributing

Contributions are welcome! See CONTRIBUTING.md for guidelines.

License

This project is licensed under the MIT License. See LICENSE for details.

Contact

For issues or suggestions, open an issue on GitHub or contact [your-email@example.com].
