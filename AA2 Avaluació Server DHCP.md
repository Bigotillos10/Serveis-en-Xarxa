# AA2 Avaluacio Server DHCP

**Alumne:** Biel Clavé Navarro  
**Mòdul:** 0227 Serveis en Xarxa  
**Curs:** CFGM SMX2  
**Data:** 2/10/2026 - 8/10/2026  

---

## ÍNDEX

1. [Objectiu](#1-objectiu)

2. [Part 1](#2-Part-1)

3. [Part 2](#3-Part-2)

4. [Part 3](#4-Part-3)

5. [Coses X](#5-coses-x)

7. [Incidències](#7-incidències)

8. [Conclusions](#8-conclusions)


---

## 1. Objectiu

- Configureu un servidor DHCP amb Kea sobre Ubuntu Server i comproveu-ne el funcionament mitjançant un client Zorin

---

## 2. Part 1

- Configura correctament el servidor Ubuntu Server i instal.la el servei de kea.

- Edita l'arxiu de configuracio de kea per desactivar eldhcpv6 i el DDNS.

- Edita l'arxiu /etc/kea/kea-dhcp4.conf per tal de tenir un
servidor DHCP que configuri correctament un client amb
els següents paràmetres:
 *Pool 192.169.x.10 fins 192.169.x.50*
 *Porta d'enllaç 192.169.x.254*
 *DNS 8.8.8.8*

- Un cop configurat, reinicia el servei.

---

## 3. Part 2

- L'equip Zorin inicialment el posem en NAT.

- Instal-lem Wireshark sudo apt install wireshark i Per obrir-lo, des del terminal sudo wireshark

---

## 4. Part 3

- Utilitzant Wireshark feu una captura de la negociació
entre client i servidor seguint aquest ordre:
 - Inicieu captura de transit amb Wireshark
 - Canvieu al client la xarxa de NAT a Xarxa Interna
 - Forceu un refresc de IP:

- Eina gràfica a Linux 

- Indiqueu quins dels paquets que has obtingut al Wireshark son broadcast i quins son unicast, tant IPcom MAC.

---

## 5. Coses X

*Detalls o apartats addicionals de l'activitat...*

---

## 7. Incidències

*Registra si has tingut algun error o problema durant la pràctica i com ho has resolt.*

---

## 8. Conclusions

### Quina part us ha resultat més fàcil?

*Escriu la teva resposta aquí...*

### Quina part us ha costat més?

*Escriu la teva resposta aquí...*

### Què heu necessitat recuperar del curs anterior?

*Escriu la teva resposta aquí...*

### Què considereu que hauríeu de repassar?

*Escriu la teva resposta aquí...*

### Podríeu repetir el procés amb més autonomia?

*Escriu la teva resposta aquí...*
