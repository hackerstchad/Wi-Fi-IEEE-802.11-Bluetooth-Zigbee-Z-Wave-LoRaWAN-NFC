Wi-Fi (IEEE 802.11), Bluetooth, Zigbee, Z-Wave, LoRaWAN, NFC

<img width="1024" height="371" alt="1c1244c3-aec8-4023-8319-1932c48933b3" src="https://github.com/user-attachments/assets/89505b00-92b7-4e39-b398-e02c118083c1" />


<div align="center">

<p>
  <img src="https://img.shields.io/badge/Wi--Fi-IEEE%20802.11-brightgreen?style=for-the-badge&logo=wifi&logoColor=white" />
  <img src="https://img.shields.io/badge/Bluetooth-Bluetooth%20SIG-blue?style=for-the-badge&logo=bluetooth&logoColor=white" />
  <img src="https://img.shields.io/badge/Zigbee-CSA%20%7C%20IEEE%20802.15.4-yellow?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Z--Wave-Z--Wave%20Alliance-red?style=for-the-badge" />
  <img src="https://img.shields.io/badge/LoRaWAN-LoRa%20Alliance-darkgreen?style=for-the-badge" />
  <img src="https://img.shields.io/badge/NFC-NFC%20Forum-lightblue?style=for-the-badge" />
</p>

**Auteur : hackers_tchad**  
**Date : 2026**  
**Version : 5.0 Master Edition**  
**Classification : Guide Technique Avancé - Formation & Pentesting Légal**

</div>

---

##  Table des Matières

