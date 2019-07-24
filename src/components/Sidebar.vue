<template>
  <div class="main">
    <div class="sidebar" id="side">
      <div class="toggle" onclick="toggleSidebar()">
        <i class="fa fa-caret-right circle c"></i>
      </div>
      <router-link to="/dashbord">
        <a href="#" class="ic">
          <i class="fa fa-tachometer icon ic"></i>
          Dashbord
        </a>
      </router-link>
      <router-link to="/uielement">
        <a href="#">
          <i class="fa fa-desktop  icon ic "></i>
          UI Elements
        </a>
      </router-link>
      <router-link to="/charts">
        <a href="#">
          <i class="fa fa-area-chart  icon ic"></i>
          Charts
        </a>
      </router-link>
      <router-link to="/tabs-panel">
        <a href="#">
          <i class="fa fa-tasks icon ic"></i>
          Tabs & Panels
        </a>
      </router-link>
      <router-link to="/responsive-table">
        <a href="#">
          <i class="fa fa-tasks icon ic"></i>
          Responsive Tables
        </a>
      </router-link>
      <router-link to="/forms">
        <a href="#">
          <i class="fa fa-pencil-square-o icon ic"></i>
          Forms
        </a>
      </router-link>
      <router-link to="/multilevel-dropdown">
        <a href="#">
          <i class="fa fa-dropbox icon ic"></i>
          Multi-Level Dropdown<i class="fa fa-chevron-left si"></i>
        </a>
      </router-link>
      <router-link to="/empty-page">
        <a href="#">
          <i class="fa fa-file icon ic"></i>
          Empty Page
        </a>
      </router-link>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.sidebar {
  margin: 0;
  padding: 0;
  width: 15%;
  background: #24c0cc;
  position: fixed;
  height: 100%;
  opacity: 0.8;
  padding-top: 5%;
  transition: all 0.5s;
}
.sidebar a {
  color: #bbf1e9;
  display: block;
  text-decoration: none;
  padding: 3%;
}
.sidebar a:hover {
  background: #16a0a6;
}
.circle {
  height: 25px;
  width: 30px;
  border-radius: 0 90px 90px 0;
  background: #d1cfcb;
}
.toggle {
  position: relative;
  left: 240px;
}
.toggle .c {
  padding: 5px;
  font-size: 15px;
  color: black;
}
#side .active {
  left: 0;
}
.ic {
  padding-right: 15px;
}
.si {
  padding-left: 30px;
}
@media screen and (max-width: 700px) {
  .sidebar {
    width: 100%;
    height: auto;
    position: relative;
  }
}
</style>
