<template>
  <div>{{ Intl.NumberFormat("en-IN").format(tweened.number.toFixed(0)) }}</div>
</template>

<script setup lang="ts">
import gsap from "gsap";
import { reactive, watch } from "vue";
const props = defineProps({ number: Number });
const tweened = reactive({ number: 0 });
watch(
  () => props.number,
  (value) => {
    gsap.to(tweened, { duration: 1, number: Number(value) || 0 });
  }
);
</script>
