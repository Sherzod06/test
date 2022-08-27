
<template>
  <div>
    <header>
      <MainHeader />
    </header>
    <main>
      <router-view />
    </main>
  </div>
</template>

<script setup lang="ts">
import MainHeader from './layouts/MainHeader.vue'
</script>