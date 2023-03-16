<template>
  <h1>{{ title }}</h1> 
  <p>Welcome ...</p>
  <div v-if="showModal">
    <Modal   theme="sale" @close="toggleModal">
        <h1>Super VueJs Tutorial</h1>
        <p>Those courses are really amazing. Im thrilled by them</p>
        <template v-slot:links>
          <a href="#">sign up</a>
          <a href="#">more info</a>

        </template>

    </Modal>
  </div>
  <button @click.shift="toggleModal">Open Modal (shift)</button>
</template>

<script>
import Modal from './components/Modal.vue';
    
export default {
  name: 'App',
  components: {
    Modal
  },
  data() {
    return {
      title: 'My first Vue App gg',
      header: 'Sign up for the giveaway',
      text: 'Im learning very nice VueJs',
      showModal: false,
    }
  },
  methods: {
    toggleModal(){
      this.showModal = !this.showModal;
    },
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
h1 {
  border-bottom: 1px solid #ddd;
  display: inline-block;
  padding-bottom: 10px;
}
</style>
