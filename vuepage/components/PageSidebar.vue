<template>
  <div>
    <button class="menu-button" @click="toggleMenu">
      <span class="burger-icon"></span>
    </button>
    <aside v-if="isMenuVisible" class="menu-bar">
      <ul class="side-menu">
        <li><router-link to="/">Home</router-link></li>
        <li><router-link to="/fan-art">Fan-Art</router-link></li>
        <li><router-link to="/talk">Talk</router-link></li>
        <li><router-link to="/history">History</router-link></li>
      </ul>
    </aside>
  </div>
</template>

<script>
export default {
  data () {
    return {
      isMenuVisible: false
    }
  },
  methods: {
    toggleMenu () {
      this.isMenuVisible = !this.isMenuVisible
    }
  }
}
</script>

<style>
.menu-bar {
  width: 130px;
  height: 100%;
  background-color: #EDBB00;
  position: fixed;
  top: 0;
  left: 0;
  padding: 20px;
  list-style: none;
  z-index: 1;
  font-size: 1.5em;
  font-weight: bolder;
}

.side-menu{
  list-style-type: none;
  padding: 10px;
  margin: 10px;
}
.side-menu li{
  margin-bottom: 100px;
  font-size: 16px;
}
.menu-button {
  position: fixed;
  top: 10px;
  left: 10px;
  width: 40px;
  height: 40px;
  background-color: transparent;
  border: none;
  outline: none;
  cursor: pointer;
  z-index: 2;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.burger-icon {
  display: block;
  width: 25px;
  height: 3px;
  background-color: #000;
  position: relative;
  transform-origin: 50% 50%;
  transition: transform 0.3s ease;
}
.burger-icon:before,
.burger-icon:after {
  background: #333;
  content: '';
  display: block;
  height: 100%;
  position: absolute;
  transition: all .2s ease-out;
  width: 100%;
}
.burger-icon:before {
  top: -10px;
}
.burger-icon:after {
  top: 10px;
}
.menu-button.active .burger-icon {
  transform: rotate(45deg);
}
.menu-button.active .burger-icon:before {
  transform: rotate(90deg) translate(0, -10px);
}
.menu-button.active .burger-icon:after {
  transform: rotate(90deg) translate(0, 10px);
}
</style>
