# AA2 – Avaluació Anàlisi Kea DHCP

**Mòdul:** M0227 – Serveis de Xarxa  
**Alumne:** Nom i cognoms  
**Curs:** SMX2  
**Empresa de l'escenari:** TechMataró SL  
**Data:**  

---

# Índex

1. Introducció
2. Bloc 1 – Fonaments del protocol i anàlisi de tràfic
3. Bloc 2 – Configuració del servidor Kea DHCP
4. Bloc 3 – Assignació estàtica i reserves MAC
5. Bloc 4 – Comprovació, diagnòstic i resolució d'incidències
6. Bloc 5 – Mapa conceptual del servei DHCP
7. Conclusió

---

# 1. Introducció

## 1.1 Objectiu de l'activitat

En aquesta activitat es treballarà el desplegament, la configuració i l'anàlisi del servei Kea DHCP4 en un entorn Linux.

## 1.2 Escenari de treball

L'empresa TechMataró SL necessita configurar un servidor DHCP centralitzat per gestionar les adreces IP dels dispositius de la seva xarxa local.

---

# 2. Bloc 1 – Fonaments del protocol i anàlisi de tràfic

## 2.1 Procés de negociació DHCP (DORA)

### Pas 1 – Discover
- Funció del missatge:
- Tipus de comunicació:
- Explicació:

### Pas 2 – Offer
- Funció del missatge:
- Tipus de comunicació:
- Explicació:

### Pas 3 – Request
- Funció del missatge:
- Tipus de comunicació:
- Explicació:

### Pas 4 – Acknowledge
- Funció del missatge:
- Tipus de comunicació:
- Explicació:

## 2.2 Captura i capçaleres dels paquets

### Pas 1 – Ports UDP
- Port UDP del client:
- Port UDP del servidor:
- Explicació:

### Pas 2 – Identificació del client
- Camp DHCP que identifica la targeta de xarxa:
- Explicació:

### Pas 3 – Opcions DHCP

| Opció DHCP | Número o nom | Funció |
|---|---|---|
| Router | | |
| DNS | | |
| Domain Name | | |

### Evidència pràctica

**Captura de Wireshark o tcpdump:**

![Captura de pantalla](captura_bloc1.png)

---

# 3. Bloc 2 – Configuració del servidor Kea DHCP

## 3.1 Configuració de la interfície de xarxa

### Pas 1
Identificar la interfície de xarxa que utilitzarà el servidor.

- Interfície:
- Comanda utilitzada:
- Resultat:

### Pas 2
Configurar la interfície `eth0` al fitxer de configuració.

## 3.2 Configuració de la base de dades

### Pas 1
Configurar el sistema d'emmagatzematge de les cessions DHCP.

- Model de base de dades:
- Persistència:

## 3.3 Configuració dels paràmetres globals

| Paràmetre | Valor requerit | Configurat |
|---|---|---|
| valid-lifetime | 7200 segons | |
| renew-timer | 3600 segons | |

## 3.4 Configuració de la subxarxa

### Pas 1 – Definir la subxarxa
- Xarxa:
- Màscara:

### Pas 2 – Definir el pool dinàmic
- IP inicial:
- IP final:

## 3.5 Configuració de les opcions de xarxa

| Opció | Valor |
|---|---|
| Router | |
| DNS primari | |
| DNS secundari | |
| Domini local | |

## 3.6 Fitxer de configuració

**Nom del fitxer:** `kea-dhcp4.conf`

### Configuració JSON

```json
// Escriu aquí la configuració del servidor Kea DHCP4
```

### Evidència pràctica

**Captura del fitxer de configuració:**

![Captura de pantalla](captura_bloc2.png)

---

# 4. Bloc 3 – Assignació estàtica i reserves per MAC

## 4.1 Configuració de la reserva DHCP

### Pas 1 – Identificar el dispositiu

