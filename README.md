# Team MKS Robotics

**Infos zum Githubaufbau**

Unsere GitHub Dokumentation ist entsprechend dem Webertungsbogen der WRO Future Engineers Kategorie aufgebaut. Unter Punkt 1-5 sind die 
Informationen und das Material entsprechung der Bewertungskriterien vorhanden. 
Darunten under Punkt a-f findest man sonstige Sachen, die unsserer Meinung auch wichtig sind.


**Einleitung**

Wir sind Nico und Julian aus dem Saarland und nehmen dieses Jahr erneut für die Maximilian-Kolbe-Schule Wiebelskirchen an der WRO-Kategorie Future-Engineers teil. Im letzten Jahr haben wir bereits erfolgreich teilgenommen und den ersten Platz im Vorentscheid in Waldkirch/Freiburg belegt. Dadurch haben wir uns für das Deutschland-Finale in Chemnitz qualifiziert, wo wir den 4. Platz erreicht haben. Darüber hinaus haben wir bereits an vielen anderen Wettbewerben teilgenommen, darunter die "Robonight" in Saarbrücken, wo wir zweimal den zweiten Platz belegt haben, und die "make-it", wo wir den ersten Platz erreicht haben. Alles begann jedoch mit der WRO, bei der wir im Jahr 2019 in der Kategorie „Mission“ erstmals teilgenommen haben.


**Programmierung Eröffnungsrennen**

Beim diesjährigen Eröffnungsrennen verwenden wir die Grundidee vom letzten Jahr. Während der Fahrt misst der Roboter kontinuierlich die Werte der Ultraschallsensoren, die vorne, links und rechts angeordnet sind. Basierend auf den Werten des linken und rechten Sensors berechnet der Roboter den Mittelpunkt und steuert das autonome Auto proportional, um sich bestmöglich wieder in die Mitte zu bringen. Das bedeutet, je weiter das Auto von der Mitte entfernt ist, desto mehr lenkt es, um diese Mitte wieder zu erreichen.

Ein Beispiel: linker Ultraschallsensor: 10, rechter Ultraschallsensor: 50. Hier zeigt der linke Sensor eine sehr kurze Entfernung, was bedeutet, dass das Auto ziemlich weit links an der Bande ist. Wenn wir nun die Summe der beiden Werte nehmen, ergibt sich die Zahl 60. Die Hälfte davon ist 30. Wenn beide Sensoren nun den Wert 30 ausgeben, wissen wir, dass der Roboter genau in der Mitte ist. Um diese Mitte zu erreichen, berechnen wir den Prozentanteil und lenken entsprechend.

Da dieser Prozess sehr schnell und sehr oft wiederholt wird, kann es manchmal zu einem leichten Schwanken kommen, das das Auto aber ausgleicht. Um am Ende der 3 Runden perfekt zu stoppen, zählt das Auto eine Variable hoch, wenn es eine Kurve fährt. Wir erkennen eine Kurve, wenn plötzlich ein Sensor einen sehr hohen Wert misst. Wenn wir also wie im Beispiel eine Summe von 60 haben und einer der Sensoren plötzlich 150 misst, können wir sicher sein, dass wir uns in einer Kurve befinden. Wenn der Roboter dies 12-mal erkannt hat, bleibt das Auto im richtigen Abschnitt stehen.

**Programmierung Hindernisrennen**

Bei dem Hindernisrennen nutzen wir als Grundlage die Programmierung von dem Eröffnungsrenenn. Denn hier müssen wir ja auch autonom fahren. Nur wenn die Kamera hier einen bunten Stein erkennt, weichen wir aus. Bei roten Steinen rechtsrum, bei Grünen linksherum. Für die Farberkennung haben wir Filter/Masken, damit wir nur die Farben sehen und die sonstigen Fehler, die die Kamera erkennen könnte, ausblenden. Des Weiteren verändern wir die Belichtung des Bildes dynamisch je nach Umgebungshelligkeit, damit wir die Fraben besser erkennen können.

