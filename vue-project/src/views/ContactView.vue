<template>
  <main class="contact-page">
    <section class="title-section">
      <h1>Contact Us</h1>
      <p class="subtitle">Get in touch with our team</p>
    </section>

    <section class="body-section">
      <p>
        We would love to hear from you. Whether you have a question about our services, need a
        quote, or just want to say hello, feel free to reach out using the information below.
      </p>

      <div class="contact-info">
        <div class="contact-item">
          <h3>Email</h3>
          <p>hello@example.com</p>
        </div>
        <div class="contact-item">
          <h3>Phone</h3>
          <p>(555) 123-4567</p>
        </div>
        <div class="contact-item">
          <h3>Address</h3>
          <p>123 Main Street, Suite 100<br />Anytown, USA 12345</p>
        </div>
      </div>
    </section>
  </main>
</template>

<style scoped>
.contact-page {
  max-width: 800px;
  margin: 0 auto;
  padding: 2rem 1.5rem;
}

.title-section {
  margin-bottom: 2.5rem;
}

.title-section h1 {
  color: var(--color-heading);
  font-size: 2rem;
  font-weight: 700;
  margin-bottom: 0.5rem;
}

.subtitle {
  color: var(--color-text);
  font-size: 1.1rem;
}

.body-section > p {
  color: var(--color-text);
  line-height: 1.7;
  margin-bottom: 2rem;
}

.contact-info {
  display: grid;
  gap: 1.5rem;
}

.contact-item {
  background: var(--color-background-soft);
  border: 1px solid var(--color-border);
  border-radius: 8px;
  padding: 1.25rem 1.5rem;
}

.contact-item h3 {
  color: var(--color-heading);
  font-size: 1rem;
  font-weight: 600;
  margin-bottom: 0.5rem;
}

.contact-item p {
  color: var(--color-text);
  line-height: 1.6;
}
</style>
