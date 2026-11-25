<script setup>
import data from '../data/kampusData.json'

const programs = data.programs
</script>

<template>
  <section class="programs-section" id="programs">
    <div class="programs-container">
      <h2>Programs</h2>
      <p class="subtitle">Choose your major</p>

      <div class="program-list">
        <div v-for="program in programs" :key="program.id" class="program-card">
          <div class="program-image">
            <img :src="program.image" :alt="program.name" />
          </div>
          <div class="program-body">
            <h3>{{ program.name }}</h3>
            <p>{{ program.description }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.programs-section {
  background-color: #ffffff;
  padding: 60px 20px;
  box-sizing: border-box;
}

.programs-container {
  max-width: 1100px;
  margin: 0 auto;
}

.programs-section h2 {
  font-size: 32px;
  margin: 0 0 10px;
  color: #183653;
}

.subtitle {
  color: #555;
  margin: 0 0 30px;
}

.program-list {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 340px));
  gap: 24px;
}

.program-card {
  background-color: #f4f7fb;
  border: 1px solid #dde5ee;
  border-radius: 10px;
  overflow: hidden;
}

.program-image {
  width: 100%;
  aspect-ratio: 1520 / 1360;
  background-color: #ffffff;
  border-bottom: 1px solid #dde5ee;
}

.program-image img {
  width: 100%;
  height: 100%;
  object-fit: contain;
  display: block;
}

.program-body {
  padding: 20px;
}

.program-body h3 {
  margin: 0 0 10px;
  color: #234b78;
}

.program-body p {
  margin: 0;
  color: #555;
  line-height: 1.6;
}
</style>