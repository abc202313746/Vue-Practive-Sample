<!-- E-06-E-05-ParentComponent.vue -->
<template>
  <div>
    <ChildComponent1 />
  </div>
</template>

<script setup>
import { provide } from 'vue'
import ChildComponent1 from "@/components/example4/ChildComponent1.vue"

provide('sharedMessage', 'Hello from provide')
</script>

<!--
<template>
  <div>
    <ChildComponent1 />
  </div>
</template>

<script>

import ChildComponent1 from "@/components/example4/ChildComponent1.vue";

export default {
  name: "E06ParentComponent",
  provide() { //전역변수, 자식에서 모두 사용
    return {
      sharedMessage: 'Hello from provide'
    };
  },
  components: {
    ChildComponent1
  }
};
</script>
-->