<template>
  <button 
    v-bind="$attrs"
    class="inline-flex items-center justify-center rounded-md border border-transparent bg-indigo-600
    px-5 py-3 text-base font-medium leading-6 transition duration-150 ease-in-out
    hover:bg-indigo-500 focus:outline-none"
  >
    <slot />
  </button>
</template>

<script setup lang="ts">

</script>

<style lang="scss" scoped>

</style>
