<template>
  <header class="shadow-sm bg-white">
    <nav class="container mx-auto p-4 flex-col justify-between">
      <div class="flex justify-between">
        <ul>
          <li><NuxtLink to="/" class="font-bold">Home</NuxtLink></li>
        </ul>
        <ul class="flex gap-4">
          <li><NuxtLink to="/about">About</NuxtLink></li>
          <li><NuxtLink to="/projects" id="parent">Projects</NuxtLink></li>
        </ul>
      </div>
      <ul class="flex gap-4 justify-end mt-2">
        <li
          v-for="(project, index) in projects"
          :key="index"
        >
          <NuxtLink :to="`/projects/${linkify(project)}`">{{ project }}</NuxtLink>
        </li>
      </ul>
    </nav>
  </header>

  <div class="container mx-auto p-4">
    <slot />
  </div>
</template>

<script setup>
const projects = [
  "EcoConnect",
  "TechHarbor",
  "HealthHub",
  "ArtVista",
  "EducationElevate"
];

const linkify = (title) => title.replace(/([a-z])([A-Z])/g, '$1-$2').toLowerCase();
</script>

<style scoped>
.router-link-exact-active, #parent {
  color: #12b488;
}
</style>
