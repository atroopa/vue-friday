<!-- ---------- template ---------- -->
<template>
  <div class="flex flex-col items-center justify-center ">
    <h1 class="text-3xl pt-20 pb-5 font-bold text-red-900">{{title}}</h1>
    <ModalVue/>
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
        title: 'this is my title'
      }
    },

    methods: {
      handleEvent(){
        console.log(this.$refs.name);
      }
    },

  }
</script>

<!-- ---------- style ---------- -->

<style>

</style>
