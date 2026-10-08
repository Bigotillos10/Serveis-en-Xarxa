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

5. [Part 4](#5-Part-4)

7. [Incidències](#7-incidències)

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

![Captura del nano](img/Captura%20de%20pantalla%202026-10-08%20171611.png)

![Captura de que tot funciona](img/Captura%20de%20pantalla%202026-10-08%20170102.png)

- Un cop configurat, reinicia el servei.

---

## 3. Part 2

- L'equip Zorin inicialment el posem en NAT.

![zorin en nat](img/zorin%20nat.png)

- Instal-lem Wireshark sudo apt install wireshark i Per obrir-lo, des del terminal sudo wireshark

![Wireshark instalant](img/Wireshark%20instalant.png)

![Wireshark instalat](img/Wireshark%20instalat.png)

---

## 4. Part 3

- Utilitzant Wireshark feu una captura de la negociació
entre client i servidor seguint aquest ordre:
- Inicieu captura de transit amb Wireshark

![Wireshark transit](img/Wireshark%20transit.png)

- Canvieu al client la xarxa de NAT a Xarxa Interna

![Wireshark xarxa interna](img/Wireshark%20xarxa%20interna.png)

- Forceu un refresc de IP

- Eina gràfica a Linux

![refresc ip](img/refresc%20ip.png)

- Indiqueu quins dels paquets que has obtingut al Wireshark son broadcast i quins son unicast, tant IPcom MAC.

![Paquets obtinguts wireshark quins broadcast i quins son unicast](img/Paquets%20obtinguts%20wireshark%20quins%20broadcast%20i%20quins%20son%20unicast.png)

-Els paquets broadcast es el 127.0.0.1/8 i els unicast son les altres ips

---

## 5. Part 4

- Comproveu que el client es configura correctament (feu una captura de prova).

![comprova que el client es configura correctament]()

- Observa les assignacions /var/lib/kea/dhcp4.leases

![Observa les assignacions /var/lib/kea/dhcp4.leases](img/Observa%20les%20assignacions%20varlibkeadhcp4.leases.png)

- Definiu una reserva amb l'adreça MAC del client i IP 192.169.x.55 i comproveu el seu funcionament (caldrà que demaneu renovar l'adreça del client).

![Definiu una reserva amb l'adreça MAC del client i IP 192.169.x.55 i comproveu el seu funcionament]()

---

## 7. Incidències

- En la part 3 hem perdut la xarxa i no ens deixaba conectar a la xarxa, pero al final hem pogut reiniciar i amb varies convinacions tornar a conectarla.
