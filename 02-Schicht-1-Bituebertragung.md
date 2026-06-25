# 2 · Schicht 1 – Bitübertragung (Physical)

Die unterste Schicht überträgt die **rohen Bits** als physikalische Signale (Spannung, Licht, Funk) über ein Medium. Sie kümmert sich um Kabel, Stecker, Pegel und Taktung – **nicht** um Adressen oder Bedeutung der Daten.

## Übertragungsmedien

### Twisted Pair (Kupfer)
Verdrillte Adernpaare (das Verdrillen reduziert Störungen/Übersprechen). Standard im LAN, Stecker **RJ45 (8P8C)**.

| Kategorie | Bandbreite | typ. Geschwindigkeit | Bemerkung |
|-----------|-----------|----------------------|-----------|
| Cat 5e | 100 MHz | 1 Gbit/s | Minimum für Gigabit |
| Cat 6 | 250 MHz | 1 Gbit/s (10 Gbit/s bis ~55 m) | weit verbreitet |
| Cat 6A | 500 MHz | 10 Gbit/s über 100 m | aktueller Standard |
| Cat 7 / 7A | 600 / 1000 MHz | 10 Gbit/s | geschirmt, GG45/TERA |
| Cat 8 | 2000 MHz | 25/40 Gbit/s (≤ 30 m) | Rechenzentrum |

**Schirmung** (Kürzel *Gesamtschirm/Aderpaarschirm*): `U/UTP` (ungeschirmt), `F/UTP` (Folie gesamt), `S/FTP` (Geflecht gesamt + Folie je Paar, beste Schirmung).

> **Maximale Länge** einer Twisted-Pair-Strecke: **100 m** (Channel) – davon 90 m feste Verlegung + 10 m Patchkabel.

### Lichtwellenleiter (LWL / Glasfaser)
Überträgt **Licht** statt Strom → unempfindlich gegen elektromagnetische Störungen (EMV), große Reichweite, hohe Bandbreite. Stecker z. B. **LC, SC**.

| Typ | Kern | Lichtquelle | Reichweite |
|-----|------|-------------|-----------|
| **Multimode** (OM3/OM4/OM5) | dick (50 µm) | LED / VCSEL | kurz (bis einige 100 m) |
| **Singlemode** (OS2) | dünn (9 µm) | Laser | sehr lang (km) |

### Koaxialkabel
Älteres Medium (BNC), heute im LAN kaum noch relevant (noch bei Kabel-Internet/Antenne).

## Ethernet-Bezeichnungen entschlüsseln

`1000BASE-T` → **1000** = 1000 Mbit/s · **BASE** = Basisband · **T** = Twisted Pair.

| Bezeichnung | Geschwindigkeit | Medium |
|-------------|-----------------|--------|
| 10BASE-T | 10 Mbit/s | TP |
| 100BASE-TX | 100 Mbit/s | TP |
| 1000BASE-T | 1 Gbit/s | TP |
| 1000BASE-SX/LX | 1 Gbit/s | LWL (S = kurz, L = lang) |
| 10GBASE-T | 10 Gbit/s | TP (Cat 6A) |

## Strukturierte Verkabelung (EN 50173 / ISO 11801)

Ein herstellerunabhängiges, hierarchisches Konzept für die Gebäudeverkabelung in **drei Ebenen**:

| Ebene | Verbindet | Medium (typisch) | Richtwert Länge |
|-------|-----------|------------------|-----------------|
| **Primär** (Gelände) | Standortverteiler ↔ Gebäudeverteiler | LWL | bis ~1500–2000 m |
| **Sekundär** (Steigleitung) | Gebäudeverteiler ↔ Etagenverteiler | LWL / Kupfer | bis ~500 m |
| **Tertiär** (Etage) | Etagenverteiler ↔ Anschlussdose | Twisted Pair | max. 90 m + 10 m |

Wichtige Komponenten: **Patchpanel** (Rangierfeld), **Patchkabel**, **Anschlussdose (TA)**, Verteilerschrank (Rack).

## Geräte auf Schicht 1
**Hub**, **Repeater**, **Medienkonverter** und das **Modem** arbeiten rein physikalisch – sie treffen keine Adressentscheidungen. Details und Abgrenzung: [Netzwerkgeräte](08-Netzwerkgeraete.md).

> ⚠️ **Achtung Hub:** Ein Hub bildet **eine einzige Kollisionsdomäne** – alle Geräte teilen sich die Bandbreite und stören sich gegenseitig. Deshalb ist er durch den Switch (Schicht 2) abgelöst worden.

## Begriffe
- **Kollisionsdomäne** – Bereich, in dem sich gleichzeitig gesendete Signale „stoßen“ können.
- **Duplexverfahren** – *Simplex* (nur eine Richtung), *Halbduplex* (abwechselnd), *Vollduplex* (gleichzeitig senden & empfangen).
- **Auto-MDI-X** – moderne Ports erkennen selbst, ob ein Crossover nötig ist → Crossover-Kabel sind kaum noch erforderlich.

---
[◀ OSI-Modell](01-OSI-Modell.md) · [Übersicht](README.md) · **Weiter:** [Schicht 2 – Sicherung ▶](03-Schicht-2-Sicherung.md)
