<script>
import { store } from '../store';

export default {
    props: {
        project: Object,
    },

    data() {
        return {
            store
        }
    },
}

</script>

<template>
    <div class="card">
        <h5 class="card-header bg-info text-white">{{ project.titolo }}</h5>
        <div class="card-body">
            <p class="fst-italic fw-lighter">{{ project.slug }}</p>
            <p class="card-text">{{ project.descrizione }}</p>
            <router-link :to="{name: 'single-project', params: {slug: project.slug}}">apri il progetto</router-link>
        </div>
    </div>
</template>

<style lang="scss" scoped>
</style>