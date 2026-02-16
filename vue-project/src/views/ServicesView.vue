<template>
  <main class="services-page">
    <section class="title-section">
      <h1>Our Services</h1>
      <p class="subtitle">What we offer</p>
    </section>

    <section class="body-section">
      <div class="service-card">
        <h2>Web Development</h2>
        <p>
          We build modern, responsive web applications using the latest frameworks and
          technologies. From single-page applications to complex enterprise platforms, our team
          delivers performant and scalable solutions tailored to your needs.
        </p>
      </div>

      <div class="service-card">
        <h2>UI/UX Design</h2>
        <p>
          Great products start with great design. Our design process focuses on user research,
          wireframing, and prototyping to create interfaces that are both beautiful and intuitive.
        </p>
      </div>

      <div class="service-card">
        <h2>Consulting</h2>
        <p>
          Not sure where to start? We provide technical consulting to help you plan your project
          architecture, choose the right technology stack, and establish best practices for your
          development workflow.
        </p>
      </div>
    </section>
  </main>
</template>

<style scoped>
.services-page {
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

.service-card {
  background: var(--color-background-soft);
  border: 1px solid var(--color-border);
  border-radius: 8px;
  padding: 1.5rem;
  margin-bottom: 1.5rem;
}

.service-card h2 {
  color: var(--color-heading);
  font-size: 1.25rem;
  font-weight: 600;
  margin-bottom: 0.75rem;
}

.service-card p {
  color: var(--color-text);
  line-height: 1.7;
}
</style>
