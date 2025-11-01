<!-- E-05-ParentComponent.vue -->
<template>
  <div>
    <ChildComponent
        :message="parentMessage"
        :id="1"
        :password="1234"
        @custom-event="handleEvent"
    />
  </div>
</template>

<script>
import { ref } from 'vue'
import ChildComponent from './ChildComponent.vue'

export default {
  name: "E05ParentComponent",
  setup() {
    const parentMessage = ref('Hello from parent')

    const handleEvent = (payload) => {
      console.log(payload)
    }

    return {
      parentMessage,
      handleEvent
    }
  },
  components: {
    ChildComponent
  }
}
</script>
<!--
<template>
  <div>
    <ChildComponent
        :message="parentMessage"
        :id="1"
        :password="1234"
        @custom-event="handleEvent"
    />
  </div>
</template>

<script>
import ChildComponent from './ChildComponent.vue';

export default {
  name: "E05ParentComponent",
  data() {
    return {
      parentMessage: 'Hello from parent'
    };
  },
  methods: {
    handleEvent(payload) {
      console.log(payload);
    }
  },
  components: {
    ChildComponent
  }
};
</script>
-->