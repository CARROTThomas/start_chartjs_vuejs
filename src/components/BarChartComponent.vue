<script setup>
import Chart from 'chart.js/auto';
import {onMounted} from "vue";

const data = {
  labels: [
    "Janvier",
    "Février",
    "Mars",
    "Avril",
    "mai",
    "Juin",
    "Juillet",
    "Aout",
    "Septembre",
    "Octobre",
    "Novembre",
    "Décembre"
  ],
  datasets : [{
    label: 'client by month',
    backgroundColor: 'rgb(255,255,255)',
    borderColor: 'rgb(206,53,53)',
    data: [18, 56, 23, 57, 33, 67, 70, 76, 23, 45, 26, 17]
  }]
}

const config = {
  type: 'bar',
  data: data,
  options: {
    animations: {}
  }
};


onMounted(()=> {
  const myChart = new Chart(
      document.getElementById('myChart'),
      config
  );
  const myChart2 = new Chart(
      document.getElementById('myChart2'),
      config
  );
})
</script>

<template>

  <div class="">
    <h2>Lieus les plus recherchés</h2>
    <canvas id="myChart" height="300" width="500"></canvas>

    <!---->
    <h2>Nombre de nuit réservé par J/S</h2>
    <canvas id="myChart2" height="300" width="500"></canvas>

  </div>

</template>

<style scoped>

</style>
