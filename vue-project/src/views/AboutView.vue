<template>
  <main class="about-page">
    <section class="title-section">
      <h1>About Us</h1>
      <p class="subtitle">Learn more about our team</p>
    </section>

    <section class="body-section">
      <p>
        We are a team of passionate developers dedicated to building high-quality web applications.
        Our focus is on clean code, great user experiences, and modern development practices.
      </p>
      <p>
        Founded with the goal of making the web a better place, we work with clients across
        industries to deliver solutions that are both functional and beautiful. We believe in
        transparency, collaboration, and continuous improvement.
      </p>
    </section>
  </main>
</template>

<style scoped>
.about-page {
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

.body-section p {
  color: var(--color-text);
  line-height: 1.8;
  margin-bottom: 1.25rem;
}
</style>
