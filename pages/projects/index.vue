<template>
  <h1>{{ title }}</h1>
  <nav>
    <ul>
      <li><NuxtLink to="/projects/1">Lorem 1</NuxtLink></li>
      <li><NuxtLink to="/projects/2">Ipsum 2</NuxtLink></li>
      <li><NuxtLink to="/projects/3">Dolor 3</NuxtLink></li>
    </ul>
  </nav>
  <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Laudantium alias
    tempora quaerat. Consectetur vel consequuntur possimus vero? Repellendus, fuga
    voluptatem modi aut veritatis sed iste optio libero labore vel, nam nisi
    mollitia quas dolore eligendi eum qui sunt a id omnis sit et aliquid quia. Sed
    amet dignissimos itaque accusamus.</p></template>

<script setup lang="ts">
const title = "Welcome to my projects";
</script>