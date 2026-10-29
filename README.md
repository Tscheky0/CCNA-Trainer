# 🛰️ CCNA Trainer 3D

![Cisco](https://img.shields.io/badge/Cisco-CCNA%20200--301-1BA0D7?logo=cisco&logoColor=white)
![Three.js](https://img.shields.io/badge/3D-Three.js-000000?logo=threedotjs&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-Single%20File-E34F26?logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-Vanilla-F7DF1E?logo=javascript&logoColor=black)
![Fragen](https://img.shields.io/badge/Fragen-537-028090)
![Sprache](https://img.shields.io/badge/Sprache-Deutsch-000000)

Ein interaktiver 3D Lerntrainer zur Vorbereitung auf die Cisco Prüfung **CCNA 200-301**. Statt Fragen in einer langweiligen Liste abzuarbeiten, bewegst du dich durch Räume und wählst die richtige Antwort, indem du durch die passende Tür gehst. Komplett auf Deutsch, ohne Installation, direkt im Browser.

## Warum dieses Projekt?

Die CCNA ist eine der wichtigsten Einstiegszertifizierungen im Netzwerkbereich, aber der Stoff ist riesig: Routing, Switching, Security, Wireless, Automatisierung und vieles mehr. Klassische Fragenkataloge sind trocken und fast ausschließlich auf Englisch.

Dieser Trainer entstand während meiner Ausbildung zum IT Netzwerktechniker, um genau diese Lücke zu schließen. Ziel war ein Werkzeug, das Lernen wie ein Spiel anfühlen lässt, gezielt an Schwächen arbeitet und eine realistische Prüfungssituation simuliert.

## So funktioniert es

Jede Frage ist ein eigener Raum. Über den Türen schwebt die Frage samt Kategorie und Schwierigkeitsstufe, jede Tür steht für eine Antwort. Wer durch die richtige Tür geht, kommt in den nächsten Raum. Nach jeder Antwort folgt eine Erklärung, damit nicht nur auswendig gelernt, sondern verstanden wird.

## Fragenpool

537 Fragen in 29 Kategorien, ausgerichtet an den offiziellen Prüfungsthemen der CCNA 200-301.

| Prüfungsbereich | Inhalte |
|:--|:--|
| Network Fundamentals | OSI und TCP/IP Modell, IPv4 Subnetting, IPv6, Netzwerkarchitektur, Virtualisierung |
| Network Access | VLANs, Trunking, STP und RSTP, EtherChannel, Wireless, WLC und CAPWAP |
| IP Connectivity | Statisches Routing, OSPF, FHRP mit HSRP, VRRP und GLBP |
| IP Services | NAT und PAT, DHCP, NTP, Syslog, SNMP, QoS |
| Security Fundamentals | ACLs mit Wildcard Masken, Port Security, DHCP Snooping, DAI, 802.1X, RADIUS und TACACS+ |
| Automation & Programmability | SDN, REST API, JSON und YAML, NETCONF und YANG, Ansible, Puppet, Chef |
| Cisco CLI | Konfigurations und Show Befehle aus der Praxis |

Jede Frage hat eine von drei Schwierigkeitsstufen, die farblich im Raum angezeigt wird.

| Stufe | Bedeutung |
|:--|:--|
| 🟢 Leicht | Grundbegriffe und Definitionen |
| 🟡 Mittel | Zusammenhänge und Anwendung |
| 🔴 Schwer | Prüfungsniveau, Detailwissen und Fallstricke |

## Spielmodi

Insgesamt stehen 10 Modi zur Verfügung. Bei der Auswahl werden Timer, Leben und Schwierigkeit automatisch passend eingestellt.

| Modus | Beschreibung |
|:--|:--|
| 🎓 Prüfungssimulation | 50 Fragen mit Zeitlimit, Auswertung erst am Ende, bestanden ab 82 % wie in der echten Prüfung |
| ⏳ Zeitjagd | 3 Minuten Gesamtzeit, so viele richtige Antworten wie möglich |
| 🎯 Präzision | 3 Leben, jeder Fehler kostet eines |
| 🔥 Boss Modus | Ausschließlich Fragen der höchsten Schwierigkeitsstufe |
| 🔁 Fehler Training | Nur Fragen, die vorher falsch beantwortet wurden |

Dazu kommen weitere Modi für freies Üben, schnelle Runden und gezieltes Lernen einzelner Kategorien. Timer, Leben und Schwierigkeitsstufen lassen sich zusätzlich frei kombinieren.

## Starten

Es ist keine Installation nötig. Repository herunterladen, die HTML Datei doppelklicken, fertig. Der Trainer läuft in jedem aktuellen Browser wie Chrome, Edge oder Firefox, am PC ebenso wie am Laptop.

```bash
git clone https://github.com/Tscheky/CCNA-Trainer.git
```

## Technik

| Bereich | Umsetzung |
|:--|:--|
| 3D Darstellung | Three.js mit WebGL |
| Logik | Reines JavaScript ohne Frameworks |
| Aufbau | Eine einzige HTML Datei, keine Abhängigkeiten zum Installieren |
| Fragentexte | Werden dynamisch auf Canvas gerendert, mit automatischer Schriftanpassung, damit auch lange Fragen immer vollständig lesbar sind |
| Qualitätssicherung | Fragenpool und Syntax wurden nach jeder Erweiterung automatisiert mit Node.js geprüft |

## Entwicklung

| Version | Meilenstein |
|:--|:--|
| v1 bis v4 | 3D Raumkonzept, Grundfragenpool, erste Spielmodi, Fehler Training |
| v5 | Erweiterung um 171 prüfungsnahe Fragen auf 537 Fragen in 29 Kategorien, vier neue Modi inklusive Prüfungssimulation |
| v6 | Überarbeitetes Fragepanel mit automatischer Schriftgrößenanpassung, Kollisionen zwischen Panel und Türen behoben |

## Was ich dabei gelernt habe

Fachlich hat mich das Schreiben der Fragen tiefer in den CCNA Stoff gebracht als reines Lesen. Wer eine Frage samt plausibler falscher Antworten formulieren muss, muss das Thema wirklich verstanden haben. Technisch habe ich mit 3D Grafik im Browser, Canvas Rendering, Zustandsverwaltung in JavaScript und automatisierten Tests gearbeitet.

## Hinweis

Dies ist ein privates Lernprojekt und steht in keiner Verbindung zu Cisco Systems. CCNA und Cisco sind Marken der Cisco Systems, Inc. Die Fragen sind selbst formuliert und keine echten Prüfungsfragen.
