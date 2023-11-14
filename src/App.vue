<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <EventCalendar msg="Eventos" :eventos="eventos" />
</template>

<script>
import EventCalendar from './components/EventCalendar.vue'

export default {
  name: 'App',
  components: {
    EventCalendar
  },
  data(){
    return{
      eventos:[
              {
              titulo:"Examen",
              fecha:"11/28/2023",
              descripcion:"Estudiar para el Examen de Practica de Desarrollo 3"
              },
              {
              titulo:"Aniversario",
              fecha:"11/28/2023",
              descripcion:"Comprar el regalo para el aniversario de mis padres"
              },
              {
              titulo:"Junta Laboral",
              fecha:"11/28/2023",
              descripcion:"Preparar el discurso para la presentacion de la junta"
              },
            ]
    }
  }
}
</script>

<style>
@import url("../public/style.css");

#app {
  font-family: var(--font-family);
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: var(--color-font);
  margin-top: 60px;
}
img{
  width: 100px;
}
</style>
