
<template>
  <div class="home">
    <header>
      <img alt="Vue logo" src="@/assets/logo.svg">
      <h2>Protección Forestal</h2>
    </header>
    <div id="main-cont">
      <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Illum quo laboriosam reiciendis ducimus, facere consectetur iusto quibusdam mollitia non ratione cum aut inventore autem illo ipsum alias quod praesentium laudantium!</p>
    </div>
    <div class="sections">
    <div id="services">
        <h3>Servicios Proveidos</h3>
        <ul>
          <li>Recuperación de Bosques</li>
          <li>Intervencion a Animales invasivos</li>
          <li>Representación Fiscal en eco-Juicios</li>
          <li>Limpieza de cuerpos acuaticos</li>
          <li>Reintegración de animales maltratados</li>
        </ul>
      </div>
      <Calendario />
    </div>
    <button @click="$refs.modal.display(true)">Mostrame el modal</button>
    <Modal ref="modal" :content="`<div>
      Todas Putas
      </div>`"/>
  </div>
</template>

<script>
/* eslint-disable */
import Calendario from '@/components/Calendario.vue'
import Modal from '@/components/modal.vue'

export default {
  name: 'Home',
  components: {
    Calendario,
    Modal
  }
}
</script>

<style lang="scss" scoped>
header{
  height: fit-content;
  margin: auto;
  width: fit-content;
  img{
    height: 60vh;
    max-width: 100vw;
  }
}
#main-cont{
  margin: auto;
  width: 50%;
  min-width: 500px;
}
.sections{
  display: flex;
  justify-content: center;

  #services, .calendario{
    width: 40%;
    margin: 0 10px;
    margin-bottom: 3vh;
    padding: 30px 50px;
    background: #C728;
  }
}
</style>
