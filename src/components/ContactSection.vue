
<template>
  <section class="contact-section" id="contact">
    <h2>Contact Us</h2>

    <p>
      Have questions about our campus?
      Contact us through the links below.
    </p>

    <div class="contact-links">
      <a href="#" target="_blank">
        Instagram
      </a>

      <a href="#" target="_blank">
        WhatsApp
      </a>
    </div>
  </section>
</template>

<style scoped>
.contact-section {
  padding: 60px 20px;
  text-align: center;
  background-color: #f4f7fb;
}

.contact-section h2 {
  font-size: 32px;
  margin-bottom: 15px;
}

.contact-section p {
  color: #555;
  margin-bottom: 25px;
}

.contact-links {
  display: flex;
  justify-content: center;
  gap: 15px;
  flex-wrap: wrap;
}

.contact-links a {
  background-color: #234b78;
  color: white;
  padding: 12px 25px;
  border-radius: 8px;
  text-decoration: none;
}
</style>

<template>
  <footer class="footer">
    <div class="footer-content">

      <div class="footer-info">
        <h2>Campus Name</h2>
        <p>
          Discover your potential and build
          your future with us.
        </p>
      </div>

      <div class="footer-navigation">
        <h3>Quick Links</h3>
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#programs">Programs</a>
        <a href="#facilities">Facilities</a>
        <a href="#tuition">Tuition</a>
      </div>

      <div class="footer-contact">
        <h3>Contact Us</h3>
        <p>Instagram: Campus Account</p>
        <p>WhatsApp: Campus Contact</p>
      </div>

    </div>

    <div class="footer-bottom">
      <p>
        © 2026 Campus Name. All Rights Reserved.
      </p>
    </div>
  </footer>
</template>

<style scoped>
.footer {
  background-color: #183653;
  color: white;
  padding: 50px 30px 20px;
}

.footer-content {
  display: flex;
  justify-content: space-between;
  gap: 40px;
  flex-wrap: wrap;
  max-width: 1100px;
  margin: auto;
}

.footer-info,
.footer-navigation,
.footer-contact {
  flex: 1;
  min-width: 180px;
}

.footer h2,
.footer h3 {
  margin-bottom: 15px;
}

.footer p {
  color: #d5dce5;
  line-height: 1.6;
}

.footer-navigation {
  display: flex;
  flex-direction: column;
}

.footer-navigation a {
  color: #d5dce5;
  text-decoration: none;
  margin-bottom: 10px;
}

.footer-navigation a:hover {
  color: white;
}

.footer-bottom {
  border-top: 1px solid #52677d;
  text-align: center;
  margin-top: 35px;
  padding-top: 20px;
}
</style>
