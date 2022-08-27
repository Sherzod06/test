<template>
  <div class="bg-gray-100 h-screen flex justify-center">
    <div class="max-w-screen-sm my-auto mx-auto p-5">
      <div class="flex justify-center mb-3">
        <img src="@/assets/icons/logo.svg" alt="">
      </div>
      <form class="w-full rounded-lg px-8 py-5 bg-white">
        <h1 class="text-4xl py-5 font-black">Kirish</h1>
        <div class="flex flex-wrap -mx-3 mb-6">
          <div class="w-full px-3 mb-6 md:mb-0">
            <label class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2" for="grid-first-name">
              Login
            </label>
            <BaseInput id="first-name" placeholder="first name" v-model="name" />
          </div>
          <div class="w-full px-3 mb-6 md:mb-0">
            <label class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2" for="grid-first-name">
              Parol
            </label>
            <BaseInput type="password" id="first-name" placeholder="first name" v-model="password" />
            <p class="text-red-500 text-xs italic">Please fill out this field.</p>
          </div>
          <div class="w-full px-3 mt-2">
            <BaseButton class="w-full">
              Kirish
            </BaseButton>
          </div>
        </div>
      </form>
    </div>
  </div>
</template>

<script setup lang="ts">

const name = ref()

</script>

<style scoped>
</style>