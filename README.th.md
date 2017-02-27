netpie-freeboard
==========

Freeboard ที่มาพร้อม NETPIE datasource and widget plugins

![netpie-freeboard-screenshot](https://lh6.googleusercontent.com/F-kQRuaLNUjUkZ_Ktc5nSrcxW43ld1_GwXAuf94CaTXt0tOOfpTplQeCk2lYPZtrNcuFypcTnsaCYrc=w1920-h950-rw)


วิธีติดตั้ง

git clone https://github.com/netpieio/netpie-freeboard

การใช้งาน ใช้ browser เปิดไฟล์ index.html  ในส่วนของ DATASOURCES คลิก ADD เลือก TYPE เป็น NETPIE Microgear ปรับแต่งค่าตามความเหมาะสม

- **NAME** - ชื่อของ datasource ซึ่งแต่ละ NETPIE microgear datasource จะมี microgear object ที่เข้าถึงจาก script ได้ทาง microgear[*NAME*]  นอกจากนั้น ชื่อนี้ยังใช้เป็น microgear device alias ที่ device อื่นสามารถ chat มาหาได้ 
- **APP ID** - App ID ของ NETPIE
- **KEY** - Key ของ microgear
- **SECRET - Secret** ของ key ข้างต้น
- **SUBSCRIBE TOPICS** - เป็น topic ที่จะให้ datasource นี้ subscribe หากมีหลาย topic ให้ใช้ comma คั่น สามารถใช้ wildcard # และ + ได้ ค่าปกติจะเป็น /# คือ subscribe ทุก topic ของ App ID นี้
- **ONCONNECTED ACTION** - เป็นการกำหนดการกระทำเริ่มต้นเมื่อ Freeboard เริ่มต้นทำงาน

![netpie-freeboard2](https://lh5.googleusercontent.com/vKpwQgVmUadXc65kJkPtSweA0_Xc_rH5_93ge2vjoMNQZiljDIoK4Lt41_3RXGHROlHoPi2twlC7H50=w1920-h950-rw)


จุดประสงค์หลักของการใช้งาน Freeboard **เพื่อสะดวกในการสร้างหน้าตาควบคุมหรือแสดงผลอย่างเรียบง่าย**
ซึ่งตัว Freeboard นี้เป็นเว็บไซต์ที่ประกอบไปด้วยเครื่องมืออำนวยความสะดวก ซึ่งในที่นี้ก็คือ **Widget**
