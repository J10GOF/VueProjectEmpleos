<template>
  <div>
    <b-card
      v-for="(empleo, index) in empleos"
      :key="index"
      class="d-flex align-items-center"
    >
      <img src="../assets/logo.png" alt="Imagen" class="custom-image">
      <div class="flex-grow-1">
        <div class="d-flex justify-content-between">
          <h1 class="mb-0">{{ empleo.titulo }}</h1>
          <div class="d-flex">
            <b-button
              v-for="tecnologia in empleo.tecnologias"
              :key="tecnologia"
              variant="primary"
            >{{ tecnologia }}</b-button>
          </div>
        </div>
        <div class="d-flex justify-content-between mt-3">
          <div class="d-flex flex-column">
            <p class="mb-0">Empresa: {{ empleo.empresa }}</p>
            <p class="mb-0">Lugar: {{ empleo.lugar }}</p>
            <p class="mb-0">Sueldo: {{ empleo.sueldo }}</p>
            <p class="mb-0">Vacantes: {{ empleo.vacantes }}</p>
            <p class="mb-0">Fecha: {{ empleo.fecha }}</p>
          </div>
        </div>
      </div>
    </b-card>
  </div>
</template>

<script>
import { BCard, BButton } from 'bootstrap-vue';

export default {
  components: {
    BCard,
    BButton
  },
  data() {
    return {
      empleos: [
        {
          titulo: 'Junior dev',
          tecnologias: ['JavaScript', 'React'],
          empresa: 'Code heaven',
          lugar: 'Latin America',
          sueldo: '$5000',
          vacantes: 3,
          fecha: '3 days ago'
        },
        {
          titulo: 'Senior Dev',
          tecnologias: ['Python', 'Django'],
          empresa: 'La empresa',
          lugar: 'Colombia',
          sueldo: '$160000',
          vacantes: 1,
          fecha: '5 days ago'
        },
        {
          titulo: 'E-consultant ',
          tecnologias: ['Result Oriented ', 'Problem Analysis'],
          empresa: 'Future company',
          lugar: 'Anywhere',
          sueldo: '$60000',
          vacantes: 2,
          fecha: '3 days ago'
        },
        
      ]
    };
  }
}
</script>

<style>
.custom-image {
  width: 80px;
}
</style>
