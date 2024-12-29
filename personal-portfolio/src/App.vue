<template>
  <div id="app">
    <!-- <Header /> -->
    <main>
      <ProfessionalSummary />
      <Skills />
      <Projects />
      <!-- <Experience />
      <Education />
      <YouTube />
      <Contact /> -->
    </main>
    <!-- <Footer /> -->
  </div>
</template>

<script>
// import Header from './components/Header.vue';
// import Footer from './components/Footer.vue';
import ProfessionalSummary from './components/ProfessionalSummary.vue';
import Skills from './components/Skills.vue';
import Projects from './components/Projects.vue';
// import Experience from './components/Experience.vue';
// import Education from './components/Education.vue';
// import YouTube from './components/YouTube.vue';
// import Contact from './components/Contact.vue';

export default {
  components: {
    // Header,
    // Footer,
    ProfessionalSummary,
    Skills,
    Projects,
    // Experience,
    // Education,
    // YouTube,
    // Contact,
  },
};
</script>

<style>
/* Global styles */
body {
  font-family: 'Inter', sans-serif;
  margin: 0;
  padding: 0;
}

.container {
  max-width: 1200px;
}
</style>
