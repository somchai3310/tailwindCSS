# Tailwind CSS 3.x
v3.4.3

> _NOTE:_  
> CSS framework

# Run project
- npm i
- npm run build
- live server


ลดเวลาการออกแบบเว็บ
Utility-First CSS Framework
สามารถปรับแต่ง class ย่อยๆ 

Tailwind Directives
@tailwind base; //จัดการ Element (Tag)
@tailwind components; //จัดการ class
@tailwind utilities;  //ปรับแต่ง class

การติดตั้ง CLI 
https://tailwindcss.com/docs/installation

การเพิ่ม script ใน package.json
ใช้ npm run build แทนคำสั่ง npx tailwindcss -i ./src/input.css -o ./src/output.css --watch

"scripts": {
    "build": "npx tailwindcss -i ./src/input.css -o ./src/output.css --watch"
  }

กำหนดสีพื้นหลัง Background
class:
bg-ชื่อสี-ความเข้มสี
Eg.
bg-red-300
bg-yellow-900

## จัดการข้อความ Typography
- สีข้อความ color
- ขนาดข้อความ size
- รูปแบบข้อความ style
- ความหนาข้อความ weight
- ตำแหน่งข้อความ alignment

### สีข้อความ Text Color
class:
text-ชื่อสี-ความเข้มสี
Eg.
text-red-300
text-yellow-900

### ขนาดข้อความ Font size
class:
text-รูปแบบ
Eg.
text-xs
text-sm
text-base
text-lg
text-xl
text-2xl->9xl

### รูปแบบข้อความ style
font-italic ตัวเอียง
uppercase ตัวพิมใหญ่
lowercase ตัวพิมเล็ก
capitalize ตัวแรกพิมใหญ่

### ความหนาข้อความ weight
class: 
font-รูปแบบ
Eg.
font-thin  font-normal  font-bold
https://tailwindcss.com/docs/font-weight

### ตำแหน่งข้อความ alignment
text-center
text-right
text-left

### ความโปร่งใส opacity
class:
text-opacity-ค่าความโปร่งใส(0-100)
text-opacity-0
text-opacity-50
text-opacity-100

### ความกว้างและความสูง
w -> width
h -> height
https://tailwindcss.com/docs/width
https://tailwindcss.com/docs/height

### margin padding
m       p
m{t,r,b,l}-{size}
t top
b bottom
l left
r right
mx-{size}
my-{size}
m-{size}

## จัดการเส้นขอบ Border
- ขนาดเส้นขอบ border width
- สีเส้นขอบ border color
- ความโค้งเส้นขอบ border radius
- รูปแบบเส้นขอบ border style

### ขนาดเส้นขอบ border width
class:
border-size
border-{t|r|b|l}-size
https://tailwindcss.com/docs/border-width

### สีเส้นขอบ border color
class:
border-ชื่อสี-ความเข้มสี
https://tailwindcss.com/docs/border-color

### ความโค้งเส้นขอบ border radius
rounded
rounded-sm
rounded-md
rounded-lg
rounded-2xl
rounded-3xl
rounded-full

rounded-t-md
rounded-b-md
rounded-r-md
rounded-l-md

### รูปแบบเส้นขอบ border style
- border-none (ไม่มีเส้น)
- border-solid (เส้นทึบ)
- border-dashed (เส้นปะ)
- border-dotted (เส้นจุด)
- border-double (เส้นคู่)

## box shadow
shadow-md
shadow-lg
shadow-xl
shadow-2xl

## pseudo selector
focus
hover
https://tailwindcss.com/docs/hover-focus-and-other-states#pseudo-classes

## Responsive Web Design
### Container
- แสดงผลอยู่กึ่งกลางหน้าจอ
### Breakpoint
- ปรับตามขนาดอุปการณ์

320-480px Mobile
481-768px iPads,Tablets
769-1024px Laptops
2015-1200px Desktops
`>1201px TV, Widescreen

## Flexbox
จัดเรียงตำแหน่ง el
Container items

## Flex Direction
- row แนวตั้งตามลำดับ
- row-revese แนวตั้งย้อนกลับ
- col แนวนอน column
- col-reverse แนวนอนย้อนกลับ

## Flex Wrap
### Wrap Flexitem
กรณีที่ขนาด items ใหญ่กว่า พื้นที่ container
- nowrap จัดวาง items ที่เกินพื้นที่ container ไปด้านขวา
- wrap จัดวาง items ที่เกินพื้นที่ container เรียงจากบนลงล่าง
- wrap-reverse จัดวาง items ที่เกินพื้นที่ container เรียงจากล่างขึ้นบน

### Grow & Shrink
ทำเกี่ยวกับ items
flex-1
- ทำให้ item ที่อยู่แถวเดียวกันมีขนาดเท่ากัน
shrink
- ทำให้ item หดตัวจำนวนเท่าใดเมื่อเทียบกับ item อื่นๆ (ค่าเริ่มต้นเป็น 1)
grow
- ทำให้ item ขยายจำนวนเท่าใดเมื่อเทียบกับ item อื่นๆ (ค่าเริ่มต้นเป็น 0)

## Grid Layout
- row
- column
grid grid-cols-4 grid-rows-4

### gap
ช่องว่างระหว่าง
gap-2
gap-x-2
gap-y-8

## Justify-Items
- start ชิดซ้าย
- center กึ่งกลาง
- end ชิดขวา
- stretch ปรับขนาด item ทั้งหมดให้เต็มพื้นที่

## Justify self
- start
- center
- end

## Layer & apply
@layer base{
  a{
    @apply text-green-500
  }
}

base -> tag
a h1 h2 div

components -> class (mix class all in one)
text-white bg-red-500 p-3

@layer components{
  .menu-button{ //new name class
    @apply text-white bg-red-500 p-3
  }
}

utilities -> ปรับแต่ง css class ของ tailwind
text-red-500 (ปรับให้เป็นสีอื่น หรือ ชื่อ class tailwind แบบเราปรับแต่งเอง)

@layer utilities{
  .text-red-500{ //tailwind class
    color:blue;
  }
}

