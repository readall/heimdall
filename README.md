[![Gitpod ready-to-code](https://img.shields.io/badge/Gitpod-ready--to--code-blue?logo=gitpod)](https://gitpod.io/#https://github.com/acriba/heimdall)

# heimdall
Comparable with fail2ban but based on Rust and optimized for high performance. Log scans log files (e.g. /var/log/apache/access_log) and bans IPs that show the malicious signs -- too many password failures, seeking for exploits, etc.

We will test it for our usecase and see if this really works

At this version on 21-Dec, we have the functionality working again.
That means, 
    - From the xml file, it pick the file to monitor
    - Using the specified pattern, it picks the IP address or hostname to block
    - Using the iptables command, it jails the endpoint
    - Jail time is managed outside of iptables by this app
    - We have changed the unjail_thread sleep time to 10000ms (10 sec)

