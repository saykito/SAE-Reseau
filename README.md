# SAE Réseau, infrastructure avec serveur DHCP

Projet de SAE Réseaux, BUT Informatique 1re année, IUT de Marne-la-Vallée (2025).

Mise en place d'une petite infrastructure réseau virtualisée : postes clients, équipements d'interconnexion, routeur et serveur DHCP sous Debian. Objectif : comprendre l'attribution dynamique des adresses IP et savoir diagnostiquer une panne.

## Ce qui a été fait

- Topologie décrite dans un lab Kathará / Netkit (`lab.conf`) : postes M1 à M4 et serveur
- Configuration des interfaces réseau (`/etc/network/interfaces`)
- Installation et configuration d'ISC DHCP Server (`dhcpd.conf`, `isc-dhcp-server`)
- Tests de connectivité (ping, vérification des baux DHCP)

## Contenu du dépôt

```
configuration/
  lab.conf.txt            topologie du lab
  interfaces.txt          configuration des interfaces
  dhcpd.conf.txt          configuration du serveur DHCP
  isc-dhcp-server.txt     interface d'écoute du service
SAE RESEAUX compte rendu (1).pdf   compte rendu
presentation.pdf          support de soutenance
```
