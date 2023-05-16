<script setup lang="ts">

</script>

<template>
  <div class="card-course">
    <div class="card-course__content">
      <!-- <img class="course-icon" alt="Vue logo" src="@/components/icons/vue-badge.svg" /> -->
      <div class="course-icon">
        <img class="badge" alt="Vue logo" src="@/components/icons/badge.svg" height="125"/>
        <img class="logo" alt="Vue logo" src="@/assets/logo.svg"  />
      </div>
      <div class="course-info">
        <h2 class="title">Front-end com Vue</h2>
        <p class="description">Aprenda o básico ao avançado com o poderoso Vue3</p>
      </div>
      <div class="course-progress">
        <div class="out-bar">
          <div class="inner-bar" />
        </div>
      </div>
    </div>
    <div class="card-course__meta">
      <!-- <div class="meta-card lesson">12</div> -->
      <div class="meta-card duration">2h</div>
    </div>
  </div>
</template>

<style scoped lang="scss">
.card-course {
  color: $white;
  background-color: seagreen;
  display: grid;
  padding: 1.5rem;
  border-radius: $radius-lg;
  gap: 2rem;
  
  @include screen(tablet-portrait-up) {
    grid: 1fr / 1fr auto;
  }
  

  @include screen(tiny-phone-up) {
    // background-color: blue;
  }

  &__content {
    display: grid;
    gap: 1rem;
    // justify-items: center;
    // grid: 1fr 1fr / 1fr 1fr;
    
    @include screen(tablet-portrait-up) {
      justify-content: start;
    }

    .course-icon {
      justify-self: center;

    }

    .course-info {
      // grid-row: 1;
      .title {
        font-weight: $font-semi-bold;
        font-size: $font-semi-bold;
      }

      .description {
        font-weight: $font-regular;
      }
    }

    .course-progress {
      // color: aquamarine;
      // background-color: tomato;
      width: 100%;
      
      @include screen(tablet-portrait-up) {
        grid-column: 1 / 3;
      }

      
      .out-bar {
        background-color: rgba($color: $white-mute, $alpha: 0.6);
        border-radius: $radius-full;
        
        .inner-bar {
          border-radius: $radius-full;
          background-color: $white;
          height: 0.6rem;
          width: 30%;
        }
      }
    }

  }

  &__meta {
    display: grid;
    align-content: start;
    // gap: 0.8rem;
    
    .meta-card {
      color: $black;
      font-size: $text-2xl;
      text-align: center;
      font-weight: $font-semi-bold;
      background-color: $white;
      border-radius: $radius-normal;
      padding: 1rem;
      height: 4rem;
      width: 4rem;
    }
  }
}</style>