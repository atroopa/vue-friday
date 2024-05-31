<!-- ---------- template ---------- -->
<template>
<div class="fixed top-0 left-0 w-full h-full bg-black bg-opacity-50">
  <div class="mt-20 w-full max-w-sm mx-auto overflow-hidden rounded-lg shadow-md"> 
    <div class="px-4 py-5 bg-white sm:px-6 opacity-100">
      <h1 class="text-2xl pt-2 pb-2 font-bold text-red-500">{{ header }}</h1>
      <p>{{ text }}</p>
    </div>
  </div>
</div>

</template>

<!-- ---------- script ---------- -->

<script>
export default {
    props: {
        header: String,
        text: String,
    }
}
</script>

<!-- ---------- style ---------- -->

<style scoped>
.modal {
    width: 400px;
    padding: 20px;
    margin: 100px auto;
    background: white;
    border-radius: 10px;
}

.backdrop {
    top: 0;
    position: fixed;
    background: rgba(0, 0, 0, 0.5);
    width: 100%;
    height: 100%;
}
</style>