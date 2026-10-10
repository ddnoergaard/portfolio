<script setup>
import HomeCodeBlock from './HomeCodeBlock.vue';
</script>

<template>
    <section>
        <div class="container c-left">
            <h1><span style="font-weight: 100;">Hello</span><span style="font-weight: 100;">.</span><span
                    style="font-weight: 900;">.</span><span style="font-weight: 300;">.</span><br><span> I'm
                    Daniel</span>
                <span style="font-style:normal"> Nørgaard</span>
            </h1>
            <p class="sub-text" style="padding-right: 25%;">
                An aspiring software developer, with an affinity for making it work no matter what.
            </p>
            <p class="sub-text">Currently studying Computer Science at Zealand in Roskilde, Denmark.</p>
            <div></div>
        </div>
        <div class="container">
            <HomeCodeBlock />
        </div>
    </section>
</template>

<style scoped>
section {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 88dvh;
    gap: 10rem;
}

.container {
    display: flex;
    flex-direction: column;
    width: 100%;
    height: 100%;
    justify-content: center;
}

.sub-text {
    color: var(--secondary-text);
}
</style>