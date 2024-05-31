<template>
  <div class="flex flex-col items-center justify-center ">
    <h1 class="text-3xl pt-20 pb-5 font-bold text-red-900">{{title}}</h1>
    <input type="text" ref="name" class="pt-3 w-1/2 
                                      bg-gray-50 border border-gray-300 text-gray-900 
                                        text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 
                                        block p-2.5 dark:bg-gray-700 dark:border-gray-600 
                                      dark:placeholder-gray-400 dark:text-white 
                                      dark:focus:ring-blue-500 dark:focus:border-blue-500">
    <button @click="handleEvent" class="my-10 bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
      Click
    </button>
  </div>
</template>

<script>

export default {
  name: 'App',
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

<style>

</style>
