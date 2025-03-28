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

Eine WRD/Box besitzt eine WWAN-Verbindung (WWAN = Wireless Wide Area Network) zum Internet, über die sich ein entsprechend autorisierter (Remote-) Experte per Fernzugriff mit diesem Entwicklungswerkzeug verbinden kann. Für diese Internetverbindung werden verschiedene Technologien, wie 4G, 5G oder Satelliten-Links genutzt. Darüber hinaus existiert auch eine lokale Schnittstelle (z. B. ein Ethernet-LAN-Interface), um einem Anwender vor Ort ebenfalls den Zugriff auf die WRD/Box-Ressourcen zu ermöglichen.

Die WRD/Box basiert auf einem Linux-Betriebssystem und bietet verschiedene Webschnittstellen sowie einem SSH-Zugang für den Benutzerzugriff. Zusätzlich ist in das Linux ein spezieller Wireless Remote Development Software Stack eingebunden, z. B. um einen Software-Update in den angeschlossenen Softsensor einzuspielen, eine Debugging-Sitzung der Softsensor-Firmware oder ein Monitoring mit Telemetriedaten zu ermöglichen. Insgesamt dient die WRD/Box als Werkzeug für Entwickler- bzw. DevOps-Teams, um im Rahmen einer Internet-basierten Remote-Sitzung vor Ort in einer Anwendungsumgebung die jeweils erforderlichen Debug-, Test- und Monitoringaufgaben auszuführen und darüber hinaus mit dem Anwender zu kooperieren.

Siehe auch: https://www.ssv-embedded.de/doks/daten/datasheet_wrd_box.pdf und https://www.ssv-embedded.de/doks/manuals/sr_rmg938a_en.pdf. 

## MLS/100EV als Evaluationssensorik

Eine geeignete Sensorplattform für die Vor-Ort-Datenevaluierung ist die Softsensor Evaluation Device MLS/100EV. Diese Baugruppe wird an einem Maschinengehäuse befestigt und per USB mit der WRD/Box verbunden. Durch den modularen Aufbau mit zwei internen mikroBUS™-Steckplätzen für Erweiterungsplatinen lässt sich die bestmöglich zur Aufgabenstellung passende Sensorik zusammenstellen.

![MLS/100EV und WSB/100EV](https://ssv-comm.de/GitHub-Pictures/mls100ev_ov1.png)

**Abb 2:** Übersicht zum MLS/100EV-Gehäuse und dem internem Aufbau

Ein MLS/100EV lässt sich in Abhängigkeit von der installierten Firmware in zwei unterschiedlichen Betriebsarten nutzen:

**Testbed Mode (TB Mode):** Es besteht eine USB/UART-Verbindung zu einem externen Rechnersystem (beispielsweise einer WRD/Box oderm einem PC). Per Node-RED lassen sich die aktuellen Konfigurationsparameter auslesen, neue Konfiguration laden oder eine andere Firmware in den MCU-Flash-Speicher übertragen. Ansonsten sendet der MLS/210I im TB Mode analog zu einem MLS/160A jeweils die erfassten IMU-Rohdaten über die USB/UART-Schnittstelle an ein externes System, um die jeweiligen Daten dort weiterzuverarbeiten. Die gewünschte Abtastfrequenz der x-, y- und z-Achsenmesswerte für Beschleunigung und Winkelgeschwindigkeit ist wie beim MLS/160A einstellbar. Der TB Mode eignet sich im Rahmen einer MLS/210I-Neuinstallation z. B. zum Erfassen der Trainingsdaten für KI- bzw. ML-Modelle.

**Normal Operation Mode (NO Mode):** Es werden gemäß der jeweiligen Konfiguration periodisch IMU-Messdaten erfasst, mit Hilfe der Sensor-spezifischen Messmethode die gewünschte Zielgröße erzeugt und periodisch bzw. ereignisgesteuert per LTE-M an einen Cloudservice gesendet. Zur Zielgrößenerzeugung wird dabei z. B. eine Fourier Transformation (FT) mit den jeweils abgetasteten IMU-Rohdaten durchgeführt und anschließend der FT-Output per Machine Learning (ML)-Inferenz klassifiziert. Das ML-Ergebnis wird sowohl zum Update der virtuellen Zähler als auch zur Anomalieerkennung genutzt.

