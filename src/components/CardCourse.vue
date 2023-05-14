<script setup lang="ts">

</script>

<template>
  <div class="card-course">
    <div class="card-course__content">
      <img class="curse-icon" alt="Vue logo" src="@/assets/logo.svg" width="125" height="125" />
      <div class="curse-info">
        <h2>Front-end com Vue</h2>
        <p>Aprenda o básico ao avançado com o poderoso Vue3</p>
      </div>
    </div>
    <div class="card-course__meta">
      <div class="meta-card lesson">12</div>
      <div class="meta-card duration">2h</div>
    </div>
  </div>
</template>

<style scoped lang="scss">
.card-course {
  color: $white;
  background-color: dodgerblue;
  display: grid;
  padding: 1.5rem;
  border-radius: $radius-lg;
  grid: 1fr / 4fr 1fr;
}
</style>