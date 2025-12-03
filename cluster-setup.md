# ⚙️ Installation et Configuration du Cluster Proxmox

1️⃣ Installer Proxmox VE sur deux nœuds (PVE1 & PVE2).  
Attribuer des IP fixes :  
- PVE1 → 192.168.204.179  
- PVE2 → 192.168.204.180  

2️⃣ Créer le cluster :


3️⃣ Sur PVE2 : rejoindre le cluster avec l’IP et la clé d’invitation du PVE1.

4️⃣ Ajouter un stockage **NFS** partagé pour la migration des VM et la HA.

5️⃣ Tester la **migration à chaud** (Live Migration) d’une VM du PVE1 → PVE2.
