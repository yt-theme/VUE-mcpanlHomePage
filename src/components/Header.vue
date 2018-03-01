<template>
  <header>
   <img class="logo" src="../assets/logo.png" alt="logo"/>
   <div class="nav">
     <ul>
       <li><div class="nav-active">首页</div></li>
       <li><div>解决议案</div></li>
       <li><div>洛神云</div></li>
       <li><div>关于我们</div></li>
       <li><div>前往控制台</div></li>
     </ul>
   </div>
 </header>
</template>

<script>
export default {
  name: 'Header',
  data () {
    return {

    }
  }
}
</script>

<style scoped>
header {
  position: fixed;
 top: 0;
 left: 0;
 width: 100%;
 background-color: #257DFF;
 z-index: 99;
}
.logo {
  position: absolute;
  margin-top:21px;
  top: 0;
  left: 24px;
}
.nav {
  display: flex;
  justify-content: center;
  width: 100%;
}
.nav ul {
  list-style: none;
}
.nav ul li {
  display: block;
  color: #BDD7FF;
  font-size: 0.875em;
  cursor: pointer;
  float: left;
  margin-right: 3px;
}
.nav ul li div {
  width: 100%;
  padding: 29px 0;
  margin: 0 15px;
  text-align: center;
  border-top: 2px solid rgba(0,0,0,0);
}
.nav ul li div:hover {
  color: #ffffff;
  border-top: 2px solid #ffffff;
  transition: all 0.3s;
}
.nav ul li .nav-active {
  color: #ffffff;
  border-top: 2px solid #ffffff;
}
</style>
