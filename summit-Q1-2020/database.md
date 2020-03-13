# Database analysis


## Relational database
### Migration
- เราจะไม่ใช้ ORM ในการ สร้าง schema เราจะเขียน SQL script เพื่อ initial database ไปเลย
- Update script จะใช้ tools ในการทำ diff
- Object relation mapping จะใช้เฉพาะใน code Create, Update, Delete, List

### Mongo
- เหมาะสำหรับ project ที่ขึ้นใหม่ที่ schema ยังไม่นิ่ง
- transaction ไม่แน่ใจว่า ok รึเปล่า
- Easy to scale

### Postgres
- transaction ดีมากๆ
- performance ดีกว่า mongodb
- Horizon Scale is too hard

### สรุป
- เลือกตาม Project ไป
