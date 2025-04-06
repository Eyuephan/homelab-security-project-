# Voranalyse: Homelab Security & Webplattform

## 1. Ziel des Projekts
Ziel dieses Projekts ist der Aufbau eines leistungsfähigen, modularen und sicheren Heimnetzwerks, das sowohl als persönliches Lernsystem im Bereich IT-Security und DevSecOps dient als auch produktive Anwendungen bereitstellt. Neben dem Netzwerk soll eine selbstentwickelte Webanwendung zur Organisation, Darstellung und Verwaltung privater Medien (Bilder/Videos) entstehen.

Das Projekt dient zudem als Portfolio für die Weiterentwicklung in Richtung Security Engineering.

---

## 2. Erwartung an das System
- Zuverlässiger Betrieb von Netzwerkdiensten (Firewall, DNS-Filter, Monitoring)
- Zentraler Speicherort für Urlaubsbilder und Videos mit strukturierter Verwaltung (z. B. nach Land, Jahr, Dateityp)
- Zugriff über Weboberfläche im lokalen Netz und optional von außerhalb (VPN)
- Trennung von Heimnetz, Gästenetz, Servernetz durch VLANs
- Intuitive Bedienbarkeit für nicht-technische Nutzer (z. B. Familienmitglieder)
- Möglichkeit zur Erweiterung (Cloud-Dienste, weitere Sicherheitsfeatures, neue Apps)
- Integration von Sicherheitstools und Logging zur eigenen Weiterbildung im Bereich Cybersecurity
- Das System darf nicht zu laut sein, da es im privaten Umfeld betrieben wird
- Das Setup soll stromsparend sein, da es dauerhaft läuft und im Alltag als Student bezahlbar bleiben muss
- Die Lösung soll kosteneffizient und langfristig tragbar sein
- Eine möglichst hohe Lernkurve ist gewünscht – insbesondere bei der Konfiguration über die CLI, im Umgang mit Firewalls, Switches und Docker

---

## 3. Auswahl der Hardware
Die Auswahl der Hardware basiert auf dem Ziel, ein möglichst stromsparendes, leises, kostengünstiges, aber dennoch professionelles System zu betreiben, das praxisnahe Erfahrungen im Bereich Netzwerk- und Systemsicherheit ermöglicht.

**Hauptserver:**
- Lenovo ThinkCentre M720q (i5-8400T)
  - Geringer Stromverbrauch bei hoher Leistung
  - Intel QuickSync für Hardware-Encoding (nützlich für Videostreaming)
  - Kompakte Bauweise, leicht erweiterbar
  - Getestet & dokumentiert von vielen Homelab-Nutzern

**NAS:**
- Noch in Überlegung (OpenMediaVault oder Synology)
- Backup-NAS als zweite Instanz geplant

**Netzwerk:**
- FortiGate 60C Firewall zur Trennung und Filterung des Traffics
- Cisco Catalyst WS-C3560CG-8PC-S Switch für VLAN-Unterstützung, PoE-Funktionalität und CLI-Konfiguration
- Pi-hole als Docker-Container auf dem Hauptserver für DNS-Werbeblocker und Tracking-Schutz

---

## 4. Verwendete Technologien & Begründung

| Bereich          | Technologie                 | Begründung                                                                 |
|------------------|-----------------------------|---------------------------------------------------------------------------|
| OS               | Ubuntu Server 22.04 LTS     | Stabil, weit verbreitet, ideal für Serverbetrieb                         |
| Netzwerk         | FortiGate, Cisco            | Professionelle VLAN-Unterstützung & Firewallkontrolle                    |
| Web-Stack        | HTML, CSS, TypeScript, Express (Node.js) | Moderne, schlanke Webentwicklung mit REST-API               |
| Datenbank        | MariaDB                     | Open Source, zuverlässig, leicht mit Node.js integrierbar               |
| Monitoring       | Zabbix, Netdata             | Visualisierung von Systemdaten & Sicherheitsüberwachung                  |
| Storage          | NAS mit OpenMediaVault      | Erweiterbar, gut dokumentiert, kompatibel mit SMB/NFS                   |
| Sicherheit       | Pi-hole (Docker), Fail2Ban, OpenVAS, Nmap | Aktive und passive Sicherheitstools für Test & Praxis     |
| Versionskontrolle| Git & GitHub                | Projektorganisation, CI/CD, Portfolio-Dokumentation                      |

---

## 5. Ziel & Funktionsweise der Webanwendung

Die Webanwendung ist das Herzstück der Benutzerinteraktion. Sie soll folgende Kernfunktionen bieten:

- Benutzer-Login & Upload-Funktion für Bilder und Videos
- Automatische Kategorisierung (z. B. Rohdatei, fertiges Video, Cloud-Datei)
- Weltkartenansicht, bei der Länder ausgewählt werden können, um Medien aus dem jeweiligen Urlaub anzuzeigen
- Flashback-Funktion: Tägliche Anzeige eines Medieninhalts von „vor 1 Jahr“
- Webbasierte Dateiverwaltung mit Download, Vorschau, Tagging und Filtern
- Optional: Zugriff von unterwegs per VPN oder gesicherter Loginmaske

Die Anwendung wird clientseitig in TypeScript (Vanilla oder Framework) und serverseitig in Express (Node.js) realisiert. Die Datenbank speichert alle Medien-Metadaten, Nutzerinformationen und Kategorisierungen.

Ziel ist es, ein modernes, sicheres und responsives Interface zu schaffen, das auch für nicht-technische Nutzer einfach zu bedienen ist.

---

## 6. Weiterentwicklung & Security-Ziele

Dieses System wird laufend erweitert und als Grundlage für folgende Lernfelder genutzt:

- Durchführung eigener Penetration Tests im Testnetz
- Analyse von Netzwerkverkehr & Systemverhalten
- Dokumentation von Angriffserkennung & Abwehrmaßnahmen
- Integration von DevSecOps-Tools (Code-Scanning, Secrets-Detection etc.)
- Deployment-Automatisierung via GitHub Actions (CI/CD)
- Aufbau einer temporären öffentlich zugänglichen Testumgebung, um realistische Angriffsversuche auf die eigene Webanwendung durchführen zu können
- Vergleich zwischen abgesichertem VPN-Zugriff und offen erreichbarem HTTPS-Zugang, um Sicherheitsmaßnahmen praktisch zu bewerten
- In weiterer Überlegung: gezielte Angriffssimulationen auf die eigene Webanwendung über das öffentliche Internet mit Tools wie OWASP ZAP oder Nikto, um das Verhalten unter realen Bedingungen zu testen und Sicherheitslücken frühzeitig zu erkennen.
  - Dabei wird auch in Betracht gezogen, gezielt freiwillige externe Personen – z. B. über Discord-Communities, Reddit oder den Hochschulkontext – zur Mitwirkung einzuladen.
  - Ziel ist es, durch verschiedene Perspektiven zusätzliche Angriffsmuster zu erkennen, Feedback aus der Community zu erhalten und so die Sicherheitsmaßnahmen weiter zu verbessern.
  - Die Organisation eines kontrollierten Bug-Bounty-ähnlichen Tests ist in Planung, jedoch noch nicht final entschieden.

**Hinweis zur ethischen Sicherheit:**  
Zugriffe auf die Webanwendung über das Internet erfolgen ausschließlich auf die eigene, kontrollierte Testumgebung. Die Versuche dienen ausschließlich der eigenen Weiterbildung, Analyse und Verbesserung des Sicherheitsniveaus. Es werden keine Angriffe auf fremde oder unautorisierte Systeme durchgeführt.
