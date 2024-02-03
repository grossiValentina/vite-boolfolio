<script>

export default {
    props: {

    },

    data() {
        return {

        }
    },
}

</script>

<template>
    <nav class="navbar navbar-light bg-light">
        <form class="container-fluid justify-content-start">
            <router-link :to="{name:'home'}" class="btn btn-outline-success me-2" type="button">Home</router-link>
            <router-link :to="{name:'about'}" class="btn btn-outline-success me-2" type="button">About</router-link>
        </form>
    </nav>
</template>

<style lang="scss" scoped></style>