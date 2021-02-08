<template>
  <div id="app">
    <button @click="toggleModal">Toggle</button>
    <Overlay :show="showModal" @close="showModal = false">
      <Dialog @cancel="showModal = false">
        <template slot="heading">
          <h1>New heading!</h1>
        </template>
        <template slot="content">
          <p>Äru säker?</p>
        </template>
      </Dialog>
    </Overlay>
  </div>
</template>

<script>
import Overlay from '@/components/Overlay' 
import Dialog from '@/components/Dialog' 
export default {
  name: 'App',
  components: {
    Overlay, Dialog
  },
  data(){return {
    showModal: true
  }},
  methods: {
    toggleModal(){
      this.showModal = !this.showModal
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
