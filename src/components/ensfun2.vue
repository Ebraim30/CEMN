<template>
  <section class="section animate-fadeInUp">
    <div class="container text-center">
      <h1 class="title mb-2">Ensino Fundamental II</h1>
      <p class="text mb-4">Desenvolvimento crítico e criativo dos alunos.</p>

      <div class="video-wrapper hover:scale-[1.01] transition-transform duration-300 ease-in-out">
        <iframe
          width="100%"
          height="315"
          src="https://www.youtube.com/embed/5MgBikgcWnY"
          title="Aprender a aprender"
          frameborder="0"
          allowfullscreen
        ></iframe>
      </div>

      <div class="mt-6 flex justify-center">
        <button class="btn-primary">Saiba mais</button>
      </div>
    </div>
  </section>
</template>

<style scoped>
@import './styles/shared.css';

.video-wrapper {
  margin-top: 2rem;
  border-radius: 1rem;
  overflow: hidden;
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
}

.btn-primary {
  background-color: #10b981;
  color: white;
  padding: 0.75rem 1.5rem;
  font-weight: 600;
  border-radius: 0.5rem;
  transition: all 0.3s ease;
}
.btn-primary:hover {
  background-color: #059669;
  transform: scale(1.05);
}
</style>
