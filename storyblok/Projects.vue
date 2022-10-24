<script setup>
defineProps({
    blok: Object,
});
</script>

<template>
    <div class="container project-page">
       <div class="project-title"> 
       <h1> {{blok.name || "New Project"}}</h1>
       <NuxtLink :to="{name:'index'}">Go Back</NuxtLink>
       </div>

       <div class="project-description">
          <img :src="blok.image?.filename || 'https://picsum.photos/300/175' " :alt="blok.image?.alt" />
          <p> {{blok.description || "Add a project description"}}</p>
       </div>

    </div>

</template>