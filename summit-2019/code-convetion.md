## Code convention
- Typescript (เป็นทุกคน)
- Golang (Primary lang, ตอนนี้ขาด Pair ที่ยังไม่เคยทำ)
- CSS ( เป็นทุกคนแล้ว )
- Kotlin (Mike, Pair)
- Swift (Pair, Aim)

## Package naming
- Environment variable naming
  - ให้ใส่ชื่อ service ข้างน้าก่อนด้วยเช่น `REEEED_PORT`
- Typescript
    - folder name ต้องเป้น lowercase เช่น `reeeed-admin`
    - ตัวแปร เป็น camelcase เช่น `userId` `userApi`
      - ตัวย่อ ก็ต้องเป็น Camelcase ด้วย เช่น `endpointUrl`
    - Abstract naming
      - Interface ต้องขึ้นชื่อด้วย `ICreetable`
      - Class Capitalize เช่น `AdminConsole`, "Icream"
      - Type alias ขึ้นด้วย T เช่น `TPaginationPropTypes`
    - method naming
      - camel case naming เช่น `getUserById`
      - public, private, protected จะใส่ strictly
      - method ที่จะ return collection
        - จะใช้ keyword list `เช่น getPaymentList`
      - method ที่จะ get 1 data
        - จะใช้ get เช่น `getPayment`
      - method ที่จะใช้สร้าง entity
        - สร้างเข้า database จะใช้ keyword คำว่า `create`
        - factory function สร้าง object ขึ้นมาใหม่ `new`
      - method ที่จะใช้ update entity ใช้ keyword `update` ( ถ้ามี upsert จะใช้ upsert ตรงๆ )
      - delete ก็ใช้ delete เลย
   
   
 - Golang
    - folder name underscore + lower case เช่น `external_database`
    - package name ใช้คำเต็ม เช่น `database` , `luna_entity`
    - ชื่อ folder กับ ชื่อ package ไม่ต้องตรงกันก็ได้
    - ตัวแปร
      - camelmase case
      - Enum ให้ใช้ Uppercase
      - convention ของการ ตั้งชื่อตัวย่อ Id , Url
    - Abstract
      - Interface จะต้องไม่มี Interface ข้างหลัง
        - ให้ใช้ `er` suffix เช่น `Stringer`, `XmlMarshaler` ( ไม่บังคับ )
    - method naming เหมือน Typescript
   
     
