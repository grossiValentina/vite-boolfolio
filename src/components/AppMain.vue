<script>
import axios from 'axios';
import ProjectCard from './ProjectCard.vue';

export default {
    data() {
        return {
            projects: []
        }
    },

    created() {
        axios.get('http://127.0.0.1:8000/api/projects')
            .then((resp) => {
                //console.log(resp);
                this.projects = resp.data.result;
            })
    },
    
    components: 
     {ProjectCard},

}

</script>

<template>
    
    <h3 class="m-3 text-center">Lista dei Progetti:</h3>

    <div class="container">
        <div class="row row-cols-3 g-4">
            <div v-for="project in projects" :key="project.id" class="col">
                <!-- componente card -->
                <ProjectCard :project="project"/>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped></style>