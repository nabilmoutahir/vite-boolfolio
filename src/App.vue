<script>

import AppHeader from './components/AppHeader.vue';
import ProjectCard from './components/ProjectCard.vue';

export default {
    data() {
      return {

        title: 'Projects',

      }

    },

    components: { AppHeader, ProjectCard },

    

};

</script>

<template> 

  <AppHeader></AppHeader>

  <div class=" container mt-4">

    <h1>{{ title }}</h1>

    <ProjectCard></ProjectCard>

  </div>

</template>

<style lang="scss">

  @use './scss/general.scss' as *;

</style>

