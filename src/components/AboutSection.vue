<script setup>
import data from '../data/kampusData.json'

const about = data.about

function hideBrokenImage(event) {
  event.target.style.display = 'none'
}
</script>

<template>
  <section class="about-section" id="about">
    <h2>About</h2>
    <p class="subtitle">Get to know us</p>

    <div class="block">
      <h3>Vision</h3>
      <p>{{ about.vision }}</p>
    </div>

    <div class="block">
      <h3>Mission</h3>
      <ul>
        <li v-for="(item, index) in about.mission" :key="index">{{ item }}</li>
      </ul>
    </div>

    <div class="block">
      <h3>History</h3>
      <div v-for="item in about.history" :key="item.year" class="history-item">
        <strong>{{ item.year }}</strong>
        <span>{{ item.text }}</span>
      </div>
    </div>

    <div class="block" v-if="about.team && about.team.length > 0">
      <h3>Leadership</h3>
      <div class="team">
        <div v-for="member in about.team" :key="member.role" class="member">
          <div class="photo">
            <img :src="member.photo" :alt="member.name" @error="hideBrokenImage" />
          </div>
          <p class="name">{{ member.name }}</p>
          <p class="role">{{ member.role }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.about-section {
  background-color: #f4f7fb;
  padding: 60px 20px;
  border-bottom: 1px solid #dde5ee;
}

.about-section > * {
  max-width: 1100px;
  margin-left: auto;
  margin-right: auto;
}

.about-section h2 {
  font-size: 32px;
  margin-top: 0;
  margin-bottom: 10px;
  color: #183653;
}

.subtitle {
  color: #555;
  margin-bottom: 30px;
}

.block {
  margin-bottom: 35px;
}

.block h3 {
  color: #234b78;
  margin-bottom: 10px;
}

.block p,
.block li {
  color: #555;
  line-height: 1.6;
}

.history-item {
  display: flex;
  gap: 16px;
  margin-bottom: 10px;
  color: #555;
}

.history-item strong {
  color: #183653;
}

.team {
  display: flex;
  flex-wrap: wrap;
  gap: 24px;
}

.member {
  width: 180px;
  text-align: center;
}

.photo {
  width: 100%;
  aspect-ratio: 3 / 4;
  background-color: #dde5ee;
  border-radius: 8px;
  overflow: hidden;
}

.photo img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: top;
  display: block;
}

.name {
  font-weight: bold;
  color: #183653;
  margin: 10px 0 0;
}

.role {
  margin: 4px 0 0;
}
</style>