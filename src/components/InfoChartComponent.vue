<script setup>

</script>

<template>

    <div class="info-container-content">
      <div class="">
        <h2>Nombre d'utilisateur</h2>
        <p class="data-key-users">56 063</p>
      </div>
      <div class="">
        <h2>DAU régulier</h2>
        <p class="data-key-dau">4 336</p>
      </div>

      <button class="btn btn-reset">RESET Data</button>
    </div>




</template>

<style scoped>


div {
  text-align: center;
}

.info-container-content {
  gap: 3em;
  display: flex;
  align-items: center;
  flex-direction: column;
  justify-content: space-between;
}

.data-key-users, .data-key-dau {
  color: white;
  font-size: 1.7em;
  font-weight: bolder;
}


.btn {
  border: none;
  color: white;
  font-weight: bold;
  cursor: pointer;
  padding: 1em 6em;
  border-radius: 10px;
}
.btn-reset {
  transition: .5s;
  background-color: rgb(157, 44, 38);
}
.btn-reset:hover {
  background-color: rgb(213, 28, 16);
}
</style>
