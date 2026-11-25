<script setup>
import data from '../data/kampusData.json'

const tuition = data.tuition
</script>

<template>
  <section class="tuition-section" id="tuition">
    <div class="tuition-container">
      <h2>{{ tuition.title }}</h2>
      <p class="subtitle">{{ tuition.subtitle }}</p>

      <h3>Tuition Details</h3>
      <div class="card">
        <p class="card-text">{{ tuition.details }}</p>
      </div>

      <h3>Admission Paths</h3>
      <div class="info-grid">
        <div v-for="path in tuition.admissionPaths" :key="path.id" class="card">
          <p class="card-title">{{ path.name }}</p>
          <p class="card-text">{{ path.description }}</p>
        </div>
      </div>

      <h3>Scholarships</h3>
      <div class="info-grid">
        <div v-for="item in tuition.scholarships" :key="item.id" class="card">
          <p class="card-title">{{ item.name }}</p>
          <p class="card-text">{{ item.description }}</p>
        </div>
      </div>

      <div class="cta">
        <p>Have questions about admission? Contact us on Instagram or WhatsApp.</p>
        <a href="#contact" class="cta-button">Contact Us</a>
      </div>
    </div>
  </section>
</template>

<style scoped>
.tuition-section {
  background-color: #ffffff;
  padding: 60px 20px;
  box-sizing: border-box;
}

.tuition-container {
  max-width: 1100px;
  margin: 0 auto;
}

.tuition-section h2 {
  font-size: 32px;
  margin: 0 0 10px;
  color: #183653;
}

.tuition-section h3 {
  font-size: 22px;
  margin: 40px 0 16px;
  color: #234b78;
}

.subtitle {
  color: #555;
  margin: 0 0 10px;
}

.info-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 24px;
}

.card {
  background-color: #f4f7fb;
  border: 1px solid #dde5ee;
  border-radius: 10px;
  padding: 20px;
}

.card-title {
  margin: 0 0 12px;
  font-weight: bold;
  color: #234b78;
}

.card-text {
  margin: 0;
  color: #555;
  line-height: 1.6;
}

.cta {
  margin-top: 48px;
  padding: 28px 20px;
  background-color: #183653;
  border-radius: 10px;
  text-align: center;
  color: #ffffff;
}

.cta p {
  margin: 0 0 16px;
}

.cta-button {
  display: inline-block;
  padding: 10px 24px;
  background-color: #ffffff;
  color: #183653;
  border-radius: 6px;
  font-weight: bold;
  text-decoration: none;
}
</style>