<template>
  <div class="about">
    <h1>This is an about page.</h1>
    <div class="chart">
      <bar-component :chartdata="data" :options="options" />
    </div>
  </div>
</template>

<script>
import BarComponent from "@/components/BarComponent.vue";

export default {
  name: "about",
  components: {
    BarComponent
  },
  data() {
    return {
      data: {
        labels: ['a', 'b', 'c', 'd', 'e', 'f', 'g'],
        datasets: [{
          label: 'My First Dataset',
          data: [65, 59, 80, 81, 56, 55, 40],
          fill: false,
          borderColor: 'rgb(75, 192, 192)',
          tension: 0.1
        }],
      },
      options: {}
    }
  }
};
</script>

<style scoped>
.chart {
  width: 500px;
  margin: 0 auto;
}
</style>