<template>
  <h1>Project {{ id }}</h1>
</template>

<script setup lang="ts">
const { id } = useRoute().params;
</script>