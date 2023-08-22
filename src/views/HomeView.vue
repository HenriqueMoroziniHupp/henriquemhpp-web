<script setup lang="ts">
import CardCourse from '@/components/CardCourse.vue';
import type { ICourse } from '@/api/interfaces/courses'


const courses: Array<ICourse> = [
  {
    title: 'Front-end com Vue',
    description: 'Aprenda o básico ao avançado com o poderoso Vue3',
    icon: 'src/assets/icons/Vue.webp'
  },
  {
    title: 'Estado global com Pinia',
    description: 'Store moderna com compositions API, seguindo padrões consistentes e boas práticas adotada pela comunidade',
    icon: 'src/assets/icons/Pinia.webp'
  },
  {
    title: 'Estado global com Pinia',
    description: 'Store moderna com compositions API, seguindo padrões consistentes e boas práticas adotada pela comunidade',
    icon: 'src/assets/icons/Pinia.webp'
  },
  {
    title: 'JavaScript ES6+',
    description: 'Aprenda JS de forma moderna, com recursos de 2022',
    icon: 'src/assets/icons/javascript.webp',
  },
  {
    title: 'JavaScript ES6+',
    description: 'Aprenda JS de forma moderna, com recursos de 2022',
    icon: 'src/assets/icons/javascript4.webp',
  },
  {
    title: 'Front-end com Vue',
    description: 'Aprenda o básico ao avançado com o poderoso Vue3',
    icon: 'src/assets/icons/Vue.webp'
  },
  {
    title: 'DefineProps',
    description: 'Aprenda a utilizar props e tipa-las',
    icon: 'src/assets/icons/Vue.webp',
  }
]
</script>

<template>
  <main>
    <h1>Heui hue teste</h1>
    <div class="course-container">
      <CardCourse
      v-for="course in courses"
      :key="course.title"
      :course-title="course.title"
      :course-description="course.description"
      :course-icon="course.icon"
      class="card-course"
    />
    </div>
  </main>
</template>

<style scoped lang="scss">

.course-container {
  // margin: 0 auto;
  display: grid;
  grid-template-columns: 1fr;
  @include screen(tablet-landscape-up) {
    grid-template-columns: 1fr 1fr;
  }
  gap: 1.2rem;
}
</style>