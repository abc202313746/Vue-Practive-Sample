<template>
  <div>
    <input v-model="id" />
    <input v-model="password" />
    <p>{{ message }}</p>
    <button @click="() => {
      message = id + ' ' + password;
    }">whoami</button>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const message = ref("Hello Vue")
const id = ref('')
const password = ref('')
</script>

<!---
<template>
  <div>
    <input v-model="id" />
    <input v-model="password" />
    <p>{{ message }}</p>
    <button @click="() => {
      this.message = this.id + ' ' + this.password;
    }">whoami</button>
  </div>
</template>

<script>
export default {
  name: "E03Binding",
  data() {
    return {
      message: "Hello Vue",
      id:'',
      password:''
    };
  }
};
</script>
--->