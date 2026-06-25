# LF09 – Netzwerke und Dienste bereitstellen
### Wiki & Zusammenfassung des Lernfelds

> Diese Zusammenfassung bündelt die Themen des Lernfelds 9 – **Netzwerkgeräte, Netzwerkprotokolle und Netzwerkfunktionen** – und sortiert sie nach den **Schichten des OSI-Modells** (von unten nach oben).
>
> *Hinweise:* Linux-Themen sind bewusst ausgeklammert. Inhalte wurden gegenüber den Kursunterlagen fachlich geprüft und korrigiert.

![Das OSI-Schichtenmodell](assets/osi-modell.svg)

---

## 📚 Inhaltsverzeichnis

**Grundlagen**
- [1 · Das OSI-Modell](01-OSI-Modell.md) – Schichten, Kapselung, TCP/IP-Modell

**Nach OSI-Schichten sortiert**
- [2 · Schicht 1 – Bitübertragung](02-Schicht-1-Bituebertragung.md) – Kabel, Medien, strukturierte Verkabelung
- [3 · Schicht 2 – Sicherung](03-Schicht-2-Sicherung.md) – MAC, Switch, MTU, STP, VLAN, ARP
- [4 · Schicht 3 – Vermittlung](04-Schicht-3-Vermittlung.md) – IP, Routing (IGP/EGP), ICMP, NAT
- [5 · IP-Adressierung & Subnetting](05-IP-Adressierung-und-Subnetting.md) – IPv4, Subnetting, IPv6
- [6 · Schicht 4 – Transport](06-Schicht-4-Transport.md) – TCP, UDP, Ports
- [7 · Schicht 5–7 – Anwendung](07-Schicht-5-7-Anwendung.md) – DHCP, DNS, HTTP, FTP, Mail

**Querschnittsthemen**
- [8 · Netzwerkgeräte im Überblick](08-Netzwerkgeraete.md) – Hub bis Firewall
- [9 · Sicherheit: Firewall, DMZ & WLAN](09-Sicherheit-Firewall-DMZ-WLAN.md) – ACL, DMZ, WLAN
- [11 · Priorisierung & QoS](11-QoS-Priorisierung.md) – CoS, DiffServ/DSCP
- [12 · WAN & Internetzugang](12-WAN-Internetzugang.md) – DSL, FTTx, Mobilfunk
- [13 · Troubleshooting](13-Troubleshooting.md) – Ping-Leiter, CLI-Werkzeuge, Fehlerbilder

**Referenz**
- [10 · Protokoll- & Port-Referenz](10-Protokoll-und-Port-Referenz.md)
- [14 · CLI-/PowerShell-Spickzettel](14-CLI-PowerShell-Spickzettel.md)
- [Glossar](Glossar.md)

> 🔧 Praxis: Seite [13 · Troubleshooting](13-Troubleshooting.md) und der [14 · CLI-/PowerShell-Spickzettel](14-CLI-PowerShell-Spickzettel.md).

---

## Wie ist dieses Wiki aufgebaut?

Das Wiki folgt dem **Bottom-Up-Prinzip** des OSI-Modells: Es beginnt beim Kabel (Schicht 1) und arbeitet sich Schicht für Schicht bis zur Anwendung (Schicht 7) hoch. Jede Seite beantwortet drei Fragen:

| Frage | Beispiel auf Schicht 3 |
|-------|------------------------|
| Welche **Geräte** arbeiten hier? | Router, Layer-3-Switch |
| Welche **Protokolle** gelten hier? | IP, ICMP, OSPF |
| Welche **Funktionen** werden umgesetzt? | Logische Adressierung, Routing, NAT |

## Schnellzugriff nach Thema

| Thema | Schicht | Seite |
|-------|:------:|-------|
| Twisted Pair, LWL, Patchpanel | 1 | [Bitübertragung](02-Schicht-1-Bituebertragung.md) |
| MAC-Adressen, Switching | 2 | [Sicherung](03-Schicht-2-Sicherung.md) |
| STP (Loop-Schutz) | 2 | [Sicherung](03-Schicht-2-Sicherung.md) |
| VLAN, Trunk, Inter-VLAN-Routing | 2–3 | [Sicherung](03-Schicht-2-Sicherung.md) |
| IP-Adresse, Subnetting | 3 | [Subnetting](05-IP-Adressierung-und-Subnetting.md) |
| Routing (RIP, OSPF) | 3 | [Vermittlung](04-Schicht-3-Vermittlung.md) |
| NAT / PAT | 3 | [Vermittlung](04-Schicht-3-Vermittlung.md) |
| MTU & Fragmentierung | 2–3 | [Sicherung](03-Schicht-2-Sicherung.md) |
| TCP vs. UDP, Ports | 4 | [Transport](06-Schicht-4-Transport.md) |
| DHCP, DNS, HTTP, FTP | 7 | [Anwendung](07-Schicht-5-7-Anwendung.md) |
| QoS, CoS, DSCP | 2–3 | [Priorisierung & QoS](11-QoS-Priorisierung.md) |
| DSL, FTTx, Mobilfunk, NAT | – | [WAN](12-WAN-Internetzugang.md) |
| Firewall, ACL, DMZ | 3–7 | [Sicherheit](09-Sicherheit-Firewall-DMZ-WLAN.md) |
| Fehlersuche, Ping-Leiter | alle | [Troubleshooting](13-Troubleshooting.md) |
| CLI-Befehle (CMD/PowerShell) | – | [Spickzettel](14-CLI-PowerShell-Spickzettel.md) |

---
*LF09 Wiki · auf Basis der Kurs-Handouts (Tag 01–10) · nach OSI-Schichten sortiert · ohne Linux · mit Infografiken*
