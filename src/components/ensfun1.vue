<template>
  <section class="section animate-fadeInUp">
    <div class="container">
      <h1 class="title">Ensino Fundamental I</h1>
      <p class="text">Base sólida para o aprendizado com apoio de jogos e gamificação.</p>
      <div class="quiz-box">
        <h3>Quiz Interativo</h3>
        <p>Qual a capital do Brasil?</p>
        <button class="quiz-btn">Rio de Janeiro</button>
        <button class="quiz-btn">São Paulo</button>
        <button class="quiz-btn">Brasília ✅</button>
      </div>
    </div>
  </section>
</template>

<style scoped>
@import './styles/shared.css';
.quiz-box {
  background: #fff;
  margin-top: 2rem;
  padding: 1.5rem;
  border-radius: 1rem;
  box-shadow: 0 10px 20px rgba(0,0,0,0.1);
}
.quiz-btn {
  background: #059669;
  color: white;
  padding: 0.75rem 1rem;
  margin: 0.5rem;
  border-radius: 9999px;
  border: none;
  cursor: pointer;
  transition: transform 0.2s;
}
.quiz-btn:hover {
  transform: scale(1.05);
}
</style>