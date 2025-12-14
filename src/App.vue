<template>
  <div class="app-container">
    <h1 class="title">Female Experience Survey</h1>
    <div class="survey-box">
      <SurveyContainer />
    </div>
  </div>
</template>

<script>
import SurveyContainer from '@/components/Survey/SurveyContainer.vue'
import { defineComponent } from 'vue'

export default defineComponent({
  components: { SurveyContainer }
})
</script>

<style scoped>
/* keep your existing styles */
.app-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 95vh;
  padding: 5px;
  font-family: Arial, sans-serif;
  background-color: #f5f5f5;
  overflow: hidden;
}

.title {
  font-size: 2.2rem;
  font-weight: bold;
  color: #333;
  margin-bottom: 15px;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
  text-align: center;
  margin-top: 0;
}

.survey-box {
  width: 600px;
  height: 400px;
  background-color: white;
  border: 2px solid #ddd;
  border-radius: 15px;
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.15);
  padding: 30px;
  box-sizing: border-box;
  overflow-y: auto;
}
</style>
