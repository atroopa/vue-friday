<!-- ---------- template ---------- -->
<template>
  <div class="flex flex-col items-center justify-center ">
    <h1 class="text-3xl pt-12 pb-5 font-bold text-red-900">{{title}}</h1>
    <div v-if="showModal">
      <ModalVue @close="changeModal" :header="header" :text="text" theme="sale" />
    </div>
    <button @click="changeModal" class="bg-red-800 px-3 py-2 rounded-xl text-red-100">Show Modal</button>
  </div>
</template>

<!-- ---------- script ---------- -->

<script>
import ModalVue from './components/Modal.vue';

  export default {
    name: 'App',

    components: {
      ModalVue
    },

    data() {
      return {
        title : 'My Website Title',
        header: 'Sign up for a Giveaway',
        text: 'Grab the Course for Half Price',
        showModal: false,
      }
    },

    methods: {
      changeModal(){
        this.showModal = !this.showModal
      }
    },

  }
</script>

<!-- ---------- style ---------- -->

<style>

</style>
