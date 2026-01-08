<script>
    export default {
        props: {
            currentPage: {
                type: String,
                default: 'home'
            }
        },
        methods: {
            isActive(pageName) {
                return this.currentPage.toLowerCase() === pageName.toLowerCase()
            }
        }
    }
</script>
<template>
    <a href="/" :style="isActive('home') ? 'background-color: green' : 'background-color: black'">Home page</a>
    <a href="/login" :style="isActive('login') ? 'background-color: green' : 'background-color: black'">Login page</a>
</template>