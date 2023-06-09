**Energie**

Unser Auto wird mit einem handelsüblichen 18V Bosch Akku betrieben. Dieser Akku wird in einen Akku-Slot eingeschoben. Von dort aus führt eine Verbindung zum Spannungswandler. Der Wandler wandelt die Spannung auf 5V um, die wir für die Raspberry Pis benötigen. Zusätzlich verwenden wir eine Motorsteuerung, die direkt mit 18V versorgt wird. Es ist erwähnenswert, dass die Ultraschallsensoren mit 5V betrieben werden, während andere Sensoren wie der Farbsensor oder der Gyrosensor mit 3,3V arbeiten.


**Sensoren**

In unserem Auto sind eine Vielzahl von Sensoren verbaut. Zum einen haben wir drei HCSR-04 Sensoren integriert, die zur Erkennung der Fahrbahn und zum entsprechenden Lenken verwendet werden. Des Weiteren haben wir einen Farbsensor installiert, der die orangenen und blauen Linien erkennt und somit die Runden zählt, damit wir nach drei Runden erfolgreich stoppen können. Außerdem haben wir einen Gyrosensor eingebaut, um eine zu starke Drehung zu vermeiden. Ganz oben befindet sich zudem eine Kamera. Es handelt sich um eine USB-Webcam von Logitech, die für die Hinderniserkennung verwendet wird.
