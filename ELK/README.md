## ขั้นตอนการใช้งานสำหรับ import เข้า Elasticsearch ด้วย Logstash

### 1. ทำการสร้าง index ชื่อว่า thai
โดยมี type ชื่อว่า doc และกำหนด field location ให้มีชนิดเป็น geo_point

```
PUT thai
{
  "mappings": {
    "doc": {
      "properties": {
        "location": {
          "type": "geo_point"
        }
      }
    }
  }
}
```

### 2. ทำการ import ด้วย Logstash

```
$logstash -f thai.conf
```

จากนั้นทำการตรวขสอบจำนวนข้อมูล

```
{
  "count": 7767,
  "_shards": {
    "total": 5,
    "successful": 5,
    "skipped": 0,
    "failed": 0
  }
}
```
