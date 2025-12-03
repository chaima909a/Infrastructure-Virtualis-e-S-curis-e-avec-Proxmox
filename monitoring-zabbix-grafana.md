# 📊 Supervision avec Zabbix et Grafana

1️⃣ Installer Zabbix Server sur une VM dédiée :
apt install zabbix-server-pgsql zabbix-frontend-php


2️⃣ Installer l’agent sur chaque nœud :
apt install zabbix-agent
nano /etc/zabbix/zabbix_agentd.conf
Server=192.168.204.171
ServerActive=192.168.204.171


3️⃣ Ajouter un hôte Proxmox dans Zabbix avec un **API Token** configuré :
Variables à définir :  
`{$PVE.URL.HOST}` `{$PVE.URL.PORT}` `{$PVE.TOKEN.ID}` `{$PVE.TOKEN.SECRET}`

4️⃣ Intégrer Grafana avec Zabbix :  
URL : `http://192.168.204.171/zabbix/api_jsonrpc.php`

5️⃣ Créer des tableaux de bord interactifs pour CPU, RAM, réseau, disponibilité VM.
