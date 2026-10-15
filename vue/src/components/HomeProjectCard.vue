<script setup>
import { ref } from 'vue'

const id = ref(0)
const name = ref('name')
const description = ref('description')
const tags = ref(['tag1', 'tag2', 'tag3', 'tag4'])
const status = ref('deployed')
const aiTag = ref()
</script>

<template>
  <div class="p-card">
    <div class="top-card">
      <div
        style="
          display: flex;
          justify-content: start;
          align-items: center;
          width: 30%;
          height: auto;
          justify-content: center;
          align-items: center;
        "
      >
        <img src="/social-media/github.png" alt="" style="height: inherit; width: inherit" />
      </div>
      <div>
        <div style="display: flex; justify-content: space-between; width: 100%">
          <h3 style="color: var(--primary-text)">{{ name }}</h3>
          <p v-if="status === 'deployed'" style="color: white; background-color: aqua">Deployed</p>
        </div>

        <p style="color: var(--secondary-text)">{{ description }}</p>
      </div>
    </div>
    <div class="bottom-card">
      <div class="tag" v-for="tag in tags">{{ tag }}</div>
    </div>
  </div>
</template>

<style scoped>
.p-card {
  display: grid;
  grid-template-columns: auto;
  grid-template-rows: auto;
  flex-direction: column;
  width: 75%;
  height: 100%;
  background-color: var(--background);
  place-self: center;
  gap: 2rem;
  border-radius: 1rem;
  padding: 1rem;
}

.top-card {
  display: flex;
  width: 100%;
  
}

.bottom-card {
  display: flex;
  gap: 1rem;
}

.tag {
  padding: 0.5rem 1rem 0.5rem 1rem;
  background-color: var(--sage-green-secondary);
  border-radius: 10px;
}
</style>
