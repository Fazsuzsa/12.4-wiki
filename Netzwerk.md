# Netzwerktechnologie

## Netwerkarten 

- `WAN`: Wide Area Network
   - Große geografische Reichweite, z. B. das Internet.
- `MAN`: Metropolitan Area Network
   - Netzwerke auf Stadtebene.
- `LAN`: Local Area Network
   - Netzwerke in Gebäuden, z. B. das Heimnetzwerk.
- `PAN`: Personal Area Network
   - Kleine, persönliche Netzwerke, z. B. Bluetooth-Verbindungen.

## Netzwerktopologie

- `Bus`:
    - Geräte sind linear verbunden, einfach, aber störanfällig.
- `Ring`:
    - Daten kreisen in einer Schleife, anfällig bei Ausfall eines Geräts.
- `Stern`:
    - Alle Geräte sind mit einem zentralen Knotenpunkt verbunden.
- `Mesh`:
    - Geräte sind miteinander vernetzt, sehr robust.


## Protokolle

- `ARP`: Address Resolution Protocol
- `ICMP`: Internet Control Message Protocol
- `IP`: Internet Protocol

## Adressen

- `IP address`: Internet Protocol address
    - stellt eine logische Adresse dar.
    - Es gibt LAN-interne Adresse (Private IP-Adressen) und öentliche IP-Adressen
    - Interne IP-Adressen werden idR von einem DHCP fähigen Gerät (Router) dynamisch vergeben
    - Öffentliche IP-Adressen/Adressräume müssen von einem ISP (Internet Service Provider) gekauft werden    
- `MAC address`: Media Access Control address
    - werden bei Fertigung auf die Platine einer NIC "eingebrannt"
    - 48 Bit Adressen, die i.d.R. als 6 Hexadezimalblöcke geschrieben werden: AA:11:BB:22:CC:33 oder 3C-E9-F7-C9-9E-0C
    - Keine MAC-Adresse darf innerhalb eines Netzwerks doppelt vorkommen (v.a. bei virtuellen NICs relevant)
    - Sie stellen eine physische Adresse dar
    - Innerhalb eines LAN zur Adressierung verwendet
- `NIC`: Network Interface Card
    - Jedes Netzwerkfähige Gerät hat ein oder mehrere Network Interface Card(s)
    - Jede NIC ermöglicht genau eine Netzwerkverbindung
    - Jede NIC hat genau eine unveränderliche MAC-Adresse
    - Bei virtuellen Maschinen (bspw einem Cloud Rechner) werden virtuelle NICs
eingebaut

## Subnetzmasken 

- `CIDR`: Classless Inter-Domain Routing