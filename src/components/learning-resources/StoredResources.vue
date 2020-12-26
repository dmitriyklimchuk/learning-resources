<template>
  <ul>
    <learning-resource
        v-for="res in resources"
        :title="res.title"
        :id="res.id"
        :description="res.description"
        :link="res.link"
        :key="res.id">
    </learning-resource>
  </ul>
</template>

<script>
  import LearningResource from "./LearningResource";
  export default {
    components: {
      LearningResource
    },
    inject: ['resources']
  }

</script>

<style scoped>
  ul {
    list-style: none;
    padding: 0;
    margin: 0 auto;
    max-width: 40rem;
  }
</style>
