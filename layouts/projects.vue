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
        <li><NuxtLink to="/projects/1">Lorem 1</NuxtLink></li>
        <li><NuxtLink to="/projects/2">Ipsum 2</NuxtLink></li>
        <li><NuxtLink to="/projects/3">Dolor 3</NuxtLink></li>
      </ul>
    </nav>
  </header>

  <div class="container mx-auto p-4">
    <slot />
  </div>
</template>

<style scoped>
.router-link-exact-active, #parent {
  color: #12b488;
}
</style>
