# Team MKS Robotics

**Infos zum Githubaufbau**

Unsere GitHub Dokumentation ist entsprechend dem Webertungsbogen der WRO Future Engineers Kategorie aufgebaut. Unter Punkt 1-5 sind die 
Informationen und das Material entsprechung der Bewertungskriterien vorhanden. 
Darunter under Punkt a-f findest man sonstige Sachen, die unsserer Meinung nach auch wichtig sind.


**Einleitung**

Wir sind Nico und Julian aus dem Saarland und nehmen dieses Jahr erneut für die Maximilian-Kolbe-Schule Wiebelskirchen an der WRO-Kategorie Future-Engineers teil. Im letzten Jahr haben wir bereits erfolgreich teilgenommen und den ersten Platz im Vorentscheid in Waldkirch/Freiburg belegt. Dadurch haben wir uns für das Deutschland-Finale in Chemnitz qualifiziert, wo wir den 4. Platz erreicht haben. Darüber hinaus haben wir bereits an vielen anderen Wettbewerben teilgenommen, darunter die "Robonight" in Saarbrücken, wo wir zweimal den zweiten Platz belegt haben, und die "make-it", wo wir den ersten Platz erreicht haben. Alles begann jedoch mit der WRO, bei der wir im Jahr 2019 in der Kategorie „Mission“ erstmals teilgenommen haben.


**Programmierung Eröffnungsrennen**

Beim diesjährigen Eröffnungsrennen verwenden wir die Grundidee vom letzten Jahr. Während der Fahrt misst der Roboter kontinuierlich die Werte der Ultraschallsensoren, die vorne, links und rechts angeordnet sind. Basierend auf den Werten des linken und rechten Sensors berechnet der Roboter den Mittelpunkt und steuert das autonome Auto proportional, um sich bestmöglich wieder in die Mitte zu bringen. Das bedeutet, je weiter das Auto von der Mitte entfernt ist, desto mehr lenkt es, um diese Mitte wieder zu erreichen.

Ein Beispiel: linker Ultraschallsensor: 10, rechter Ultraschallsensor: 50. Hier zeigt der linke Sensor eine sehr kurze Entfernung, was bedeutet, dass das Auto ziemlich weit links an der Bande ist. Wenn wir nun die Summe der beiden Werte nehmen, ergibt sich die Zahl 60. Die Hälfte davon ist 30. Wenn beide Sensoren nun den Wert 30 ausgeben, wissen wir, dass der Roboter genau in der Mitte ist. Um diese Mitte zu erreichen, berechnen wir den Prozentanteil und lenken entsprechend.

Da dieser Prozess sehr schnell und sehr oft wiederholt wird, kann es manchmal zu einem leichten Schwanken kommen, das das Auto aber ausgleicht. Um am Ende der 3 Runden perfekt zu stoppen, zählt das Auto eine Variable hoch, wenn es eine Kurve fährt. Wir erkennen eine Kurve, wenn plötzlich ein Sensor einen sehr hohen Wert misst. Wenn wir also wie im Beispiel eine Summe von 60 haben und einer der Sensoren plötzlich 150 misst, können wir sicher sein, dass wir uns in einer Kurve befinden. Wenn der Roboter dies 12-mal erkannt hat, bleibt das Auto im richtigen Abschnitt stehen.

**Programmierung Hindernisrennen**

Bei dem Hindernisrennen nutzen wir als Grundlage die Programmierung von dem Eröffnungsrenenn. Denn hier müssen wir ja auch autonom fahren. Nur wenn die Kamera hier einen bunten Stein erkennt, weichen wir aus. Bei roten Steinen rechtsrum, bei Grünen linksherum. Für die Farberkennung haben wir Filter/Masken, damit wir nur die Farben sehen und die sonstigen Fehler, die die Kamera erkennen könnte, ausblenden. Des Weiteren verändern wir die Belichtung des Bildes dynamisch je nach Umgebungshelligkeit, damit wir die Fraben besser erkennen können.


**Technische Komponenten**

