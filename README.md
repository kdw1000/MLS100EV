## 1) Beispiel: Maschinendatenevaluierung mit der WRD/Box

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

## 2) Technische Daten WRD/Box mit RMG/938AL

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

## 3) MLS/100EV als Evaluationssensorik

Eine geeignete Sensorplattform für die Vor-Ort-Datenevaluierung ist die Softsensor Evaluation Device MLS/100EV. Diese Baugruppe wird an einem Maschinengehäuse befestigt und per USB mit der WRD/Box verbunden. Durch den modularen Aufbau mit zwei internen mikroBUS™-Steckplätzen für Erweiterungsplatinen bzw. Erweiterungsmodule lässt sich die bestmöglich zur Aufgabenstellung passende Sensorik zusammenstellen.

![MLS/100EV und WSB/100EV](https://ssv-comm.de/GitHub-Pictures/mls100ev_ov1.png)

**Abb 2:** Übersicht zum MLS/100EV-Gehäuse und dem internem Aufbau

Ein MLS/100EV lässt sich in Abhängigkeit von der installierten Firmware in zwei unterschiedlichen Betriebsarten nutzen:

**Testbed Mode (TB Mode):** Es besteht eine USB/UART-Verbindung zu einem externen Rechnersystem (beispielsweise einer WRD/Box oder einem PC), um fortlaufend Sensordaten zu übertragen. Diese werden mit Hilfe der in den mikroBUS-Steckplätzen installierten Sensormodule periodisch erfasst, aufbereitet und an das externe System gesendet. Dort lassen sich die Daten gemäß den jeweiligen Anforderungen weiterverarbeiten bzw. im Rahmen einer Maschinenzustandsdatenperspektive evaluieren. Die USB/UART-Schnittstellenverbindung wird auch für Konfigurationsaufgaben genutzt, z. B. um die Abtastfrequenz der x-, y- und z-Achsenmesswerte für Beschleunigung und Winkelgeschwindigkeit des IMU-Sensorelements auf einem mikroBUS-Modul wunschgemäß einzustellen. Der TB Mode eignet sich im Rahmen einer Vor-Ort-Datenevaluierung für die Erfassung von IMU-Rohdaten, um die Trainingsdaten für KI- bzw. ML-Modelle zu erzeugen.

**Normal Operation Mode (NO Mode):** Es werden gemäß der jeweiligen Konfiguration periodisch IMU-Messdaten erfasst, mit Hilfe der Sensor-spezifischen Messmethode die gewünschte Zielgröße erzeugt und periodisch bzw. ereignisgesteuert per LTE-M an einen Cloudservice gesendet. Zur Zielgrößenerzeugung wird dabei z. B. eine Fourier Transformation (FT) mit den jeweils abgetasteten IMU-Rohdaten durchgeführt und anschließend der FT-Output per Machine Learning (ML)-Inferenz klassifiziert. Das ML-Ergebnis lässt sich in der Zielumgebung bestimmungsgemäß nutzen, beispielsweise zum Update virtueller Zähler oder auch zur Anomalieerkennung.

## 4) Technische Daten MLS/100EV

* 2x interner mikroBUS™-Steckplatz für Sensorik-Erweiterungsmodule
* 1x interner Qwicc-Steckverbinder für I2C-basierte Erweiterungen
* 1x LM75A Digitaler Temperatursensor
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

## 5) TensorFlow-Modell für Vorhersagen und Konvertierungen erzeugen

Die folgenden Colab-Codebausteine bilden so etwas wie ein „Hallo Welt!“ des Supervised Machine Learning mit TensorFlow. Es wird ein Modell für eine lineare Regression `y = mx + b` erzeugt und für Vorhersagen genutzt.  

Ein Lernalgorithmus soll in diesem Beispiel die Gewichtungen für ein Modell aus den zur Verfügung stehenden Trainingsdaten erlernen. Diese Gewichtungen beschreiben die Wahrscheinlichkeit, dass die Datenmuster, die das Modell aus den Daten erlernt (in unserem Beispiel `x = np.array([…])` und `y = np.array([…])`), die tatsächlichen Beziehungen in diesen Daten widerspiegeln. Mit diesem erlernten Modell kann man anschließend für einen bisher unbekannten x-Wert den jeweiligen y-Wert vorhersagen, wenn für x und y die gleichen Beziehungen wie für die Trainingsdaten gelten.  

### 5.1) ML-Regressionsmodell mit TensorFlow und Keras erzeugen 

Der hier folgende Code beinhaltet die Trainingsdaten `x = np.array([…])` und `y = np.array([…])` sowie die erforderlichen TensorFlow-Funktionsaufrufe zur Modellbildung. Durch die Codeausführung in einer Colab-Zelle wird die Datei *my_model.keras* im Colab-Dateibereich erzeugt. Diese Datei bildet das neue Modell.

```python
import tensorflow as tf
import numpy as np
from tensorflow import keras

x = np.array([-1.0, 0.0, 1.0, 2.0,  3.0,  4.0], dtype=float)
y = np.array([-2.0, 1.0, 4.0, 7.0, 10.0, 13.0], dtype=float)

model = tf.keras.Sequential([keras.layers.Dense(units=1, input_shape=[1])])

model.compile(optimizer='sgd', loss='mean_squared_error')

history = model.fit(x, y, epochs=100)

# Save the Keras model to .keras file ...
model.save('my_model.keras')
```

### 5.2) Lernkurve des Modells visualisieren 

Der eigentliche Lernvorgang zur Modellbildung einer Supervised Machine Learning-Anwendung erfolgt in einer Trainingsschleife. Dabei entstehen TensorFlow und Keras interne Daten zum Verlauf der Lernkurve (Training loss). Der folgende Code bewirkt die Darstellung eines Diagramms mit dem *Training loss*. 

```python
import matplotlib.pyplot as plt

loss = history.history['loss']
epochs = range(1, len(loss) + 1)

plt.plot(epochs, loss, 'bo', label='Training loss')
plt.title('Training loss')
plt.show()
```

### 5.3) Modellparameter ausgeben

Das Machine Learning-Modell wird in unserem Beispiel durch ein künstliches neuronales Netzwerk mit je einem Eingang und Ausgang gebildet. Es gibt für die lineare Regression `y = mx + b` genau zwei „lernfähige“ Parameter: *m* und *b*. Die Detailinformationen zum neuronalen Netz lassen sich mit dem folgenden Code in Textform ausgeben:

```python
import tensorflow as tf
import numpy as np
from tensorflow import keras

model = keras.models.load_model("my_model.keras")
model.summary()
```

### 5.4) Modell in einer TensorFlow-Laufzeitumgebung für Vorhersagen nutzen 

Nachdem ein Machine-Learning-Modell vorliegt, lässt es sich für Vorhersagen nutzen (also, um für einen neuen x-Wert den jeweiligen y-Wert zu bestimmen. Der folgende Code bildet den erfoderlichen Inferenzbaustein:

```python
import tensorflow as tf
import numpy as np
from tensorflow import keras

model = keras.models.load_model("my_model.keras")
#print(np.round(model.predict([3]), 1))
print(np.round(model.predict(np.array([[3.0]])), 1))
```
Der neue x-Wert ist in diesem Beispiel die *3* in der letzten Codezeile `print(np.round(model.predict([3]), 1))`. Sie können hier auch andere Werte eintragen und die Codsezelle unter Colab immer wieder ausführen.

### 5.5) Modell in TensorFlow Lite-Format konvertieren 

Um ein TensorFlow-Modell für die Inferenz in einer OT-Umgebung zu nutzen, ist auf dem Zielsystem auch eine vollständige TensorFlow-Laufzeitumgebung erforderlich. Falls Ihre OT-Hardware dafür nicht die erforderlichen Ressourcen bietet, können Sie das Modell in ein TensorFlow Lite-Modell umwandeln. Der folgende Code führt diese Umwandlung aus: Die Datei *my_model.keras* wird TensorFlow Lite-Modell mit dem Namen *my_model.tflite* konvertiert.

```python
import tensorflow as tf
import numpy as np
from tensorflow import keras

model = keras.models.load_model("my_model.keras")

# Convert the Keras model to .tflite file ...
converter = tf.lite.TFLiteConverter.from_keras_model(model)
#converter.optimizations = [tf.lite.Optimize.OPTIMIZE_FOR_SIZE]
#converter.optimizations = [tf.lite.Optimize.DEFAULT]
tflite_model = converter.convert()
open('my_model.tflite', 'wb').write(tflite_model)
```

### 5.6) TensorFlow Lite-Interpreter für Vorhersagen nutzen 

Eine Inferenzmaschine, die TensorFlow Lite-Modelle nutzt (also z. B. Dateien im *tflite*-Format), benötigt einen sogenannten Interpreter. Der hier folgende Code dient als Beispiel für einen solchen TensorFlow Lite-Interpreter.

```python
import numpy as np
import tensorflow as tf

# Load TFLite model and allocate tensors.
interpreter = tf.lite.Interpreter(model_path="my_model.tflite")
interpreter.allocate_tensors()

# Get input and output tensors.
input_details = interpreter.get_input_details()
output_details = interpreter.get_output_details()

# Use model with input data.
input_shape = input_details[0]['shape']
input_data = np.array([[3.0]], dtype=np.float32)
interpreter.set_tensor(input_details[0]['index'], input_data)

interpreter.invoke()

# The function `get_tensor()` returns a copy of the tensor data.
# Use `tensor()` in order to get a pointer to the tensor.
output_data = interpreter.get_tensor(output_details[0]['index'])
print(np.round(output_data, 1))
```

### 5.7) Modell für Embedded Systeme mit einer C/C++ Laufzeitumgebung konvertieren   

Eine Inferenzmaschine für ein TensorFlow/Keras-Modell lässt sich auch auf Embedded Systemen realisieren, die C/C++ unterstützen. Es ist in diesem Fall ...: ... Dafür wird das *xxd*-Hexdump-Werkzeug (Hexdump Utility) aus der Linux-Welt genutzt. Mit diesem Werkzeug lassen sich beispielsweise beliebige Eingaben in eine hexadezimale Ausgabe umwandeln.      

```python
!apt-get update && apt-get install -y xxd

model = keras.models.load_model("my_model.keras")

# Convert the Keras model to .tflite file
converter = tf.lite.TFLiteConverter.from_keras_model(model)
tflite_model = converter.convert()

# Save the .tflite model to a file
tflite_model_path = 'my_model.tflite'
with open(tflite_model_path, 'wb') as f:
    f.write(tflite_model)

# Convert the .tflite model to a C header file
!xxd -i {tflite_model_path} > my_model.h

print(f"TensorFlow Lite model saved as {tflite_model_path} and converted to my_model.h")
```

### 5.8) Trainingsdaten für weitere Regressionsmodelle 

Die Trainingsdaten `x = np.array([…])` und `y = np.array([…])` unter *5.1 Beispiel für ein TensorFlow-Regressionsmodell* können Sie gegen eines der beiden folgenden Beispiele austauschen, um anschließend ein neues TensorFlow-Modell zu erzeugen.

```python
# More data to learn (y = mx + b)

x = np.array([-1.0, 0.0, 1.0, 2.0, 3.0, 4.0,  5.0,  6.0], dtype=float)
y = np.array([-0.5, 1.5, 3.5, 5.5, 7.5, 9.5, 11.5, 13.5], dtype=float)

x = np.array([-1.0, 0.0,  1.0, 2.0,  3.0, 4.0,  5.0, 6.0], dtype=float)
y = np.array([0.75, 1.0, 1.25, 1.5, 1.75, 2.0, 2.25, 2.5], dtype=float)
```
