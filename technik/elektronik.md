# Elektronik & BMS

Das Herzstück von Akku-Craft ist die intelligente Steuerung, die rohe Energie in eine sicher kontrollierte Ressource verwandelt.

### Komponenten
* **Arduino**: Übernimmt die Überwachung der Betriebsparameter wie Spannung, Strom und Temperatur.
* **Spannungsteiler**: Skalieren die Zellspannung (z.B. 8,4V) auf ein für den Arduino verträgliches Maß (unter 5V) herunter.
* **MOSFET-Schutzschaltung**: Eine Back-to-Back-Konfiguration dient als Hochgeschwindigkeitsschalter zum Schutz vor Über- und Tiefentladung.
* **DC-DC-Wandler**: Ermöglicht dem Nutzer, die Ausgangsspannung individuell einzustellen (z.B. 5V für Kleingeräte).


### Berechnungsbeispiel (Balancing)
Wenn eine Zelle zu voll ist, wird Energie über einen 47Ω Widerstand kontrolliert in Wärme umgewandelt. Bei einer Zellspannung von 4,2V fließt ein Strom von ca. 89mA.