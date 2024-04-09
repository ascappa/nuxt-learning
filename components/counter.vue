<script lang="ts" setup>
const count = useState("counter", () => 0)
const countNotKept = ref(0)
</script>

<template>
  <p>{{ count }}  {{ countNotKept }}</p>
  <button @click="count++, countNotKept++">increment</button>
</template>

<style scoped>
button {
  all: unset;
  background-color: rgb(6, 57, 40);
  color: aliceblue;
  border-radius: 8px;
  text-transform: capitalize;
  padding: 8px;
}
</style>
