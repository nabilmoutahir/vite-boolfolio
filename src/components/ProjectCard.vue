<script>

export default {

    props: { project: Object },

    computed: {
       abstract(){
            return this.project.content.length > 50 ? this.project.content.substr(0, 50) + '...' : this.project.content;
       }
    }
}
</script>

<template>

    <div class="col">

        <div class="card h-100">
            <img v-if="project.image" :src="project.image" class="card-img-top" alt="...">
            <div class="card-body">

                <h5 class="card-title">
                    {{ project.id }}: {{ project.title }}
                </h5>

                <p class="card-text">
                    {{ abstract }}
                </p>
                <a href="#" class="btn btn-primary">Details</a>
            </div>
        </div>

    </div>

</template>

<style lang="scss" scoped></style>