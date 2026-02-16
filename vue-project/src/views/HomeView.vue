<template>
  <main class="home-page">
    <section class="title-section">
      <h1>Welcome to My Vue App</h1>
      <p class="subtitle">A modern web application built with Vue 3</p>
    </section>

    <section class="body-section">
      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt
        ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation
        ullamco laboris nisi ut aliquip ex ea commodo consequat.
      </p>
      <p>
        Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat
        nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia
        deserunt mollit anim id est laborum.
      </p>
      <p>
        Curabitur pretium tincidunt lacus. Nulla gravida orci a odio. Nullam varius, turpis et
        commodo pharetra, est eros bibendum elit, nec luctus magna felis sollicitudin mauris.
        Integer in mauris eu nibh euismod gravida. Duis ac tellus et risus vulputate vehicula.
        Donec lobortis risus a elit.
      </p>
    </section>
  </main>
</template>

<style scoped>
.home-page {
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
