## Code convention

### Langs
- Typescript (เป็นทุกคน)
- Golang (Primary lang, ตอนนี้ขาด Pair ที่ยังไม่เคยทำ)
- CSS (เป็นทุกคนแล้ว)
- Kotlin (Mike, Pair)
- Swift (Pair, Aim)
- Python (Mai, Oe, Tung)

## Package naming
- Yaml
  - Follow your project
- Environment variable naming
  - UPPER SNAKE CASE (ex. AUTH_KEY)
  - Optional add service name (ex. REEEED_AUTH_KEY)
  
- Typescript
    - folder name ต้องเป็น lowercase เช่น `reeeed-admin`
    - ตัวแปร เป็น camelcase เช่น `userId` `userApi`
      - ตัวย่อ ก็ต้องเป็น Camelcase ด้วย เช่น `endpointUrl`
    - Abstract naming
      - Interface ต้องขึ้นชื่อด้วย `ICreetable`
      - Class Capitalize เช่น `AdminConsole`, "Icream"
      - Type alias ขึ้นด้วย T เช่น `TPaginationProps`
      - or Type alias แบบไม่มี T เช่น `PaginationProps`
    - method naming
      - camel case naming เช่น `getUserById`
      - public, private, protected จะใส่ strictly
      - method ที่จะ return collection
        - ใช้ keyword list `เช่น getPaymentList`
        - ใช้ keyword plural `เช่น getPayments`
        - ใช้ keyword list of `เช่น getListOfPayment`
        - ใช้ keyword list `เช่น find`
      - method ที่จะ get 1 data
        - `getPayment`
        - `findOne`
        - `find + entityName` ex. `findPayment`
      - filter on collection
        - ใช้ argument filter
        - ใช้ by ตามด้วยชื่อที่ต้องการ filter ex. `findPaymentByUsername`, `getPaymentsByCompany`
      - method ที่จะใช้สร้าง entity
        - สร้างเข้า database จะใช้ keyword คำว่า `create`
        - สร้างเข้า database หลาย entities ใช้ keyword ว่า `createMany`
      - soft delete ใช้ `remove`
      - hard delete ใช้ `delete`
      - class constructor สร้าง object ขึ้นมาใหม่ `new` ex. new Author({})
      - method ที่จะใช้ update entity ใช้ keyword `update` ( ถ้ามี upsert จะใช้ upsert ตรงๆ )
          ให้ใช้ id อย่างเดียวเท่านั้นห้าม upsert โดย unique key อื่น ex. upsert(doc: { id: "", name: "" })
   
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
    - ให้ encapsulate struct ให้ Export ไปแค่ interface เท่านั้น (แต่พวก Entity ไม่ต้อง)
      ex. NewAuthorRepository(...) => interface AuthorRepository
  
  - CSS
    - tailwind for utility
    - naming BEM `ex. btn--is-active btn__label btn__label--hover`
    - StyledComponent / SCSS
  
  - UI Framework
    - Ant
    - Blueprint
    
  - Component Framwork
    - ไปหามา แล้วมาใส่ด้วย
    
  - Swift
    - ใช้ Swift Gen สำหรับ asset ex. string รูป สี คำ i81n
