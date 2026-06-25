# 10 · Protokoll- & Port-Referenz

Nachschlagewerk für die wichtigsten Protokolle und Ports des Lernfelds.

## Protokolle nach OSI-Schicht

| Schicht | Protokolle (Auswahl) |
|:------:|----------------------|
| 7 · Anwendung | HTTP, HTTPS, DNS, DHCP, FTP, SMTP, POP3, IMAP, SSH, Telnet |
| 4 · Transport | **TCP**, **UDP** |
| 3 · Vermittlung | **IP**, ICMP, ARP\*, OSPF, RIP, EIGRP, BGP, IGMP, IPsec |
| 2 · Sicherung | Ethernet, 802.1Q (VLAN), STP, WLAN (802.11), PPP |
| 1 · Bitübertragung | 10/100/1000BASE-T, LWL-Standards, DSL |

> \* ARP wird je nach Quelle Schicht 2 oder 3 zugeordnet.

## Wichtige Ports (Well-Known)

| Port | Protokoll | L4 | Zweck |
|:----:|-----------|:--:|-------|
| 20 / 21 | FTP | TCP | Dateiübertragung (Daten / Steuerung) |
| 22 | SSH | TCP | sicherer Fernzugriff |
| 23 | Telnet | TCP | Fernzugriff (unverschlüsselt, veraltet) |
| 25 | SMTP | TCP | E-Mail senden |
| 53 | DNS | UDP/TCP | Namensauflösung |
| 67 / 68 | DHCP | UDP | automatische IP-Vergabe |
| 80 | HTTP | TCP | Web (unverschlüsselt) |
| 110 | POP3 | TCP | E-Mail abholen |
| 143 | IMAP | TCP | E-Mail (serverseitig) |
| 443 | HTTPS | TCP | Web über TLS |
| 587 | SMTP (Submission) | TCP | E-Mail senden (Client→Server) |
| 993 | IMAPS | TCP | IMAP über TLS |
| 995 | POP3S | TCP | POP3 über TLS |
| 3389 | RDP | TCP | Remote Desktop |

### Port-Bereiche

| Bereich | Name |
|---------|------|
| 0 – 1023 | Well-Known Ports |
| 1024 – 49151 | Registered Ports |
| 49152 – 65535 | Dynamic / Private Ports (Quellports) |

## Protokollnummern im IP-Header

Das Feld **Protokoll** im [IPv4-Header](04-Schicht-3-Vermittlung.md#der-ipv4-header) gibt an, welche Schicht-4-Nutzlast folgt:

| Nummer | Protokoll |
|:------:|-----------|
| 1 | ICMP |
| 6 | TCP |
| 17 | UDP |

---
[◀ Troubleshooting](13-Troubleshooting.md) · [Übersicht](README.md) · **Weiter:** [CLI-/PowerShell-Spickzettel ▶](14-CLI-PowerShell-Spickzettel.md)
