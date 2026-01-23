# Softwarebasierte Steuerung

Die Steuerung wurde in C++ realisiert und nutzt eine duale Betriebslogik.

### Systemarchitektur
Das System unterscheidet zwischen zwei Rollen:
1.  **Master-Modus (Head-Zelle)**: Koordiniert die Datenströme aller Module.
2.  **Slave-Modus (n-te Zelle)**: Fokussiert sich auf lokale Datenerhebung und führt Schaltbefehle aus.

### Kommunikation
Der Datenaustausch erfolgt dezentral über das **UART-Protokoll**. Die Head-Zelle aggregiert alle Telemetriedaten (Spannung, Temperatur, ID) in einer zentralen Datenstruktur. Wenn das System eine Abweichung vom Idealzustand (z.B. Zielwert 4,0V pro Zelle) feststellt, sendet die Head-Zelle aktive Steuerbefehle zum Ausgleich an die betroffenen Module.