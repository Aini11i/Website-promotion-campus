
<template>
  <footer class="footer">
    <div class="footer-content">
      <div class="footer-info">
        <h2>PresUniv Pekanbaru</h2>
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

        <p>
          Instagram:
          <a
            href="https://www.instagram.com/presunivpekanbaru/"
            target="_blank"
            rel="noopener noreferrer"
          >
            @presunivpekanbaru
          </a>
        </p>

        <p>
          WhatsApp:
          <a
            href="https://wa.me/6285942363468"
            target="_blank"
            rel="noopener noreferrer"
          >
            +62 859-4236-3468
          </a>
        </p>

        <p>
          Email:
          <a href="mailto:presuniv_pekanbaru@president.ac.id">
            presuniv_pekanbaru@president.ac.id
          </a>
        </p>
      </div>
    </div>

    <div class="footer-bottom">
      <p>
        © 2026 PresUniv Pekanbaru. All Rights Reserved.
      </p>
    </div>
  </footer>
</template>

<style scoped>
.footer {
  width: 100%;
  background-color: #183653;
  color: white;
  padding: 55px 5% 20px;
  box-sizing: border-box;
}

.footer-content {
  display: grid;
  grid-template-columns: 1.2fr 1fr 1.2fr;
  gap: 40px;
  max-width: 1200px;
  margin: 0 auto;
}

.footer-info,
.footer-navigation,
.footer-contact {
  min-width: 0;
}

.footer h2,
.footer h3 {
  margin: 0 0 18px;
}

.footer h2 {
  font-size: 27px;
}

.footer h3 {
  font-size: 21px;
}

.footer p {
  color: #d5dce5;
  line-height: 1.7;
  overflow-wrap: anywhere;
}

.footer-navigation {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}

.footer-navigation a,
.footer-contact a {
  color: #d5dce5;
  text-decoration: none;
  transition: color 0.3s ease;
}

.footer-navigation a {
  margin-bottom: 12px;
}

.footer-navigation a:hover,
.footer-contact a:hover {
  color: white;
  text-decoration: underline;
}

.footer-bottom {
  border-top: 1px solid #52677d;
  text-align: center;
  margin: 40px auto 0;
  padding-top: 18px;
  max-width: 1200px;
}

.footer-bottom p {
  margin-bottom: 0;
  font-size: 14px;
}

@media (max-width: 768px) {
  .footer-content {
    grid-template-columns: 1fr 1fr;
    gap: 30px;
  }

  .footer-info {
    grid-column: 1 / -1;
  }
}

@media (max-width: 480px) {
  .footer {
    padding: 40px 24px 20px;
  }

  .footer-content {
    grid-template-columns: 1fr;
    gap: 25px;
  }

  .footer-info {
    grid-column: auto;
  }

  .footer h2 {
    font-size: 24px;
  }

  .footer h3 {
    font-size: 19px;
  }
}
</style>