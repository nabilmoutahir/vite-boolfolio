<script>

import axios from 'axios';

export default {
    data() {
      return {

        title: 'hello',


      }

    },


    created() {
      
      axios.get('http://127.0.0.1:8000/api/projects').then((response) => {

        console.log(response.data);

      });

    },

};

</script>

<template>

  <div class=" container mt-4">

    <h1>{{ title }}</h1>

  </div>

</template>

<style lang="scss">

  @use './scss/general.scss' as *;

</style>

