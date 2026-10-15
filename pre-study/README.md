# Modul 0 – Vorbereitung: Vernetzung und IoT-Lösungen

Beginn: 15.10.2026

Status: In Bearbeitung

## 1. Portfolio einrichten

- [x] Persönliches GitHub-Repository aus der Kursvorlage erstellt.
- [x] Repository auf den Laptop geklont.
- [x] Diesen Vorbereitungseintrag angelegt.
- [ ] Vorbereitung bearbeitet und Ergebnisse dokumentiert.
- [ ] Notizen und Belege mit Git gespeichert und zu GitHub hochgeladen.

## 2. Inspiration – Schritt A

Video: [Teaching the IoTempower Way](https://video.iotempower.us/)

- [x] Video angesehen.

### Was finde ich spannend?

Mich spricht an, dass man mit erschwinglicher Hardware Lösungen für alltägliche Probleme entwickeln kann. Besonders interessant finde ich das intelligente Pflanzgefäß, weil es Menschen mit wenig Platz oder Erfahrung beim Anbau eigener Pflanzen unterstützen kann.

### Leitfrage 1: Meine IoT-Idee

**Welche vernetzte Anwendung würde ich selbst gern bauen?**

Ich würde gern eine Pflanzenüberwachung bauen, die die Bodenfeuchtigkeit misst und anzeigt, wann die Pflanze Wasser braucht. Als Erweiterung könnte das System die Pflanze automatisch bewässern.

**Wer würde sie nutzen, und welche Geräte müssten miteinander kommunizieren?**

Die Anwendung wäre beispielsweise für Studierende im Wohnheim oder Menschen mit Zimmerpflanzen hilfreich. Ein Bodenfeuchtigkeitssensor würde seine Messwerte an einen kleinen Computer wie den ESP32 liefern. Dieser würde die Werte über WLAN und MQTT an eine Anzeige auf dem Laptop oder einem Display senden. Für eine automatische Bewässerung könnte zusätzlich eine steuerbare Wasserpumpe eingebunden werden.

## 3. Netzwerkgrundlagen – Schritt B

Quelle: [How Data Moves Through the Internet – Ed Harmoush](https://www.practicalnetworking.net/index/networking-fundamentals-how-data-moves-through-the-internet/)

Pflichtlektionen:

- [ ] 1a: Hosts, IP Addresses, Networks.
- [ ] 1b: Repeaters, Hubs, Bridges, Switches, Routers.
- [ ] 2a: OSI Model – Layers 1, 2, 3.

Zusätzlich empfohlen: 2b sowie 3a und 3b.

Meine Notizen zu den Videos:

*Noch ergänzen.*

### Leitfrage 2: IP-Adresse und Subnetzmaske

Was sind eine IP-Adresse und eine Subnetzmaske? Warum dürfen zwei Geräte im selben lokalen Subnetz nicht dieselbe IP-Adresse haben?

*In eigenen Worten ergänzen.*

### Leitfrage 3: OSI und TCP/IP

Warum wird praktisch häufig mit dem TCP/IP-Modell mit vier Schichten gearbeitet? Wo sind starre Grenzen des OSI-Modells mit sieben Schichten für IoT unpraktisch? Welche Rolle spielen kleine Sensornachrichten und zusätzliche Protokollheader?

*In eigenen Worten ergänzen.*

## 4. Mein Netzwerk untersuchen – Schritt C

### 4.1 IP-Adresse und Standardgateway

Unter Windows: `ipconfig /all` und `route print`.

| Eigenschaft der aktiven Netzwerkverbindung | Ergebnis |
|---|---|
| Netzwerkadapter, beispielsweise WLAN | Noch ermitteln |
| Lokale IPv4-Adresse | Noch ermitteln |
| Subnetzmaske beziehungsweise CIDR | Noch ermitteln |
| Standardgateway | Noch ermitteln |

Terminalbeleg und meine Erklärung dazu:

*Relevante Ausgabe oder Screenshot ergänzen.*

### 4.2 Weg zu 1.1.1.1

Befehl unter Windows: `tracert 1.1.1.1`.

- Wurde das Ziel erreicht? *Noch ermitteln.*
- Anzahl der sichtbaren Routerstationen (Hops): *Noch ermitteln.*
- Wo erscheinen private und wo öffentliche IP-Adressen? *Noch untersuchen.*
- Gab es Zeitüberschreitungen oder andere Auffälligkeiten? *Noch ergänzen.*

Terminalbeleg:

*Ausgabe oder Screenshot ergänzen.*

### 4.3 MQTT ausprobieren

- [ ] MQTT-Client ausgewählt und mit dem Testbroker verbunden.
- [ ] Ein eigenes Topic mit Pseudonym oder Zufallskennung abonniert.
- [ ] Eine Nachricht an dieses Topic veröffentlicht.
- [ ] Empfang der Nachricht geprüft.
- [ ] Screenshot der empfangenen Nachricht hinzugefügt.

| Einstellung | Verwendeter Wert |
|---|---|
| Client | Noch ergänzen |
| Broker | `broker.hivemq.com` |
| Verbindung und Port | Noch ergänzen; laut Guide TCP 1883 oder WebSocket 8000 |
| Topic | Noch festlegen: `hsbi/student/<pseudonym-oder-zufallskennung>/test` |

Vorgeschlagene Nachricht:

```json
{"status": "online", "message": "Hello Vernetzung!"}
```

Beobachtung und Screenshot:

*Nach dem Versuch ergänzen. Auf dem öffentlichen Broker kein echter Name und keine persönlichen Daten.*

### Leitfrage 4: Nachrichten mit Publish/Subscribe verteilen

Warum ist bei zehn Temperatursensoren und drei Displays ein MQTT-Broker leichter zu pflegen als direkte HTTP-Verbindungen von jedem Sensor zu jedem Display?

*In eigenen Worten ergänzen.*

### Leitfrage 5: Grenzen zwischen Netzwerken

Kann mein Laptop von zu Hause direkt ein Gerät im Heim-WLAN eines Kommilitonen anpingen? Warum beziehungsweise warum nicht? Was würde ein Overlay-Netzwerk wie Nebula oder Yggdrasil verändern?

*In eigenen Worten ergänzen.*

## 5. Rückblick und offene Fragen

- Was habe ich verstanden? *Noch ergänzen.*
- Was hat nicht funktioniert, und was habe ich versucht? *Noch ergänzen.*
- Was ist noch unklar? *Noch ergänzen.*
- Rückmeldung zum Guide: Was war merkwürdig, überflüssig oder fehlte? *Bei Bedarf ergänzen.*

## 6. Vor der ersten Sitzung prüfen

- [ ] Fünf Leitfragen beantwortet.
- [ ] Video- und Inspirationsnotizen ergänzt.
- [ ] Terminalbelege zur Netzwerkuntersuchung ergänzt.
- [ ] MQTT-Screenshot ergänzt.
- [ ] Ergebnisse committet und zu GitHub gepusht.
- [ ] Laptop mit WLAN und SSH-Client bereit; Wireshark und MQTTX optional.

Modul 0 ist verpflichtend, zählt einen Modulpunkt und wird in der zweiten Sitzung bewertet.