Raspberry Pi 4
3x HC-SR04 Ultraschallsensoren
Motor
Motorsteuerung
18V Bosch Bohrmaschinen-Akku
Spannungswandler von 18V zu 5V
Knopf
Schalter
Led-Lampe
JumperKabel / sonstige Kabel
Pi-Cam
Verschiedene Widerstände
Servo-Motor (mg996r)


**Sonstige Komponenten**

Metall Grundplatte
Metall Schraubstützen
Selbst modellierte 3D-Modelle aus dem 3D-Drucker
Verschiedene Schrauben
Kabelbinder
Heißkleber / Sekundenkleber
Schrumpfschläuche
Platine für Ultraschallsensoren



Um eine Tabelle wie die beschriebene auf GitHub darzustellen, kannst du Markdown verwenden. GitHub unterstützt Markdown-Tabellen, die einfach formatiert und leicht lesbar sind. Hier ist die entsprechende Markdown-Syntax für die Tabelle, die du erstellen möchtest:

markdown
Code kopieren
# 🤖 Hardware 🤖

## ⚙️ Components ⚙️

| Name               | Product                              | Price |
|--------------------|--------------------------------------|-------|
| **RC Car**         | Carisma GT24                         | $263  |
| **RC Car Battery** | Gens Ace 1300mAh Battery            | $35   |
| **Drive Motor & ESC** | Furitek Komodo Motor + Lizard Pro ESC | $226  |
| **Turning Motor**  | Hitec HS-5055MG Servo Motor         | $38   |
| **Motor Mount**    | GT24 High Performance Alloy Motor Mount | $17 |
| **CSI Camera**     | SainSmart Wide Angle Fish-Eye Camera | $19   |
| **Raspberry Pi HAT** | HiWonder TurboPi HAT               | $61   |
| **Raspberry Pi**   | Vemico Raspberry Pi 4               | $176  |
| **Raspberry Pi Fan** | GeeekPi Fan                        | $19   |
| **ON/OFF Switch**  | DaierTek Switch                     | $13   |

**Total Car Cost:** $867 CAD

---

*3D printed parts were made with the BambuLab P1P*






# ⚙️ Hardware & Components ⚙️

| Category           | Component                               | Quantity | Price |
|--------------------|-----------------------------------------|----------|-------|
| **Computing**      | Raspberry Pi 4                          | 2        |       |
|                    | Arduino Nano                            | 1        |       |
|                    | Raspberry Pi 3                          | 1        |       |
| **Sensors**        | HC-SR04 Ultrasonic Sensor               | 3        |       |
| **Motors**         | Brushless Motor 12V                     | 1        |       |
|                    | Servo Motor (MG996R)                    | 1        |       |
| **Motor Control**  | Motor Controller (L298N)               | 1        |       |
| **Power**          | 18V Bosch Drill Battery                 | 1        |       |
|                    | Voltage Converter (18V to 5V)          | 1        |       |
| **Controls**       | Button                                 | 1        |       |
|                    | Switch                                 | 1        |       |
|                    | LED Lamps                              | 2        |       |
| **Connectivity**   | Jumper Wires / Other Cables            | Various  |       |
|                    | USB Webcam (Logitech Brio 500)         | 1        |       |

### 🛠️ Other Components:

- **Metal Baseplate**
- **Metal Standoffs**
- **Self-modeled 3D Prints from a 3D Printer**
- **Various Screws**
- **Cable Ties**
- **Hot Glue / Super Glue / Metal Glue**
- **Heat Shrink Tubing**

---

**Total Cost:** (Bitte hier Gesamtkosten eintragen)

*Hinweis: Einige der Komponenten sind 3D-gedruckt und selbst modelliert.*




# ⚙️ Hardware & Components ⚙️

