<!-- ---------- template ---------- -->
<template>
  <div class="flex flex-col items-center justify-center ">
    <h1 class="text-3xl pt-12 pb-5 font-bold text-red-900">{{title}}</h1>
    <div v-if="showModal">
      <ModalVue @close="changeModal"  theme="sale" >
        <h1 class="text-2xl pt-2 pb-2 font-bold text-red-500">OpenCode Giveaway !</h1>
        <p>Grab the Course for half price</p>

        <template v-slot:links>           
          <a href="">sing up</a><br>
          <a href="">more info</a><br>
        </template>

      </ModalVue>
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
