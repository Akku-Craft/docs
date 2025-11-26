# 🔧 Technische Umsetzung

## 🏗️ Das modulare Akkusystem

### Standardisierte Zellformate

- **18650-Zellen**: 18mm Durchmesser, 65mm Länge
- **21700-Zellen**: 21mm Durchmesser, 70mm Länge
- **Vorteile**: Weltweit verfügbar, kostengünstig, in Millionen Geräten verbaut

### Modulare Trägerstruktur

**Konfigurationen:**

- 4-Zellen-Module
- 6-Zellen-Module
- 8-Zellen-Module

**Features:**

- 🧲 Gefederte Kontakte mit Verpolungsschutz
- 🧱 Stapelbare Module
- 🔌 Standardisierte Steckverbindungen
- 🛡️ Robuste Gehäuse aus 3D-gedruckten Komponenten

---

## 🧠 Batterie-Management-System (BMS)

Das BMS ist das "Gehirn" jedes sicheren Akku-Systems und überwacht kontinuierlich alle relevanten Parameter.

### Sicherheitsfunktionen

| Funktion                  | Schutzbereich         | Reaktion                |
| ------------------------- | --------------------- | ----------------------- |
| **Überspannungsschutz**   | > 4,2V pro Zelle      | Ladevorgang stoppen     |
| **Unterspannungsschutz**  | < 2,5V pro Zelle      | Entladung unterbrechen  |
| **Kurzschlussschutz**     | > 10A Strom           | Sofortige Trennung      |
| **Temperaturüberwachung** | > 60°C                | Abschaltung             |
| **Zellen-Balancing**      | Spannungsunterschiede | Automatischer Ausgleich |

### Technische Basis

- **Mikrocontroller**: ATmega328P
- **Zellüberwachungs-IC**: BQ76920 (Texas Instruments)
- **Visualisierung**: LCD-Display + USB-Schnittstelle

---

## 📊 Sensorik und Intelligentes Monitoring

Unser System erfasst nicht nur Sicherheitsparameter, sondern dokumentiert auch den "Gesundheitszustand" des Akkus:

### Überwachte Parameter

- **🔋 Kapazitätsmessung**: Tatsächliche Ladezyklen und verbleibende Kapazität
- **📈 Innenwiderstand**: Indikator für Zellalterung und -zustand
- **🕒 Zyklenhistorie**: Alle Lade- und Entladezyklen mit Zeitstempel
- **🆔 Zellenidentifikation**: Eindeutige ID für jede Zelle zur gezielten Wartung

### Bildungsdaten

Die gesammelten Daten werden für Bildungszwecke aufbereitet:

- Physikalische und chemische Prozesse in Echtzeit nachvollziehbar
- Alterungsverhalten von Lithium-Ionen-Zellen
- Wirkungsgrad-Berechnungen und Energiebilanzen

---

## 🛡️ Sicherheitskonzept

### Mechanische Sicherheit

- Integrierte Sollbruchstellen
- Entgasungsöffnungen für Zelldefekte
- Farbcodierung und eindeutige Beschriftungen
- Verpolungsschutz an allen Kontakten

### Elektrische Sicherheit

- Mehrstufiger Überstromschutz
- Isolierte Leiterbahnen
- Überspannableiter an sensiblen Bauteilen
- Regelmäßige Selbsttests des BMS
