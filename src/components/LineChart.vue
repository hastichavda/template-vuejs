<template>
  <div class="container card-content">
    <div class="row">
      <div class="col-8">
        <div class="card">
          <span class="inner-font">Line Chart</span>
          <div class="card-body graph-content">
            <canvas id="graph" ref="graph"></canvas>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Chart from "chart.js";
export default {
  props: {
    labels: {
      type: Array,
      require: true,
      default: Array
    },
    values: {
      type: Array,
      require: true,
      default: Array
    }
  },
  mounted() {
    let context = this.$refs.graph.getContext("2d");
    let options = {
      responsive: true,
      maintainAspectRatio: false,
      legend: {
        display: false
      }
    };
    let data = {
      labels: this.labels,
      datasets: [
        {
          label: "Sales",
          fill: false,
          lineTension: 0.1,
          backgroundColor: "rgba(0,125,204,0.4)",
          borderColor: "rgba(0,125,204,1)",
          borderCapStyle: "butt",
          borderDash: [],
          borderDashOffset: 0.0,
          borderJoinStyle: "miter",
          pointBorderColor: "rgba(75,192,192,1)",
          pointBackgroundColor: "#fff",
          pointBorderWidth: 1,
          pointHoverRadius: 5,
          pointHoverBackgroundColor: "rgba(75,192,192,1)",
          pointHoverBorderColor: "rgba(220,220,220,1)",
          pointHoverBorderWidth: 2,
          pointRadius: 1,
          pointHitRadius: 10,
          data: this.values
        }
      ]
    };
    this.myLineChart = new Chart(context, {
      type: "line",
      data: data,
      options: options
    });
  },
  beforeDestroy() {
    this.myLineChart.destroy();
  }
};
</script>

<style scoped>
.card-content {
  margin-top: 3%;
  padding: 1% 6% 6% 6%;
  margin-left: 4%;
  background: white;
  height: 250%;
  width: 90%;
}
.graph-content {
  width: 114%;
  height: 490%;
  padding-top: 5%;
}
.inner-font {
  font-size: 15px;
  font-weight: bold;
}
</style>