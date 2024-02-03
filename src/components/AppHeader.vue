<script>

export default {
    props: {

    },

    data() {
        return {
            links: [
                {
                    name: 'home',
                    title: 'Home',
                },
                {
                    name: 'about',
                    title: 'Chi siamo',
                }
            ]

        }
    },
}

</script>

<template>
    <nav class="navbar navbar-light bg-light">
        <form class="container-fluid justify-content-start">
            <div v-for="link in links" :key="link.titolo" >
                <router-link :to="{name:link.name}" class="btn btn-outline-success me-2" type="button">{{ link.title }}</router-link>
            </div>
        </form>
    </nav>
</template>

<style lang="scss" scoped></style>