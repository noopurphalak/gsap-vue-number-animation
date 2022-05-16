<script setup lang="ts">
import AnimatedNumber from "@/components/AnimatedNumber.vue";
import { onMounted, ref } from "vue";

const number = ref(0);

onMounted(() => {
  number.value = 10;
});
</script>

<template>
  <AnimatedNumber :number="number" />
</template>

<style></style>
