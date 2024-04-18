<script>

import axios from 'axios';

export default {
    data() {
      return {

        title: 'Projects',

        projects: [],




      }

    },


    created() {
      
      axios.get('http://127.0.0.1:8000/api/projects').then((response) => {

        console.log(response.data.data);

        this.projects = response.data.data;

      });

    },

};

</script>

<template>

  <div class=" container mt-4">

    <h1>{{ title }}</h1>

    <div>
      <table class="table">
        <thead>
          <th>Id</th>
          <th>Title</th>
          <th>Content</th>
        </thead>

        <tbody>
          <tr v-for="proj in projects">
            <td>
              {{ proj.id }}
            </td>

            <td>
              {{ proj.title }}
            </td>

            <td>
              {{ proj.content }}
            </td>
          </tr>
        </tbody>
      </table>

    </div>

  </div>

</template>

<style lang="scss">

  @use './scss/general.scss' as *;

</style>

