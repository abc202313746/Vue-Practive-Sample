<template>
  <div>
    <input ref="inputField" type="text" placeholder="Click the button to focus" />
    <button @click="focusInput">Focus Input</button>
  </div>
</template>

<script>
import {ref, onMounted, onBeforeMount, onBeforeUpdate, onUpdated, onBeforeUnmount, onUnmounted} from 'vue';

export default {
  name: 'E12RefComponent',
  setup() {
    const inputField = ref(null); // DOM 요소에 대한 ref 선언

    const focusInput = () => {
      inputField.value.focus(); // ref를 통해 DOM 요소에 접근
    };

    onMounted(() => {
      console.log(inputField); // 컴포넌트가 마운트된 후, inputField에 접근 가능
      if(inputField.value) {
        inputField.value.focus();
      }
    });

    // onBeforeMount(() => console.log('beforeMount hook'));
    // onMounted(() => console.log('mounted hook'));
    // onBeforeUpdate(() => console.log('beforeUpdate hook'));
    // onUpdated(() => console.log('updated hook'));
    // onBeforeUnmount(() => console.log('beforeUnmount hook'));
    // onUnmounted(() => console.log('unmounted hook'));

    onBeforeMount(()=>console.log(inputField));
    onMounted(()=>console.log(inputField));
    onBeforeUpdate(()=>console.log(inputField));
    onUpdated(()=>console.log(inputField));
    onBeforeUnmount(()=>console.log(inputField));
    onUnmounted(()=>console.log(inputField));

    return {
      inputField,
      focusInput
    };
  }
};
</script>