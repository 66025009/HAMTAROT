<template>
  <div class="login-container">
    <div class="login-box">
      <h1>เข้าสู่ระบบ</h1>
      <br><br>
      <form @submit.prevent="login">
        <div class="input-box">
          <input v-model="username" type="text" placeholder="อีเมล/ชื่อผู้ใช้" required>
          <i class='bx bxs-user'></i>
        </div>
        <div class="input-box">
          <input v-model="password" type="password" placeholder="รหัสผ่าน..." required>
          <i class='bx bxs-lock-alt'></i>
        </div>
        <div class="register-forgot">
          <div style="float: left;"><a href="/register">ลงทะเบียน</a>
          </div>
          <div style="float: right;"><a href="/forget">ลืมรหัสผ่าน</a>
          </div>
          <div style="clear: both;"></div>
        </div>
        <button type="submit" class="btn">ลงชื่อเข้าใช้</button>
        <table width="100%">
          <tbody>
            <tr>
              <td>
                <hr>
              </td>
              <td style="width: 1px; padding: 0px 10px; white-space: nowrap;">
                หรือ
              </td>
              <td>
                <hr>
              </td>
            </tr>
          </tbody>
        </table>
        <div class="social-icons-container">
          <a href="https://accounts.google.com/" target="_blank" class="social-icon"><img class="rounded-full"
              src="/public/ICON/Google.jpg" width="40px" /></a>
          <a href="https://www.facebook.com/login.php/" target="_blank" class="social-icon"><img class="rounded-full"
              src="/public/ICON/Facebook.png" width="90px" /></a>
          <a href="https://access.line.me/oauth2/v2.1/login?returnUri=%2Foauth2%2Fv2.1%2Fauthorize%2Fconsent&   loginChannelId=1521958360&loginState=CLn4LYQoulJIgLFHIw15nw#/"
            target="_blank" class="social-icon"><img class="rounded-full" src="/public/ICON/Line.png" width="60px" /></a>
        </div>
      </form>

    </div>
  </div>
</template>
  
<script>
export default {
  data() {
    return {
      username: '',
      password: '',
    };
  },
  methods: {
    login() {
      // เพิ่มโค้ดการตรวจสอบและดำเนินการเข้าสู่ระบบตรงนี้
      console.log('Logging in with:', this.username, this.password);
    },
  },
};
</script>
  
<style scoped>
.login-container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

.login-box h1 {
  color: #F8E559;
  font-weight: bold;
}

.login-box {
  text-align: center;
  width: 340px;
  padding: 20px;
  border: 10px solid #F8EDFF;
  border-radius: 10px;
  background: #3B3486;
}

form {
  display: flex;
  flex-direction: column;
}

label {
  margin-bottom: 8px;
}

input {
  padding: 8px;
  margin-bottom: 16px;
  background: #F8EDFF;
  border-radius: 10px;
  width: 280px;
}

button {
  padding: 10px;
  font-weight: bold;
  background-color: #F8E559;
  color: #000000;
  border-radius: 10px;
}

.social-icons-container {
  display: flex;
  justify-content: space-around;
  align-items: center;
}
</style>
  