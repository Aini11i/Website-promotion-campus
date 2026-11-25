<script setup>
import data from '../data/kampusData.json'

const facilities = data.facilities
</script>

<template>
  <section class="facilities-section" id="facilities">
    <div class="facilities-container">
      <h2>Facilities</h2>
      <p class="subtitle">Available facilities</p>

      <div class="facility-grid">
        <div v-for="facility in facilities" :key="facility.id" class="facility-card">
          <div class="facility-image">
            <img :src="facility.image" :alt="facility.name" />
          </div>
          <p class="facility-name">{{ facility.name }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.facilities-section {
  background-color: #f4f7fb;
  padding: 60px 20px;
  box-sizing: border-box;
}

.facilities-container {
  max-width: 1100px;
  margin: 0 auto;
}

.facilities-section h2 {
  font-size: 32px;
  margin: 0 0 10px;
  color: #183653;
}

.subtitle {
  color: #555;
  margin: 0 0 30px;
}

.facility-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 24px;
}

.facility-card {
  background-color: #ffffff;
  border: 1px solid #dde5ee;
  border-radius: 10px;
  overflow: hidden;
}

.facility-image {
  width: 100%;
  aspect-ratio: 4 / 3;
  background-color: #dde5ee;
}

.facility-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
}

.facility-name {
  margin: 0;
  padding: 16px 20px;
  font-weight: bold;
  color: #234b78;
}
</style>