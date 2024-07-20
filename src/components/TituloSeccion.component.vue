<template>
  <h3 class="text-center text-white font-medium">{{ props.titulo }}</h3>
</template>

<script setup>
import defineProps from "vue";
const props = defineProps({
  titulo: String,
});
</script>

<style></style>
