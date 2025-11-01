<template>
  <div>{{ fullName }}</div>
</template>

<script setup>
import { ref, computed, onMounted } from 'vue'

const firstName = ref("Kyungsu")
const lastName = ref("Lee")

const fullName = computed(() => {
  return firstName.value + " " + lastName.value
})

onMounted(() => {
  console.log('mounted')

  let a = 10

  setTimeout(() => {
    console.log('setTimeout')
    a = 20
    console.log(a)
  }, 500)

  setTimeout(() => {
    lastName.value = "123"
  }, 1000)

  setTimeout(() => {
    firstName.value = "KSL"
  }, 2000)
})
</script>

<!--
<template>
  <div>{{ fullName }}</div>
</template>

<script>
export default {
  name: "E02Reactive",
  data() {
    return {
      firstName: "Kyungsu",
      lastName: "Lee"
    };
  },
  mounted() {

    console.log('mounted');

    let a = 10;

    setTimeout(()=> {
      console.log('setTimeout');
      a=20;
      console.log(a);
    }, 500);

    setTimeout(()=> {
      this.lastName = "123";
        }, 1000);

    setTimeout(() => {
      this.firstName = "KSL";
    }, 2000);
  },
  computed: {
    fullName() {
      return this.firstName + " " + this.lastName;
    }
  }
};
</script>
-->