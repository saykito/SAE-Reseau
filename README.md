# SAE Réseau : mise en place et analyse d'un serveur DHCP

SAE Réseau du BUT Informatique 1re année, IUT de Marne-la-Vallée, Université Gustave Eiffel (2025 - 2026).
Réalisée par Nasser-Edine Cheikh-Bencheikh, Yasin Boukraa et Hugo Challaye.

Installation d'un serveur DHCP (ISC DHCP) sur Debian dans un réseau virtuel Netkit, puis analyse des échanges DHCP avec tcpdump et Wireshark.

## Topologie

Un serveur et quatre clients (M1 à M4) reliés au même hub (`HubA`), dans le réseau `192.168.1.0/24`.

| Élément | Valeur |
| --- | --- |
| Serveur DHCP | `192.168.1.1` (interface `eth1`, adresse statique) |
| Plage distribuée | `192.168.1.100` à `192.168.1.109` |
| Passerelle | `192.168.1.254` |
| Serveurs DNS | `192.168.1.1`, `192.168.1.2`, `192.168.1.3` |
| Domaine | `projet.local` |
| Durée du bail | 600 s par défaut, 7200 s maximum |

## Travail réalisé

1. Création du lab Netkit et configuration IP statique du serveur
2. Installation et configuration de `isc-dhcp-server`
3. Attribution des adresses aux clients et tests de communication
4. Capture des échanges avec tcpdump, analyse dans Wireshark (les 4 messages DHCP, adresses de destination, ports UDP 67 et 68)
5. Renouvellement du bail avec des durées réduites
6. Adresses IP fixes pour M1 et M4

## Contenu du dépôt

| Fichier | Rôle |
| --- | --- |
| `SAE RESEAUX compte rendu  (1).pdf` | Compte rendu complet |
| `presentation.pdf` | Support de soutenance |
| `configuration/lab.conf.txt` | Topologie Netkit (`lab.conf`) |
| `configuration/interfaces.txt` | `/etc/network/interfaces` du serveur |
| `configuration/isc-dhcp-server.txt` | `/etc/default/isc-dhcp-server` (interface d'écoute) |
| `configuration/dhcpd.conf.txt` | `/etc/dhcp/dhcpd.conf` (sous-réseau et options DHCP) |
