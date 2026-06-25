# Glossar

Kurzdefinitionen der wichtigsten Begriffe des Lernfelds. Querverweise führen zur ausführlichen Seite.

## A–F
- **APIPA** – Selbstvergebene Adresse `169.254.x.x`, wenn DHCP fehlschlägt; nicht geroutet. → [Schicht 3](04-Schicht-3-Vermittlung.md)
- **ARP** – Findet zu einer IP-Adresse die MAC-Adresse im LAN. → [Schicht 2](03-Schicht-2-Sicherung.md)
- **Bandbreite** – Übertragungskapazität eines Mediums (z. B. Mbit/s).
- **Broadcast** – Nachricht an *alle* im Segment (MAC `FF:FF:FF:FF:FF:FF`).
- **Broadcastdomäne** – Bereich, den ein Broadcast erreicht; wird von Routern (und VLANs) getrennt.
- **CIDR** – Schreibweise `/n` für die Anzahl der Netzbits (z. B. `/24`). → [Subnetting](05-IP-Adressierung-und-Subnetting.md)
- **CSMA/CD** – Altes Zugriffsverfahren bei Halbduplex/Hub; bei Switch (Vollduplex) hinfällig.
- **Default Gateway** – Router, über den ein Host alles erreicht, was außerhalb seines Netzes liegt.
- **DHCP** – Vergibt automatisch IP, Maske, Gateway, DNS (Ablauf DORA). → [Anwendung](07-Schicht-5-7-Anwendung.md)
- **DMZ** – Abgeschottete Zone für öffentlich erreichbare Server. → [Sicherheit](09-Sicherheit-Firewall-DMZ-WLAN.md)
- **DNS** – Übersetzt Namen ↔ IP-Adressen. → [Anwendung](07-Schicht-5-7-Anwendung.md)
- **Duplex** – Simplex / Halbduplex / Vollduplex (Senden & Empfangen gleichzeitig).
- **FCS** – Prüfsumme am Frame-Ende zur Fehlererkennung (CRC).
- **Frame** – PDU der Schicht 2.
- **ACL** – Access Control List: Regelliste zur Paketfilterung (Permit/Deny). → [Sicherheit](09-Sicherheit-Firewall-DMZ-WLAN.md)
- **AS / ASN** – Autonomes System / dessen eindeutige Nummer. → [Schicht 3](04-Schicht-3-Vermittlung.md)
- **CoS** – Class of Service: QoS-Priorisierung auf Schicht 2 (3-Bit-Feld 0–7). → [QoS](11-QoS-Priorisierung.md)
- **Cut-Through / Store-and-Forward** – Switching-Modi (sofort weiterleiten vs. ganzen Frame prüfen).
- **DiffServ / DSCP** – QoS auf Schicht 3 (6-Bit-DSCP im IP-Header). → [QoS](11-QoS-Priorisierung.md)
- **DNAT** – Destination NAT / Portweiterleitung (Server von außen erreichbar machen).
- **DOCSIS** – Internetzugang über das TV-Kabelnetz. → [WAN](12-WAN-Internetzugang.md)
- **EIGRP** – hybrides Routing-IGP (ursprünglich Cisco). → [Schicht 3](04-Schicht-3-Vermittlung.md)
- **FQDN** – vollständig qualifizierter Domainname (z. B. `www.gfn.de.`).
- **FTTx** – Glasfaser bis Curb/Building/Home/Desk. → [WAN](12-WAN-Internetzugang.md)

## G–N
- **Hub** – Schicht-1-Gerät, verteilt Signale an alle Ports (eine Kollisionsdomäne).
- **ICMP** – Diagnose-/Fehlerprotokoll (Basis von ping, tracert). → [Schicht 3](04-Schicht-3-Vermittlung.md)
- **IP-Adresse** – Logische 32-Bit-Adresse (IPv4) bzw. 128-Bit (IPv6). → [Subnetting](05-IP-Adressierung-und-Subnetting.md)
- **Kollisionsdomäne** – Bereich, in dem sich Signale stoßen können; pro Switch-Port eine eigene.
- **MAC-Adresse** – Physikalische 48-Bit-Adresse der Netzwerkkarte (Hersteller-OUI + Gerät).
- **Magic Number** – Blockgröße beim Subnetting = 256 − Maskenoktett.
- **NAT / PAT** – Übersetzt private ↔ öffentliche IP; PAT unterscheidet über Ports. → [Schicht 3](04-Schicht-3-Vermittlung.md)
- **IGP / EGP** – Routing innerhalb (OSPF/RIP) bzw. zwischen (BGP) Autonomen Systemen.
- **Jitter** – Schwankung der Verzögerung (kritisch für Echtzeit).
- **Konvergenzzeit** – Dauer bis zum stabilen Routing nach einer Änderung.
- **Lease-Time** – Reservierungsdauer einer per DHCP vergebenen IP.
- **MIMO** – mehrere parallele Datenströme im WLAN.
- **MTU** – Maximum Transmission Unit: max. IP-Paketgröße (üblich 1500 Byte). → [Schicht 2](03-Schicht-2-Sicherung.md)

