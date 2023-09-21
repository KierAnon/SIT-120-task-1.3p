<script setup>
import { defineProps } from 'vue'
const { data } = defineProps({
  data: {
    type: Object
  }
})





</script>

<template>
  <div class="portfolio-piece">
    <a :href="data.link">
        <img :src="data.image" :alt="data.title" />
        <h2>{{ data.title }}</h2>
        <p>{{ data.description }}</p>
    </a>
  </div>
</template>
  
  <style scoped>
.portfolio-piece {
  display: flex;
  flex-direction: column;
  align-items: center;
  border: 1px solid #ccc;
  padding: 20px;
  margin-bottom: 20px;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  cursor: pointer;

  /* hover effect */
  &:hover {
    transform: scale(1.05);
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  }
}

a{
    text-decoration: none;
    text-align: center;
}

img {
  max-width: 100%;
  height: auto;
  margin-bottom: 15px;
  border-radius: 10px;
}

h2 {
  margin-bottom: 10px;
  font-size: 1.5rem;
  color: #333;
}

p {
  font-size: 1rem;
  color: #666;
  text-align: center;
  max-width: 300px;
}

/* Media queries for responsiveness */
@media (max-width: 768px) {
  .portfolio-piece {
    margin: 20px 10px;
  }

  h2 {
    font-size: 1.2rem;
  }

  p {
    font-size: 0.9rem;
  }
}
</style>
  