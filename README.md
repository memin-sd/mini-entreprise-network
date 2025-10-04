# Projet Réseau d’Entreprise (Packet Tracer)

## Présentation
Ce projet a été réalisé dans le cadre de ma formation en TIC - Télécommunications.  
L’objectif est de simuler un réseau d’entreprise complet et sécurisé en utilisant Packet Tracer.  
J’ai voulu mettre en pratique les notions de VLAN, routage, services réseaux et sécurité.

---

## Architecture Réseau
Le réseau est divisé en 3 VLANs :
- VLAN 10 – Employés : accès Web et FTP  
- VLAN 20 – Finance : accès limité pour plus de sécurité  
- VLAN 30 – Administration : gestion du réseau et des services

Un serveur central (dans le VLAN 30) fournit plusieurs services à toute l’entreprise.

---

## Services mis en place
- DHCP → attribution automatique des adresses IP  
- DNS → résolution du nom de domaine `entreprise.local`  
- HTTP/HTTPS → page intranet "Bienvenue dans l’entreprise"  
- FTP → partage de fichiers  
- Mail (SMTP/IMAP) → messagerie interne  

---

## Sécurité
- Routage Inter-VLAN avec OSPF  
- ACL configurées pour jouer le rôle de firewall :  
  - VLAN Finance ne peut pas accéder à certains services sensibles  
  - VLAN Employés et VLAN Admin ont des accès contrôlés  

---

## Matériel simulé
- 1 Routeur (Cisco) → routage + ACL (firewall)  
- 2 Switchs → gestion des VLANs et trunks  
- 1 Serveur → DHCP, DNS, HTTP/HTTPS, FTP, Mail  
- Des PC dans chaque VLAN (tests de connectivité et services)  

---

## Résultat
- Les VLANs peuvent accéder au serveur intranet via :  
  - http://192.168.30.100  

- La communication entre VLANs est contrôlée par les ACL.  
- Le projet fonctionne comme un mini-système d’information d’entreprise.

---

## Contenu du dépôt
- `entreprise.pkt` → fichier Packet Tracer du projet  
- `config/` → configurations du routeur, switch et ACL  
- `docs/` → rapport + capture d’écran du réseau  
- `README.md` → ce fichier d’explication  

---

## Conclusion
Ce projet m’a permis de mieux comprendre la conception d’un réseau d’entreprise :  
- Segmentation avec VLANs  
- Routage dynamique avec OSPF  
- Mise en place de services réseau  
- Sécurité avec ACL  

C’est un premier pas vers l’administration réseau et la cybersécurité.
