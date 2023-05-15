<script setup lang="ts">

</script>

<template>
  <div class="card-course">
    <div class="card-course__content">
      <img class="course-icon" alt="Vue logo" src="@/assets/logo.svg" width="125" height="125" />
      <div class="course-info">
        <h2>Front-end com Vue</h2>
        <p>Aprenda o básico ao avançado com o poderoso Vue3</p>
      </div>
      <div class="course-progress">
        <div class="out-bar">
          <div class="inner-bar" />
        </div>
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

  @include screen(tiny-phone-up) {
    background-color: blue;
  }

  &__content {
    display: grid;
    gap: 1rem;
    // grid: 1fr 1fr / 1fr 1fr;

    .course-icon {
      // grid-area: 1 / ;
      // grid-row: 1 / 1;
    }

    .course-info {
      // grid-row: 1;
    }

    .course-progress {
      // color: aquamarine;
      // background-color: tomato;
      grid-column: 1 / 3;
      width: 100%;

      
      .out-bar {
        background-color: $white-mute;
        border-radius: $radius-full;
        
        .inner-bar {
          border-radius: $radius-full;
          background-color: $green-100;
          height: 0.7rem;
          width: 30%;
        }
      }
    }

  }
}</style>