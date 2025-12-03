# 💾 Sauvegardes avec Proxmox Backup Server (PBS)

1️⃣ Installer PBS sur une machine dédiée (192.168.204.182).  
2️⃣ Créer un datastore :
mkdir /mnt/pbs-datastore
mount /dev/sdc1 /mnt/pbs-datastore


3️⃣ Configurer le datastore dans l’interface PBS :  

`Datastore → Add → /mnt/pbs-datastore → Nom : pbs-local`

4️⃣ Configurer les sauvegardes automatiques toutes les 30 min :

crontab -e
*/30 * * * * proxmox-backup-manager backup proxmox-backups --compression lzo


5️⃣ Tester la restauration d’une VM :
Datacenter → Backup → Restore

Copier le code
