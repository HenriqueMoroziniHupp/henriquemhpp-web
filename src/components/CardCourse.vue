<script setup lang="ts">

defineProps({
  courseTitle: {
    type: String,
    required: true,
  },
  courseDescription: {
    type: String,
    required: true,
  },
  courseIcon: {
    type: String,
    required: true,
  }
})

</script>

<template>
  <div class="card-course">
    <div class="card-course__content">
      <img class="course-icon" alt="Vue logo" :src="courseIcon"  />
      <div class="course-info">
        <h2 class="title">{{ courseTitle}}</h2>
        <p class="description">{{ courseDescription }}</p>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
.card-course {
  color: $soft-gray-500;
  background-color: rgba($soft-green, 0.6);
  display: grid;
  padding: 1.5rem;
  border-radius: $radius-md;
  gap: 2rem;
  transition: all 0.2s ease;


  &__content {
    display: grid;
    gap: 1rem;
    
    @include screen(tablet-portrait-up) {
      grid: auto / 90px auto;
      justify-content: start;
    }

    .course-icon {
      height: 90px;
      width: 100%;
      display: grid;
      place-items: center;
      place-self: center;
      object-fit: contain;
      transition: all 0.2s ease;
      aspect-ratio: 1 / 1;
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
        background-color: rgba($color: $soft-gray-400, $alpha: 0.6);
        border-radius: $radius-full;
        
        .inner-bar {
          border-radius: $radius-full;
          background-color: $white;
          background-color: $soft-gray-500;
          height: 0.6rem;
          width: 30%;
        }
      }
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