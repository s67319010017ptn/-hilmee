<template>
  <div>
    <h2>กรอกชื่อผู้ใช้</h2>
    <form @submit.prevent="submitName">
      <input 
        type="text" 
        placeholder="กรอกชื่อของคุณ" 
        v-model="userName"
        required
      />
      <button type="submit">ส่งข้อมูล</button>
    </form>

    <p>ชื่อที่คุณกรอก: {{ userName }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      userName: "", 
    };
  },
  methods: {
    submitName() {
      alert(`คุณกรอกชื่อว่า: ${this.userName}`);
    },
  },
};
</script>

<style scoped>
input {
  padding: 8px;
  font-size: 16px;
  margin-right: 8px;
}
button {
  padding: 8px 12px;
  font-size: 16px;
  cursor: pointer;
}
</style>



