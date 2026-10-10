<script setup>
import { ref } from 'vue';
import { RouterLink } from 'vue-router'

const logoText = ref("{ Daniel_DN }");

const navItems = ref([
    { label: 'Home', to: '/' },
    { label: 'Projects', to: '/projects' },
    { label: 'About Me', to: '/about-me' },
    { label: 'Resume', to: '/resume' },
]);

const socialItems = ref([
    { label: 'github', href: 'https://github.com/ddnoergaard', src: '/social-media/github.png', id: 'github-logo', alt: 'github logo', containerId: 'github-container' },
    { label: 'linkedin', href: 'https://www.linkedin.com/in/danieldnoergaard/', src: '/social-media/linkedin.png', id: 'linkedin-logo', alt: 'linkedin logo', containerId: 'github-container' }
]);

function changeImage(currentUrl) {
    //const ghContainer = document.getElementById('github-container')
    if (currentUrl.includes("github")) {
        if (socialItems.value[0].src === '/social-media/github.png') {
            socialItems.value[0].src = '/social-media/github-color-svg.svg';
            return;
        }
        socialItems.value[0].src = '/social-media/github.png';
        return;
    } else {
        if (socialItems.value[1].src === '/social-media/linkedin.png') {
            socialItems.value[1].src = '/social-media/linkedin_blue.png';
            return;
        }
        socialItems.value[1].src = '/social-media/linkedin.png';
        return;
    }
}

</script>

<template>
    <nav>
        <RouterLink class="nav-logo" to="/">{{ logoText }}</RouterLink>
        <div class="nav-item-container">
            <RouterLink v-for="item in navItems" :key="item.to" :to="item.to" class="nav-item">{{ item.label }}
            </RouterLink>
            <a v-for="item in socialItems" :key="item.id" :href="item.href" target="_blank" class="some-container"
                :id="item.containerId"><img :src="item.src" :alt="item.alt" :id="item.id"
                    v-on:mouseover="changeImage(item.href)" v-on:mouseout="changeImage(item.href)"></a>
        </div>
    </nav>
</template>

<style scoped>
nav {
    display: flex;
    justify-content: space-between;
    height: 10dvh;
}

.nav-item-container {
    display: flex;
    gap: 2rem;
    align-items: center;
}

.nav-logo {
    transition: 0.3s;
    place-self: center;
}

.nav-item {
    text-decoration: underline;
    text-decoration-color: transparent;
    transition: text-decoration-color 0.3s;
}

.nav-item:hover {
    text-decoration-color: var(--primary-text);
}

.some-container {
    display: flex;
    content: "";
    height: 2rem;
    width: 2rem;
    transition: all 0.3s;
}

.some-img {
    height: 100%;
    width: 100%;
    place-self: center;
    transition: all 0.3s;
}
</style>