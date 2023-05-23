<script setup lang="ts">

</script>

<template>
  <div class="card-course">
    <div class="card-course__content">
      <img class="course-icon" alt="Vue logo" src="@/assets/icons/Pinia.webp"  />
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
    <!-- <div class="card-course__meta">
      <div class="meta-card lesson">12</div>
      <div class="meta-card duration">2h</div>
    </div> -->
  </div>
  <br>
  <div class="card-course">
    <div class="card-course__content">
      <img class="course-icon" alt="Vue logo" src="@/assets/icons/Vue.webp"  />
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
    <!-- <div class="card-course__meta">
      <div class="meta-card lesson">12</div>
      <div class="meta-card duration">2h</div>
    </div> -->
  </div>

</template>

<style scoped lang="scss">
.card-course {
  color: $white;
  color: black;
  background-color: seagreen;
  // background: -webkit-linear-gradient(315deg,#42d392 25%,#647eff);
  // background: -webkit-linear-gradient(144deg, #A1CDCE 25%, #647eff);
  // background: -webkit-linear-gradient(144deg, #A1CDCE 25%, #5566b7);
  display: grid;
  padding: 1.5rem;
  border-radius: $radius-lg;
  gap: 2rem;
  transition: all 0.2s ease;
  
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
      grid: 90px auto / 90px auto;
      justify-content: start;
    }

    .course-icon {
      height: 90px;
      width: 100%;
      justify-self: center;
      display: grid;
      place-items: center;
      object-fit: contain;
      transition: all 0.2s ease;
    }

    .course-info {
      // grid-row: 1;
      display: grid;
      align-content: start;
      gap: 0.5rem;
      .title {
        font-weight: $font-semi-bold;
        font-size: $font-semi-bold;
        line-height: 1;
      }

      .description {
        font-weight: $font-regular;
      }
    }

    .course-progress {
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
}

.card-course:hover {
  transform: scale(1.02);

  .course-icon {
    transform: scale(1.3);
  }
}
</style>