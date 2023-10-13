<template>
  <header>
    <nav>
      <ul>
        <li><NuxtLink to="/">Home</NuxtLink></li>
        <li><NuxtLink to="/about">About</NuxtLink></li>
        <li><NuxtLink to="/projects">Projects</NuxtLink></li>
      </ul>
    </nav>
  </header>
  <slot />

  <footer>
    <ul>
      <li><NuxtLink to="/projects/1">Lorem 1</NuxtLink></li>
      <li><NuxtLink to="/projects/2">Ipsum 2</NuxtLink></li>
      <li><NuxtLink to="/projects/3">Dolor 3</NuxtLink></li>
    </ul>
  </footer>
</template>

<style scoped>
.router-link-exact-active {
  color: #12b488;
}
</style>
