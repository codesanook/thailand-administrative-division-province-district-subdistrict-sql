## ฐานข้อมูล จังหวัด อำเภอ ตำบล ละติจูด ลองจิจูด
ข้อมูลจาก Open Government Data [data.go.th]( https://data.go.th) 

[ข้อมูลพิกัด LAT/LONG ที่ตั้งตำบล]( https://data.go.th/DatasetDetail.aspx?id=c6d42e1b-3219-47e1-b6b7-dfe914f27910)

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
![thai-administrative-division-province-district-subdistrict-sqld-iagram](https://raw.githubusercontent.com/aaronamm/thai-administrative-division-province-district-subdistrict-sql/master/table-relationship-diagram.png)

# ความถูกต้องของข้อมูล

ฐานข้อมูลมีจำนวนข้อมูลดังนี้
* จำนวนจังหวัด 77 จังหวัด
* จำนวนอำเภอ 928 อำเภอ
* จำนวนตำบล 7364 ตำบล

### SQL statement to verify number of row 
```
select count(id) from provinces;
select count(id) from districts;
select count(id) from subdistricts;
```
*หากข้อมูลส่วนใดไม่ถูกต้อง ต้องการให้แก้ไข สามารถสร้าง PR หรือติดต่อมาที่ facebook page codesanook.com  ได้เลยครับ*

## [codesanook page](https://www.facebook.com/codesanookpage/)


# Credit

* [ข้อมูลพิกัด LAT/LONG ที่ตั้งตำบล](https://data.go.th/DatasetDetail.aspx?id=c6d42e1b-3219-47e1-b6b7-dfe914f27910) 
จาก Open Government Data [data.go.th]( https://data.go.th) 
* [อาจารย์เอนก กนกอภิวัฒน์](https://www.facebook.com/anekpage)
* [Taipan Prasithpongchai](https://www.facebook.com/dewnoibkk)
