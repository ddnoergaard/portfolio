<script setup>
import { ref } from 'vue';
import { RouterLink } from 'vue-router';

const logoText = ref("{ Daniel_DN }");

const d = new Date();
const year = d.getFullYear();

</script>

<template>
    <footer>
        <RouterLink to="/">{{ logoText }}</RouterLink>
        <span>|</span>
        <p>{{ year }} &copy; All rights reserved</p>
        <span>|</span>
        <p>Good to see ya down here :)</p>
    </footer>
</template>

<style scoped>
footer {
    display: flex;
    place-items: center;
    justify-content: center;
    gap: 2rem;
}
</style>