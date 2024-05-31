<!-- ---------- template ---------- -->

<template>
<div @click.self="changeFromBg" class="fixed top-0 left-0 w-full h-full bg-black bg-opacity-50">
  <div class="mt-20 w-full max-w-sm mx-auto overflow-hidden rounded-lg shadow-md" > 
    <div class="px-4 py-5 bg-white sm:px-6 opacity-100" :class="{sale: theme === 'sale'}">
        <slot></slot>
        <div class="action">
            <slot name="links"></slot>
        </div>
    </div>
  </div>
</div>
</template>

<!-- ---------- script ---------- -->

<script>
export default {
    props: {
        theme: String,
    },
    methods: {
        changeFromBg(){
            this.$emit('close')
        }
    }
}
</script>

<!-- ---------- style ---------- -->

<style scoped>
.sale {
    background: crimson;
    color: white;
}
.sale h1 {
    color: white;
}
</style>