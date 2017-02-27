netpie-freeboard
==========

Freeboard ที่มาพร้อม NETPIE datasource and widget plugins

![netpie-freeboard-screenshot](https://raw.githubusercontent.com/mineanthat/netpie-freeboard/master/docs/public/images/overview.PNG)


วิธีติดตั้ง

git clone https://github.com/netpieio/netpie-freeboard

การใช้งาน ใช้ browser เปิดไฟล์ index.html  ในส่วนของ DATASOURCES คลิก ADD เลือก TYPE เป็น NETPIE Microgear ปรับแต่งค่าตามความเหมาะสม

- **NAME** - ชื่อของ datasource ซึ่งแต่ละ NETPIE microgear datasource จะมี microgear object ที่เข้าถึงจาก script ได้ทาง microgear[*NAME*]  นอกจากนั้น ชื่อนี้ยังใช้เป็น microgear device alias ที่ device อื่นสามารถ chat มาหาได้ 
- **APP ID** - App ID ของ NETPIE
- **KEY** - Key ของ microgear
- **SECRET - Secret** ของ key ข้างต้น
- **SUBSCRIBE TOPICS** - เป็น topic ที่จะให้ datasource นี้ subscribe หากมีหลาย topic ให้ใช้ comma คั่น สามารถใช้ wildcard # และ + ได้ ค่าปกติจะเป็น /# คือ subscribe ทุก topic ของ App ID นี้
- **ONCONNECTED ACTION** - เป็นการกำหนดการกระทำเริ่มต้นเมื่อ Freeboard เริ่มต้นทำงาน

![netpie-freeboard2](https://raw.githubusercontent.com/mineanthat/netpie-freeboard/master/docs/public/images/addDatasource.PNG)


จุดประสงค์หลักของการใช้งาน Freeboard **เพื่อสะดวกในการสร้างหน้าตาควบคุมหรือแสดงผลอย่างเรียบง่าย**
ซึ่งตัว Freeboard นี้เป็นเว็บไซต์ที่ประกอบไปด้วยเครื่องมืออำนวยความสะดวก นั่นก็คือ **Widget**

![netpie-freeboard3](https://raw.githubusercontent.com/mineanthat/netpie-freeboard/master/docs/public/images/showWidget.png)

โดยพื้นฐานของการใช้งาน **Widget** ใน Freeboard นั่นก็คือ Javascript
ตัวอย่างการใช้งาน จะมีอยู่ 2 อย่างก็คือการแสดงค่าและการส่งค่า

การแสดงค่านั้นเราจะนำค่าออกมาแสดงโดยการใช้
>> datasources["ชื่อของ Datasource"]["ที่อยู่ของข้อมูลที่เราต้องการ (topic หรือ alias) "]

ข้างต้นนี้เป็นข้อมูลหนึ่งตัว นั่นคือเราสามารถนำไปประยุกต์ได้ดังนี้
- **Text** เป็นการแสดงค่ามาในรูปแบบของข้อความ

![netpie-freeboard4](https://raw.githubusercontent.com/mineanthat/netpie-freeboard/master/docs/public/images/textWidget.PNG)

>> datasources["GameBlackJack"]["/GameBlackJack/player1/point"]

ชื่อ Datasource คือ GameBlackJack
และข้อความที่แสดงมาจาก Topic player1/point

![netpie-freeboard5](https://raw.githubusercontent.com/mineanthat/netpie-freeboard/master/docs/public/images/textWidgetShow.PNG)

- **Gauge** เป็นการแสดงค่าออกมาในรูปแบบของเกจ

![netpie-freeboard10](https://raw.githubusercontent.com/mineanthat/netpie-freeboard/master/docs/public/images/gaugeWidget.PNG)

>> datasources["GameBlackJack"]["/GameBlackJack/player1/lifepoint"]

ชื่อ Datasource คือ GameBlackJack
และข้อความที่แสดงมาจาก Topic player1/lifepoint

![netpie-freeboard11](https://raw.githubusercontent.com/mineanthat/netpie-freeboard/master/docs/public/images/gaugeWidgetShow.PNG)

- **Indicator Light** 

![netpie-freeboard12](https://raw.githubusercontent.com/mineanthat/netpie-freeboard/master/docs/public/images/indicatorLightWidget.PNG)

>> datasources["GameBlackJack"]["/GameBlackJack/startgame"] == "start"

เป็นการนำข้อมูลที่ได้มาประยุกต์ใช้ โดยหากข้อมูลที่ได้คือ start จะทำให้ไฟติด

![netpie-freeboard13](https://raw.githubusercontent.com/mineanthat/netpie-freeboard/master/docs/public/images/indicatorLightWidgetshow.PNG)

- **Button** เป็นปุ่มกดเพื่อนำส่งค่าออกไป

รูปแบบการส่งจะมีอยู่ 2 รูปแบบคือ chat และ publish 
โดย chat จะส่งตรงไปที่ alias และ publish จะส่งผ่านทาง topic

**การส่งแบบ chat**
>> Microgear["ชื่อของ Datasource"].chat("ชื่อ alias", ข้อความที่ต้องการส่ง)

**การส่งแบบ publish**
>> Microgear["ชื่อของ Datasource].publish("topic", ข้อความที่ต้องการส่ง)

![netpie-freeboard6](https://raw.githubusercontent.com/mineanthat/netpie-freeboard/master/docs/public/images/buttonWidget.PNG)

>> Microgear["GameBlackJack"].publish("/player1/status","hit")

![netpie-freeboard7](https://raw.githubusercontent.com/mineanthat/netpie-freeboard/master/docs/public/images/buttonWidget2.PNG)

>> Microgear["GameBlackJack"].publish("/player1/status","stand")

![netpie-freeboard8](https://raw.githubusercontent.com/mineanthat/netpie-freeboard/master/docs/public/images/buttonWidget3.PNG)

>> microgear["GameBlackJack"].publish("/startgame","start")

![netpie-freeboard9](https://raw.githubusercontent.com/mineanthat/netpie-freeboard/master/docs/public/images/buttonWidgetShow.PNG)

