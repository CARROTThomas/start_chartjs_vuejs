<script setup>

import DoughnutChartComponent from "@/components/DoughnutChartComponent.vue";
import BarChartComponent from "@/components/BarChartComponent.vue";
import InfoChartComponent from "@/components/InfoChartComponent.vue";
import MapChartComponent from "@/components/MapChartComponent.vue";
</script>

<template>
  <div class="container">

    <header>
      <div class="site-visite">
        <h2>Site Visite</h2>
        <p class="sv-data-key">45 678</p>
      </div>
      <div class="ca">
        <h2>Chiffre d'affaire</h2>
        <p class="ca-data-key">45 678</p>
      </div>
    </header>

    <div class="page">

      <div class="left">

        <MapChartComponent />
        <BarChartComponent />
      </div>
      <div class="middle">
        <DoughnutChartComponent />
      </div>
      <div class="right">
        <InfoChartComponent />
      </div>


    </div>
  </div>



</template>

<style scoped>

.container {
  margin: auto;
  display: flex;
  min-height: 100vh;
  align-items: center;
  flex-direction: column;
  width: calc(100% - 160px);
  justify-content: space-between;
}

header {
  gap: 5em;
  width: 100%;
  display: flex;
  margin: 1.5em 0;
  align-items: center;
}

.page {
  width: 100%;
  display: flex;
  margin-bottom: 1em;
  align-items: center;
  justify-content: space-between;
}

.left, .middle, .right {
}

.right {
  width: 33vw;
  height: 75vh;
  border-radius: 46px;
  background: #e0e0e0;
  box-shadow:  25px 25px 50px #a8a8a8,
  -25px -25px 50px #ffffff;
}

.site-visite, .ca {
  gap: 1em;
  display: flex;
  align-items: center;
  flex-direction: column;
}

.sv-data-key, .ca-data-key {
  color: rgb(122, 160, 216);
  font-weight: 900;
  font-size: 1.5em;
}

</style>
