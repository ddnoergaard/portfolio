<script setup>
import { ref } from 'vue'
import HomeProjectCard from './HomeProjectCard.vue'

const codingLang = ['C#', 'HTML', 'CSS', 'JavaScript']

const frameworks = ['.NET', 'Vue', 'React', 'React Native']

const libraries = ['Axios']

const databases = ['MSSQL', 'PostgreSQL']

const statusTags = ref(['Deployed', 'In progress', 'Paused'])

const aiTags = ref(['AI used', 'Not used'])

const projects = ref([
  {
    id: 1,
    name: 'Lockhub',
    description: 'A no-knowledge password manager targeted organizations.',
    tags: ['C#', 'React', '.NET', 'TypeScript'],
    status: 'Paused',
    aiTag: 'Used',
  },
  {
    id: 2,
    name: 'CMS / Blog site',
    description:
      'A custom CMS aimed at a blog site. User will be able to create an account, and create a blog if they want, or they can follow other bloggers, and simply be an observer.',
    tags: ['C#', 'Vue', '.NET', 'JavaScript'],
    status: 'In Progress',
    aiTag: 'Not used',
  },
  {
    id: 3,
    name: 'MediaK Insight',
    description:
      'A custom analytics tool for a marketing agency. Pulling data from marketing platforms through a third party service (Windsor), storing it in a BigQuery data warehouse, and then delivering the data to the agency in a simple overview. Having the marketing data stored in a BigQuery data warehouse, Ive implemented a chatbot into the analytics tool, to give the agency the option of having chatting with an AI about their marketing data.',
    tags: ['React', 'TypeScript'],
    status: 'Deployed',
    aiTag: 'Ai used',
  },
])
</script>

<template>
  <section>
    <div class="padding-container">
      <div class="intro">
        <h2>My projects</h2>
        <p>
          Here you'll find some of the projects I've worked on, currently working on, and maybe even
          some planning on future projects.
        </p>
      </div>
      <div class="project-card-container">
        <HomeProjectCard v-for="project in projects" :key="project.id" />
      </div>
    </div>
  </section>
</template>

<style scoped>
.padding-container {
  flex-direction: column;
}

section {
  display: flex;
  flex-direction: column;
  background-color: white;
  justify-content: center;
  align-items: center;
  height: fit-content;
  width: 100%;
  padding: 1rem 0 1rem 0;
  /*border-bottom: 1px solid black;*/
}

.intro {
  display: flex;
  width: 100%;
  flex-direction: column;
  justify-content: start;
  padding: 0 20dvw 0 20dvw;
}

.intro > p {
  color: var(--secondary-text);
}

.project-card-container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  height: fit-content;
  width: 100%;
}
</style>
