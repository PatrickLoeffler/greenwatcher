# Greenwatcher -  Selbstbewässerungssystem mit Raspberry Pi, Arduino und Mycodo

## Übersicht
Dieses Projekt zielt darauf ab, ein automatisiertes Selbstbewässerungssystem mit einem Raspberry Pi und einem Arduino zu bauen. Das System sammelt Bodendaten über Feuchtigkeitssensoren und steuert eine peristaltische Wasserpumpe, um eine optimale Bodenfeuchtigkeit sicherzustellen. Die Frontend-Schnittstelle wird mit Mycodo verwaltet, das Echtzeitüberwachung und Steuerungsmöglichkeiten bietet.

## Komponenten
- **Raspberry Pi**: Dient als zentrale Verarbeitungseinheit des Systems, die Datenverarbeitung, Steuerlogik und Schnittstellen zu Mycodo übernimmt.
- **Arduino**: Verantwortlich für das Auslesen der Sensordaten und die Kommunikation mit dem Raspberry Pi.
- **Bodenfeuchtigkeitssensoren**: Messen die Feuchtigkeitswerte im Boden.
- **Peristaltische Wasserpumpe**: Versorgt den Boden basierend auf den Feuchtigkeitssensormessungen mit Wasser.
- **Mycodo**: Eine Open-Source-Monitoring- und Steuerungssoftware, die die Frontend-Schnittstelle für die Systemverwaltung bietet.

## Systemarchitektur
1. **Sensordatenerfassung**: Der Arduino liest Daten von den Bodenfeuchtigkeitssensoren.
2. **Datenkommunikation**: Der Arduino sendet die Sensordaten an den Raspberry Pi.
3. **Datenverarbeitung und Steuerung**: Der Raspberry Pi verarbeitet die Sensordaten und entscheidet, ob eine Bewässerung erforderlich ist. Wenn die Bodenfeuchtigkeit unter dem Schwellenwert liegt, aktiviert der Raspberry Pi die peristaltische Wasserpumpe.
4. **Frontend-Schnittstelle**: Mycodo läuft auf dem Raspberry Pi und bietet eine benutzerfreundliche Schnittstelle zur Überwachung der Bodenfeuchtigkeitswerte, zur Konfiguration der Systemparameter und zur manuellen Steuerung der Pumpe.

## Detaillierter Workflow
1. **Setup**: 
    - Mycodo auf dem Raspberry Pi installieren und konfigurieren.
    - Den Arduino per USB oder serielle Kommunikation mit dem Raspberry Pi verbinden.
    - Bodenfeuchtigkeitssensoren an den Arduino anschließen.
    - Die peristaltische Wasserpumpe an die GPIO-Pins des Raspberry Pi anschließen.

2. **Programmierung**:
    - **Arduino**: Ein Sketch schreiben, um die Feuchtigkeitssensordaten auszulesen und an den Raspberry Pi zu senden.
    - **Raspberry Pi**: Ein Python-Skript schreiben, um die Daten vom Arduino zu empfangen, zu verarbeiten und die Wasserpumpe basierend auf vordefinierten Schwellenwerten zu steuern.

3. **Integration mit Mycodo**:
    - Mycodo konfigurieren, um Sensordaten zu empfangen und anzuzeigen.
    - Steuerlogik in Mycodo einrichten, um die Wasserpumpe basierend auf den Bodenfeuchtigkeitsmessungen zu automatisieren.
    - Ein Dashboard in Mycodo erstellen für Echtzeitüberwachung und manuelle Steuerung.

4. **Testen und Kalibrieren**:
    - Die Bodenfeuchtigkeitssensoren kalibrieren, um genaue Messwerte zu gewährleisten.
    - Das System testen, um sicherzustellen, dass die Pumpe basierend auf den Bodenfeuchtigkeitswerten korrekt aktiviert wird.

## Anforderungen
- **Hardware**:
    - Raspberry Pi (mit installiertem Mycodo)
    - Arduino (z.B. Arduino Uno)
    - Bodenfeuchtigkeitssensoren
    - Peristaltische Wasserpumpe
    - Relaismodul (falls erforderlich zur Pumpensteuerung)
    - Stromversorgung
    - Verbindungskabel und Steckbrett

- **Software**:
    - Mycodo auf dem Raspberry Pi installiert
    - Arduino IDE zur Programmierung des Arduino
    - Python für die Skripterstellung auf dem Raspberry Pi

## Vorteile
- **Automatisierung**: Reduziert den Bedarf an manueller Bewässerung und stellt sicher, dass die Pflanzen die richtige Menge Wasser erhalten.
- **Effizienz**: Verhindert Überbewässerung und Unterbewässerung und optimiert den Wasserverbrauch.
- **Skalierbarkeit**: Das System kann mit zusätzlichen Sensoren und Pumpen für größere Setups erweitert werden.
- **Benutzerfreundliche Schnittstelle**: Mycodo bietet ein intuitives Dashboard zur Überwachung und Steuerung.

## Zukünftige Verbesserungen
- Integration zusätzlicher Umweltsensoren (z.B. Temperatur, Luftfeuchtigkeit).
- Fernüberwachung und -steuerung über eine Webschnittstelle.
- Erweiterte Datenanalyse für bessere Wassermanagementstrategien.
- Integration von Solarenergie für eine netzunabhängige Lösung.

## Fazit
Dieses Projekt kombiniert die Fähigkeiten von Raspberry Pi, Arduino und Mycodo, um ein effizientes, automatisiertes Selbstbewässerungssystem zu schaffen. Es nutzt moderne IoT-Technologien, um optimale Bodenfe


![Alt text here](diagram.svg)
