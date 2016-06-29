## Squid Proxy Config
Quick notes on getting a Squid proxy up and running on a dev Fedora 24 box. This is not secure and shouldn't be used in production or left unattended on the wild-wild-webs.

### Installation
1. Install Squid and a basic auth tool on Fedora:
`$ dnf -y install squid httpd-tools`

2. Create a new `.htpasswd` and a user named `heroku`:
`$ htpasswd -c /etc/squid/.htpasswd heroku`

3. Replace ` /etc/squid/squid.conf` with the `squid.conf` in this repo.

4. Enable the squid service:
`$ systemctl enable squid.service`

5. Start the squid service:
`$ systemctl enable squid.service`

6. Profit.

### Useful Links
[Squid on Fedora Notes](http://www.server-world.info/en/note?os=Fedora_24&p=squid&f=3)
[Official Docs](http://www.squid-cache.org/Doc/man/)
