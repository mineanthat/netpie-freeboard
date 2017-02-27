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

โดยพื้นฐานของการใช้งาน **Widget** ใน Freeboard นั้นก็คือ Javascript
ตัวอย่างการใช้งาน
- **Text**

![netpie-freeboard4](https://raw.githubusercontent.com/mineanthat/netpie-freeboard/master/docs/public/images/textWidget.PNG)
![netpie-freeboard5](https://raw.githubusercontent.com/mineanthat/netpie-freeboard/master/docs/public/images/textWidgetShow.PNG)

- **Gauge**

![netpie-freeboard10](https://raw.githubusercontent.com/mineanthat/netpie-freeboard/master/docs/public/images/gaugeWidget.PNG)
![netpie-freeboard11](https://raw.githubusercontent.com/mineanthat/netpie-freeboard/master/docs/public/images/gaugeWidgetShow.PNG)

- **Button**

![netpie-freeboard6](https://raw.githubusercontent.com/mineanthat/netpie-freeboard/master/docs/public/images/buttonWidget.PNG)
![netpie-freeboard7](https://raw.githubusercontent.com/mineanthat/netpie-freeboard/master/docs/public/images/buttonWidget2.PNG)
![netpie-freeboard8](https://raw.githubusercontent.com/mineanthat/netpie-freeboard/master/docs/public/images/buttonWidget3.PNG)
![netpie-freeboard9](https://raw.githubusercontent.com/mineanthat/netpie-freeboard/master/docs/public/images/buttonWidgetShow.PNG)

