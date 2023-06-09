**Motorisierung**

Beim letztjährigen Future Engineers Wettbewerb haben wir auf Fischertechnik-Teile gesetzt. Dieses Jahr wollten wir das ändern. Stattdessen nutzen wir im Deutschlandfinale unser komplett selbstgebautes Auto, das wir größtenteils auch im Vorentscheid verwendet haben.
Dafür haben wir als Grundlage ein Funduino-Kit genutzt, das speziell für Future Engineers entwickelt wurde. Von diesem Kit haben wir jedoch nur die Grundplatten und die Distanzhülsen verwendet. In der Bauanleitung („e Bauanleitung“) findet man die genauen Maße und Abmessungen der Platten, Schrauben und aller weiteren Komponenten.



**Lenkung**

Für die Lenkung nutzen wir einen 20kg-Servolenkungsmotor. Dieser Motor liegt quer auf unserer Grundplatte. Von dem Gewinde des Servos führt eine kleine Stange, die mit Schrauben befestigt ist, zur eigentlichen Lenkachse. Diese Lenkachse verbindet die beiden Vorderräder miteinander. Wenn der Servo in eine Richtung lenkt, wird die Lenkachse als Ganzes verschoben, und somit auch die Räder.



**Antriebsmotor**

Als Antriebsmotor verwenden wir einen herkömmlichen Motor, der über die Motorsteuerung "L298N" betrieben wird. An diese Motorsteuerung werden direkt 18V vom Akku angeschlossen. Der Motor wird ebenfalls darüber betrieben. Vom Motor gehen noch drei Kabel ab, die wir zur Steuerung des Motors nutzen und die direkt in den "Lenk- und Fahr-Raspberry Pi" führen. Um beide Räder gleichzeitig antreiben zu können, verwenden wir eine Zahnradübersetzung, die die Motorumdrehungen auf ein Zahnrad überträgt, das fest an der Antriebsachse angebracht ist.
