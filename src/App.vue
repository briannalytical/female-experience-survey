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
.app-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  min-height: 100vh;
  padding: 20px;
  font-family: Arial, sans-serif;
  background-color: #f5f5f5;
  box-sizing: border-box;
}

.title {
  font-size: 2.2rem;
  font-weight: bold;
  color: #333;
  margin: 0 0 20px 0;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
  text-align: center;
}

.survey-box {
  width: 100%;
  max-width: 700px;
  height: 500px;
  background-color: white;
  border: 2px solid #ddd;
  border-radius: 15px;
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.15);
  padding: 30px;
  box-sizing: border-box;
  overflow: hidden;
}
</style>

<style>
body {
  margin: 0;
  padding: 0;
  overflow: hidden;
}
</style>
