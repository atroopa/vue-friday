<!-- ---------- template ---------- -->
<template>
  <div class="flex flex-col items-center justify-center ">
    <h1 class="text-3xl pt-12 pb-5 font-bold text-red-900">{{title}}</h1>
    <ModalVue :header="header" :text="text" theme="sale" />
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
