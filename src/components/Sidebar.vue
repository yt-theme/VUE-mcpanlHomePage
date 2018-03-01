<template>
  
  <!-- sidebar -->
  <div v-bind:class="[this.hide ? sidebarActive : '', sidebar]">
    <ul>
      <li>
        <img src="../assets/u.svg" alt="cooperate"/>
        <p>合作</p>
      </li>
      <li class="sidebar-consult">
        <span></span>
        <span></span>
        <span></span>
        <img src="../assets/059.png" alt="consult"/>
        <p>咨询</p>
      </li>
      <li>
        <img src="../assets/i.svg" alt="help"/>
        <p>帮助</p>
      </li>
    </ul>
    <div class="sidebar-totop">
      <img src="../assets/d.svg" alt="top"/>
      <img src="../assets/d1.svg" alt="top"/>
      <p>Top</p>
    </div>

    <!-- sidebar-hide -->
    <div v-on:click="Hidden" class="sidebar-hide">

    <!-- sidebar-vis -->
    </div>
    <div v-bind:class="[this.hide ? sidebarVisActive : '', sidebarVis]">

    </div>
  </div>
</template>

<script>
export default {
  name: 'Sidebar',
  data () {
    return {
      hide: false,

      // sidebar
      sidebarActive: 'sidebar-active',
      sidebar: 'sidebar',

      // sidebar vis button
      sidebarVis: 'sidebar-vis',
      sidebarVisActive: 'sidebar-vis-active'
    }
  },
  methods: {
    Hidden: () => {
      this.hide = !this.hide
      console.log(this.hide)
    },
    Vis: () => {

    }
  }
}
</script>

<style scoped>
@keyframes  sidebarSpan {
  0%   { top: 5px; }
  12%  { top: 3px; }
  25%  { top: 2px; }
  50%  { top: -7px; }
  75%  { top: 2px; }
  83%  { top: 3px; }
  100% { top: 5px; }
}
.sidebar {
  position: fixed;
  right: 0px;
  width: 42px;
  height: 100vh;
  background-image: url("../assets/aside.jpg");
  z-index: 101;
  box-shadow: 0 0 12px #2275F0;
  transition: all 0.3s;
}
.sidebar-active {
  right: -42px;
}
.sidebar> ul {
  display: block;
  margin: 0;
  padding: 0;
  margin-top: 98px;
  list-style: none;
}
.sidebar> ul> li {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin-bottom: 30px;
  width: 100%;
  cursor: pointer;
}
.sidebar> ul> li> img {
  width: 24px;
  height: 24px;
}
.sidebar> ul> li> p {
  font-size: 0.875em;
  color: #ffffff;
}
.sidebar> ul .sidebar-consult {
  position: relative;
  transition: all 0.3s;
  margin: 27px 0;
}
.sidebar> ul .sidebar-consult img {
  margin-top: 3px;
  width: 24px;
  height: 14px;
}
.sidebar> ul .sidebar-consult p {
  margin-bottom: 3px;
}
.sidebar> ul .sidebar-consult .sidebar-consult-p-active {
  color: #288EF0;
}
.sidebar-consult> span {
  position: absolute;
  top: 4px;
  display: block;
  width: 5px;
  height: 5px;
  background-color: #ffffff;
  border-radius: 50%;
}
.sidebar-consult span:nth-child(1){
  left: 10px;
  animation: sidebarSpan 0.7s infinite 0.1s;
}
.sidebar-consult span:nth-child(2){
  left: 20px;
  animation: sidebarSpan 0.7s infinite 0.2s;
}
.sidebar-consult span:nth-child(3){
  left: 29px;
  animation: sidebarSpan 0.7s infinite 0.3s;
}
.sidebar-totop {
  position: absolute;
  bottom: 73px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 100%;
  height: 50px;
  overflow: hidden;
  transition: background-color 0.5s;
  cursor: pointer;
}
.sidebar-totop:hover {
  background: #ffffff;
  color: #2792F2;
}
.sidebar-totop>img {
  position: absolute;
  top: 0;
  left: 16px;
  display: block;
  font-size: 10px;
  transition: all 0.5s;
}
.sidebar-totop>img:nth-child(2){
  position: absolute;
  top: 50px;
  left: 16px;
  transition: all 0.5s;
}
.sidebar-totop p {
  font-size: 0.875em;
  color: #ffffff;
}
.sidebar-hide {
  position: absolute;
  bottom: 17px;
  width: 100%;
  height: 40px;
  background-image: url("../assets/right-menu-icons.png");
  background-position: 281px 13px;
  transition: all 0.3s;
}
.sidebar-hide:hover {
  background-color: #fff;
  background-image: url("../assets/right-menu-icons.png");
  background-position: 281px -92px;
  cursor: pointer;
}
.sidebar-vis {
  position: absolute;
  width: 100%;
  height: 40px;
  background-image: url("../assets/sidebar-vis.jpg");
  bottom: 17px;
  right: -42px;
  transition: all 0.3s;
}
.sidebar-vis-active {
  right: 42px;
}
</style>
