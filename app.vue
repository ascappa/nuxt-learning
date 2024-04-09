<script setup lang="ts">
const count = ref(0)
const route = useRoute()
const nav = reactive(["home", "about", "contacts", "/"])


</script>

<template>
  <NuxtLayout>
    <header>my header! {{ count }}</header>
    <nav><ul><li v-for="item in nav" :key="item"><NuxtLink :to="item">{{ item }}</NuxtLink></li></ul></nav>
    <NuxtPage />
  </NuxtLayout>
</template>

<style>
@import "open-props/style";
p {
  color: var(--green-5);
  animation: var(--animation-shake-z);
  text-shadow: 0px 0px 10px green;
}
.page-enter-active,
.page-leave-active {
  transition: all 0.4s;
}
.page-enter-from,
.page-leave-to {
  opacity: 0;
  filter: blur(1rem);
}
</style>