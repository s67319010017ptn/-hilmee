<template>
  <!-- ส่วน Template ใช้สำหรับเขียนโครงสร้าง HTML ของหน้าจอ -->
  <div id="app">
    <!-- แสดงข้อความจากตัวแปร message ด้วย data binding {{ }} -->
    <h1>{{ message}}</h1>
    <!-- ปุ่มที่มี event @click ซึ่งจะเรียกฟังก์ชัน changeMessage เมื่อคลิก -->
    <button @click="changeMessage">คลิกฉัน!</button>
  </div>
</template>

<script>
// ส่วน Script สำหรับใส่ logic และจัดการข้อมูลของ component
export default {
// ส่วน Script สำหรับใส่ logic และจัดการข้อมูลของ component
  name: "App",
// data() เป็นฟังก์ชันที่คืนค่า object ที่เก็บตัวแปรของเราไว้
data() {
  return {

    message: 'สวัสดีครับ ผมชื่อฮิลมี'
  }
},

// methods คือกลุ่มของฟังก์ชันที่เราสร้างขึ้นเพื่อจัดการ event ต่างๆ
methods: {
  // ฟังก์ชันนี้จะถูกเรียกเมื่อผู้ใช้คลิกปุ่ม
 changeMessage() {
  this.message = 'ขอบคุณที่คลิก!'
 }

},

}

</script>

<style>
#app {

  text-align: center;
  color: #ba0bff;
  
}

button {
  border-radius: 200px;
  color: white;
  background-color: rgb(119, 0, 255);
  width: 100px;
  height: 50px;
}

button:hover {
  background-color: blue;
}
</style>
