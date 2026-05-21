## Curs
CFGM Sistemes Microinformàtics i Xarxes  

## Matèria
0227 Serveis de Xarxa  

## Durada
2 h  

## Professor/s
C. Alonso, B. Redondo  

## Alumne/a
  

---

# UD1. Repàs TCP/IP

## Activitat 1

A partir de les següents parelles d'adreça IP i màscara de xarxa, identificar:
- Classe de xarxa  
- Si s’utilitza la màscara per defecte  
- Adreça de xarxa  
- Primera adreça IP possible  
- Adreça de broadcast  

### Taula

| Dades | Classe | Màscara per defecte? | Adreça de xarxa | Primera IP | Broadcast |
|------|--------|----------------------|-----------------|-----------|-----------|
| 192.168.14.3 / 255.255.0.0 | C | /16 | 192.168.0.0 | 192.168.0.1 | 192.168.255.255 |
| 10.23.31.7 / 255.255.255.0 | A | /24 | 10.23.31.0 | 10.23.31.1 | 10.23.31.255 |
| 8.45.127.12 / 255.0.0.0 | A | /8 | 8.0.0.0 | 8.0.0.1 | 8.255.255.255 |
| 8.45.127.12 / 255.255.240.0 | A | /20 | 8.45.112.0 | 8.45.112.1 | 8.45.127.255 |
| 223.145.90.131 / 255.255.255.192 | C | /26 | 223.145.90.128 | 223.145.90.129 | 223.145.90.191 |
| 140.30.23.31 / 255.224.0.0 | B | /11 | 140.0.0.0 | 140.0.0.1 | 140.31.255.255 |

---

## Activitat 2

Quina és l’adreça de xarxa i de broadcast de:

- IP: **10.254.96.104**  
- Màscara: **255.255.252.0**  

Opcions:

- a) 10.254.255.255 – 10.254.0.0  
- b) 10.255.255.255 – 10.0.0.0  
- c) 10.254.96.255 – 10.254.96.0  
- d) 10.254.99.255 – 10.254.96.0  

---

## Activitat 3

Indica si són possibles:

- IP: 170.100.4.10  
  - Màscara: 255.255.255.0  
  - Porta d’enllaç: 170.100.5.140  

- IP: 201.100.4.10  
  - Màscara: 255.255.255.0  
  - Porta d’enllaç: 201.100.4.255  

---

## Activitat 4

### Taula d’encaminament

| Destinació | Màscara | Següent salt |
|-----------|--------|-------------|
| 10.10.20.0 | 255.255.255.224 | 10.1.2.2 |
| 10.10.30.0 | 255.255.255.128 | 10.1.3.2 |
| 10.1.2.0 | 255.255.255.0 | 0.0.0.0 |
| 10.1.3.0 | 255.255.255.0 | 0.0.0.0 |
| 0.0.0.0 | 0.0.0.0 | 10.1.4.254 |

**Recordeu:**  
Una adreça de salt `0.0.0.0` indica que la xarxa està directament connectada al router.

### IPs a analitzar

- a) 10.10.20.36  
- b) 10.10.20.9  
- c) 10.1.2.3  
- d) 10.10.30.16  

---

## Activitat 5

Utilitza la comanda:

```

netstat -h

```

Tasques:

- Obrir www.upc.edu i comprovar connexions TCP  
- Identificar la connexió  
- Consultar ports UDP oberts  
- Consultar connexions TCP establertes  
- Comparar TCP vs UDP  
- Mostrar aplicacions de connexions TCP  

---

## Activitat 6

- Completar les adreces IP dels equips  
- Representar la xarxa amb Packet Tracer  
- Comprovar funcionament  

**Requisit:**  
Configurar encaminament dinàmic amb **RIP**