## O–S
- **OSI-Modell** – Referenzmodell mit 7 Schichten. → [OSI-Modell](01-OSI-Modell.md)
- **OUI** – Herstellerkennung (erste 3 Byte der MAC-Adresse).
- **Paket** – PDU der Schicht 3.
- **PDU** – *Protocol Data Unit*: Daten → Segment → Paket → Frame → Bit.
- **Port** – 16-Bit-Nummer zur Adressierung von Diensten/Verbindungen (Schicht 4).
- **Repeater** – Frischt Signale auf (Schicht 1).
- **RIP / OSPF** – Dynamische Routingprotokolle (Distance-Vector / Link-State). → [Schicht 3](04-Schicht-3-Vermittlung.md)
- **Router** – Verbindet Netze, routet per IP, trennt Broadcastdomänen.
- **Segment** – PDU der Schicht 4 (bei TCP).
- **SLAAC** – Zustandslose IPv6-Autokonfiguration über Router Advertisements.
- **Socket** – Kombination aus IP-Adresse und Port.
- **SSID** – Name eines WLAN.
- **STP** – Spanning Tree Protocol, verhindert Schleifen zwischen Switches. → [Schicht 2](03-Schicht-2-Sicherung.md)
- **Subnetzmaske** – Trennt Netz- von Hostanteil einer IP-Adresse.
- **Switch** – Schicht-2-Gerät, vermittelt per MAC-Tabelle.
- **QoS** – Quality of Service: Oberbegriff für Verkehrssteuerung/Priorisierung. → [QoS](11-QoS-Priorisierung.md)
- **RADIUS** – Authentifizierungsserver (WPA2/3-Enterprise).
- **RARP** – Reverse ARP: MAC → IP (Umkehrung von ARP).
- **SAE** – Simultaneous Authentication of Equals (WPA3).
- **SPB** – Shortest Path Bridging: nutzt alle gleich teuren Pfade (statt zu blocken wie STP).
- **Subnet-Router-Anycast** – reservierte erste Adresse eines IPv6-Netzes.

## T–Z
- **TCP** – Verbindungsorientiertes, zuverlässiges Transportprotokoll. → [Schicht 4](06-Schicht-4-Transport.md)
- **Trunk** – Switch-Port, der mehrere VLANs (getaggt) überträgt. → [Schicht 2](03-Schicht-2-Sicherung.md)
- **TTL** – „Time to Live“: max. Anzahl Router-Hops; sinkt pro Hop um 1.
- **UDP** – Verbindungsloses, schnelles Transportprotokoll. → [Schicht 4](06-Schicht-4-Transport.md)
- **Traffic Shaping** – Glätten/Steuern von Datenraten über Warteschlangen (Teil von QoS).
- **VLAN** – Logisches Teilnetz (IEEE 802.1Q); eine eigene Broadcastdomäne. → [Schicht 2](03-Schicht-2-Sicherung.md)
- **WEP / WPA / WPA2 / WPA3** – WLAN-Verschlüsselung von unsicher (WEP) bis aktuell (WPA3/SAE). → [Sicherheit](09-Sicherheit-Firewall-DMZ-WLAN.md)
- **Zeroconf** – herstellerneutrale Entsprechung zu APIPA (Selbstkonfiguration bei DHCP-Ausfall).

---

## Zahlensysteme

Netzwerktechnik rechnet selten dezimal: **Subnetting** funktioniert **binär**, **MAC- und IPv6-Adressen** werden **hexadezimal** geschrieben. Drei Systeme muss man sicher umrechnen können.

| System | Basis | Ziffern | Einsatz |
|--------|:-----:|---------|---------|
| Dezimal | 10 | 0–9 | Alltag, IPv4-Schreibweise |
| Dual / Binär | 2 | 0, 1 | Subnetzmaske, Netz-/Hostbits |
| Hexadezimal | 16 | 0–9, A–F | MAC-Adresse, IPv6, IPv4-Header |

### Dual → Dezimal (Stellenwerte)
Jede Stelle hat einen Wert (Zweierpotenz). Bits mit „1“ addieren:

| Stellenwert | 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 |
|-------------|:---:|:--:|:--:|:--:|:-:|:-:|:-:|:-:|
| Beispiel `11000000` | 1 | 1 | 0 | 0 | 0 | 0 | 0 | 0 |

→ 128 + 64 = **192**. (So wird aus einer `/26`-Maske `255.255.255.192`.)

### Hexadezimal → Dezimal
Stellenwerte sind Potenzen von 16, A = 10 … F = 15.
`1FC` = 1·256 + 15·16 + 12·1 = 256 + 240 + 12 = **508**.

### Dual ↔ Hexadezimal (Nibble)
**4 Bit = 1 Hexstelle.** Das macht die Umrechnung einfach:

| Dual | Hex | Dual | Hex |
|------|:---:|------|:---:|
| 0000 | 0 | 1000 | 8 |
| 0001 | 1 | 1001 | 9 |
| 0010 | 2 | 1010 | A |
| 0011 | 3 | 1011 | B |
| 0100 | 4 | 1100 | C |
| 0101 | 5 | 1101 | D |
| 0110 | 6 | 1110 | E |
| 0111 | 7 | 1111 | F |

Beispiel: `1010 1100` → `A C` → **AC** (hex) = 172 (dez).

---
[◀ CLI-/PowerShell-Spickzettel](14-CLI-PowerShell-Spickzettel.md) · [Übersicht](README.md)
