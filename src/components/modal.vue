// Modelo de implementación
// <button @click="$refs.modal.display(true)">Mostrame el modal</button>

<template>
  <div class="modal-cont" v-if="displayModal" @click="display(false)" >
    <div class="modal" v-html="content"></div>
  </div>
</template>

<script>
export default {
  name: 'modal',
  emits: ['display'],
  data () {
    return {
      displayModal: false
    }
  },
  methods: {
    display (val) { this.displayModal = val }
  },
  props: ['content']
  // mounted () {
  //   console.log(this.$refs.content.innerHTML)
  // }
}
</script>

<style lang="scss" scoped>
//modal
.modal-cont{
  position: fixed;
  left: 0; right: 0;
  top: 0; bottom: 0;
  z-index: 100;
  background: #0009;

  display:flex;
  justify-content: center;
  align-items: center;

  .modal{
    padding: 10px 20px;
    background: #fff;
    border-radius: 15px;
  }
}
</style>
