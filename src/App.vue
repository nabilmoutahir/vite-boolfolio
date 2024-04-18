<script>

import AppHeader from './components/AppHeader.vue';
import ProjectCard from './components/ProjectCard.vue';
import ProjectCardsList from './components/ProjectCardsList.vue';

export default {
    data() {
      return {

        title: 'Projects',

      }

    },

    components: { AppHeader, ProjectCardsList},

    

};

</script>

<template> 

  <AppHeader></AppHeader>

  <div class=" container mt-4">

    <h1>{{ title }}</h1>

    <ProjectCardsList></ProjectCardsList>

  </div>

</template>

<style lang="scss">

  @use './scss/general.scss' as *;

</style>

