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
    <div class="px-24 py-6 flex justify-between items-center bg-white drop-shadow-sm">
      <div>
        <BaseButton class="rounded-r-none bg-inherit border border-indigo-500 text-xs px-16"
          :class="{'bg-indigo-500 text-white': route.name === '/admin/'}">
          Dashboard
        </BaseButton>
        <BaseButton class="rounded-none bg-inherit border border-indigo-500 text-xs px-16 text-indigo-500"
          :class="{'bg-indigo-500 text-white': route.name === '/admin/[type]/' && route.params.type === 'sponsors'}">
          Homiylar
        </BaseButton>
        <BaseButton class="rounded-l-none bg-inherit border border-indigo-500 text-xs px-16"
          :class="{'bg-indigo-500 text-white': route.name === '/admin/[type]/' && route.params.type === 'students'}">
          Talabalar
        </BaseButton>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
const route = useRoute()
onMounted(() => {
  console.log(route)
})
</script>

<style scoped>
</style>
