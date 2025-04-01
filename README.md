## Beispiel: Maschinendatenevaluierung mit der WRD/Box

Für jede Condition Monitoring-Aufgabe im Rahmen eines Digitalisierungs-Retrofits, bei der keine passende Schnittstelle zur Maschinensteuerung als Datenquelle genutzt werden kann, muss zuerst ein geeignetes Eingangsdatenbild erzeugt werden, wofür in der Regel eine externe Sensorik als Datenquelle erforderlich ist.

Dafür sind zunächst verschiedene Fragen zu beantworten und Details zu klären. Schließlich müssen sich die Sensorrohdaten als Basis zur Informationsgewinnung eignen, um die jeweilige Aufgabe zufriedenstellend erfüllen zu können.

Ein sinnvoller erster Schritt ist eine Vor-Ort-Datenevaluierung mit Schwingungsdaten, die mit der Maschinennutzung korrelieren. Dazu wird ein Sensor am Maschinengehäuse befestigt und mit einer industrietauglichen Rechnerbaugruppe verbunden, um die Schwingungsdaten über einen längeren Zeitraum zu erfassen. Anschließend werden die so erzeugten Zeitreihendaten analysiert, bewertet und ggf. weiteren Beteiligten präsentiert. Dabei sind besonders die Zustandsübergänge von Bedeutung, also z. B. vom Standby in den Betrieb mit geringer Last, der Wechsel zum Volllastbetrieb, Betriebsunterbrechungen durch Rüstphasen usw.

