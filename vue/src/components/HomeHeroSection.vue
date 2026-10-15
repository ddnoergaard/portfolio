<script setup>
import { RouterLink } from 'vue-router'
import HomeCodeBlock from './HomeCodeBlock.vue'
</script>

<template>
  <section>
    <div class="padding-container">
      <div class="container c-left">
        <h1>
          <span style="font-weight: 100">Hello</span><span style="font-weight: 900">.</span
          ><span style="font-weight: 100">.</span><span style="font-weight: 900">.</span
          ><br /><span> I'm Daniel</span>
          <span style="font-style: normal"> Nørgaard</span>
        </h1>
        <p class="sub-text" style="padding-right: 25%">
          An aspiring software developer, with an affinity for making it work no matter what.
        </p>
        <p class="sub-text">Currently studying Computer Science at Zealand in Roskilde, Denmark.</p>
        <p class="sub-text">No AI written code was used to develop this portfolio.</p>
        <div class="button-container">
          <RouterLink to="/projects">See projects</RouterLink>
          <RouterLink to="/resume">View resume</RouterLink>
        </div>
      </div>
      <div class="container">
        <HomeCodeBlock />
      </div>
    </div>
  </section>
</template>

<style scoped>
section {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 88dvh;
  width: 100%;
  border-bottom: 1px solid black;
}

.container {
  display: flex;
  grid-template-columns: 1fr 1fr;
  flex-direction: column;
  width: 100%;
  height: 100%;
  justify-content: center;
}

.sub-text {
  color: var(--secondary-text);
}

.button-container {
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  margin: 16px 0 16px 0;
}

.button-container > a:first-child {
  background-color: var(--sage-green-secondary);
  padding: 1rem;
  border-radius: var(--button-padding);
}

.button-container > a:last-child {
  background-color: var(--secondary-text);
  color: var(--background);
  padding: 1rem;
  border-radius: var(--button-padding);
}
</style>
