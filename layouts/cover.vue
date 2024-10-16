<script setup lang="ts">
import { computed } from "vue";

const props = defineProps({
  background: {
    default: "",
  },
});

const style = computed(() => {
  backgroundImage: `url("images/sky.jpeg")`;
});
</script>

<template>
  <div class="slidev-layout cover" :style="style">
    <div class="my-auto w-full">
      <slot />
    </div>
  </div>
</template>
