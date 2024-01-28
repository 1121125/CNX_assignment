# CnxDevSoft_Junior_Frontend_Test

## Answer for each Question

### 1.

- เว็บ หรือ โมบายแอบพิเคชั่น มีโครงสร้างที่ประกอบด้วยส่วนของ frontend และ backend ที่ทำงานร่วมกัน โดย frontend คือส่วนที่ใช้สำหรับเชื่อมต่อกับ ผู้ใช้งาน ให้ผู้ใช้งานสามารถมองเห็นและโต้ตอบกับเว็บของเราได้ และ frontend จะติดต่อกับ backend โดยผ่าน HTTP requests ในส่วนของ backend จะใช้ในการจัดการรีเควสต่างๆที่ถูกส่งเข้ามา เช่นการขอ แก้ไข ลบ ข้อมูลใน database server ส่วน file server จะจัดการเรื่องของไฟล์ต่างๆ และ internet จะเป็นส่วนอำนวยความสะดวกในการทำให้ frontend และ backend สือสารกันได้ถึงแม้ว่าทั้งสองส่วนจะอยู่กันคนละที่ก็ตาม

### 2.

- Bootstrap Frameworks
  คือ หนึ่งใน frontend framework ที่ช่วนสร้างหน้าเว็บได้ง่ายขึ้น ด้วยระบบต่างๆ เช่น การจัดการ layout ที่รองรับแบบ responsive หรือจะเป็น component สำเร็จรูป ทำให้เราไม่ต้องมานั่งสร้างเอง

  #### Example

  HTML

  ```html
  <button class="btn btn-primary">Bootstrap Button</button>
  ```

- การออกแบบ css ด้วย BEM
  BEM หรือ Block Element Modifier คือมาตราฐานรูปแบบในการจัดการส่วนต่างๆบนหน้าเว็บไชต์ โดยจะมองส่วนต่างๆเป็น block(ส่วนที่ครอบ element ย่อยๆ),element(html element ต่างๆที่อยู่ภายใน block) และ modifier(ส่วนที่มีหน้าตาคล้ายกัน แตกต่างกันเล็กน้อย)
  โดนการเขียน selector จะเขียนผ่าน class ทั้งหมด และจะใช้ \_\_ คั่นระหว่าง block และ element เช่น header\_\_logo,header\_\_menu และใช้ -- ใส่หน้า modifier เช่น header\_\_menu--top,header\_\_menu--buttom

  #### Example

  CSS
  .button {
  display: inline-block;
  padding: 10px 20px;
  background-color: #007bff;
  color: #fff;
  text-decoration: none;
  }

  .button--large {
  font-size: 18px;
  }

  HTML
  <a href="#" class="button">BEM Button</a>
  <a href="#" class="button button--large">BEM Large Button</a>

- การใช้ #id
  การอ้างอิงถึงelement id ใดๆนั้น ใน css จะใช้ สัญญลักษณ์ # แล้วตามด้วยชื่อ id ที่ต้องการระบุถึง โดยชื่อตัวแรกต้องเป็น a-z ห้ามเป็นสัญญลักษณ์หรือตัวเลข และในแต่ละชื่อจะเป็นแบบ case insensitive โดยใน 1 หน้าเว็บ id ที่ถูกตั่งขึ้นมาจะสามารถใช้ได้เพียงครั้งเดียวเท่านั้น และ 1 tag จะมีได้เพียง 1 ไอดีเท่านั้น โดยระดับควมสำคัญนั้น การใช้ id จะสูงกว่า class

  #### Example

  CSS
  #submit {
  background-color: green;
  }

  HTML
  <button id="submit">Submit</button>

- การใช้ .class
  คล้ายกับ id ต่างกันตรงที่จะใช้ สัญญลักษณ์ . ในส่วนของการใช้งานที่หน้าเว็บ 1 หน้าเว็บจะสามารถเรียกใช้ได้หลายครั้ง และใน 1 tag สามารถมีหลาย class ได้

  #### Example

  CSS
  .submit {
  background-color: green;
  }

  HTML
  <button class="submit">Submit</button>

- AJAX
  คือ Asynchronous JavaScript และ XML เป็นเทคนิคการสร้างเว็บแอปพลิเคชันสามารถตอบสนองต่อ การโต้ตอบของผู้ใช้งานได้รวดเร็วขึ้น เช่น เมื่อพวกเขากดส่งหรือแลกเปลี่ยนข้อมูลอะไรบางอย่างกับเชิร์ฟเวอร์ จะทำให้เกิดการใช้เวลาส่วนหนึ่งในการทำงาน ทำให้ขัดจังหวะผู้ใช้งานได้ โดย AJAX จะสามารถส่งและรับข้อมูลในพื้นหลัง เพื่อให้มีการรีเฟรชหน้าเว็บเฉพาะเพียงส่วนย่อยๆ เท่าที่จำเป็นเท่านั้น โดยไม่จำเป็นต้องมารอโหลดเว็บเพจใหม่ทั้งหมด

  #### Example

  HTML
  <html>
  <head>
  ....
  </head>
  <body>
  <div id="ajaxResult"></div>
  <script>
    fetch('https://jsonplaceholder.typicode.com/todos/1')
      .then(response => response.json())
      .then(data => {
        document.getElementById('ajaxResult').innerText = `Ajax Result: ${JSON.stringify(data)}`;
      });
  </script>
  </body>
  </html>

- Console
  คือเครื่องมือตัวหนึ่งที่ใช้สำหรับ log,debug,test javascript code โดยจะแสดง ข้อมูล,ข้อผิดพลาด หรือคำเตือน ต่างๆ ที่เกิดจากการทำงานใน code ของเรา
- Debugger
  คือ เครื่องมือหนึ่งที่ใช้ในการค้นหาและแก้ไขข้อบกพร่องหรือปัญหาในโค้ดของเรา ผู้พัฒนาสามารถหยุดการทำงานชั่วคราว(Breakpoint) เพื่อเช็คสภานะของตัวแปรต่างๆได้ ในจังหวะนั้นๆ หรือสามารถอ่านโค้ดทีละบรรทัดหรือทีละคำสั่งได้ ซึ่งช่วยระบุสาเหตุของปัญหา และอำนวยความสะดวกในการดีบักและเพิ่มประสิทธิภาพของโค้ด

### 3.

To run this project

```bash
git clone https://github.com/1121125/web_restaurant_react.git
```

```bash
pnpm install
```

```bash
pnpm dev
```

I also deploy this project on [Na-Udon](https://na-udon.vercel.app/)
Please be aware that there might be a slight delay during the initial visit as the database server may need some time to wake up. We appreciate your patience and understanding.
