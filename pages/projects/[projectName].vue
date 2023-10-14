<template>
  <h1>{{ post().title }}</h1>
  <p>{{ post().body }}</p>
</template>

<script setup lang="ts">
definePageMeta({
  layout: 'projects',
});

const { projectName } = useRoute().params;

const projects = [
  {
    name: "eco-connect",
    title: "EcoConnect: Connecting Communities for a Greener Tomorrow",
    body: "Explore our EcoConnect project, a platform that unites eco-conscious individuals, businesses, and communities to foster sustainable practices. Join the movement towards a healthier planet and discover innovative solutions for a greener future."
  },
  {
    name: "tech-harbor",
    title: "Navigating Innovation with TechHarbor",
    body: "Embark on a journey of technological exploration with TechHarbor. This project serves as a harbor for cutting-edge ideas and solutions. Discover the latest in technology, from software development to hardware innovations, as we navigate the ever-changing seas of the digital world."
  },
  {
    name: "health-hub",
    title: "Welcome to HealthHub",
    body: "Step into the realm of well-being with HealthHub, where technology meets healthcare. Our project aims to empower individuals with accessible health solutions. Explore the intersection of health and technology, and learn how HealthHub is revolutionizing the way we approach well-being."
  },
  {
    name: "art-vista",
    title: "Where Art Comes to Life: ArtVista",
    body: "Immerse yourself in the world of creativity and expression with ArtVista. This project is a vibrant canvas that celebrates the arts in all its forms. Explore the intersection of technology and artistic expression as we showcase the beauty and diversity of human creativity."
  },
  {
    name: "education-elevate",
    title: "Elevating Education: Welcome to our journey",
    body: "Embark on a transformation educational journey with EduElevate, where learning knows no bounds. Explore innovative educational solutions that empower individuals of all ages. Join us in reshaping the future of education through technology and visionary pedagogy."
  }
];

const post = () => projects.find(project => project.name === projectName as string) || {name: "", title: "My title", body: "My body"};
</script>
