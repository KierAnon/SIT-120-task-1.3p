<script setup>
import PortfolioPiece from '../components/PortfolioPiece.vue'
import { ref } from 'vue';

const portfolioPieces = ref([
      { id: 1, title: 'The Best Things to Do', description: 'A VueJS website that lets users compare different items and their negative effects', image: '/Picture1.png', link: 'https://github.com/KierAnon/SIT-120-task-3.1D'},
      { id: 2, title: 'Proof of concept', description: 'A mockup of a website made in Figma', image: '/design-1.png', link: 'https://github.com/KierAnon/SIT-120-task-3.1D' },
      { id: 4, title: 'Portfolio', description: 'This website!', image: '/portfolio.png', link: 'https://github.com/KierAnon/SIT-120-task-1.3p' },
      { id: 4, title: 'To-Do App', description: 'This website!', image: '/to-do.png', link: 'https://github.com/KierAnon/SIT-120-task-2.1C/tree/main/todo-app' },
      // ... add more example data
    ])

</script>

<template>
  <div id="portfolio-container">
    <h1>My Portfolio</h1>
    <div id="portfolio-grid">
      <PortfolioPiece v-for="piece in portfolioPieces" :key="piece.id" :data="piece" />
    </div>
  </div>
</template>

<style scoped>
/* Main portfolio container */
#portfolio-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  max-width: 1200px;
  margin: 40px auto;
  padding: 0 20px;
}

h1 {
  font-size: 2.5rem;
  color: #444;
  margin-bottom: 30px;
  text-align: center;
}

/* Grid layout for portfolio pieces */
#portfolio-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
  width: 100%;
}

/* Responsive adjustments */
@media (max-width: 1024px) {
  #portfolio-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 768px) {
  h1 {
    font-size: 2rem;
  }

  #portfolio-grid {
    grid-template-columns: 1fr;
  }
}
</style>
