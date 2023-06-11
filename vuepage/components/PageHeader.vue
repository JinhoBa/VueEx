<template>
    <header>
      <router-link class='login-link' to="/login">Login</router-link>
      <router-link to="/"><img src="../assets/icon.png" class='icon-size' alt=""></router-link>
    </header>
</template>
<script>
export default {
}
</script>
<style>
.icon-size{
  width: 50px;
  height: 50px;
 }
 .login-link{
  position: fixed;
  right: 20px;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  font-size: 12px;
  font-weight: bold;
 }
</style>
