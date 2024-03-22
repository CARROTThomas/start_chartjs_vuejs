<script setup>
  import Chart from 'chart.js/auto';
  import {onMounted} from "vue";

  const dataDoughnut1 = {
    labels: [
      'Hotel',
      'AirBnb',
      'Auberges'
    ],
    datasets : [{
      label: 'établissement',
      data: [300, 50, 100],
      backgroundColor: [
        'rgb(255, 99, 132)',
        'rgb(54, 162, 235)',
        'rgb(255, 205, 86)'
      ],
      borderColor: 'rgb(255,255,255)',
    }]
  }
  const dataDoughnut2 = {
    labels: [
      '1 Nuit',
      '2 Nuit',
      '4 Nuit',
      '3 Nuit',
      '6 Nuit',
      '13 Nuit',
    ],
    datasets : [{
      label: 'popular count night',
      data: [50, 17, 10, 10, 7, 6],
      backgroundColor: [
        'rgb(229,25,70)',
        'rgb(51,159,232)',
        'rgb(255, 205, 86)',
        'rgb(51,126,34)',
        'rgb(14,51,143)',
        'rgb(245,29,227)'
      ],
      borderColor: 'rgb(255,255,255)',
    }]
  }
  const dataDoughnut3 = {
    labels: [
      'Revenue',
      'Dépense',
    ],
    datasets : [{
      label: 'Bénéfice / Dépense',
      data: [65, 35],
      backgroundColor: [
        'rgb(56,255,0)',
        'rgb(255,0,0)',
      ],
      borderColor: 'rgb(255,255,255)',
    }]
  }

  const configDoughnut1 = {
    type: 'doughnut',
    data: dataDoughnut1,
    options: {
      animations: {}
    }
  };
  const configDoughnut2 = {
    type: 'doughnut',
    data: dataDoughnut2,
    options: {
      animations: {}
    }
  };
  const configDoughnut3 = {
    type: 'doughnut',
    data: dataDoughnut3,
    options: {
      animations: {}
    }
  };

  onMounted(()=> {
    const myChart1 = new Chart(
        document.getElementById('myDoughnutChart1'),
        configDoughnut1
    );
    const myChart2 = new Chart(
        document.getElementById('myDoughnutChart2'),
        configDoughnut2
    );
    const myChart3 = new Chart(
        document.getElementById('myDoughnutChart3'),
        configDoughnut3
    );
  })
</script>

<template>

  <div class="">
    <canvas id="myDoughnutChart1" height="100" width="100"></canvas>
    <canvas id="myDoughnutChart2" height="100" width="100"></canvas>
    <canvas id="myDoughnutChart3" height="100" width="100"></canvas>
  </div>

</template>

<style scoped>

</style>
