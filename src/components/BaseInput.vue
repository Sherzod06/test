<template>
  <input
    class="appearance-none block w-full bg-gray-200 text-gray-700 border rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
    type="text" v-bind="$attrs"
    :value="modelValue" @input="updateValue"
    >
</template>

<script setup lang="ts">
  const props = defineProps({
    modelValue: String
  })

  const emit = defineEmits(['update:modelValue'])

  const updateValue = (event) => {
    emit('update:modelValue', event.target.value)
  }
</script>

<style scoped>
</style>