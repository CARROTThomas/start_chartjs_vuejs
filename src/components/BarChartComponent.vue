<script setup>
import Chart from 'chart.js/auto';
import { onMounted } from "vue";

const fetchData = async () => {
  try {
    const response = await fetch('./data.json');
    console.log(response)
    return await response.json();
  } catch (error) {
    console.error('Error fetching data:', error);
    return null;
  }
};

onMounted(async () => {
  const data = await fetchData();

  if (data) {
    const config = {
      type: 'bar',
      data: {
        labels: data.labels,
        datasets: [{
          label: 'Client by month',
          backgroundColor: 'rgb(255,255,255)',
          borderColor: 'rgb(206,53,53)',
          data: data.values
        }]
      },
      options: {
        animations: {}
      }
    };

    const myChart = new Chart(
        document.getElementById('myChart'),
        config
    );

    const myChart2 = new Chart(
        document.getElementById('myChart2'),
        config
    );
  }
});
</script>


<template>
  <div class="">
    <h2>Lieux les plus recherchés</h2>
    <canvas id="myChart" height="300" width="500"></canvas>

    <h2>Nombre de nuit réservées par J/S</h2>
    <canvas id="myChart2" height="300" width="500"></canvas>
  </div>
</template>


<style scoped>

</style>
