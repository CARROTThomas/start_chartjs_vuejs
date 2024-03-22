<script setup>
import Chart from 'chart.js/auto';
import { onMounted } from "vue";

const fetchData = async () => {
  try {
    const response = await fetch('data.json');
    return await response.json();
  } catch (error) {
    console.error('Error fetching data:', error);
    return null;
  }
};

onMounted(async () => {
  const data = await fetchData();
  if (data) {
    const chartConfigs = [
      {id: 'myDoughnutChart1', dataKey: 'doughnut1'},
      {id: 'myDoughnutChart2', dataKey: 'doughnut2'},
      {id: 'myDoughnutChart3', dataKey: 'doughnut3'}
    ];

    for (const {id, dataKey} of chartConfigs) {
      const chartData = data[dataKey];
      const config = {
        type: 'doughnut',
        data: chartData,
        options: {
          animations: {}
        }
      };
      new Chart(
          document.getElementById(id),
          config
      );
    }
  }
});
</script>

<template>
  <div class="">
    <canvas id="myDoughnutChart1" height="100" width="100"></canvas>
    <canvas id="myDoughnutChart2" height="100" width="100"></canvas>
    <canvas id="myDoughnutChart3" height="100" width="100"></canvas>
  </div>
</template>

<style scoped>
/* Ajoutez des styles si nécessaire */
</style>
