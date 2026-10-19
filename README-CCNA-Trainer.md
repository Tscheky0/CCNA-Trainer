# CCNA 200-301 Trainer 3D

Lernspiel für die CCNA Prüfung als 3D Korridor im Browser. Du stehst vor vier Türen, über den Türen steht die Frage, die richtige Tür bringt dich einen Raum weiter, eine falsche wirft dich zurück. Am Ende wartet das Ziel.

Der Schwerpunkt liegt auf Troubleshooting: Du liest ein Symptom, manchmal mit IOS Ausgabe im Fragetext, und wählst Ursache oder Lösung. Dazu kommen Wissensfragen zu Subnetting, Binär, Ports und Grundlagen.

Eine einzige HTML Datei, kein Build, keine Installation, kein Server. Three.js ist direkt eingebettet, die Datei läuft deshalb auch komplett offline.

## Starten

Datei `CCNA-Trainer-v5.html` herunterladen und im Browser öffnen. Fertig.

Für GitHub Pages die Datei in `index.html` umbenennen und unter Settings, Pages den Branch `main` aktivieren.

## Inhalt

29 Themen, 537 Fragen, 3 Schwierigkeitsstufen: leicht (133), mittel (268), schwer (136). Doppelte Fragen werden beim Laden automatisch entfernt.

| Thema | Fragen | Thema | Fragen |
|---|---|---|---|
| Subnetting | 96 | Security | 37 |
| Automation/API | 31 | Wireless | 30 |
| Ports | 30 | Switching | 27 |
| OSPF | 26 | IPv6 | 26 |
| Routing-Grundlagen | 25 | STP | 20 |
| VLAN & Trunk | 20 | Monitoring | 20 |
| Binär | 20 | OSI-Modell | 18 |
| IP-Services | 15 | NAT/PAT | 11 |
| Netzwerk-Grundlagen | 11 | ACL | 10 |
| FHRP | 10 | DHCP | 9 |
| Cisco CLI | 8 | EtherChannel | 8 |
| QoS | 8 | Architektur | 8 |
| DNS | 6 | ARP & Routing | 3 |
| Interface | 2 | Betrieb | 1 |
| Port Security | 1 | | |

## Spielmodi

| Modus | Regel |
|---|---|
| Klassisch | falsch bedeutet ein Raum zurück |
| Lernmodus | kein Zurück, Erklärung ohne Countdown |
| Prüfung | Auflösung erst am Ende |
| Blitz | 7 Sekunden pro Frage, immer vorwärts |
| Sudden Death | ein Fehler beendet die Runde |
| Fehler-Training | nur Fragen, die früher falsch waren |
| Prüfungssimulation | 50 Fragen mit Zeitdruck, Auswertung am Ende, bestanden ab 82 Prozent |
| Zeitjagd | 3 Minuten, so viele Fragen wie möglich |
| Präzision | 3 Leben, immer vorwärts |
| Boss-Modus | nur schwere Fragen |

Zusätzlich einzeln zuschaltbar: Zeitdruck (20 Sekunden pro Frage), 3 Leben statt Zurücksetzen und Sound.

## Funktionen

* Auswahl nach Thema und Schwierigkeit, Anzahl der Fragen bis 200 per Regler
* Nach jeder Antwort bleibt die Erklärung 12 Sekunden stehen, mit Countdown (im Blitz Modus 4 Sekunden)
* Live Uhr pro Frage, in der Zeitjagd der Countdown der Gesamtzeit
* Spaced Repetition: falsch beantwortete Fragen werden in späteren Runden bevorzugt gezogen
* Statistik mit Fehlerquote pro Thema über alle Runden
* Rekord pro Auswahl aus Thema, Stufe, Anzahl und Modus
* Seed Feld: gleicher Seed ergibt dieselben Fragen in derselben Reihenfolge, zum Vergleichen mit anderen
* XP und Level: 10 XP pro richtiger Antwort, 5 XP pro Frage der besten Serie, 50 XP Bonus bei fehlerfreier Runde, 500 XP pro Level
* Menü Button während des Spiels, mit Rückfrage vor dem Abbruch

## Auswertung

Am Ende zeigt die Datei die Trefferquote als Prozentring mit Medaille, dazu vier Kennzahlen: Gesamtzeit, Fehler, beste Serie und Durchschnittszeit pro Frage. Ab 75 Prozent gibt es Konfetti, dazu je nach Ergebnis einen anderen Abschlusssound.

Darunter steht das Review mit allen falschen Fragen, der richtigen Antwort, deiner Antwort und der Erklärung. Mit einem Klick startet eine neue Runde nur aus diesen Fragen.

## Bedienung

Per Maus oder Touch auf die richtige Tür gehen.

## Daten

Alles bleibt im Browser (`localStorage`). Es werden keine Daten gesendet und es gibt keine externen Anfragen. Gespeichert werden Fehlerpool (`nt_srs`), Statistik (`nt_stats`), XP (`nt_xp`) und Rekorde (`nt_best`). Statistik und Fehlerpool lassen sich im Statistik Screen zurücksetzen.

## Technik

HTML, CSS und JavaScript in einer Datei, Rendering mit Three.js (r160, MIT Lizenz), Sound über Web Audio API, Oberfläche im Glas Stil mit `backdrop-filter`.
