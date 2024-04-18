<script>

    import axios from 'axios';
    import { api, store } from '../store';

    import ProjectCard from './ProjectCard.vue';

    export default {

        data() {
            return {
                store,
            }
        },

        components: { ProjectCard },

        created() {

            axios.get(api.rootUrl + 'projects').then((response) => {
                console.log(response.data.data);

                store.projects = response.data.data;
            });

        },

    }
    
</script>

<template>
    <div class="row row-cols-3 g-4">

        <ProjectCard v-for="project in store.projects" :project="project"/>

    </div>
</template>

<style lang="scss" scoped></style>