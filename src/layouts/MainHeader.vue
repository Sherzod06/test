<template>
  <div>
    <div class="flex justify-between items-center drop-shadow-md px-24 py-5 bg-white">
      <div class="flex items-center">
        <img width="60.18" height="22.38" src="@/assets/icons/mainlogoIcon.svg" alt="main logo">
        <div class="flex flex-col ml-2">
          <span class="font-bold text-base mb-0">METSENAT</span>
          <small class="text-[8px] text-green-800">PRO</small>
        </div>
      </div>
      <div class="flex">
        <div class="flex items-center bg-slate-200 rounded p-1">
          <span class="mx-5 text-sm font-semibold">Shohrux</span>
          <div class="bg-green-400 px-1 pt-2 rounded">
            <img src="@/assets/icons/avatar.svg" alt="avatar">
          </div>
        </div>
        <div>
          <BaseButton class="bg-inherit hover:bg-inherit ml-5">
            <img src="@/assets/icons/logoutIcon.svg" alt="logout">
          </BaseButton>
        </div>
      </div>
    </div>
    <div class="px-24 py-6 flex justify-between items-center bg-slate-100">
      <div>
        <BaseButton class="rounded-r-none bg-inherit border border-indigo-500 text-xs px-16"
          :class="route.name === '/admin/' ? 'bg-indigo-500 text-white' : 'bg-inherit text-indigo-500'">
          Dashboard
        </BaseButton>
        <BaseButton class="rounded-none bg-inherit border border-indigo-500 text-xs px-16 text-indigo-500  hover:text-white"
          :class="route.name === '/admin/[type]/' && route.params.type === 'sponsors' ? 'bg-indigo-500 text-white' : 'bg-inherit text-indigo-500'">
          Homiylar
        </BaseButton>
        <BaseButton class="rounded-l-none bg-inherit border border-indigo-500 text-xs px-16 text-indigo-500 hover:text-white"
          :class="route.name === '/admin/[type]/' && route.params.type === 'students' ? 'bg-indigo-500 text-white' : 'bg-inherit text-indigo-500'">
          Talabalar
        </BaseButton>
      </div>
      <div class="flex items-center">
        <div class="bg-slate-300 rounded-md flex">
          <PaperClipIcon class="w-12 text-slate-400" />
          <BaseInput class="bg-inherit border-0 focus:bg-inherit h-full mb-0" />
        </div>
        <div class="ml-5">
          <BaseButton class="bg-emerald-200 py-1 px-12 text-cyan-500">
            <PaperClipIcon class="w-8 mr-2" />
            Filter
          </BaseButton>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { PaperClipIcon } from '@heroicons/vue/solid'

const route = useRoute()
onMounted(() => {
  console.log(route)
})
</script>

<style scoped>
</style>
