<template>
    <header>
      <div class="header-content">
          <img src="../assets/icon.png" alt="">
          <router-link to="/login" class="login-link">Login</router-link>
        <nav>
          <ul class="menu-list">
            <li>전체글</li>
            <li>팬아트</li>
            <li>토론 게시판</li>
            <li>역사알아보기</li>
          </ul>
        </nav>
      </div>
    </header>
  </template>
<script>
export default {
}
</script>
<style>
.header-content {
    height: 100px;
    width: 700px;
    margin: 0 auto;
    overflow: auto;
}
nav {
    background-color: #004d98;
    color: #fff;
    text-align: center;
    height: 3em;
}
.menu-list {
    display: flex;
    justify-content: center;
    align-items: center;
    list-style: none;
    padding: 0;
    margin: 0;
}
.menu-list li {
    margin: 10px;
}
.login-link {
  position: absolute;
  top: 10px;
  right: 60px;
  color: #004d98;
  font-weight: bold;
}
.login-link {
  position: absolute;
  top: 10px;
  right: 60px;
  color: #004d98;
  font-weight: bold;
  text-align: right;
}
</style>
