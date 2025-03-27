## Beispiel: Maschinendatenevaluierung mit der WRD/Box

Für jede Condition Monitoring-Aufgabe im Rahmen eines Digitalisierungs-Retrofits, bei der keine passende Schnittstelle zur Maschinensteuerung als Datenquelle genutzt werden kann, muss zuerst ein geeignetes Eingangsdatenbild erzeugt werden, wofür in der Regel eine externe Sensorik als Datenquelle erforderlich ist.

Dafür sind zunächst verschiedene Fragen zu beantworten und Details zu klären. Schließlich müssen sich die Sensorrohdaten als Basis zur Informationsgewinnung eignen, um die jeweilige Aufgabe zufriedenstellend erfüllen zu können.

Ein sinnvoller erster Schritt ist eine Vor-Ort-Datenevaluierung mit Schwingungsdaten, die mit der Maschinennutzung korrelieren. Dazu wird ein Sensor am Maschinengehäuse befestigt und mit einer industrietauglichen Rechnerbaugruppe verbunden, um die Schwingungsdaten über einen längeren Zeitraum zu erfassen. Anschließend werden die so erzeugten Zeitreihendaten analysiert, bewertet und ggf. weiteren Beteiligten präsentiert. Dabei sind besonders die Zustandsübergänge von Bedeutung, also z. B. vom Standby in den Betrieb mit geringer Last, der Wechsel zum Volllastbetrieb, Betriebsunterbrechungen durch Rüstphasen usw.

![WRD/Box mit Workflow](https://ssv-comm.de/GitHub-Pictures/softsensor_wrd-box_datenevaluierung.png)

**Abb 1:** Testbed zur Maschinendatenevaluierung mit der WRD/Box

Das Testbed zur Maschinendatenevaluierung besteht aus einer WRD/Box mit externer Evaluationssensorik an der Maschine als Datenquelle. Die WRD/Box besitzt ein 4G-Mobilfunkmodem und ist **sowohl** für den Datenexperten als auch den Maschinenbetreiber über eine gesicherte Internetverbindung erreichbar.

Der Datenexperte startet die Datenerfassung, verschafft sich das notwendige Datenverständnis, bereitet die erfassten Daten auf und analysiert sie zusammen mit dem Betreiber, um daraus ein geeignetes Eingangsdatenbild für die gewünschte Aufgabe, wie bspw. virtuelle Bestriebsstundenzähler, zu erzeugen.

## Technische Daten WRD/Box mit RMG/938AL

* 1x Mobilfunk-Interface (4G) für LTE Cat 4-Verbindungen
* GNSS (Global Navigation Satellite System) Option verfügbar 
* 1x SIM-Kartensteckplatz (IGW/938L-Gehäuserückwand)
* Mobile Virtual Network Operator (MVNO) SIM-Karte mit IoT-Datenplan vorinstalliert
* 2x SMA-Stecker für externe Mobilfunkantennen
* Unterstützung aller gängigen Cloud-Protokolle
* 2x 10/100 Mbps Ethernet LAN
* 1x USB 2.0 Host
* 1x RS485 serieller Port (Schraubklemme)
* 1x RS232/RS485 serieller Port (Schraubklemme)
* Integriertes 110 - 230 VAC/24 VDC Netzteil mit Netzanschlusskabel
* Leuchtdioden zur Statusanzeige
* Embedded Debian Linux Betriebssystem
* SSV Wireless Remote Development Software Stack
* PKI-basierte Vertrauenskette für End-2-End Security
* Zwei alternative Gehäusevarianten 110 x 180mm, 254 x 180mm mit Staubschutzdeckel
* Interner Aufbau über 35mm DIN-Hutschienen
* 1x externe LTE-Mobilfunkantenne mit 3m Kabel

## MLS/100EV als Evaluationssensorik

Eine geeignete Sensorplattform für die Vor-Ort-Datenevaluierung ist die Softsensor Evaluation Device MLS/100EV. Diese Baugruppe wird an einem Maschinengehäuse befestigt und per USB mit der WRD/Box verbunden. Durch den modularen Aufbau mit zwei internen mikroBUS™-Steckplätzen für Erweiterungsplatinen lässt sich die bestmöglich zur Aufgabenstellung passende Sensorik zusammenstellen.


