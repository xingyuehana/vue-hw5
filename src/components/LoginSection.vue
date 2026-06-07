<script setup>
const handleLogin = (e) => {
  alert('系統連線逾時或忙線中，請稍後再試。');
  e.target.reset(); 
}
</script>

<template>
  <section class="login-wrapper">
    <div class="login-ad-container">
      
      <div class="login-panel">
        <div class="tabs">
          <div class="tab active">一般登入</div>
          <div class="tab">QRCode 登入</div>
          <div class="tab">玉山金融卡</div>
        </div>

        <form class="form-container" @submit.prevent="handleLogin">
          <h3 class="form-title">使用者登入</h3>
          
          <div class="input-group">
            <label>身分證字號<br>或統一編號</label>
            <div class="input-wrapper">
              <input type="text" required>
              <span class="icon-eye">👁️</span>
            </div>
          </div>

          <div class="input-group">
            <label>使用者名稱</label>
            <div class="input-wrapper">
              <input type="text" required>
              <span class="icon-eye">👁️</span>
            </div>
          </div>

          <div class="input-group">
            <label>使用者密碼</label>
            <div class="input-wrapper">
              <input type="password" required>
              <span class="icon-eye">👁️</span>
            </div>
          </div>

          <div class="form-actions">
            <div class="links">
              <a href="#">申請網銀</a><br>
              <a href="#">忘記使用者名稱/密碼</a>
            </div>
            <button type="submit" class="submit-btn">登入</button>
          </div>
        </form>
      </div>

      <div class="ad-panel">
        <div class="ad-main">
          <div class="ad-main-inner">
            <img src="/images/ad-main1.png" alt="主廣告1">
            <img src="/images/ad-main2.png" alt="主廣告2">
            <img src="/images/ad-main3.png" alt="主廣告3">
            <img src="/images/ad-main4.png" alt="主廣告4">
          </div>
        </div>
        <div class="ad-sidebar">
          <img src="/images/ad-sub1.jpg" alt="小廣告1">
          <img src="/images/ad-sub2.jpg" alt="小廣告2">
          <img src="/images/ad-sub3.jpg" alt="小廣告3">
          <img src="/images/ad-sub4.jpg" alt="小廣告4">
        </div>
      </div>

    </div>
  </section>
</template>

<style scoped>
/* 最外層推移，讓上方留出背景圖的空間 */
.login-wrapper {
  padding-top: 40px; 
}

/* 核心白框與左右並排設定 */
.login-ad-container {
  display: flex; /* 這個屬性是讓表單和廣告左右並排的魔法！ */
  background-color: #ffffff;
  max-width: 1000px;
  margin: 0 auto;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.15); /* 加上陰影更逼真 */
}

/* 左側登入面板寬度 */
.login-panel {
  width: 350px;
  border-right: 1px solid #e0e0e0;
}

/* 頁籤排版 */
.tabs {
  display: flex;
  background-color: #f8f8f8;
}
.tab {
  flex: 1;
  text-align: center;
  padding: 15px 0;
  font-size: 14px;
  color: #888;
  cursor: pointer;
  border-bottom: 1px solid #e0e0e0;
  border-right: 1px solid #e0e0e0;
}
.tab:last-child {
  border-right: none;
}
.tab.active {
  background-color: #fff;
  color: #009e96; /* 玉山綠 */
  font-weight: bold;
  border-bottom: none;
  border-top: 3px solid #009e96;
}

/* 表單內部細節 */
.form-container {
  padding: 25px;
}
.form-title {
  font-size: 16px;
  color: #333;
  font-weight: normal;
  margin-bottom: 20px;
}
.input-group {
  display: flex;
  align-items: center;
  margin-bottom: 15px;
  border-bottom: 1px solid #eee;
  padding-bottom: 5px;
}
.input-group label {
  width: 90px;
  font-size: 13px;
  color: #666;
  line-height: 1.4;
}
.input-wrapper {
  flex: 1;
  position: relative;
}
.input-wrapper input {
  width: 100%;
  padding: 8px 30px 8px 8px;
  border: 1px solid #ccc;
  font-size: 14px;
}
.icon-eye {
  position: absolute;
  right: 8px;
  top: 50%;
  transform: translateY(-50%);
  font-size: 14px;
  color: #999;
  cursor: pointer;
}

/* 按鈕與連結區塊 */
.form-actions {
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
  margin-top: 25px;
}
.links a {
  font-size: 13px;
  color: #009e96;
  text-decoration: none;
  line-height: 1.8;
}
.submit-btn {
  background-color: #009e96;
  color: white;
  border: none;
  padding: 10px 35px;
  border-radius: 3px;
  font-size: 15px;
  cursor: pointer;
}

/* 右側廣告排版 */
.ad-panel {
  width: 650px;
  display: flex;
  padding: 15px;
  gap: 15px;
  background-color: #fff;
}
.ad-main {
  width: 440px;
  height: 310px;
  overflow: hidden;
  position: relative;
}
.ad-main-inner {
  display: flex;
  width: 1760px;
  height: 310px;
  animation: slideAd 16s infinite;
}
.ad-main-inner img {
  width: 440px;
  height: 310px;
  object-fit: cover;
}
.ad-sidebar {
  display: flex;
  flex-direction: column;
  gap: 10px;
  flex: 1;
}
.ad-sidebar img {
  width: 100%;
  height: auto;
  border: 1px solid #eee;
}

@keyframes slideAd {
  0%, 20% { transform: translateX(0); }
  25%, 45% { transform: translateX(-440px); }
  50%, 70% { transform: translateX(-880px); }
  75%, 95% { transform: translateX(-1320px); }
  100% { transform: translateX(0); }
}
</style>