1. [Introduction Générale](#introduction-générale)
2. [Méthodologie de Ce Guide](#méthodologie-de-ce-guide)
3. [Wi-Fi - IEEE 802.11](#wi-fi---ieee-80211)
4. [Bluetooth](#bluetooth)
5. [Zigbee](#zigbee)
6. [Z-Wave](#z-wave)
7. [LoRaWAN](#lorawan)
8. [NFC](#nfc)
9. [Comparatif Global des Protocoles](#comparatif-global-des-protocoles)
10. [Sécurité Offensive & Défensive](#sécurité-offensive--défensive)
11. [Outils Universels d'Analyse](#outils-universels-danalyse)
12. [Ressources, Livres & Liens](#ressources-livres--liens)
13. [Glossaire](#glossaire)
14. [Licence & Avertissement Légal](#licence--avertissement-légal)

---

## Introduction Générale

Bienvenue dans ce **manuel maître des protocoles de communication sans fil modernes**. Ce document est conçu pour fournir une compréhension approfondie, technique et pratique des six familles de protocoles sans fil dominantes dans l'écosystème numérique contemporain :

- **Wi-Fi (IEEE 802.11)**
- **Bluetooth**
- **Zigbee**
- **Z-Wave**
- **LoRaWAN**
- **NFC**

Chaque section aborde : la définition formelle, l'histoire et les créateurs, l'architecture protocolaire, les couches OSI concernées, les fréquences et modulations utilisées, la configuration matérielle et logicielle, les commandes de vérification et de diagnostic, les cas d'usage, les applications concrètes, la sécurité, et enfin les ressources bibliographiques ainsi que des liens utiles.

Ce guide s'adresse aux :
- Administrateurs réseaux et systèmes
- Ingénieurs IoT et télécommunications
- Éthical hackers et auditeurs de sécurité
- Étudiants en informatique et électronique
- Passionnés de domotique, de smart city et de cybersécurité

---

## Méthodologie de Ce Guide

Chaque protocole est présenté selon le schéma suivant :

1. **Définition et description générale**
2. **Historique et créateurs**
3. **Architecture et couches OSI**
4. **Fréquences, débits et portées**
5. **Topologies réseau supportées**
6. **Sécurité intégrée**
7. **Configuration matérielle et logicielle**
8. **Commandes de vérification et diagnostic**
9. **Applications et cas d'usage**
10. **Avantages et limitations**
11. **Ressources et liens**

---

## Wi-Fi - IEEE 802.11

### 1. Définition et Description Générale

Le **Wi-Fi** est une technologie de réseau local sans fil (WLAN, Wireless Local Area Network) basée sur la famille de normes **IEEE 802.11**. Elle permet à des appareils tels que des ordinateurs, smartphones, imprimantes, caméras et objets connectés de communiquer entre eux et avec Internet via des ondes radio, sans utiliser de câbles Ethernet.

Le terme **Wi-Fi** est une marque commerciale déposée par la **Wi-Fi Alliance**, créée en 1999. Cette alliance est responsable de la certification des équipements compatibles avec les normes IEEE 802.11. Un appareil certifié Wi-Fi a été testé pour garantir son interopérabilité avec d'autres équipements du même standard.

Le Wi-Fi repose sur la couche physique (PHY) et la sous-couche MAC (Media Access Control) du modèle OSI, respectivement aux couches 1 et 2. Il fonctionne principalement dans les bandes de fréquences ISM (Industrial, Scientific and Medical) :
- **2.4 GHz**
- **5 GHz**
- **6 GHz** (Wi-Fi 6E et Wi-Fi 7)

### 2. Historique et Créateurs

Le Wi-Fi trouve ses origines dans un ensemble de travaux menés à l'**CSIRO** (Commonwealth Scientific and Industrial Research Organisation) en Australie, dirigés par le Dr **John O'Sullivan** et son équipe dans les années 1990. Leur brevet fondamental sur la technologie OFDM (Orthogonal Frequency Division Multiplexing), déposé en 1992 et accordé en 1996, est considéré comme la pierre angulaire du Wi-Fi moderne.

La norme IEEE 802.11 originale a été ratifiée en **1997** par l'**IEEE** (Institute of Electrical and Electronics Engineers). Depuis, de multiples amendements ont été publiés :

| Année | Norme | Nom commercial | Débit maximal théorique | Bande |
|-------|-------|---------------|------------------------|-------|
| 1997 | IEEE 802.11 | Wi-Fi 1 | 1 à 2 Mbps | 2.4 GHz |
| 1999 | IEEE 802.11b | Wi-Fi 1 | 11 Mbps | 2.4 GHz |
| 1999 | IEEE 802.11a | Wi-Fi 2 | 54 Mbps | 5 GHz |
| 2003 | IEEE 802.11g | Wi-Fi 3 | 54 Mbps | 2.4 GHz |
| 2009 | IEEE 802.11n | Wi-Fi 4 | 600 Mbps | 2.4/5 GHz |
| 2013 | IEEE 802.11ac | Wi-Fi 5 | 6.93 Gbps | 5 GHz |
| 2019 | IEEE 802.11ax | Wi-Fi 6 | 9.6 Gbps | 2.4/5 GHz |
| 2020 | IEEE 802.11ax (6E) | Wi-Fi 6E | 9.6 Gbps | 6 GHz |
| 2024 | IEEE 802.11be | Wi-Fi 7 | 46 Gbps | 2.4/5/6 GHz |

### 3. Architecture et Couches OSI

Le Wi-Fi s'appuie sur les deux premières couches du modèle OSI :

#### Couche 1 - Couche Physique (PHY)

La couche physique du Wi-Fi définit comment les données sont transmises sous forme de signaux radio. Elle gère :
- La modulation et le codage
- La gestion des fréquences
- La puissance d'émission
- La synchronisation entre émetteur et récepteur

Techniques de modulation utilisées :
- **DSSS** (Direct Sequence Spread Spectrum) - 802.11b
- **OFDM** (Orthogonal Frequency Division Multiplexing) - 802.11a/g/n/ac/ax
- **OFDMA** (Orthogonal Frequency Division Multiple Access) - 802.11ax
- **MIMO** (Multiple Input Multiple Output) - 802.11n/ac/ax/be
- **MU-MIMO** (Multi-User MIMO)
- **1024-QAM** et **4096-QAM** - Wi-Fi 6/7

#### Couche 2 - Sous-couche MAC

La sous-couche MAC gère l'accès au médium partagé. Elle utilise le protocole **CSMA/CA** (Carrier Sense Multiple Access with Collision Avoidance) pour éviter les collisions dans un environnement radio half-duplex.

Les principales fonctions MAC incluent :
- L'adressage MAC (adresses de 48 bits)
- La fragmentation et le réassemblage des trames
- La gestion de l'association/dissociation
- Le contrôle d'accès via les mécanismes de sécurité
- La gestion de l'économie d'énergie (Power Save Mode)

### 4. Fréquences, Débits et Portées

#### Bande 2.4 GHz

- **Canaux disponibles** : 14 canaux (selon les régions)
- **Canaux non chevauchants** : 1, 6, 11 (en Europe/Amérique du Nord)
- **Largeur de canal** : 20/40 MHz
- **Portée typique** : 30 à 100 m en intérieur, jusqu'à 250 m en extérieur
- **Avantages** : Bonne pénétration des obstacles, grande portée
- **Inconvénients** : Forte congestion, interférences avec Bluetooth, micro-ondes, etc.

#### Bande 5 GHz

- **Canaux disponibles** : jusqu'à 24 canaux non chevauchants selon la région
- **Largeur de canal** : 20/40/80/160 MHz
- **Portée typique** : 10 à 50 m en intérieur
- **Avantages** : Moins congestionnée, débits élevés
- **Inconvénients** : Moins bonne pénétration des murs

#### Bande 6 GHz

- **Canaux disponibles** : 59 canaux de 20 MHz
- **Largeur de canal** : 20/40/80/160 MHz
- **Avantages** : Bande dédiée au Wi-Fi 6E/7, très faible congestion
- **Inconvénients** : Portée réduite, réglementation variable selon les pays

### 5. Topologies Réseau

Le Wi-Fi supporte deux topologies principales :

#### Infrastructure Mode (mode infrastructure)

Dans ce mode, les stations (STA) communiquent entre elles via un **Point d'Accès (AP)** ou une **Borne Wi-Fi**. C'est le mode le plus courant dans les réseaux domestiques et d'entreprise.

Composants :
- **BSS** (Basic Service Set) : ensemble formé par un AP et ses clients
- **BSSID** : adresse MAC de l'AP
- **ESS** (Extended Service Set) : plusieurs BSS interconnectés par un système de distribution (DS)
- **SSID** : nom du réseau visible par les utilisateurs

#### Ad-hoc Mode (mode ad-hoc)

Dans ce mode, deux ou plusieurs stations communiquent directement entre elles sans point d'accès central. Cette topologie est appelée **IBSS** (Independent Basic Service Set).

#### Wi-Fi Direct

Wi-Fi Direct permet à deux appareils de se connecter directement entre eux sans point d'accès traditionnel. L'un des appareils joue le rôle de "group owner" (GO), équivalent à un AP logiciel.

### 6. Sécurité Wi-Fi

L'évolution de la sécurité Wi-Fi a connu plusieurs étapes :

| Protocole | Année | Caractéristiques | Sécurité |
|-----------|-------|-----------------|----------|
| WEP (Wired Equivalent Privacy) | 1997 | Clé 40/104 bits, RC4 | Cassé, obsolète |
| WPA (Wi-Fi Protected Access) | 2003 | TKIP/RC4, 802.1X | Obsolète |
| WPA2 | 2004 | AES-CCMP, 802.1X | Standard jusqu'à 2018 |
| WPA3 | 2018 | SAE, AES-GCMP, forward secrecy | Recommandé |

#### WPA3

WPA3 apporte plusieurs améliorations :
- **SAE** (Simultaneous Authentication of Equals) : remplace le PSK (Pre-Shared Key)
- Protection contre les attaques par dictionnaire hors ligne
- **Forward secrecy** : protection des communications passées en cas de compromission de clé
- **OWE** (Opportunistic Wireless Encryption) : chiffrement dans les réseaux ouverts
- **WPA3-Enterprise** : authentification 802.1X avec 192-bit security mode

### 7. Configuration Matérielle et Logicielle

#### Matériel nécessaire

- Routeur Wi-Fi ou point d'accès compatible avec la norme souhaitée
- Carte réseau Wi-Fi (client) compatible
- Antennes adaptées (omnidirectionnelles, directionnelles, sectorielles)
- Câbles Ethernet pour la connexion au réseau filaire

#### Configuration d'un point d'accès OpenWrt

OpenWrt est un firmware Linux embarqué très populaire pour les routeurs Wi-Fi.

Exemple de configuration via l'interface web LuCI ou en ligne de commande UCI :

```bash
# Se connecter au routeur en SSH
ssh root@192.168.1.1

# Configurer le SSID et la sécurité
uci set wireless.radio0.disabled='0'
uci set wireless.default_radio0.ssid='MonReseauSecurise'
uci set wireless.default_radio0.encryption='psk2+ccmp'
uci set wireless.default_radio0.key='MotDePasseFort2026!'
uci set wireless.default_radio0.mode='ap'
uci set wireless.default_radio0.network='lan'

# Valider et appliquer
uci commit wireless
wifi reload
```

#### Configuration hostapd (Linux)

hostapd est un démon permettant de transformer une interface Wi-Fi en point d'accès.

Exemple de fichier `/etc/hostapd/hostapd.conf` :

```ini
interface=wlan0
driver=nl80211
ssid=MonAPSecurise
hw_mode=g
channel=6
wmm_enabled=1
ieee80211n=1
ieee80211ac=1
ht_capab=[HT40+][SHORT-GI-20][SHORT-GI-40][DSSS_CCK-40]
vht_capab=[MAX-MPDU-11454][RXLDPC][SHORT-GI-80]
auth_algs=1
wpa=2
wpa_key_mgmt=WPA-PSK
rsn_pairwise=CCMP
wpa_passphrase=MonMotDePasseFort
```

Lancement :
```bash
sudo hostapd /etc/hostapd/hostapd.conf
```

### 8. Commandes de Vérification et Diagnostic

#### Sous Linux

```bash
# Afficher les interfaces réseau sans fil
ip link show
iw dev

# Lister les réseaux Wi-Fi disponibles
nmcli dev wifi list
iwlist wlan0 scan

# Afficher les informations détaillées de l'interface
iw dev wlan0 info
iw dev wlan0 link

# Afficher la configuration IP
ip addr show wlan0

# Tester la connectivité
ping -I wlan0 8.8.8.8

# Vérifier les statistiques de l'interface
iw dev wlan0 station dump

# Analyse avancée avec aircrack-ng
sudo airmon-ng start wlan0
sudo airodump-ng wlan0mon
```

#### Sous Windows

```powershell
# Lister les réseaux disponibles
netsh wlan show networks

# Afficher le profil d'un réseau
netsh wlan show profile name="MonReseau" key=clear

# Afficher les interfaces Wi-Fi
netsh wlan show interfaces

# Se connecter à un réseau
netsh wlan connect name="MonReseau"
```

#### Sous macOS

```bash
# Lister les réseaux
/System/Library/PrivateFrameworks/Apple80211.framework/Versions/Current/Resources/airport -s

# Afficher les informations de connexion
/System/Library/PrivateFrameworks/Apple80211.framework/Versions/Current/Resources/airport -I

# Scanner les réseaux
airport -s
```

### 9. Applications et Cas d'Usage

- Réseaux domestiques et d'entreprise
- Hotspots publics et gratuits
- Téléphonie Wi-Fi (VoWiFi)
- Streaming vidéo haute définition
- Jeux en ligne et cloud gaming
- Objets connectés (IoT)
- Caméras de surveillance IP
- Imprimantes sans fil
- Smartphones, tablettes, ordinateurs portables

### 10. Avantages et Limitations

**Avantages :**
- Hauts débits
- Compatibilité universelle
- Large éventail de matériel
- Facilité de déploiement
- Évolution constante (Wi-Fi 6/7)

**Limitations :**
- Interférences dans la bande 2.4 GHz
- Portée limitée par rapport à d'autres technologies LPWAN
- Consommation énergétique élevée pour l'IoT
- Sécurité historique perfectible (WEP, WPA)

### 11. Ressources et Liens Wi-Fi

- [IEEE 802.11 Working Group](https://www.ieee802.org/11/)
- [Wi-Fi Alliance](https://www.wi-fi.org/)
- [Aircrack-ng](https://www.aircrack-ng.org/)
- [OpenWrt](https://openwrt.org/)
- [hostapd](https://w1.fi/hostapd/)

---

## Bluetooth

### 1. Définition et Description Générale

**Bluetooth** est une spécification de télécommunications sans fil permettant l'échange de données entre appareils à courte portée. Développée à l'origine pour remplacer les câbles reliant les appareils mobiles et leurs accessoires, Bluetooth est aujourd'hui omniprésent dans les écouteurs, claviers, souris, smartphones, montres connectées, systèmes automobiles et objets IoT.

Bluetooth fonctionne dans la bande ISM **2.4 GHz** et utilise une technique de saut de fréquence appelée **FHSS** (Frequency-Hopping Spread Spectrum). Il est standardisé sous l'**IEEE 802.15.1**.

### 2. Historique et Créateurs

Bluetooth a été développé par **Ericsson** en **1994** sous le nom de projet **MC-Link**. Le nom "Bluetooth" est un hommage au roi viking du Xe siècle **Harald Blåtand** (Harold à la dent bleue), qui unifia les tribus danoises et norvégiennes. Le logo Bluetooth est d'ailleurs composé des runes nordiques Hagall et Bjarkan.

En **1998**, Ericsson, Nokia, IBM, Toshiba et Intel créent le **Bluetooth Special Interest Group (SIG)** pour promouvoir et standardiser la technologie. La première spécification commerciale (Bluetooth 1.0) sort en **1999**.

| Version | Année | Caractéristiques principales |
|---------|-------|------------------------------|
| Bluetooth 1.0 | 1999 | 732 kbps |
| Bluetooth 1.2 | 2003 | 1 Mbps, meilleure coexistence avec Wi-Fi |
| Bluetooth 2.0 + EDR | 2004 | 3 Mbps |
| Bluetooth 3.0 + HS | 2009 | 24 Mbps via Wi-Fi |
| Bluetooth 4.0 | 2010 | BLE (Bluetooth Low Energy) |
| Bluetooth 4.1 | 2013 | Améliorations IoT |
| Bluetooth 4.2 | 2014 | IPv6, LE Secure Connections |
| Bluetooth 5.0 | 2016 | 2 Mbps LE, 4x portée, 8x broadcasting |
| Bluetooth 5.1 | 2019 | Direction finding, AoA/AoD |
| Bluetooth 5.2 | 2020 | LE Audio, LC3 codec, Isochronous channels |
| Bluetooth 5.3 | 2021 | Optimisations de latence et sécurité |
| Bluetooth 5.4 | 2023 | PAwR, Encrypted Advertising Data |
| Bluetooth 6.0 | 2024 | Channel Sounding pour localisation précise |

### 3. Architecture et Couches OSI

Bluetooth définit une architecture en couches propre, appelée **protocole Bluetooth**.

#### Couches principales

- **Radio Layer** : couche physique, définit la modulation GFSK, la puissance, les canaux
- **Baseband Layer** : gestion des liens, adressage, correction d'erreurs, saut de fréquence
- **Link Manager Protocol (LMP)** : authentification, chiffrement, gestion de la connexion
- **Host Controller Interface (HCI)** : interface entre le contrôleur Bluetooth et l'hôte
- **Logical Link Control and Adaptation Protocol (L2CAP)** : multiplexage, segmentation
- **RFCOMM** : émulation de port série virtuel
- **SDP** (Service Discovery Protocol) : découverte des services
- **ATT/GATT** (Attribute Protocol / Generic Attribute Profile) : utilisés en BLE
- **GAP** (Generic Access Profile) : gestion des modes de connexion et de découverte

#### Bluetooth Classic vs Bluetooth Low Energy (BLE)

| Caractéristique | Bluetooth Classic | BLE |
|-----------------|-------------------|-----|
| Introduction | 1999 | 2010 (Bluetooth 4.0) |
| Bande | 2.4 GHz | 2.4 GHz |
| Canaux | 79 canaux de 1 MHz | 40 canaux de 2 MHz |
| Débit max | 3 Mbps (EDR), 24 Mbps (HS) | 2 Mbps |
| Consommation | Élevée | Très faible |
| Portée | ~100 m | Jusqu'à 1 km en champ libre (BLE 5+) |
| Cas d'usage | Audio, transfert de fichiers | IoT, capteurs, balises |

### 4. Fréquences, Débits et Portées

Bluetooth utilise la bande **2.400 - 2.4835 GHz** avec 40 canaux physiques en BLE et 79 en Classic.

| Version | Débit max | Portée typique | Application |
|---------|-----------|----------------|-------------|
| BR/EDR | 3 Mbps | 10-100 m | Audio, données |
| BLE 4.x | 1 Mbps | 10-100 m | Capteurs |
| BLE 5.0 | 2 Mbps | Jusqu'à 400 m en intérieur | IoT, localisation |
| BLE 5.4 | 2 Mbps | Étendue | Réseaux de capteurs |
| Bluetooth 6.0 | 2 Mbps | Améliorée | Ranging, localisation |

### 5. Topologies Réseau

Bluetooth supporte plusieurs topologies :

- **Piconet** : un maître (master) et jusqu'à 7 esclaves actifs (slaves)
- **Scatternet** : interconnexion de plusieurs piconets via des nœuds partagés
- **Broadcasting** : un émetteur, plusieurs récepteurs en écoute (BLE)
- **Mesh** : réseau maillé introduit avec **Bluetooth Mesh** en 2017

### 6. Sécurité Bluetooth

Bluetooth dispose de plusieurs mécanismes de sécurité :

| Mécanisme | Description |
|-----------|-------------|
| Pairing | Association initiale entre deux appareils |
| Authentication | Vérification de l'identité via challenge-response |
| Encryption | Chiffrement des données (E0, AES-CCM) |
| Authorization | Contrôle d'accès aux services |

#### Historique des vulnérabilités

- **Bluejacking** : envoi non sollicité de messages
- **Bluesnarfing** : accès non autorisé à des données
- **Bluebugging** : prise de contrôle à distance
- **KNOB** (Key Negotiation of Bluetooth) : attaque sur la longueur de clé
- **BIAS** (Bluetooth Impersonation AttackS) : usurpation d'identité
- **BLURtooth** : attaque sur le cross-transport key derivation

#### Bluetooth LE Secure Connections

Introduit en Bluetooth 4.2, LE Secure Connections utilise **ECDH P-256** pour l'échange de clés et **AES-CCM** pour le chiffrement. Il est beaucoup plus résistant que le pairing legacy.

### 7. Configuration Matérielle et Logicielle

#### Matériel

- Dongle USB Bluetooth (CSR8510 A10, Realtek, etc.)
- Module HC-05/HC-06 (Bluetooth Classic SPP)
- Module BLE : Nordic nRF52, ESP32, HM-10, CC2541
- Antennes intégrées ou externes

#### Configuration sous Linux avec bluetoothctl

```bash
# Démarrer le service Bluetooth
sudo systemctl start bluetooth

# Lancer l'outil interactif
bluetoothctl

# Commandes dans bluetoothctl
power on
agent on
default-agent
scan on
pair XX:XX:XX:XX:XX:XX
trust XX:XX:XX:XX:XX:XX
connect XX:XX:XX:XX:XX:XX
```

#### Configuration BLE avec gatttool

```bash
# Scanner les périphériques BLE
sudo hcitool lescan

# Se connecter à un périphérique BLE
sudo gatttool -b XX:XX:XX:XX:XX:XX -I

# Dans le prompt :
connect
primary
characteristics
char-read-hnd 0x0002
```

### 8. Commandes de Vérification et Diagnostic

```bash
# Vérifier l'état du contrôleur Bluetooth
hciconfig
hciconfig -a

# Activer l'interface
sudo hciconfig hci0 up

# Scanner les appareils classiques
sudo hcitool scan

# Scanner les appareils BLE
sudo hcitool lescan

# Afficher les services d'un appareil
sdptool browse XX:XX:XX:XX:XX:XX

# Vérifier les périphériques appairés
bluetoothctl paired-devices

# Afficher les informations de l'adaptateur
btmgmt info

# Capture Bluetooth avec Ubertooth
ubertooth-btle -f -c capture.pcap
```

### 9. Applications et Cas d'Usage

- Écouteurs et casques sans fil
- Claviers, souris et manettes
- Montres connectées et trackers d'activité
- Systèmes audio automobiles
- Téléphonie mains libres
- Localisation indoor (beacons BLE)
- Smart home (serrures connectées, capteurs)
- Santé connectée (glucomètres, tensiomètres)
- Réseaux maillés industriels (Bluetooth Mesh)

### 10. Avantages et Limitations

**Avantages :**
- Consommation réduite en BLE
- Facilité de connexion
- Écosystème mature
- Faible coût des modules
- Support natif sur la plupart des appareils

**Limitations :**
- Interférences avec Wi-Fi dans la bande 2.4 GHz
- Portée limitée en Classic
- Latence variable
- Historique de vulnérabilités

### 11. Ressources et Liens Bluetooth

- [Bluetooth SIG](https://www.bluetooth.com/)
- [Bluetooth Protocol Stack](https://www.bluetooth.com/learn-about-bluetooth/tech-overview/)
- [BlueZ - Linux Bluetooth Stack](http://www.bluez.org/)
- [Ubertooth One](https://github.com/greatscottgadgets/ubertooth)
- [Nordic Semiconductor](https://www.nordicsemi.com/)

---

## Zigbee

### 1. Définition et Description Générale

**Zigbee** est un protocole de communication sans fil à haut niveau, conçu pour les réseaux de capteurs et les objets connectés nécessitant une faible consommation énergétique, un faible débit et une faible latence. Il repose sur les couches physique et MAC de la norme **IEEE 802.15.4**.

Zigbee est particulièrement adapté à la domotique, à l'éclairage intelligent, aux thermostats connectés et aux capteurs industriels. Il est promu par la **Connectivity Standards Alliance (CSA)**, anciennement Zigbee Alliance.

### 2. Historique et Créateurs

Le développement de Zigbee débute en **1998**. Le nom "Zigbee" est inspiré du "waggle dance" (danse en zigzag) des abeilles mellifères, symbolisant la communication entre les nœuds d'un réseau.

- **2002** : création de la Zigbee Alliance par plusieurs grands industriels
- **2003** : ratification de la spécification Zigbee 1.0
- **2004** : première version disponible publiquement
- **2007** : Zigbee PRO, apportant de meilleures capacités réseau
- **2023** : Zigbee continue d'évoluer avec Matter et les nouveaux profils

La Zigbee Alliance a été renommée **Connectivity Standards Alliance** en 2021 pour refléter l'élargissement de son périmètre à d'autres protocoles comme Matter.

### 3. Architecture et Couches OSI

Zigbee s'appuie sur les couches 1 et 2 de la norme IEEE 802.15.4, et ajoute ses propres couches réseau et application.

#### Couche Physique (PHY) - IEEE 802.15.4

- Bandes de fréquences : 868 MHz (Europe), 915 MHz (Amérique du Nord), 2.4 GHz (mondial)
- Modulation : DSSS avec O-QPSK
- Débits : 20 kbps (868 MHz), 40 kbps (915 MHz), 250 kbps (2.4 GHz)

#### Couche MAC - IEEE 802.15.4

- Accès au médium : CSMA-CA
- Adressage court (16 bits) et étendu (64 bits)
- Mécanismes d'accusé de réception (ACK)
- Gestion de la sécurité via AES-128

#### Couche Réseau (NWK)

Gère le routage, la découverte de route, la formation du réseau et l'adressage des nœuds.

#### Couche Application (APL)

- **APS** (Application Support Sublayer) : liaison entre ZDO et les applications
- **ZDO** (Zigbee Device Object) : gestion des appareils, découverte, sécurité
- **AF** (Application Framework) : abrite les objets d'application

#### Profils d'Application Zigbee

- **Zigbee Home Automation (ZHA)**
- **Zigbee Light Link (ZLL)**
- **Zigbee Smart Energy (ZSE)**
- **Zigbee Building Automation (ZBA)**
- **Zigbee Retail Services (ZRS)**
- **Zigbee Health Care (ZHC)**
- **Zigbee Telecom Services (ZTS)**
- **Zigbee 3.0** : unification des profils

### 4. Fréquences, Débits et Portées

| Bande | Région | Débit | Canaux | Portée |
|-------|--------|-------|--------|--------|
| 868.0 - 868.6 MHz | Europe | 20 kbps | 1 | Jusqu'à 1 km |
| 902 - 928 MHz | Amérique du Nord | 40 kbps | 10 | Jusqu'à 1 km |
| 2.4 GHz | Mondial | 250 kbps | 16 | 10-100 m |

### 5. Topologies Réseau

Zigbee supporte trois topologies :

- **Étoile (Star)** : tous les nœuds communiquent via le coordinateur
- **Arbre (Tree)** : hiérarchie de routeurs et d'end devices
- **Maillée (Mesh)** : chaque nœud peut relayer les messages, offrant une redondance

#### Types de nœuds

- **Coordinateur (ZC)** : unique par réseau, forme le réseau, stocke les informations
- **Routeur (ZR)** : relaie les messages, alimenté en permanence
- **End Device (ZED)** : nœud terminal, peut dormir pour économiser l'énergie

### 6. Sécurité Zigbee

Zigbee intègre la sécurité à plusieurs niveaux :

- **AES-128** pour le chiffrement
- **Intégrité des messages** via MIC (Message Integrity Code)
- **Link keys** : clés partagées entre deux appareils
- **Network keys** : clé partagée par tous les nœuds du réseau
- **Trust Center** : géré par le coordinateur, distribue les clés

#### Vulnérabilités connues

- Attaques sur la clé de transport
- Interception si la network key est compromise
- Attaques physiques sur les appareils
- Réutilisation de clés par défaut

### 7. Configuration Matérielle et Logicielle

#### Matériel

- Coordinateur USB : CC2531, CC2652P, Sonoff ZBDongle-P/E
- Modules Zigbee : XBee, CC2530, EByte E18
- Passerelles : Philips Hue Bridge, Samsung SmartThings, Hubitat, Home Assistant SkyConnect
- Analyseurs : CC2531 avec firmware sniffer

#### Configuration avec zigbee2mqtt

zigbee2mqtt est un pont logiciel très populaire pour connecter les appareils Zigbee à un réseau IP.

Installation sur Linux (Debian/Ubuntu) :

```bash
# Prérequis
sudo apt update
sudo apt install -y nodejs npm git make g++ gcc

# Cloner le dépôt
git clone https://github.com/Koenkk/zigbee2mqtt.git
cd zigbee2mqtt
git checkout $(git describe --tags --abbrev=0)

# Installer les dépendances
npm install

# Configurer
cp data/configuration.example.yaml data/configuration.yaml
```

Exemple de `data/configuration.yaml` :

```yaml
homeassistant: true
permit_join: true
mqtt:
  server: 'mqtt://localhost'
  user: mqtt_user
  password: mqtt_password
serial:
  port: /dev/ttyUSB0
  adapter: zstack
frontend:
  port: 8080
advanced:
  log_level: info
  pan_id: 6754
  channel: 11
  network_key: GENERATE
```

Démarrage :
```bash
npm start
```

### 8. Commandes de Vérification et Diagnostic

```bash
# Lister les ports série
ls -l /dev/ttyUSB*
dmesg | grep tty

# Vérifier les permissions
sudo usermod -a -G dialout $USER

# Vérifier le statut de zigbee2mqtt
systemctl status zigbee2mqtt

# Journaux
journalctl -u zigbee2mqtt -f

# Scanner le canal Zigbee avec le CC2531 sniffer
# Utiliser Wireshark avec le plugin zigbee

# Vérifier les appareils appairés
curl http://localhost:8080/api/devices
```

### 9. Applications et Cas d'Usage

- Éclairage intelligent (Philips Hue, IKEA TRÅDFRI)
- Thermostats connectés (Nest, Tado, Netatmo)
- Capteurs de mouvement, d'ouverture, de fumée
- Serrures connectées
- Télécommandes universelles
- Réseaux de capteurs industriels
- Smart metering (compteurs intelligents)
- Agriculture intelligente

### 10. Avantages et Limitations

**Avantages :**
- Très faible consommation
- Topologie maillée robuste
- Coût des modules faible
- Interopérabilité via profils standardisés
- Grand écosystème domotique

**Limitations :**
- Faible débit
- Interférences possibles avec Wi-Fi (2.4 GHz)
- Complexité de déploiement à grande échelle
- Nécessite un coordinateur

### 11. Ressources et Liens Zigbee

- [Connectivity Standards Alliance](https://csa-iot.org/)
- [Zigbee Alliance (archive)](https://zigbeealliance.org/)
- [zigbee2mqtt](https://www.zigbee2mqtt.io/)
- [ZHA Integration - Home Assistant](https://www.home-assistant.io/integrations/zha/)
- [Texas Instruments Z-Stack](https://www.ti.com/tool/Z-STACK)

---

## Z-Wave

### 1. Définition et Description Générale

**Z-Wave** est un protocole de communication sans fil propriétaire, conçu spécifiquement pour la domotique et les réseaux de contrôle résidentiels. Contrairement à Zigbee, Z-Wave fonctionne en **sous-gigahertz** (868 MHz en Europe, 908 MHz aux États-Unis, 920 MHz au Japon), ce qui lui confère une meilleure pénétration des murs et moins d'interférences avec les technologies 2.4 GHz.

Z-Wave est promu par la **Z-Wave Alliance** et géré par **Silicon Labs**.

### 2. Historique et Créateurs

Z-Wave a été développé par la société danoise **Zen-Sys** en **1999**. En **2005**, la **Z-Wave Alliance** est créée pour standardiser et promouvoir la technologie. En **2009**, Sigma Designs rachète Zen-Sys, puis **Silicon Labs** acquiert la division Z-Wave de Sigma Designs en **2018**.

- **1999** : développement par Zen-Sys
- **2003** : première certification commerciale
- **2005** : création de la Z-Wave Alliance
- **2013** : Z-Wave Plus, amélioration de la portée et de la batterie
- **2019** : Z-Wave Long Range (LR)
- **2023** : Z-Wave Plus v2 et améliorations de sécurité

### 3. Architecture et Couches OSI

Z-Wave définit sa propre pile protocolaire, centrée sur une architecture maillée.

#### Couche Physique

- Bandes sous-gigahertz
- Modulation FSK (Frequency-Shift Keying)
- Débits : 9.6 / 40 / 100 kbps selon les versions
- Version Z-Wave Long Range : jusqu'à plusieurs kilomètres

#### Couche MAC et Réseau

- Protocole maillé propriétaire
- Routage dynamique
- Adressage sur 8 bits (jusqu'à 232 nœuds en réseau classique)
- Jusqu'à 4000 nœuds en Z-Wave Long Range

#### Couche Transport et Application

- **Z-Wave Transport Layer** : fiabilité des messages
- **Z-Wave Application Layer** : commandes classes (Command Classes)
- **Z-Wave Plus** : améliorations de sécurité et de performances

### 4. Fréquences, Débits et Portées

| Région | Fréquence | Débit | Portée typique |
|--------|-----------|-------|----------------|
| Europe | 868.42 MHz | 9.6 / 40 / 100 kbps | 30-100 m |
| États-Unis | 908.42 MHz | 9.6 / 40 / 100 kbps | 30-100 m |
| Japon | 920 MHz | 9.6 / 40 / 100 kbps | 30-100 m |
| Z-Wave LR | Sous-GHz | 100 kbps | Jusqu'à 1-2 km |

### 5. Topologies Réseau

Z-Wave utilise exclusivement une topologie **maillée** (mesh). Chaque nœud alimenté sur secteur peut servir de répéteur pour étendre la portée du réseau.

#### Types de nœuds

- **Controller** : contrôleur principal, gère le réseau
- **Slave** : nœud qui répond aux commandes
- **Routing Slave** : nœud capable de router les messages
- **Portable Controller** : contrôleur mobile
- **Z-Wave Long Range** : nœuds en étoile avec portée étendue

### 6. Sécurité Z-Wave

Z-Wave intègre plusieurs niveaux de sécurité :

- **S0** : chiffrement AES-128, introduit pour sécuriser les commandes critiques
- **S2** : amélioration majeure introduite en 2016, avec chiffrement AEAD et authentification
- **S2 Access Control** : pour les serrures et dispositifs d'accès
- **S2 Authenticated** : pour les dispositifs avec interface utilisateur
- **S2 Unauthenticated** : pour les capteurs simples

#### Avantages de S2

- Échange de clés sécurisé via ECDH
- Authentification du réseau
- Protection contre les attaques Man-in-the-Middle
- Réduction de la latence par rapport à S0

### 7. Configuration Matérielle et Logicielle

#### Matériel

- Contrôleur USB : Aeotec Z-Stick, Zooz ZST10, Silicon Labs UZB3
- Passerelles : Samsung SmartThings, Hubitat Elevation, HomeSeer
- Modules Z-Wave : Fibaro, Qubino, Aeotec, Zooz

#### Configuration avec Z-Wave JS

Z-Wave JS est une implémentation moderne de la pile Z-Wave pour Node.js.

```bash
# Installation via Docker
docker run -d \
  --name zwavejs2mqtt \
  --restart always \
  --device=/dev/ttyUSB0:/dev/zwave \
  -v $(pwd)/store:/usr/src/app/store \
  -p 8091:8091 \
  -p 3000:3000 \
  zwavejs/zwave-js-ui:latest
```

Accéder à l'interface web : `http://localhost:8091`

#### Configuration d'un contrôleur Aeotec Z-Stick

```bash
# Insérer le dongle et vérifier le port
ls -l /dev/ttyACM*

# Démarrer Z-Wave JS UI et inclure un périphérique
# Aller dans Settings > Z-Wave > Serial Port : /dev/ttyACM0
# Cliquer sur "Manage Nodes" > "Inclusion"
```

### 8. Commandes de Vérification et Diagnostic

```bash
# Lister les ports série
ls /dev/tty*

# Vérifier les logs Z-Wave JS
docker logs -f zwavejs2mqtt

# Interroger l'API REST
curl http://localhost:8091/api/health

# Vérifier les nœuds du réseau
curl http://localhost:8091/api/nodes
```

### 9. Applications et Cas d'Usage

- Automatisation résidentielle
- Serrures connectées
- Volets et stores motorisés
- Thermostats et chauffage
- Détecteurs d'ouverture, de fuite, de fumée
- Interrupteurs et prises intelligentes
- Éclairage connecté
- Systèmes de sécurité

### 10. Avantages et Limitations

**Avantages :**
- Excellente pénétration des murs (sous-GHz)
- Faible interférence avec Wi-Fi/Bluetooth
- Réseau maillé très fiable
- Sécurité S2 robuste
- Interopérabilité certifiée

**Limitations :**
- Propriétaire et coût des modules parfois élevé
- Moins populaire en dehors de l'Amérique du Nord et de l'Europe
- Bandes régionales différentes (incompatibilité inter-régions)
- Moins flexible que Zigbee pour les développeurs

### 11. Ressources et Liens Z-Wave

- [Z-Wave Alliance](https://z-wavealliance.org/)
- [Silicon Labs Z-Wave](https://www.silabs.com/wireless/z-wave)
- [Z-Wave JS](https://zwave-js.github.io/)
- [OpenZWave](https://github.com/OpenZWave) (obsolète, remplacé par Z-Wave JS)

---

## LoRaWAN

### 1. Définition et Description Générale

**LoRaWAN** (Long Range Wide Area Network) est un protocole de télécommunication bas débit et longue portée, conçu pour les réseaux d'objets connectés (IoT). Il repose sur la technologie de modulation **LoRa** (Long Range) développée par **Semtech**.

LoRaWAN est particulièrement adapté aux applications nécessitant une faible consommation énergétique, une longue portée et un faible coût d'infrastructure. Il est utilisé massivement dans les smart cities, l'agriculture, la gestion des déchets, le suivi d'actifs et l'environnement.

### 2. Historique et Créateurs

- **2009** : Cycleo, une startup française, développe la technologie LoRa
- **2012** : Semtech rachète Cycleo pour 5 millions de dollars
- **2015** : création de la **LoRa Alliance**, consortium d'industriels
- **2016** : spécification LoRaWAN 1.0 publiée
- **2017** : LoRaWAN 1.0.2
- **2018** : LoRaWAN 1.0.3
- **2020** : LoRaWAN 1.0.4
- **2021** : LoRaWAN 1.1 avec sécurité renforcée
- **2024** : LoRaWAN 1.1 continue d'être déployé, avec des améliorations régionales

### 3. Architecture et Couches OSI

LoRaWAN s'appuie sur une architecture en trois couches principales.

#### Couche Physique LoRa

- Bandes ISM : 868 MHz (Europe), 915 MHz (Amérique du Nord), 433 MHz, 923 MHz (Asie)
- Modulation : Chirp Spread Spectrum (CSS)
- Débits : 0.3 kbps à 50 kbps
- Facteurs d'étalement (Spreading Factor) : SF7 à SF12
- Portée : 2-15 km en zone urbaine, jusqu'à 50 km en zone rurale

#### Couche MAC LoRaWAN

Gère l'accès au réseau, le routage des messages vers les serveurs applicatifs, la sécurité et la gestion des appareils.

#### Architecture Réseau LoRaWAN

```
[End Device] <--LoRa--> [Gateway] <--IP--> [Network Server] <--IP--> [Application Server]
```

- **End Device** : capteur ou objet connecté
- **Gateway** : passerelle recevant les messages radio et les transmettant au serveur
- **Network Server** : gère les paquets, le routage, l'ADR (Adaptive Data Rate)
- **Application Server** : traite les données applicatives
- **Join Server** : gère l'activation et les clés (architecture 1.1)

### 4. Fréquences, Débits et Portées

| Région | Bande | Canaux | Débit typique | Portée |
|--------|-------|--------|---------------|--------|
| Europe | 863-870 MHz | Plusieurs | 0.3-50 kbps | 2-15 km urbain |
| États-Unis | 902-928 MHz | 64+8 | 0.9-50 kbps | 2-15 km urbain |
| Chine | 470-510 MHz | - | 0.3-50 kbps | 2-15 km urbain |
| Asie-Pacifique | 923 MHz | - | 0.3-50 kbps | 2-15 km urbain |

### 5. Topologies Réseau

LoRaWAN utilise une topologie en **étoile sur étoile** (star-of-stars) :

- Les end devices communiquent avec une ou plusieurs gateways
- Les gateways sont connectées au Network Server via IP
- Un message peut être reçu par plusieurs gateways simultanément

#### Classes d'appareils

| Classe | Caractéristiques | Cas d'usage |
|--------|-----------------|-------------|
| Classe A | Réception après chaque transmission (downlink uniquement après uplink) | Capteurs, économie d'énergie maximale |
| Classe B | Réception périodique synchronisée par balises | Compteurs, applications temps réel modérées |
| Classe C | Réception continue (hors transmission) | Actionneurs, vannes, éclairage |

### 6. Sécurité LoRaWAN

LoRaWAN intègre une sécurité robuste dès la conception :

- **AES-128** pour le chiffrement et l'intégrité
- **DevEUI** : identifiant unique de l'appareil (64 bits)
- **AppEUI / JoinEUI** : identifiant de l'application/join server
- **AppKey** : clé racine partagée entre appareil et join server
- **NwkSKey** : clé de session réseau
- **AppSKey** : clé de session applicative

#### Modes d'activation

- **ABP** (Activation By Personalization) : clés prédéfinies manuellement
- **OTAA** (Over-The-Air Activation) : clés négociées dynamiquement (recommandé)

LoRaWAN 1.1 introduit une séparation renforcée entre les clés réseau et applicatives, ainsi qu'un **Join Server** dédié.

### 7. Configuration Matérielle et Logicielle

#### Matériel

- **End devices** : capteurs Dragino, Elsys, Milesight, Seeed Studio
- **Gateways** : Dragino LG01, RAKWireless RAK7246, The Things Indoor Gateway, MikroTik wAP
- **Modules LoRa** : SX1276, SX1272, RFM95W, RN2483
- **Développement** : Arduino + module LoRa, ESP32 + LoRa, Raspberry Pi + concentrateur SX1301

#### Configuration d'un nœud avec Arduino

```cpp
#include <LoRa.h>

const int csPin = 10;
const int resetPin = 9;
const int irqPin = 2;

void setup() {
  Serial.begin(9600);
  while (!Serial);
  LoRa.setPins(csPin, resetPin, irqPin);
  if (!LoRa.begin(868E6)) {
    Serial.println("Erreur initialisation LoRa");
    while (1);
  }
  LoRa.setSpreadingFactor(7);
  LoRa.setSignalBandwidth(125E3);
  LoRa.setCodingRate4(5);
}

void loop() {
  LoRa.beginPacket();
  LoRa.print("Hello LoRaWAN");
  LoRa.endPacket();
  delay(10000);
}
```

#### Configuration d'une passerelle avec The Things Network (TTN)

1. Créer un compte sur [The Things Network](https://www.thethingsnetwork.org/)
2. Enregistrer la gateway dans la console
3. Configurer le packet forwarder sur la passerelle
4. Connecter l'end device avec les clés DevEUI, AppEUI, AppKey

Exemple de configuration d'une passerelle Dragino LG01-P :

```bash
# Se connecter à la gateway via SSH
ssh root@10.130.1.1

# Configurer le packet forwarder
vi /etc/lora/local_conf.json

# Exemple de configuration
{
  "gateway_conf": {
    "gateway_ID": "YOUR_GATEWAY_EUI",
    "server_address": "eu1.cloud.thethings.network",
    "serv_port_up": 1700,
    "serv_port_down": 1700
  }
}
```

### 8. Commandes de Vérification et Diagnostic

```bash
# Vérifier les logs du packet forwarder
tail -f /var/log/lora-pkt-fwd.log

# Vérifier la connectivité gateway -> Network Server
ping eu1.cloud.thethings.network

# Interroger TTN via CLI
ttn-lw-cli end-devices list application-id

# Vérifier les statistiques du concentrateur LoRa
# Sur gateway basée sur SX1301
./util_spi_stress -h

# Analyse spectrale avec un SDR (HackRF, RTL-SDR)
gqrx
```

### 9. Applications et Cas d'Usage

- Compteurs d'eau, de gaz, d'électricité intelligents
- Gestion des déchets (capteurs de remplissage)
- Station météorologique et environnementale
- Suivi d'actifs et de flottes
- Agriculture de précision (humidité du sol, température)
- Smart parking
- Surveillance de bâtiments
- Gestion de l'éclairage public
- Tracking de colis et de bétail

### 10. Avantages et Limitations

**Avantages :**
- Très longue portée
- Très faible consommation énergétique
- Coût réduit des modules
- Architecture décentralisée
- Pénétration correcte des obstacles
- Sécurité intégrée

**Limitations :**
- Très faible débit
- Latence élevée
- Bande passante limitée et partagée
- Réglementation stricte du duty cycle (1% en Europe)
- Risque d'interférences dans les bandes ISM
- Pas adapté aux applications temps réel ou streaming

### 11. Ressources et Liens LoRaWAN

- [LoRa Alliance](https://lora-alliance.org/)
- [The Things Network](https://www.thethingsnetwork.org/)
- [Semtech LoRa](https://www.semtech.com/lora)
- [ChirpStack](https://www.chirpstack.io/)
- [Arduino-LoRa Library](https://github.com/sandeepmistry/arduino-LoRa)

---

## NFC

### 1. Définition et Description Générale

**NFC** (Near Field Communication) est une technologie de communication sans fil à très courte portée, généralement inférieure à 10 cm. Elle dérive de la RFID (Radio Frequency Identification) et fonctionne à la fréquence de **13.56 MHz**.

NFC permet l'échange bidirectionnel de données entre deux appareils compatibles. Elle est largement utilisée pour les paiements sans contact, le transport en commun, le contrôle d'accès, le pairing de devices et le partage de données.

### 2. Historique et Créateurs

Les racines du NFC remontent à la technologie RFID des années 1980.

- **2002** : Sony et Philips (devenu NXP Semiconductors) développent conjointement la technologie NFC
- **2004** : création du **NFC Forum** pour standardiser et promouvoir NFC
- **2006** : premières spécifications NFC Forum publiées
- **2010** : premiers smartphones avec NFC (Nexus S, Samsung)
- **2011** : lancement de Google Wallet
- **2014** : lancement d'Apple Pay
- **2024** : NFC omniprésent dans les smartphones, cartes bancaires et transports

### 3. Architecture et Couches OSI

NFC s'appuie sur les normes ISO/IEC et NFC Forum.

#### Normes de base

- **ISO/IEC 14443** : cartes à proximité (Type A, Type B)
- **ISO/IEC 18092** : NFC Interface and Protocol (NFCIP-1), définit les modes actif et passif
- **ISO/IEC 15693** : cartes à champ lointain
- **ECMA-340/ECMA-352** : standards proches de NFCIP
- **NFC Forum Type 1/2/3/4/5** : définitions des tags NFC

#### Modes de communication

- **Mode actif** : les deux appareils génèrent leur propre champ
- **Mode passif** : un appareil alimente le tag par induction, l'autre communique en chargeant la modulation

#### Modes opérationnels

- **Reader/Writer** : le smartphone lit ou écrit un tag NFC
- **Peer-to-Peer** : deux appareils échangent des données
- **Card Emulation** : le smartphone se comporte comme une carte (paiement, transport)

#### Pile protocolaire NFC Forum

```
Application Layer (NDEF, RTD, Handover, etc.)
LLCP (Logical Link Control Protocol)
NFC-DEP (Data Exchange Protocol)
Analog/Digital Layer (RF, modulation)
```

### 4. Fréquences, Débits et Portées

| Caractéristique | Valeur |
|-----------------|--------|
| Fréquence | 13.56 MHz |
| Débit | 106, 212, 424 kbps |
| Portée | 0-10 cm (typiquement < 4 cm) |
| Modulation | ASK, BPSK selon le mode |
| Alimentation | Induction électromagnétique |

### 5. Topologies Réseau

NFC n'est pas un réseau au sens classique. Il s'agit d'une communication point-à-point très courte portée. Les topologies possibles sont :

- **Point-à-point** : deux appareils NFC
- **Lecteur-tag** : un lecteur actif interroge un tag passif
- **Émulation de carte** : un appareil actif se fait passer pour une carte

### 6. Sécurité NFC

La sécurité NFC repose sur plusieurs mécanismes :

- **Très courte portée** : réduit les risques d'interception à distance
- **SE** (Secure Element) : puce sécurisée hébergeant les applications sensibles
- **HCE** (Host Card Emulation) : émulation de carte sans SE physique
- **Tokenisation** : utilisation de numéros virtuels pour les paiements
- **Authentification mutuelle** dans les protocoles de paiement
- **NDEF** avec champs protégés en lecture/écriture

#### Vulnérabilités et attaques

- **Eavesdropping** : interception du signal à très courte distance
- **Relay attacks** : relais du signal NFC à distance
- **Skimming** : lecture frauduleuse de tags/cartes
- **Tag cloning** : clonage de tags non protégés
- **Malicious tags** : tags NFC malveillants redirigeant vers des sites dangereux

### 7. Configuration Matérielle et Logicielle

#### Matériel

- Smartphones équipés de NFC (Android, iPhone)
- Lecteurs NFC USB : ACR122U, PN532, RC522
- Tags NFC : NTAG213/215/216, MIFARE Classic, MIFARE DESFire
- Cartes NFC : cartes bancaires, cartes de transport

#### Lecture/écriture de tags NFC sous Linux

Avec libnfc et un lecteur PN532/ACR122U :

```bash
# Installer libnfc
sudo apt install libnfc-bin libnfc-examples

# Lister les lecteurs
nfc-list

# Lire un tag
nfc-poll

# Écrire un tag NDEF
python3 -m pip install nfcpy
python3
```

Script Python avec nfcpy :

```python
import nfc
import ndef

def on_connect(tag):
    print("Tag détecté:", tag)
    record = ndef.UriRecord("https://hackers_tchad.github.io")
    tag.ndef.records = [record]
    print("Écriture terminée")
    return True

clf = nfc.ContactlessFrontend('usb')
clf.connect(rdwr={'on-connect': on_connect})
```

#### Paiement NFC avec card emulation

Les terminaux de paiement NFC utilisent généralement les protocoles EMVCo et des applications hébergées dans un Secure Element ou via HCE.

### 8. Commandes de Vérification et Diagnostic

```bash
# Lister les périphériques NFC
lsusb

# Vérifier que le lecteur est reconnu
dmesg | grep -i nfc

# Scanner avec nfc-list
nfc-list

# Tester la communication avec un tag
nfc-poll

# Lire les informations d'un tag MIFARE
mifare-classic-read-ndef

# Écrire un tag MIFARE
mifare-classic-write-ndef

# Analyse avec Proxmark3
proxmark3> hf search
proxmark3> hf 14a reader
proxmark3> hf 14a info
```

### 9. Applications et Cas d'Usage

- Paiements sans contact (Visa, Mastercard, Apple Pay, Google Pay)
- Billettique et transport en commun
- Contrôle d'accès physique
- Authentification à deux facteurs (clés FIDO2 NFC)
- Pairing rapide d'appareils (enceintes, écouteurs)
- Partage de fichiers et contacts
- Tags intelligents pour la domotique
- Marketing et objets publicitaires connectés
- Cartes de fidélité et tickets

### 10. Avantages et Limitations

**Avantages :**
- Très simple d'utilisation (rapprochement)
- Faible consommation énergétique
- Coût des tags très faible
- Sécurité renforcée par la proximité physique
- Compatibilité avec l'infrastructure RFID existante

**Limitations :**
- Portée très courte
- Débit faible
- Nécessite un approchement précis
- Vulnérabilité aux relay attacks
- Interopérabilité variable selon les implémentations

### 11. Ressources et Liens NFC

- [NFC Forum](https://nfc-forum.org/)
- [NXP NFC](https://www.nxp.com/products/rfid-nfc/nfc)
- [libnfc](https://github.com/nfc-tools/libnfc)
- [nfcpy](https://github.com/nfcpy/nfcpy)
- [Proxmark3](http://www.proxmark.org/)

---

## Comparatif Global des Protocoles

| Critère | Wi-Fi | Bluetooth | Zigbee | Z-Wave | LoRaWAN | NFC |
|---------|-------|-----------|--------|--------|---------|-----|
| Standard | IEEE 802.11 | IEEE 802.15.1 | IEEE 802.15.4 + Zigbee | Propriétaire Z-Wave | LoRa Alliance | NFC Forum / ISO |
| Fréquence | 2.4/5/6 GHz | 2.4 GHz | 2.4/868/915 MHz | 868/908/920 MHz | 868/915/433/923 MHz | 13.56 MHz |
| Débit | 1 Mbps - 46 Gbps | 1-3 Mbps (Classic), 2 Mbps (BLE) | 20-250 kbps | 9.6-100 kbps | 0.3-50 kbps | 106-424 kbps |
| Portée | 30-250 m | 10-100 m (Classic), 1 km+ (BLE 5+) | 10-100 m (2.4 GHz), 1 km (sous-GHz) | 30-100 m, 1-2 km (LR) | 2-15 km urbain, 50 km rural | < 10 cm |
| Consommation | Élevée | Faible à moyenne | Très faible | Faible | Très faible | Très faible |
| Topologie | Infrastructure, Ad-hoc | Piconet, Mesh | Star, Tree, Mesh | Mesh | Star-of-stars | Point-à-point |
| Cas d'usage | Internet haut débit | Audio, périphériques | Domotique, capteurs | Domotique | IoT longue portée | Paiement, accès |
| Sécurité | WPA3, AES | LE Secure Connections, AES | AES-128 | S2, AES-128 | AES-128 | SE, HCE, tokenisation |
| Coût module | Moyen | Faible | Très faible | Moyen à élevé | Faible | Très faible |

---

## Sécurité Offensive & Défensive

### Principes généraux

La sécurité des réseaux sans fil repose sur trois piliers :

1. **Confidentialité** : empêcher la lecture non autorisée des données
2. **Intégrité** : garantir que les données n'ont pas été altérées
3. **Disponibilité** : assurer le bon fonctionnement du réseau

### Wi-Fi - Attaques et défenses

#### Attaques

- **Wardriving** : recherche de réseaux Wi-Fi accessibles
- **WPA handshake capture** : capture du handshake pour cassage offline
- **Evil Twin** : faux point d'accès usurpant un SSID légitime
- **Deauthentication** : déconnexion forcée des clients
- **KRACK** (Key Reinstallation Attack)
- **Dragonblood** : attaques sur WPA3

#### Défenses

- Utiliser WPA3 ou WPA2-Enterprise avec RADIUS
- Masquer le SSID (efficacité limitée)
- Filtrage MAC (efficacité limitée)
- Segmenter les réseaux invités et IoT
- Surveiller les points d'accès non autorisés
- Mettre à jour régulièrement le firmware

### Bluetooth - Attaques et défenses

#### Attaques

- Bluejacking, Bluesnarfing, Bluebugging
- KNOB et BIAS
- Pairing sans authentification
- Sniffing avec Ubertooth

#### Défenses

- Désactiver la visibilité permanente
- Utiliser LE Secure Connections
- Refuser les appairages inconnus
- Mettre à jour les appareils
- Activer le chiffrement

### Zigbee - Attaques et défenses

#### Attaques

- Capture de la network key
- Réenclenchement d'appareil compromis
- Attaques physiques sur les nœuds
- Spoofing de coordinateur

#### Défenses

- Changer les clés par défaut
- Utiliser le Trust Center
- Segmenter les réseaux
- Surveiller les appairages
- Protéger physiquement les appareils

### Z-Wave - Attaques et défenses

#### Attaques

- Interception si clés compromises
- Inclusion d'appareils non autorisés
- Attaques sur S0 (latence)

#### Défenses

- Utiliser S2 exclusivement
- Vérifier l'authenticité des appareils
- Restreindre l'inclusion
- Surveiller le réseau

### LoRaWAN - Attaques et défenses

#### Attaques

- Brouillage (jamming)
- Eavesdropping si clés compromises
- Replay attacks
- Attaques sur les gateways

#### Défenses

- Utiliser OTAA plutôt qu'ABP
- Protéger les clés AppKey
- Sécuriser les gateways
- Utiliser des serveurs d'application fiables
- Chiffrement applicatif supplémentaire

### NFC - Attaques et défenses

#### Attaques

- Skimming
- Relay attacks
- Tag malveillant
- Clonage de tags simples

#### Défenses

- Utiliser des tags cryptographiques (DESFire)
- Activer la protection en écriture
- Sensibiliser les utilisateurs
- Vérifier les URLs des tags
- Utiliser l'authentification mutuelle

---

## Outils Universels d'Analyse

### Wi-Fi

- **Aircrack-ng** : suite complète d'audit Wi-Fi
- **Wireshark** : analyseur de protocoles
- **Kismet** : détection de réseaux sans fil
- **Wifite** : automatisation des audits Wi-Fi
- **Reaver** : attaques WPS
- **Bettercap** : MITM et Wi-Fi
- **Fern Wi-Fi Cracker** : interface graphique
- **Hashcat** : cassage de mots de passe
- **hcxtools** : conversion et analyse de captures

### Bluetooth

- **BlueZ** : pile Bluetooth officielle Linux
- **bluetoothctl** : contrôle interactif
- **gatttool** : interaction BLE
- **Ubertooth One** : sniffing Bluetooth
- **BLEAH** : scanner BLE
- **Bettercap** : attaques Bluetooth
- **nRF Connect** : application mobile de scan BLE

### Zigbee

- **zigbee2mqtt** : passerelle Zigbee-MQTT
- **ZHA** : intégration Home Assistant
- **CC2531 sniffer** : analyse avec Wireshark
- **KillerBee** : framework d'audit Zigbee
- **SecBee** : outils de sécurité Zigbee

### Z-Wave

- **Z-Wave JS UI** : interface moderne
- **OpenZWave** (obsolète)
- **PC Controller** (Silicon Labs)
- **Zensys Tools** (anciens)

### LoRaWAN

- **ChirpStack** : Network Server open source
- **The Things Stack** : infrastructure LoRaWAN
- **RTL-SDR + GQRX** : analyse spectrale
- **LoStik** : dongle USB LoRa
- **Universal Radio Hacker** : analyse SDR

### NFC

- **libnfc** : bibliothèque NFC pour Linux
- **nfcpy** : bibliothèque Python
- **Proxmark3** : plateforme RFID/NFC avancée
- **MIFARE Classic Tool** (Android)
- **NFC Tools** (Android/iOS)

---

## Ressources, Livres & Liens

### Livres recommandés

| Titre | Auteur(s) | Sujet |
|-------|-----------|-------|
| "802.11 Wireless Networks: The Definitive Guide" | Matthew S. Gast | Wi-Fi |
| "Real 802.11 Security: Wi-Fi Protected Access and 802.11i" | Jon Edney, William A. Arbaugh | Sécurité Wi-Fi |
| "Bluetooth Low Energy: The Developer's Handbook" | Robin Heydon | BLE |
| "Zigbee Wireless Networking" | Drew Gislason | Zigbee |
| "The Handbook of Personal Area Networking Technologies and Protocols" | Francis DaCosta | PAN |
| "LoRaWAN in Action" | Thomas Telkamp, Johan Stokking | LoRaWAN |
| "The Art of RFID and NFC Hacking" | Multiple | RFID/NFC |
| "Hacking Exposed Wireless" | Johnny Cache, Joshua Wright | Sécurité sans fil |
| "Kali Linux Wireless Penetration Testing Beginner's Guide" | Vivek Ramachandran | Pentesting Wi-Fi |
| "Practical IoT Hacking" | Fotios Chantzis, Ioannis Stais, et al. | IoT et protocoles |

### Liens web essentiels

- [IEEE 802.11](https://www.ieee802.org/11/)
- [Wi-Fi Alliance](https://www.wi-fi.org/)
- [Bluetooth SIG](https://www.bluetooth.com/)
- [Connectivity Standards Alliance](https://csa-iot.org/)
- [Z-Wave Alliance](https://z-wavealliance.org/)
- [LoRa Alliance](https://lora-alliance.org/)
- [NFC Forum](https://nfc-forum.org/)
- [Aircrack-ng](https://www.aircrack-ng.org/)
- [Kismet](https://www.kismetwireless.net/)
- [Wireshark](https://www.wireshark.org/)
- [The Things Network](https://www.thethingsnetwork.org/)
- [ChirpStack](https://www.chirpstack.io/)
- [OpenWrt](https://openwrt.org/)
- [Home Assistant](https://www.home-assistant.io/)
- [hackers_tchad GitHub](https://github.com/hackers_tchad)

### Communautés et forums

- [Reddit r/RTLSDR](https://www.reddit.com/r/RTLSDR/)
- [Reddit r/wireless](https://www.reddit.com/r/wireless/)
- [Reddit r/hacking](https://www.reddit.com/r/hacking/)
- [Hackaday.io](https://hackaday.io/)
- [Wireless LAN Professionals](https://www.wlanpros.com/)

---

## Glossaire

| Terme | Définition |
|-------|------------|
| **ACK** | Accusé de réception |
| **ADR** | Adaptive Data Rate (LoRaWAN) |
| **AES** | Advanced Encryption Standard |
| **AP** | Access Point (point d'accès Wi-Fi) |
| **BSSID** | Basic Service Set Identifier |
| **BLE** | Bluetooth Low Energy |
| **CSMA/CA** | Carrier Sense Multiple Access with Collision Avoidance |
| **CSS** | Chirp Spread Spectrum |
| **DSSS** | Direct Sequence Spread Spectrum |
| **EDR** | Enhanced Data Rate (Bluetooth) |
| **FHSS** | Frequency-Hopping Spread Spectrum |
| **FSK** | Frequency-Shift Keying |
| **GFSK** | Gaussian Frequency-Shift Keying |
| **HCI** | Host Controller Interface |
| **ISM** | Industrial, Scientific and Medical (bandes de fréquences) |
| **LoRa** | Long Range (modulation) |
| **MAC** | Media Access Control |
| **Mesh** | Topologie maillée |
| **MIMO** | Multiple Input Multiple Output |
| **MQTT** | Message Queuing Telemetry Transport |
| **NDEF** | NFC Data Exchange Format |
| **OFDM** | Orthogonal Frequency Division Multiplexing |
| **OFDMA** | Orthogonal Frequency Division Multiple Access |
| **OTAA** | Over-The-Air Activation (LoRaWAN) |
| **PHY** | Couche physique |
| **PSK** | Pre-Shared Key |
| **RADIUS** | Remote Authentication Dial-In User Service |
| **RFID** | Radio Frequency Identification |
| **SAE** | Simultaneous Authentication of Equals |
| **SDR** | Software Defined Radio |
| **SSID** | Service Set Identifier |
| **STA** | Station Wi-Fi |
| **WPA** | Wi-Fi Protected Access |
| **ZDO** | Zigbee Device Object |
| **ZED** | Zigbee End Device |

---

## Licence & Avertissement Légal

### Auteur

**hackers_tchad**

### Date

**2026**


<p>
  <font color="green">████████████████████████████████████████████████████████</font>
</p>
<p>
  <font color="green">FIN DU CYBER-NETWORK PROTOCOLS MASTER HANDBOOK</font>
</p>
<p>
  <font color="green">████████████████████████████████████████████████████████</font>
</p>

</div>
