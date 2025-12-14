<template>
  <div class="survey-container">
    <div class="question-content">
      <SurveyQuestion />
    </div>
    <div class="nav-buttons">
      <NavButtons
        :can-go-back="currentIndex > 0"
        :can-go-next="hasAnswered"
        @previous="goToPrevious"
        @next="goToNext"
      />
    </div>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue'
import SurveyQuestion from './SurveyQuestion.vue'
import NavButtons from './NavButtons.vue'

// State
const currentIndex = ref(0)
const responses = ref({})

// Computed
const hasAnswered = computed(() => {
  return true
})

// Methods
const goToPrevious = () => {
  if (currentIndex.value > 0) {
    currentIndex.value--
  }
}

const goToNext = () => {
  currentIndex.value++
}
</script>

<style scoped>
.survey-container {
  display: flex;
  flex-direction: column;
  height: 100%;
  justify-content: space-between;
}

.question-content {
  flex: 1;
  overflow-y: auto;
}

.nav-buttons {
  display: flex;
  justify-content: center;
  margin-top: 20px;
  padding: 20px 0 0 0;
  border-top: 1px solid #e5e5e5;
}
</style>