| Quantity | Component                               | Price per Unit | Total Price | Product Link |
|----------|-----------------------------------------|----------------|-------------|--------------|
| 2        | [Raspberry Pi 4](#)                     | €X.XX          | €XX.XX      | [Link](#)    |
| 1        | [Arduino Nano](#)                       | €X.XX          | €X.XX       | [Link](#)    |
| 1        | [Raspberry Pi 3](#)                     | €X.XX          | €X.XX       | [Link](#)    |
| 3        | [HC-SR04 Ultrasonic Sensor](#)          | €X.XX          | €XX.XX      | [Link](#)    |
| 1        | [Brushless Motor 12V](#)                | €X.XX          | €X.XX       | [Link](#)    |
| 1        | [Servo Motor (MG996R)](#)               | €X.XX          | €X.XX       | [Link](#)    |
| 1        | [Motor Controller (L298N)](#)           | €X.XX          | €X.XX       | [Link](#)    |
| 1        | [18V Bosch Drill Battery](#)            | €X.XX          | €X.XX       | [Link](#)    |
| 1        | [Voltage Converter (18V to 5V)](#)      | €X.XX          | €X.XX       | [Link](#)    |
| 1        | [Button](#)                             | €X.XX          | €X.XX       | [Link](#)    |
| 1        | [Switch](#)                             | €X.XX          | €X.XX       | [Link](#)    |
| 2        | [LED Lamps](#)                          | €X.XX          | €XX.XX      | [Link](#)    |
| Various  | [Jumper Wires / Other Cables](#)        | €X.XX          | €X.XX       | [Link](#)    |
| 1        | [USB Webcam (Logitech Brio 500)](#)     | €X.XX          | €X.XX       | [Link](#)    |

### 🛠️ Other Components:

- **Metal Baseplate**
- **Metal Standoffs**
- **Self-modeled 3D Prints from a 3D Printer**
- **Various Screws**
- **Cable Ties**
- **Hot Glue / Super Glue / Metal Glue**
- **Heat Shrink Tubing**

---

**Total Cost:** €X.XX (Bitte hier Gesamtkosten eintragen)

*Hinweis: Einige der Komponenten sind 3D-gedruckt und selbst modelliert.*



# ⚙️ Hardware & Components ⚙️

| Quantity | Component                               | Price per Unit | Total Price |
|----------|-----------------------------------------|----------------|-------------|
| 2        | [Raspberry Pi 4]([https://www.google.com](https://www.amazon.com/-/de/dp/B0899VXM8F/ref=sr_1_1?__mk_de_DE=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=V8IYCBGA81XN&dib=eyJ2IjoiMSJ9.HObwdfV1ZrZREqhAOJnYQc4aw8BjV7yP7sbtUB4UMEyDqicDxVoBsPNVvoTwbNJAI2Zwr2Z6K1z9NvmkA37oCjCtzP857Q2QLKQGp_wTY_hH6tGgNLzkj_5H-RlEmm-k-EK0cRTkqHMQoI84eIgVCwdquUKrooxnL3WxWiuz2aV7Tn-Av0r_21uxY_7Myb3hE4Uq9huyvRydgHo-aVbBXVdjnVnZ91gtJM9EJCXVquA.Vu4ipiV5-XWeR7LO28GZZMkY3UhHBCaKtgzCKeIz4E0&dib_tag=se&keywords=raspberry+pi+4+8gb&qid=1731242848&sprefix=raspberry+pi+4+8gb%2Caps%2C406&sr=8-1)) | $86         | $172     |
| 1        | [Arduino Nano]([https://www.google.com](https://www.amazon.com/-/de/dp/B0DFGR288F/ref=sr_1_3?__mk_de_DE=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=173RZIX5A8Z84&dib=eyJ2IjoiMSJ9.FsAZZs88q_ax19rwGF0va21V-jlYApKcpL0-QvPR11N4-bvCjYD7ZLvS1NDfX_kGz_G0L07dERDxv6Yyd86oCnWAkLkSd6HeFWD3dv8RhqUVtwJUTx4UFLfWWZqOQwOVINK5jRn3R2ZxWmEmHMl-ElKsKjrHuAVcTHqpSvevTcyUMGihuZOpe6IjgMOTCWzM7egUnt0VwrXSyUiYje31VmQYr5wzunG_UVxyQXHDVBY.rRlj9LOORroxyDiJNxipLkRuaFAAMCAEVtZEWcoiIpc&dib_tag=se&keywords=arduino%2Bnano%2Beinzeln&qid=1731242972&sprefix=arduino%2Bnano%2Beinzeln%2Caps%2C274&sr=8-3&th=1))   | $8          | $8       |
| 1        | [Gyro Sensor]([https://www.google.com](https://www.amazon.com/-/de/dp/B07MMZ37PT/ref=sr_1_3?__mk_de_DE=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=3WZFQ2RB7VLV&dib=eyJ2IjoiMSJ9.rUh5dbWAJPoh1HRLZCAF2kTGURDiSs5rhCraBYpSl1fGjHj071QN20LucGBJIEps.iM1hcT_QZg9EvQy9JylDwWaGEVvMDDNlMDi_1RlZixk&dib_tag=se&keywords=gyro+sensor+mpu+911&qid=1731243053&sprefix=gyro+sensor+mpu+911%2Caps%2C428&sr=8-3)) | $5         | $5       |
| 1        | [Color Sensor]([https://www.google.com](https://www.amazon.com/-/de/dp/B087Z3K6P5/ref=sr_1_1?__mk_de_DE=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=2FRFQ5HGAN7O0&dib=eyJ2IjoiMSJ9.fhIWiUmX92C2IlJN20U8ehW8MdNcoAkqDs436CZOeu3JVspHcYen-8qqr1wmI7qsZTzEUXpXj4uH6RrWYNTbYokRn7mHC3eJOWbTwb_ten6iy46vQwpiM0zr8brUh2laWfIJVX4x3rU5wy1yO99wzGP2mbB-AEsdrAnrgFT0zUiUCfNyZM_xpIQ6k0K186LLJSYMYSE9CNBYieicwONA5sfH6Ckcm3k45j6tVfRHGdM.0ZpZce-0bTD3dIozf9aaXEjgdPOszdZ-LvZbPtGK6Tg&dib_tag=se&keywords=color+sensor+adafruit+tcs34725&qid=1731243156&sprefix=color+sensor+adafruit+tcs347%2Caps%2C361&sr=8-1)) | $4   | $4       |
| 3        | [HC-SR04 Ultrasonic Sensor]([https://www.google.com](https://www.amazon.com/-/de/dp/B0BDFLPZ2R/ref=sr_1_8?__mk_de_DE=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=1X0XJDGBGPTF&dib=eyJ2IjoiMSJ9.E2SIkElJhtFWCJCHL5Q6YwwtxyRhETnroFHfs4vAAJOe54iZNDm7z43wzn_pxu0iQsF42eVpl2-TVTK19t7z7d-ipIsgWMquhMOWScSy9SrOe_WA16Kx2P91cSd649mbSwzz3ncv9xQ5ypgvODgOm1k2JqhuLCNX9y459I4thPPytc_5V0ejWPtU7yEuoVWCh7aO7Be_N9cM3_lRrSE3DkQhdNGisjT0yZK35neD6xx1gCBKNIvgQrSnXZLCIPrVNMA61nLTgz0z0BBvqP_m5Ue7Tx_LhEJ3hVExsRiI6Kc.xFZ-7ctfAZs7K_xD7CwRVeROarpZJARSqLr4zJ4Fs40&dib_tag=se&keywords=hcsr04&qid=1731243242&sprefix=hcsr0%2Caps%2C286&sr=8-8&th=1)) | $4 | $12      |
| 1        | [Brushless Motor 12V]([https://www.google.com](https://www.amazon.com/-/de/dp/B07D297L9F/ref=sr_1_42?__mk_de_DE=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=222UOQ0MRUN0A&dib=eyJ2IjoiMSJ9.ovwz6I0biXFj-Q04wjL6Xqrypga2FIHpAWCkrIgr27r0Dff2wRMJCyV-aid47Scru_MTPw-AhAlBDuzHENDG2Ri2ggAJQYDqap1TzlG3_jMa0vtXmLGnqXvWnKL0WMydW9khXUh_z2ZdwFsOyHuWErx8ebqdpsHccOyecff_ZwfgeQmfWxeHoYV3EI5eraXg2TBIYUo5WQ1QWXGalz8wOANAoOSZ1R05J2rq6asl4P9ktpZmEUbBx6gwTEGJ2P_6PBNipyiz4AzZBXE9mDzPX3ZFq6P5qn71I2HBH1j7FjI.coMBC9eXf0oW2S2avvttdWPxoaRX4pWhIsh6fIKustk&dib_tag=se&keywords=12v%2Bmotor&qid=1731243416&sprefix=12v%2Bmoto%2Caps%2C295&sr=8-42&th=1)) | $14         | $14       |
| 1        | [Servo Motor (A81BHP)]([https://www.google.com](https://www.vgr-technology.de/p/agf-rc-servo-a81bhp-hochgeschwindigkeitslenkung-rc-servomotor-0-052-sec-23kg-programmierbar)) | $95        | $95       |
| 1        | [Servo Motor small]([https://www.google.com](https://www.amazon.com/-/de/dp/B0BKPL2Y21/ref=sr_1_24?__mk_de_DE=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=J32NA46BMFBR&dib=eyJ2IjoiMSJ9.gA6jP-aloj6JVxs6UyQ98cwqNUStpBzIWdi0EBTbPl_Y1Rs-cfjijhjkL59owBfu5nv1sw5rIEO21QGci34KMQ0dG0OB6ijufQLJQ3Jl8ezlq2xBy6tM45Pt6iOSy_6mVsigFJpgsBOhVYzF8-CHTjsbCKxCt4_fLA8gaDG-_4Jtswl7Z79xpvvlVuAm7EUCQyEURvF-mVbhNA0hdWC3loaEGLC_G0Qb1n1Atx6-FtePmbeZ6s8b_YVbxeFNsZskZK04g4FBLG2xtXZ4Oj-lM_WBqexj3Y0U8W-CJpjI5do.5EZwpQ7ocJpE0gGEAQpqR1ZK2IYDM6TD1yukaP8WabE&dib_tag=se&keywords=servo&qid=1731243482&sprefix=servo%2Bmg996r%2Caps%2C489&sr=8-24&th=1)) | $3        | $3       |
| 1        | [Motor Controller (L298N)]([https://www.google.com](https://www.amazon.com/-/de/dp/B0CR6BX5QL/ref=sr_1_4?__mk_de_DE=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=12X6B70XQJ1WZ&dib=eyJ2IjoiMSJ9.hK2FjV8Ukp8CCyVTI1seMp-tnBOvyzY3UC2hgErQrotpMv1PG9H2P2rp8weGgNYVRybCYrSyE3rY2yoMGUm9BWFPHaZ9Rv5SxW08K5fNdy5KhYNATbn6cdd6lWGVFuJuewibmOOBojydMnO1dpfEio5pDwujbHR7M8DQCV1j2xgmSLzTWZ7D28WAesnkMk0M_TDDggQAx6MaruoxR2cuDsrDl_gdBOYsfUEjxApmqb4.zzgBtyN6LtLeClzVX-2oKEs5UgCwnbtkjGTC3eTlNTE&dib_tag=se&keywords=L298N&qid=1731243707&sprefix=l298n%2Caps%2C649&sr=8-4)) | €X.XX      | €X.XX       |
| 1        | [18V Bosch Drill Battery]([https://www.google.com](https://www.bosch-professional.com/de/de/products/gba-18v-2-0ah-1600Z00036)) | $65      | $65       |
| 1        | [Voltage Converter (18V to 5V)]([[https://www.google.com](https://www.joy-it.net/de/products/SBC-Buck03](https://www.reichelt.de/de/de/entwicklerboards-spannungsregler-dc-dc-wandler-debo-dcdc-down-7-p333858.html?PROVID=2788&&r=1))) | $20   | $20       |
| 1        | [Button]([https://www.google.com](https://www.amazon.com/-/de/dp/B08SQHRRDH/ref=sr_1_2?__mk_de_DE=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=3OAYGVVZ2L0DB&dib=eyJ2IjoiMSJ9.s5xKaeD9LIj3IYNK6XcRHuyedaAqn2KJDWtt6Xx24u0OZZASUtmYWzooFpEeI2UrmxgMN2srpgkpw9oLww0VXTk35CYzOEzRSWJ-Z6V7nT5lr9iOH80eFMmP9SURIf-uBRyWx-wLRsCXT3gCEYN5Tm7j4CmN3Jd5CTgRbfuw-FV2m1jfXSJEewbxzPgl3qm4aVxabynC9rHBEkSk_ZaDZCf0KsKdnuNsVgY-abk-CUw.7ORhEtuMC1TjdKswdw45Nr5baOczWl1Nyh1i3TQ0qAM&dib_tag=se&keywords=raspberry%2Bpi%2Bbutton&qid=1731244081&sprefix=raspberry%2Bpi%2Bbutt%2Caps%2C361&sr=8-2&th=1))         | $2          | $2       |
| 1        | [Switch]([https://www.google.com](https://www.amazon.com/-/de/dp/B00004WLKC/ref=sr_1_4?__mk_de_DE=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=1HSOKXDBD3S0B&dib=eyJ2IjoiMSJ9.OzWtfhE7YQIhpon4bgZXiyV64ugKAYdKqs83Zbrccow-BsOA2kepbRbC427QoVER9czynD0Isdj1CMas_-S4iDB0MKJmasq2VMpFBT0BNLyrI5H_esfeqay2iTIxsIIt9A-71fZOs-uRIQ70fUnGS0uPQs28Hz7mFWVVgACqzOe2SlA7YJXayYna2BY9wR9pP7Gs0569SmF9ECjFCLLk5OA5bgn5L6PV-5F0VjxUcr0.JgL58QCt_zPHJkbyRUj6NrG1zOBjF-kV6SoleHHtOUQ&dib_tag=se&keywords=metal%2Bswitch%2Bsmall&qid=1731244134&sprefix=metall%2Bswitch%2Bsmall%2Caps%2C291&sr=8-4&th=1))         | $8          | $8       |
| 2        | [LED Lamps]([https://www.google.com](https://www.amazon.com/-/de/dp/B0BXKM8PN3/ref=sr_1_6?__mk_de_DE=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=37DXXCMD6DB7K&dib=eyJ2IjoiMSJ9.xpz902ZKSsJRxAO7IQkxDQ8jiLDRo9NqkTd2mKmaVLkeizezzALilK18UoAr2x7l4bwTG8_fGk0FrJrAqbqxdl97j08pfMGniRfgmBKNriKg6PHRHafEoXMUvo9RPBfd9uL5f9w03H0NHsxyjh5xUIGkQHEFz_5jl6t72cbl8zDEk_ZgNEl_GZi2AMF-srLO4goOGMhJzBfREMjYJk9J3mC_dQWxPL3ktXzZF97h4tU.5uPV4hTRWMLjn2hmSvopBocJtOvEqTFKMQpYzJavjfM&dib_tag=se&keywords=led+raspberry+pi&qid=1731244200&sprefix=led+raspberry+pi%2Caps%2C330&sr=8-6))      | $1          | $2      |
| Various  | [Jumper Wires / Other Cables]([https://www.google.com](https://www.amazon.com/-/de/dp/B01EV70C78/ref=sr_1_3?__mk_de_DE=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=2A54IVO4KIECV&dib=eyJ2IjoiMSJ9.tjHxIQLJsk16_0YVtUGN6dGzV2wHYrdA_LNt2EBckEg2xcbQMpJP-tZhKHEuWRR-MW4OEUzxcuhDJWmZwkqQIS1B8R4KD9VPknZsY7K80ef8j7pG0HtHMmLqeqU7-A3Xsv5YYc2QReX4JbUyhsl0Q5pEnLjNCOn6odp-5DuUfT3mG8HtShQf_jbzv7-HTr3zvCq-5_0rhPXqgLbhG9gjPLVPjci9S5ODpgwZ0-cLdX4.BJ1rVbT8hocV1kpTSv17AsJTxlT80S-MM0gOof1DPbk&dib_tag=se&keywords=raspberry%2Bpi%2Bjumper%2Bwires&qid=1731244240&sprefix=raspberry%2Bpi%2Bjumper%2Bwire%2Caps%2C330&sr=8-3&th=1)) | €X.XX    | €X.XX       |
| 1        | [USB Webcam (Logitech Brio 500)]([https://www.google.com](https://www.amazon.com/-/de/dp/B0CPBD3PDD/ref=sr_1_1?__mk_de_DE=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=7ZQNS66EJBUT&dib=eyJ2IjoiMSJ9.5JBAAXI2W2GAe0dnd2k3fzh8xG2w92PgrZLofe05k9R7C9J0SGVdJ1CrUPVsijePnceRI9-XwwjDsmvHAZZzooxrtw36UPSvf49IPpy-2MkuZ9_0KSDsF_znLFZdEqBWqxqaY7rmAhDMpHbEkrGqTjjyo1Lokoya4oQA4kxdzMHMJRWTdgsD7TwZ9tNo70xg0E9DpU7XZEwZSlVwdQHSABFXsXhOYJ3VAnVS-sYVYUI.o1jl4hsQ-5yH-51D6xdre10_dbS-6l_PN2ER7FN66pY&dib_tag=se&keywords=Logitech+Brio+500&qid=1731244276&sprefix=logitech+brio+500%2Caps%2C357&sr=8-1)) | $84   | $84       |

---

### 🛠️ Other Components:

| Component                             | Price   |
|---------------------------------------|---------|
| [Metal Baseplate / Chasi]([https://www.google.com](https://funduinoshop.com/diy-werkstatt/bausaetze/chassis/yfrobot-chassis-kit-mit-lenkachse))  | $50   |
| [Metal Standoffs]([https://www.google.com](https://www.amazon.com/-/de/dp/B06Y5TJXY1/ref=sr_1_1?__mk_de_DE=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=1DRWOS518Z1OI&dib=eyJ2IjoiMSJ9.4rGRj3Rhs7qbv27W1Pwo9Hwdc_9R5AEErgMUp4I2UhBZIAU3Yhpl8djU1ZK_abFb_UVIRTTjofxITB2sJf6Uqadtz2Fm3rATTG-kTpdQbs4-Fid0x8GTZfEdc-BceX9SNuuolijmh7x9Fj7aYA8yuclsxF5_hgMVhUwsnu8AoU0R1kQAReyBUMStQJAHMMiN9JFG6RAZuui7DDukJzoj4VDp3W8T_DC_1lTb6pJRi6tm5FSOtiYG41ZeZh7g_qYtzw9qInQNpPuCNFTpPK_3SzYLNxaReL6HbrY58iENVHM.PVKNc9v5kssJN2VK6X6aYyrHRJVF2UPkPCITnXmV_CE&dib_tag=se&keywords=metal%2Bstands%2Bm3&qid=1731244332&sprefix=metal%2Bstands%2Bm%2Caps%2C242&sr=8-1&th=1))  | $15   |
| [Self-modeled 3D Prints from a 3D Printer]([https://www.google.com](https://www.amazon.com/-/de/dp/B0D421Q2Q2/ref=sr_1_4?__mk_de_DE=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=1GPVONWTP36HM&dib=eyJ2IjoiMSJ9.MHelaoH7c41HZbj1LqWM6fZ8pcWt8eHClmSr37vZZGlrvEFkYIf7y1WqkWa5zzPYyDL_Kt85a_LGAeQrDS6w8J-PDSO7o61g08ElLA6biRkrS2s3lMJTr4iXXK766SGM3RM5SjOVMlt4naO3D5ouQzhVmnopYVvuUzEBAkowtykMKbI1ywCViYlDpxt9qXYLdsD1D2qJ0aihABtQtDZuG0kj11uh__zKAKcP2igJC7U.UHIe6RALVnZpCLJwDbNMs2CRN1mmfCdurHuUoqtVFRk&dib_tag=se&keywords=filament+1k&qid=1731244367&sprefix=filament+1k%2Caps%2C271&sr=8-4)) | $13   |
| [Various Screws]([https://www.google.com](https://www.amazon.com/-/de/dp/B0BMQFHDBH/ref=sr_1_3?__mk_de_DE=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=1L2JXKIISI5O7&dib=eyJ2IjoiMSJ9.YdekpzHmrUtAo9ohe8Hopjih0ebReTECCoWIsnPCAA5G-dXgu0pME28c0ENXkEmsYPZOiZ6Eaz_CshUspEXxC8BSvLcnZatdBYGMqby9VesFuNNAdpvWXN8qiPrA1pTZYvs4f0l97ynD5NOxQ9rOzkzKDymLbWuBxKOWEkHwJvDV6BFhbvegVQntyiI56OwAgS8k9UTa7UvXcg1mTp_OzjGeCtTZh7UcA9vtDUPJtec.LXp5KDD5IJCRROhLoNES8ZiktiekJbXya2nolaJ1z4w&dib_tag=se&keywords=screws+m3&qid=1731244397&sprefix=screws+m%2Caps%2C238&sr=8-3))    | &10   |
| [Cable Ties]([https://www.google.com](https://www.amazon.com/-/de/dp/B08TVLYB3Q/ref=sr_1_3?__mk_de_DE=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=W2C1NCCH5JFS&dib=eyJ2IjoiMSJ9.h9TpTr5-aOVSnYPMexRs1VE37_mN8eTM-h-qz9kALdK-4KrLdaYBLDO8TnsLhpLp3-Ceb8eBdxWjM5QB-lItbq5_KXsUYCCHLoZnsZECI1iW6c6zonadO40j-MJG023jrJektHdiSafgCtOQkxe75cSOdsr7RpxSxdgvo1Ybd-30EZtrJ6sKZ_Iq8kaRwNqFG2H_3f5j7CYn_VCgqEK98NWt5_jdy2zsi5La_eF8sXE.Sv785j23sR_vROWQOy4VNttKBzhHVtj28f_ooZmmtds&dib_tag=se&keywords=cable+Ties&qid=1731244433&sprefix=cable+ties%2Caps%2C315&sr=8-3))       | $5   |
| [Hot Glue / Super Glue / Metal Glue]([https://www.google.com](https://www.amazon.com/-/de/dp/B09XY1WDTX/ref=sr_1_1?__mk_de_DE=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=1KGRM2DAUH3LZ&dib=eyJ2IjoiMSJ9.RT2mM8ttSkNNPnKt75SYGSdQTARxdqkiJsze78kKXhN9xhIiXriH3q5YZ5ucBfAIJtsoKz92zEfzxBZmMHhhO8QlxQGZF-V9LPqb1Y3H4Qcr8SwIvVDlLt3IUu2HUpRrnE0aE8zzYo1aNkEikEBAGHUJldu71ZP2e8YNMRoxG3jBYic6VTOvxBfmuyyJWvDSXXh6oglXZONLuESBO0D8JMrV_NCdPj4yWgsIfu5VzE6Pa-1ncuOi9tU6vsits5NItLJS5KgVsJn2r3p-CpmCGQyCXI7Y5_Ky6KrmVccW8gA.u61LCuZTbI9ayVzK2OR1P3MvcXAXQrF8J_E8FVCys3g&dib_tag=se&keywords=Hot+Glue+%2F+Super+Glue+%2F+Metal+Glue&qid=1731244459&sprefix=hot+glue+%2F+super+glue+%2F+metal+glue%2Caps%2C392&sr=8-1)) | $10   |
| [Heat Shrink Tubing]([https://www.google.com](https://www.amazon.com/-/de/dp/B0BG6V4HV4/ref=sr_1_4?__mk_de_DE=%C3%85M%C3%85%C5%BD%C3%95%C3%91&dib=eyJ2IjoiMSJ9.cJ5517VLS3-3VE6l5W55xSWKGeE1051iEiqmAFc6h5Ym6dItU_Ai2hdfrkv8LRfoetRytJy_Ki-OuSWMYxwzPv_PurpErzRXLc3IDH_B3Oezqir4z9Pd8IfSly3fvRjq_sZGtaXiiNvWWOPAc07DWGKGCmsGZN7XDm-oRGm1roBRw19nwVj2NHJ32MQzHH1hvI90sHh_wGgFe40zxJNUwpbLnidHEPGP08MNI9Mv1gw.To9hz6PBoSlo2USUSiKCstSNHZBeA0dIzjlUc9NYCkA&dib_tag=se&keywords=Heat%2BShrink%2BTubing&qid=1731244505&sr=8-4&th=1)) | $5   | 

---

**Total Cost:** €X.XX (Bitte hier Gesamtkosten eintragen)

*Hinweis: Einige der Komponenten sind 3D-gedruckt und selbst modelliert.*

