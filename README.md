## ฐานข้อมูล จังหวัด อำเภอ ตำบล ละติจูด ลองจิจูด
ข้อมูลจาก Open Government Data [data.go.th]( https://data.go.th)

[ข้อมูลพิกัด LAT/LONG ที่ตั้งตำบล]( https://data.go.th/DatasetDetail.aspx?id=c6d42e1b-3219-47e1-b6b7-dfe914f27910)

### โดย
# [codesanook page](https://www.facebook.com/codesanookpage)

# [codesanook.com](http://codesanook.com)

* ปรับปรุงความถูกต้องของข้อมูลที่ซ้ำกัน
* ปรับข้อมูลให้อยู่ในรูปแบบ relational database
* เพิ่ม Foreign key
* Indexing
* Unique constraint
* Rename column
* Surrogate Id

# How to use it/การใช้งาน

* connect to your database
* execute **thai-administrative-division-full-my-sql.sql** for MySQL database
* execute **thai-administrative-division-full-sql-server.sql** for SQL Server database

# database diagram
![thai-administrative-division-province-district-subdistrict-sqld-iagram](https://raw.githubusercontent.com/aaronamm/thai-administrative-division-province-district-subdistrict-sql/master/tables-relationship-diagram.png)

# database dictionary

# ความถูกต้องของข้อมูล

ฐานข้อมูลมีจำนวนข้อมูลดังนี้
* จำนวนจังหวัด 77 จังหวัด
* จำนวนอำเภอ 928 อำเภอ
* จำนวนตำบล 7,364 ตำบล
* จำนวนเลขรหัสไปรษณีย์ของแต่ละตำบล 7,348 จำนวน (มีบางตำบลไม่มีรหัสไปรษณีย์ ฐานข้อมูลขาดข้อมูลส่วนนี้ไป)

### SQL statement to verify number of row
```
SELECT COUNT(Id) FROM Provinces;
SELECT COUNT(Id) FROM Districts;
SELECT COUNT(Id) FROM Subdistricts;
SELECT COUNT(Id) FROM Subdistricts WHERE ZipCode IS NOT NULL;
```
*หากข้อมูลส่วนใดไม่ถูกต้อง ต้องการให้แก้ไข สามารถสร้าง PR หรือติดต่อมาที่ facebook page codesanook.com  ได้เลยครับ*

# [codesanook page](https://www.facebook.com/codesanookpage)

# [codesanook.com](http://codesanook.com)


# ความถูกต้องของข้อมูล
* ข้อมูลบางส่วนไม่ได้ update เป็นล่าสุด เช่น ตำบล รหัสไปรษณีย์
* ข้อมูลละติจูด ลองจิจูดไม่แม่นยำสำหรับพื้นที่ตำบลที่เป็นเกาะ เพราะต้องใช้ข้อมูลหลายจุด ไม่สามารถใช้ข้อมูลจุดเดียวได้ จะปรับปรุงในอนาคต
* ความถูกต้องของข้อมูลจะได้รับการปรับปรุงเมื่อพัฒนาเป็นระบบเป็น web application ที่ทุกคนสามารถเข้าไปร่วมแก้ไข และช่วยกันตรวจสอบความถูกต้อง


# Credit & Thank you

* [ข้อมูลพิกัด LAT/LONG ที่ตั้งตำบล](https://data.go.th/DatasetDetail.aspx?id=c6d42e1b-3219-47e1-b6b7-dfe914f27910)
จาก Open Government Data [data.go.th]( https://data.go.th)

* ข้อมูลรหัสไปรษณีย์จาก [http://thai-db-download.blogspot.com/] (http://thai-db-download.blogspot.com/2015/02/sql-77-full-version.html)
* [อาจารย์เอนก กนกอภิวัฒน์](https://www.facebook.com/anekpage)
* [Taipan Prasithpongchai](https://www.facebook.com/dewnoibkk)


# useful information

## index and key naming convention
* If Index is **Primary** Clustered Index, use **PK_TableName**
* If Index is **Non-clustered** Index, use **IX_TableName_ColumnName1_ColumnName2…**
* If Index is **Unique** Non-clustered Index, use **UX_TableName_ColumnName1_ColumnName2…** (unique key should be index)
* If **Foreign key** : **FK_TableName_ColumnName1_ColumnName2…** (Use IX.. if you want to create index for this foreign key)

* credit https://blog.sqlauthority.com/2012/05/21/sql-server-renaming-index-index-naming-conventions/





# TO DO
- [x] SQL script for SQL server
- [x] SQL script for MySQL
- [x] zip code
- [ ] CodeSanook Module
- [ ] allow to edit correctness/approve
- [ ] Export to multiple types of RDMS with NHibernate e.g.
- [ ] SQL Server
- [ ] MySQL
- [ ] Oracle
- [ ] SQLite
- [ ] SQL Server Compact
- [ ] PostgreSQL
