<template>
  <section id="projects" class="bg-white shadow rounded-lg p-6 mb-8">
    <h1 class="text-2xl font-bold mb-4">Key Projects</h1>
    <div v-for="project in projects" :key="project.title" class="mb-6">
      <h2 class="text-xl font-semibold">{{ project.title }}</h2>
      <p class="text-gray-600">{{ project.description }}</p>
      <button class="text-blue-500 mt-2" @click="toggleDetails(project)">Read More</button>
      <div v-if="project.showDetails" class="mt-4">
        <p class="text-gray-700">{{ project.details }}</p>
        <ul class="list-disc pl-5 mt-2">
          <li v-for="tech in project.techStack" :key="tech">{{ tech }}</li>
        </ul>
        <img v-if="project.image" :src="project.image" alt="Project screenshot" class="mt-4 rounded shadow" />
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Projects',
  data() {
    return {
      projects: [
        {
          title: 'Hivemind Forecast Platform',
          description: 'Developed features for a Python-based user and LLM prediction platform.',
          details: 'Led automated infrastructure development on Azure, ensuring reliability and scalability. Integrated CI/CD pipelines, reducing deployment time by 40%.',
          techStack: ['Python', 'Azure', 'CI/CD'],
          image: 'hivemind.png',
          showDetails: false,
        },
        {
          title: 'Cortex',
          description: 'Built Python/Flask automation tools for data generation.',
          details: 'Enhanced team collaboration through efficient tooling and Agile methodologies.',
          techStack: ['Python', 'Flask', 'Agile'],
          image: 'cortex.png',
          showDetails: false,
        },
      ],
    };
  },
  methods: {
    toggleDetails(project) {
      project.showDetails = !project.showDetails;
    },
  },
};
</script>

<style scoped>
h2 {
  color: #2d3748;
}
button {
  cursor: pointer;
}
</style>