- Dispositiu:
- Adreça MAC:
- Adreça IP reservada:
- Nom de l'equip:

### Pas 2 – Afegir la reserva

Escriure la configuració de la reserva dins de la secció corresponent de `kea-dhcp4.conf`.

```json
// Escriu aquí la configuració de la reserva
```

## 4.2 Validació de la sintaxi

### Pas 1
Indicar les eines o comandes que permeten comprovar la sintaxi del fitxer JSON.

- Eina o comanda:
- Funció:
- Resultat:

### Evidència pràctica

**Captura de la validació de la configuració:**

![Captura de pantalla](captura_bloc3.png)

---

# 5. Bloc 4 – Comprovació, diagnòstic i resolució d'incidències

## 5.1 Comprovacions al servidor

### Pas 1 – Consultar l'estat del servei
- Comanda:
- Resultat:
- Explicació:

### Pas 2 – Reiniciar el servei
- Comanda:
- Resultat:

### Pas 3 – Aturar el servei
- Comanda:
- Resultat:

## 5.2 Consulta dels registres

### Pas 1
Indicar les comandes necessàries per consultar els registres de Kea DHCP.

- Comanda:
- Ruta dels registres:
- Informació que es pot consultar:

## 5.3 Fitxer de cessions actives

- Ruta del fitxer:
- Nom del fitxer:
- Informació que emmagatzema:

## 5.4 Proves des d'un client Linux

### Pas 1 – Alliberar l'adreça IP actual
- Comanda:
- Resultat:

### Pas 2 – Sol·licitar una nova adreça IP
- Comanda:
- Resultat:

### Pas 3 – Comprovar la configuració IP
- Comanda:
- Resultat:

## 5.5 Proves des d'un client Windows

### Pas 1 – Alliberar l'adreça IP
- Comanda:
- Resultat:

### Pas 2 – Sol·licitar una nova adreça IP
- Comanda:
- Resultat:

### Pas 3 – Comprovar la configuració
- Comanda:
- Resultat:

## 5.6 Evidències pràctiques

### Captura del servidor Linux

![Captura de pantalla](captura_bloc4_linux.png)

### Captura del client Linux

![Captura de pantalla](captura_bloc4_client_linux.png)

### Captura del client Windows

![Captura de pantalla](captura_bloc4_windows.png)

---

# 6. Bloc 5 – Mapa conceptual del servei DHCP

## 6.1 Mapa conceptual

En aquest apartat s'inclourà un mapa conceptual que connecti els components principals del servei DHCP i Kea.

### Conceptes obligatoris

- Ports UDP 67 i 68
- Broadcast i Unicast
- Discover, Offer, Request i Acknowledge
- `kea-dhcp4.conf`
- `interfaces-config`
- `lease-database`
- `valid-lifetime`
- `renew-timer`
- `subnet4`
- `pools`
- `option-data`
- `reservations`
- `hw-address`
- `hostname`
- `kea-leases4.csv`
- `kea-dhcp4-server`
- `journalctl`
- `tcpdump`
- Wireshark
- `ipconfig`
- `dhclient`

### Imatge del mapa conceptual

![Mapa conceptual DHCP](mapa_conceptual.png)

---

# 7. Conclusió

En aquesta activitat he treballat el servei Kea DHCP4, la seva configuració i les diferents eines que permeten comprovar el seu funcionament.

**Valoració personal:**

- Què he après?
- Quina part m'ha resultat més difícil?
- Per a què em pot servir aquest servei en un entorn professional?

---

# 8. Evidències i lliurament

- [ ] Configuració del servidor Kea DHCP4.
- [ ] Captures reals de la terminal amb el meu nom d'usuari visible.
- [ ] Captura de la validació del JSON.
- [ ] Captures de les proves amb clients.
- [ ] Mapa conceptual complet.
- [ ] Document exportat a PDF.

**Nom final del document:** `M0227_RA1_Nom_Cognom.pdf`
