<template>
  <b-card class="d-flex align-items-center">
    <img src="../assets/logo.png" alt="Imagen" class="custom-image">
    <div class="flex-grow-1">
      <div class="d-flex justify-content-between">
        <h1 class="mb-0">Empleo</h1>
        <div class="d-flex">
          <b-button variant="primary">Tecnologia 1</b-button>
          <b-button variant="primary">Tecnologia 2</b-button>
          <b-button variant="primary">Tecnologia 3</b-button>
        </div>
      </div>
      <div class="d-flex justify-content-between mt-3">
        <div class="d-flex flex-column">
          <p class="mb-0">Empresa</p>
          <p class="mb-0">Lugar</p>
          <p class="mb-0">Sueldo</p>
          <p class="mb-0">Vacantes</p>
          <p class="mb-0">Fecha</p>
  </div>
</div>

    </div>
  </b-card>
</template>

<script>
import { BCard, BButton } from 'bootstrap-vue';

export default {
  components: {
    BCard,
    BButton
  }
}
</script>

<style>
.custom-image {
  width: 80px;
}
</style>
