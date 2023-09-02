<template>
  <div>
    <b-card
      v-for="(empleo, index) in empleos"
      :key="index"
      class="d-flex align-items-center"
    >
    <div class="d-flex justify-content-between">
      <div>
      <img src="../assets/logo.png" alt="Imagen" class="custom-image">
    </div>
    <div>
      <div class="flex-grow-1">
        <div class="d-flex justify-content-between pr-5 pl-5">
          <h3 class="mb-0">{{ empleo.titulo }}</h3>
          <div class="d-flex pl-2">
            <b-button
              v-for="tecnologia in empleo.tecnologias"
              :key="tecnologia"
              variant="outline-secondary"
            >{{ tecnologia }}</b-button>
          </div>
        </div>
        <div class="d-flex justify-content-between mt-3">
          <div class="d-flex justify-content-between">
            <p class="mb-0 pl-5">Empresa: {{ empleo.empresa }}</p>
            <p class="mb-0 pl-5">Lugar: {{ empleo.lugar }}</p>
            <p class="mb-0 pl-5">Sueldo: {{ empleo.sueldo }}</p>
            <p class="mb-0 pl-5">Vacantes: {{ empleo.vacantes }}</p>
            <p class="mb-0 pl-5">Fecha: {{ empleo.fecha }}</p>
          </div>
        </div>
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
        {
          titulo: 'Frontend Developer',
          tecnologias: ['HTML', 'CSS', 'JavaScript'],
          empresa: 'WebTech Solutions',
          lugar: 'United States',
          sueldo: '$75000',
          vacantes: 2,
          fecha: '2 days ago'
        },
        {
          titulo: 'Data Scientist',
          tecnologias: ['Python', 'Machine Learning'],
          empresa: 'Data Insights',
          lugar: 'Canada',
          sueldo: '$90000',
          vacantes: 1,
          fecha: '1 day ago'
        }
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