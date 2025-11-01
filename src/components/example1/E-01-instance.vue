<template>
  <div>Hello, {{ message }}</div>
</template>

<script setup>
import { ref } from 'vue'

const name = 'Sookyoung In'
const message = ref(name)
</script>

<style scoped>
div {
  color: blue;
  font-size: 20px;
  font-weight: bold;
}
</style>

<!--
<template>
  <div>Hello, {{ message }}</div>
</template>

<script>
export default {
  name: "E01Instance",
  data() {

    const name  = 'Sookyoung In'

    return {
      message: name,
    };
  }
};
</script>

<style scoped>
div {
  color: blue;
  font-size: 20px;
  font-weight: bold;
}
</style>
-->