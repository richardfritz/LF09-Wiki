# 14 · CLI-/PowerShell-Spickzettel

Kurzreferenz der wichtigsten Befehle für **Netzwerkdiagnose und -verwaltung unter Windows** (klassische Eingabeaufforderung ↔ PowerShell). Zur systematischen Vorgehensweise siehe [13 · Troubleshooting](13-Troubleshooting.md).

## Ping-Kaskade (von innen nach außen)

| # | Befehl | prüft |
|:-:|--------|-------|
| 1 | `ping 127.0.0.1` | TCP/IP-Stack des OS |
| 2 | `ping <eigene IP>` | Netzwerkkarte |
| 3 | `ping <Gateway>` | lokales Netz (LAN) |
| 4 | `ping 8.8.8.8` | Internet (per IP) |
| 5 | `ping www.google.de` | Namensauflösung (DNS) |

> Der erste Schritt, der fehlschlägt, grenzt die Ursache ein.

## Befehlsreferenz: CMD ↔ PowerShell

| Aufgabe | CMD (klassisch) | PowerShell |
|---------|-----------------|------------|
| IP-Konfiguration anzeigen | `ipconfig` | `Get-NetIPConfiguration` |
| Details (MAC, DHCP, DNS) | `ipconfig /all` | `Get-NetAdapter` |
| DHCP-Lease neu beziehen | `ipconfig /release` + `/renew` | `Restart-NetAdapter` |
| DNS-Cache leeren | `ipconfig /flushdns` | `Clear-DnsClientCache` |
| Erreichbarkeit + Laufzeit | `ping <Ziel>` | `Test-Connection <Ziel>` |
| Weg (Hops) zum Ziel | `tracert <Ziel>` | `Test-NetConnection <Ziel> -TraceRoute` |
| DNS-Auflösung testen | `nslookup <Name>` | `Resolve-DnsName <Name>` |
| Port-Erreichbarkeit prüfen | `telnet <Host> <Port>` | `Test-NetConnection <Host> -Port <p>` |
| Aktive Verbindungen & Ports | `netstat -ano` / `-b` | `Get-NetTCPConnection` |
| Routingtabelle | `route print` | `Get-NetRoute` |
| ARP-/Nachbartabelle | `arp -a` | `Get-NetNeighbor` |
| Dienst starten/stoppen | `net start`/`net stop <Dienst>` | `Start-Service`/`Stop-Service` |
| Netzlaufwerk verbinden | `net use X: \\Srv\Share` | `New-SmbMapping` |

## Nützliche Optionen

**`ipconfig`** · `/all` (Details inkl. MAC) · `/release` + `/renew` (DHCP neu) · `/flushdns` (Cache leeren) · `/displaydns` (Cache anzeigen)

**`netstat`** · `-a` (alle Verbindungen/Ports) · `-b` (mit Programm – **als Administrator!**) · `-n` (nur IP-Adressen, schneller)

**MTU einer Strecke ermitteln** · `ping -f -l 1472 8.8.8.8` (`-f` = DF-Bit, `-l` = Payload; 1472 = 1500 − 20 − 8)

## Sofort-Checks

- **LEDs & Kabel zuerst** – keine LED, kein Netz.
- Betrifft es **einen** PC = lokal, **alle** = zentral.
- Immer nur **EINE** Sache ändern, dann testen.
- Firewalls blocken oft **ICMP** → `ping`/`tracert` können täuschen.
- Windows: `ncpa.cpl` öffnet schnell die Netzwerkverbindungen.

## Zwei Merksätze

- **169.254.x.x (APIPA):** DHCP nicht erreicht → Kabel/Switch/DHCP-Server prüfen.
- **IP-Konflikt:** doppelte feste IP → ändern oder DHCP nutzen, dann Adapter neu starten.

---
[◀ Protokoll- & Port-Referenz](10-Protokoll-und-Port-Referenz.md) · [Übersicht](README.md) · **Weiter:** [Glossar ▶](Glossar.md)

*Inhalt entspricht dem CLI-/PowerShell-Spickzettel des Lernfelds (Tag 10).*
