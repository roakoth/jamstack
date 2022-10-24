<script setup>
const story = await useStoryblok('home', {
  version: useRoute().query._storyblok ? "draft" : "published",
  resolve_relations: 'featuredProjects.projects'
},{
    resolveRelations: 'featuredProjects.projects'
})
</script>

<template>
  <div>
    <StoryblokComponent v-if="story" :blok="story.content"></StoryblokComponent>
  </div>
</template>