#  homelab-security-project

Ein vollständiges Heimserver-Setup mit Fokus auf **IT-Security**, **Netzwerksegmentierung**, **Media-Hosting** und **automatisierten Sicherheitsmaßnahmen**.  
Dieses Projekt dient als **Lernplattform** und persönliches **Portfolio im Bereich Security Engineering & DevSecOps**.

---

##  Ziel

Aufbau und Dokumentation eines sicheren, modularen Heimnetzwerks mit eigener Webanwendung, Firewall-Architektur, VLAN-Struktur, NAS-Funktionalität und Monitoring – mit dem Ziel, praxisnahe Erfahrung in den Bereichen **Netzwerksicherheit**, **Systemhärtung**, **DevSecOps** und **automatisiertes Monitoring** zu sammeln.

---

##  Features

- Eigene Webanwendung zur Verwaltung & Anzeige von Bildern und Videos  
- Weltkarte mit standortbasiertem Medienzugriff (Flashback-Funktion: „Vor 1 Jahr“)  
- NAS-System mit Kategorien für Rohdateien, fertige Videos, private Cloud  
- VLAN-gestütztes Heimnetzwerk mit FortiGate-Firewall  
- DNS-Filterung & Tracking-Schutz mit Pi-hole  
- Zabbix-Monitoring & Logging  
- Sicherheitsanalysen mit Nmap, OWASP ZAP, Fail2Ban  
- Dokumentation & Automatisierung via GitHub

---

##  Tech Stack

| Komponente       | Tool/Technologie                                    |
|------------------|-----------------------------------------------------|
| **Server-Hardware** | Lenovo ThinkCentre M720q                         |
| **OS**           | Ubuntu Server 22.04 LTS                             |
| **Firewall**     | FortiGate 60C (physisch) + UFW (lokal auf Server)   |
| **Switching**    | Cisco Catalyst 2960C,                               |
| **Monitoring**   | Zabbix (zentral), Netdata (lokal)                   |
| **DNS Filter**   | Pi-hole auf Raspberry Pi                            |
| **Web**          | HTML, CSS, TypeScript, Express (Backend in Node.js) |
| **Datenbank**    | Mysql für Web-App / Logging                         |
| **Storage**      | Synology, 2. NAS als Backup-Ziel                    |
| **Security Tools**| Nmap, Fail2Ban, OpenVAS, Lynis, ClamAV             |
| **CI/CD**        | GitHub Actions, Deployment lokal                    |
| **Dokumentation**| GitHub Pages + PDF-Export                           |


## 📄 Dokumentation

➡️ [Zur ausführlichen Voranalyse](/Voranalyse.md)



