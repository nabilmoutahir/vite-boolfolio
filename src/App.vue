<script>

import axios from 'axios';
import { api, store } from './store';


export default {
    data() {
      return {
        store,

        title: 'Projects',

        projects: [],

      }

    },


    created() {
      
      axios.get(api.rootUrl + 'projects').then((response) => {

        console.log(response.data.data);

        store.projects = response.data.data;

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
          <tr v-for="proj in store.projects">
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

