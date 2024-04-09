<script lang="ts" setup>
const route = useRoute()
const title = computed(() => route.fullPath)
useSeoMeta({title})

watchEffect(() => {
  console.log(route.fullPath)
})
</script>

<template>
  <div>
    Layout: default {{ route.fullPath }}

    <slot />
  </div>
</template>

<style scoped></style>
