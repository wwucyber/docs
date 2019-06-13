---
layout: default
---


checklist for the 5 minutes after getting dropped in a random *nix box

- `w -f` to see who's logged in and how long the server's been up

- `ss -tlnp` (linux) `netstat -an` (bsd) to see what processes have listening sockets

- `getent passwd` to list users, `passwd <x>` to change, `passwd -l <x>` to lock an account (on bsd: `pw lock <x>`)

- `visudo` to open the sudoers config - remove any users or groups that shouldn't have access to sudo

- `crontab -l` and `atq` to see what tasks are scheduled to run later (use `sudo -u <user> crontab -l` for each user to list that user's crontab, or just poke around /var/spool/cron or /var/cron/tabs or /etc/crontab.d, etc

- `iptables -L -n -v` to list firewall rules

- check users' (esp. root's) ~/.bash_history and/or ~/.histfile

- edit `/etc/groups` to manage what users should be in what groups (esp. check on `wheel` and `sudo` groups)


## how to be a linux sysadmin
   
   https://gist.github.com/phroa/6a50d14f926218c24bc7

- browse `journalctl -xef` (shift pgup/down) (linux) or `/var/log/all.log` (bsd) + the rest of `/var/log` for any funny business

- `top` or `ps` to see processes (edited) 

- `systemctl list-unit-files` (recent linux) or `service --status-all`/`ls /etc/rc.d` (bsd, olderish linux) to see what services are enabled

- check `/etc/rc.conf` and `/usr/local/etc/rc.conf` (both bsd only) for any funny system configuration

- check `uname -a`, `cat /etc/issue`, `lsb_release -a` to find out what kind of *nix this is

- debian/ubuntu: `apt-get update -y && apt-get upgrade && apt-get dist-upgrade`, freebsd: `pkg upgrade`, redhat/centos/fedora: `yum upgrade`/`dnf upgrade`, suse: `zypper upgrade`

- ip6tables to check ipv6 stuff - maybe just disable all ipv6 with a sysctl or kernel boot param

- /etc/inetd.conf /etc/inetd.d /etc/xinetd.conf /etc/xinetd.d


- Tom's Honey Pot used in 2019 comp

   https://github.com/inguardians/toms_honeypot/blob/master/toms_honeypot.py

   mimics RDP MSSQL VNC  RemoteAdmin SIP
