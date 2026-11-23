
<template>
  <section class="contact-section" id="contact">
    <div class="contact-container">
      <h2>Contact Us</h2>

      <p>
        Have questions about PresUniv Pekanbaru?
        Contact us through the links below.
      </p>

      <div class="contact-links">
        <a
          href="https://www.instagram.com/presunivpekanbaru/"
          target="_blank"
          rel="noopener noreferrer"
          class="contact-button"
        >
          Instagram
        </a>

        <a
          href="https://wa.me/6285942363468"
          target="_blank"
          rel="noopener noreferrer"
          class="contact-button"
        >
          WhatsApp
        </a>

        <a
          href="mailto:presuniv_pekanbaru@president.ac.id"
          class="contact-button"
        >
          Email
        </a>
      </div>
    </div>
  </section>
</template>

<style scoped>
.contact-section {
  width: 100%;
  padding: 80px 20px;
  background-color: #f4f7fb;
  text-align: center;
  box-sizing: border-box;
}

.contact-container {
  max-width: 800px;
  margin: 0 auto;
}

.contact-section h2 {
  font-size: 36px;
  margin: 0 0 18px;
  color: #183653;
}

.contact-section p {
  color: #555;
  font-size: 17px;
  line-height: 1.7;
  margin-bottom: 30px;
}

.contact-links {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 16px;
  flex-wrap: wrap;
}

.contact-button {
  display: inline-block;
  min-width: 130px;
  padding: 14px 24px;
  background-color: #234b78;
  color: white;
  border-radius: 8px;
  text-decoration: none;
  font-weight: 600;
  transition: background-color 0.3s ease;
}

.contact-button:hover {
  background-color: #183653;
}

@media (max-width: 600px) {
  .contact-section {
    padding: 55px 20px;
  }

  .contact-section h2 {
    font-size: 28px;
  }

  .contact-section p {
    font-size: 15px;
  }

  .contact-links {
    flex-direction: column;
    gap: 12px;
  }

  .contact-button {
    width: 100%;
    max-width: 260px;
    box-sizing: border-box;
  }
}
</style>
