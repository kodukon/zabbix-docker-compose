# zabbix-docker-compose
Zabbix in Docker compose environment

# Intro
There is Docker compose example for Zabbix server.
Including:
1. Zabbix server
2. Zabbix web frontend
3. Postgres DB
4. Example conf for Nginx based reverse proxy

# To do list
1. Compose project use mounted volumes. You must create appropriate folders before deploying

For zabbix-server:
- ./.zabbix-data/alertscripts
- ./.zabbix-data/externalscripts
- ./.zabbix-data/export
- ./.zabbix-data/modules
- ./.zabbix-data/enc
- ./.zabbix-data/ssh_keys
- ./.zabbix-data/mibs
- ./.zabbix-data/ssl/certs
- ./.zabbix-data/ssl/keys
- ./.zabbix-data/ssl/ssl_ca
- ./.zabbix-data/snmtptraps

For Posrgres DB:
- ./.db_data

2. Create docker-compose.yaml in main project folder witn zabbiz-server's folders
3. Type in console 'docker compose up -d'
4. Go to 127.0.0.1:8080 in your fav browser

# Opt
If you wonna deploy zabbix throught reverse proxy, for example, Nginx, you could use example config from zabbix_nginx_proxy.conf

For HTTPS you could use Let's encrypt cert. 

Install certbot for your OS and use this command ONLY for Nginx: 'certbot --nginx -d "zabbix.example.com"'
