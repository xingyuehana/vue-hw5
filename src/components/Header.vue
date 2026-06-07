<template>
  <header class="top-header">
    <div class="header-container">
      <div class="logo-wrap">
        <img class="main-logo" src="/images/logo.png" alt="玉山銀行 Logo" />
      </div>
      <div class="header-links">
        <a class="lang-btn" href="#">Language ▾</a>
        <a class="home-link" href="#">玉山銀行首頁</a>
      </div>
    </div>
  </header>
</template>

<script setup>
// Header is presentational; no script logic needed yet.
</script>

<style scoped>
/* 這裡只放 Header 專用的 CSS */
.top-header {
    border-top: 5px solid #00A3A9;
    background-color: #fff;
    padding: 15px 0;
}
.header-container {
    max-width: 1000px;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
}
.main-logo { height: 40px; }
.header-links a {
    text-decoration: none;
    font-size: 13px;
    margin-left: 15px;
}
.lang-btn {
    background-color: #00A3A9;
    color: white;
    padding: 5px 10px;
    border-radius: 3px;
}
.home-link { color: #666; }
</style>
