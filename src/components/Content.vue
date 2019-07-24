<template>
  <div class="container">
    <!-- <Dashbord></Dashbord> -->
    <router-view />
    <div class="card-group cards">
      <div class="card card1">
        <div class="card-header">
          <span class="fa-stack fa-3x">
            <i class="fa fa-circle fa-stack-2x icon-background1"></i>
            <i class="fa fa-eye fa-stack-1x"></i>
          </span>
        </div>
        <div class="card-body">
          <h1 class="card-font">8,457</h1>
        </div>
        <div class="card-footer">
          <p class="card-p">Daily Visits</p>
        </div>
      </div>
      <div class="card card2">
        <div class="card-header">
          <span class="fa-stack fa-3x">
            <i class="fa fa-circle fa-stack-2x icon-background2"></i>
            <i class="fa fa-shopping-cart fa-stack-1x"></i>
          </span>
        </div>
        <div class="card-body">
          <h1 class="card-font">52,160</h1>
        </div>
        <div class="card-footer">
          <p class="card-p">Sales</p>
        </div>
      </div>
      <div class="card card3">
        <div class="card-header">
          <span class="fa-stack fa-3x">
            <i class="fa fa-circle fa-stack-2x icon-background3"></i>
            <i class="fa fa-comments fa-stack-1x"></i>
          </span>
        </div>
        <div class="card-body">
          <h1 class="card-font">15,823</h1>
        </div>
        <div class="card-footer">
          <p class="card-p">Comments</p>
        </div>
      </div>
      <div class="card card4">
        <div class="card-header">
          <span class="fa-stack fa-3x">
            <i class="fa fa-circle fa-stack-2x icon-background4"></i>
            <i class="fa fa-users fa-stack-1x"></i>
          </span>
        </div>
        <div class="card-body">
          <h1 class="card-font">36,752</h1>
        </div>
        <div class="card-footer">
          <p class="card-p">No, of Visits</p>
        </div>
      </div>
    </div>
    <div class="charts">
      <AreaChart
        :labels="[
          'Sunday',
          'Monday',
          'Tuesday',
          'Wednesday',
          'Thursday',
          'Friday',
          'Satuerday'
        ]"
        :values="[50, 100, 150, 200]"
      >
      </AreaChart>
      <LineChart
        :labels="[
          'Sunday',
          'Monday',
          'Tuesday',
          'Wednesday',
          'Thursday',
          'Friday',
          'Satuerday'
        ]"
        :values="[50, 100, 150, 200]"
      >
      </LineChart>
    </div>
  </div>
</template>
<script>
// import Dashbord from "../views/Dashbord.vue";
import LineChart from "../components/LineChart.vue";
import AreaChart from "../components/AreaChart.vue";
export default {
  components: {
    LineChart,
    AreaChart,
    // Dashbord
  }
};
</script>
<style>
body {
  background-color: #e6e6e6;
}
.content {
  padding-top: 15%;
  margin-left: 5%;
}
.cards {
  display: flex;
  padding-top: 2%;
  margin-left: 6%;
}
.card1 {
  height: auto;
  width: 30%;
  background-color: white;
  padding: 1% 13.5% 2% 2%;
}
.card2 {
  height: auto;
  width: 50%;
  background-color: white;
  padding: 1% 13.5% 2% 2%;
  margin-left: 5%;
}
.card3 {
  height: auto;
  width: 30%;
  background-color: white;
  padding: 1% 13.5% 2% 2%;
  margin-left: 5%;
}
.card4 {
  height: auto;
  width: 30%;
  background-color: white;
  padding: 1% 13.5% 2% 2%;
  margin-left: 5%;
}
.icon-background1 {
  color: #2fd489;
}
.icon-background2 {
  color: #34ccdf;
}
.icon-background3 {
  color: #fe6e52;
}
.icon-background4 {
  color: #f9ab54;
}
.card-font {
  color: #8a8e8c;
}
.card-p {
  color: #676d6b;
  font-size: 15px;
  font-weight: bold;
}
.charts {
  display: flex;
}
@media screen and (max-width: 667px) {
  body {
    overflow-x: hidden !important;
  }
  .container {
    max-width: 100% !important;
    overflow-x: hidden !important;
  }
}
</style>
