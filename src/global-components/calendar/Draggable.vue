<template>
  <div ref="draggableRef">
    <slot></slot>
  </div>
</template>

<script setup>
import { ref, onMounted } from "vue";


const props = defineProps({
  options: {
    type: Object,
    default: () => ({}),
  },
});

const draggableRef = ref();
const init = () => {
  new Draggable(draggableRef.value, props.options);
};

onMounted(() => {
  init();
});
</script>
