<template>
    <aside>
      <input class="burger-check" type="checkbox" id="burger-check" v-model="isSidebarVisible" />
      <label class="burger-icon" for="burger-check">
        <span class="burger-sticks"></span>
      </label>
      <div class="menu" :style="{ 'max-width': isSidebarVisible ? '200px' : '0' }">
        <ul class="menu-item">
          <li>전체글</li>
          <li>팬아트</li>
          <li>토론 게시판</li>
          <li>역사관</li>
        </ul>
        <div style="width: 200px;"></div>
      </div>
    </aside>
</template>

<script>
export default {
  data () {
    return {
      isSidebarVisible: false
    }
  }
}
</script>
<style>
.menu {
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 0;
  transition: 0.5s ease;
  z-index: 1;
  background-color: #EDBB00;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  overflow: hidden;
}
.menu-item {
  position: absolute;
  top: 70px;
  padding: 17px;
  margin: 17px;
  list-style: none;
}
.menu-item li{
  height: 60px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 20px;
}
.burger-icon {
  cursor: pointer;
  display: inline-block;
  position: fixed;
  z-index: 2;
  padding: 8px 0;
  top: 4px;
  left: 4px;
  user-select: none;
  width: auto;
  margin: 0;
}
.burger-icon .burger-sticks {
  background: #333;
  display: block;
  height: 2px;
  position: relative;
  transition: background .2s ease-out;
  width: 18px;
}
.burger-icon .burger-sticks:before,
.burger-icon .burger-sticks:after {
  background: #333;
  content: '';
  display: block;
  height: 100%;
  position: absolute;
  transition: all .2s ease-out;
  width: 100%;
}
.burger-icon .burger-sticks:before {
  top: 5px;
}
.burger-icon .burger-sticks:after {
  top: -5px;
}
.burger-check {
  display: none;
}
.burger-check:checked~.menu {
  width: 200px;
}
.burger-check:checked~.burger-icon .burger-sticks {
  background: transparent;
}
.burger-check:checked~.burger-icon .burger-sticks:before {
  transform: rotate(-45deg);
}
.burger-check:checked~.burger-icon .burger-sticks:after {
  transform: rotate(45deg);
}
.burger-check:checked~.burger-icon:not(.steps) .burger-sticks:before,
.burger-check:checked~.burger-icon:not(.steps) .burger-sticks:after {
  top: 0;
}
.burger-check:not(:checked)~.menu {
  width: 0;
}
</style>
