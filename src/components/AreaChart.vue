<template>
  <div class="container card-content">
    <div class="row">
      <div class="col-6">
        <div class="card">
          <span class="inner-font">Area Chart</span>
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
  mounted () {
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
          label: "My First dataset",
          backgroundColor: "rgba(79, 196, 127,0.2)",
          borderColor: "rgba(79, 196, 127,1)",
          borderWidth: 1,
          hoverBackgroundColor: "rgba(79, 196, 127,0.4)",
          hoverBorderColor: "rgba(79, 196, 127,1)",
          data: this.values
        }
      ]
    };
    this.myBarChart = new Chart(context, {
      type: "bar",
      data: data,
      options: options
    });
  },
  beforeDestroy() {
    this.myBarChart.destroy();
  }
};
</script>

<style scoped>
.card-content {
  margin-top: 3%;
  padding: 1% 6% 6% 6%;
  margin-left: 6%;
  background: white;
  height: 300%;
  width: 50%;
}
.graph-content {
  width: 110%;
  height: 490%;
  padding-top: 8%;
}

.inner-font {
  font-size: 15px;
  font-weight: bold;
}
</style>