![WRD/Box mit Workflow](https://ssv-comm.de/GitHub-Pictures/softsensor_wrd-box_datenevaluierung.png)

**Abb 1:** Testbed zur Maschinendatenevaluierung mit der WRD/Box

Das Testbed zur Maschinendatenevaluierung besteht aus einer WRD/Box mit externer Evaluationssensorik an der Maschine als Datenquelle. Die WRD/Box besitzt ein 4G-Mobilfunkmodem und ist **sowohl** für den Datenexperten als auch den Maschinenbetreiber über eine gesicherte Internetverbindung erreichbar.

Der Datenexperte startet die Datenerfassung, verschafft sich das notwendige Datenverständnis, bereitet die erfassten Daten auf und analysiert sie zusammen mit dem Betreiber, um daraus ein geeignetes Eingangsdatenbild für die gewünschte Aufgabe, wie bspw. virtuelle Bestriebsstundenzähler, zu erzeugen.

Die beiden großen Herausforderungen hinsichtlich einer erfolgreichen Maschinendatenevaluierung sind die Datenquantität und die Datenqualität. Insofern eignet sich ein Top-Down-Ansatz als zielführende Vorgehensweise, z. B. mit der hier folgenden Gliederung:

1. Welche Fragestellung soll beantwortet werden?
2. Welche Informationen werden für die Antwort benötigt?
3. Welche Daten sind zur Informationsgewinnung erforderlich?
4. Welche Sensoren werden zur Datenerzeugung benötigt?

Besonders die letzte Frage (Welche Sensoren werden benötigt?) erfordert eine gewisse Flexibilität. Es ist davon auszugehen, dass diverse Datenerfassungsversuche mit verschiedenen Sensorelementen durchgeführt werden.

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

Eine geeignete Sensorplattform für die Vor-Ort-Datenevaluierung ist die Softsensor Evaluation Device MLS/100EV. Diese Baugruppe wird an einem Maschinengehäuse befestigt und per USB mit der WRD/Box verbunden. Durch den modularen Aufbau mit zwei internen mikroBUS™-Steckplätzen für Erweiterungsplatinen bzw. Erweiterungsmodule lässt sich die bestmöglich zur Aufgabenstellung passende Sensorik zusammenstellen.

![MLS/100EV und WSB/100EV](https://ssv-comm.de/GitHub-Pictures/mls100ev_ov1.png)

**Abb 2:** Übersicht zum MLS/100EV-Gehäuse und dem internem Aufbau

Ein MLS/100EV lässt sich in Abhängigkeit von der installierten Firmware in zwei unterschiedlichen Betriebsarten nutzen:

**Testbed Mode (TB Mode):** Es besteht eine USB/UART-Verbindung zu einem externen Rechnersystem (beispielsweise einer WRD/Box oder einem PC), um fortlaufend Sensordaten zu übertragen. Diese werden mit Hilfe der in den mikroBUS-Steckplätzen installierten Sensormodule periodisch erfasst, aufbereitet und an das externe System gesendet. Dort lassen sich die Daten gemäß den jeweiligen Anforderungen weiterverarbeiten bzw. evaluieren. Die USB/UART-Schnittstellenverbindung wird auch für Konfigurationsaufgaben genutzt, z. B. um die Abtastfrequenz der x-, y- und z-Achsenmesswerte für Beschleunigung und Winkelgeschwindigkeit des IMU-Sensorelements auf einem mikroBUS-Modul wunschgemäß einzustellen. Der TB Mode eignet sich im Rahmen einer Vor-Ort-Datenevaluierung für die Erfassung von IMU-Rohdaten, um die Trainingsdaten für KI- bzw. ML-Modelle zu erzeugen.

**Normal Operation Mode (NO Mode):** Es werden gemäß der jeweiligen Konfiguration periodisch IMU-Messdaten erfasst, mit Hilfe der Sensor-spezifischen Messmethode die gewünschte Zielgröße erzeugt und periodisch bzw. ereignisgesteuert per LTE-M an einen Cloudservice gesendet. Zur Zielgrößenerzeugung wird dabei z. B. eine Fourier Transformation (FT) mit den jeweils abgetasteten IMU-Rohdaten durchgeführt und anschließend der FT-Output per Machine Learning (ML)-Inferenz klassifiziert. Das ML-Ergebnis wird sowohl zum Update der virtuellen Zähler als auch zur Anomalieerkennung genutzt.

## Technische Daten MLS/100EV

* 2x interner mikroBUS™-Steckplatz für Sensorik-Erweiterungsmodule
* 1x interner Qwicc-Steckverbinder für I2C-basierte Erweiterungen
* RFSoC-basiertes LTE-M-Mobilfunkmodem (vorzertifiziert)
* Frequenzbereich 700 - 2.200 MHz 
* Unterstützung der internationalen LTE-M-Bänder B1 - B5, B8, B12, B13, B14, B17 - B20, B25, B26, B28, B66 
* Max. Datenrate LTE-M: 300 Kbps Downlink / 375 kbps Uplink
* 3GPP AT-Kommandos gemäß TS 27.007 plus Erweiterungen
* IoT-Protokollstack mit (D)TLS-Support für Internet-Funkverbindungen
* Interner nanoSIM-Kartenhalter (Fourth Form Factor 4FF)
* Mobile Virtual Network Operator (MVNO)-SIM-Karte mit IoT-Datenplan vorinstalliert (weltweit nutzbar)
* Arm Cortex M33 Application MCU zur KI-basierten Sensordatenanalyse
* 1 Mbytes Flash, 256 Kbytes RAM
* Embedded LTE-M-Antenne im Gehäuseinneren
* USB-Steckverbinder zur Spannungsversorgung und Datenkommunikation 
* Firmware Updates und Konfigurationseinstellungen per USB
* Optionale Firmware-Varianten für den Normal- und Testbed-Betrieb 
* Gehäuseabmessungen 109,96 x 57,04 x 27mm, Haube 83,77 x 54,57mm 
* Mehrfarbige Status-LED (RGB LED)
* Interner Debug-Steckverbinder plus Tasten für DFU-Mode
* Maschinenmontage durch Aufkleben auf glatte Oberflächen (alternativ Montage per Schraubverbindung oder Magnethalterung)

