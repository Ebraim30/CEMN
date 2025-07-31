<template>
  <section class="section animate-fadeInUp">
    <div class="container">
      <h1 class="title">Educação Infantil</h1>
      <p class="text">Desenvolvimento integral das crianças por meio do brincar e da imaginação.</p>
      <div class="cards">
        <div class="feature-card">
          <span class="emoji">🧩</span>
          <h3>Brincar com Sentido</h3>
          <p>Atividades lúdicas e pedagógicas que estimulam o raciocínio e a coordenação motora.</p>
        </div>
        <div class="feature-card">
          <span class="emoji">🌈</span>
          <h3>Ambiente Acolhedor</h3>
          <p>Espaços coloridos, seguros e preparados para acolher e estimular a criatividade.</p>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
@import './styles/shared.css';
.cards {
  display: flex;
  flex-wrap: wrap;
  gap: 2rem;
  justify-content: center;
  margin-top: 2rem;
}
.feature-card {
  background-color: #ffffff;
  border-radius: 1rem;
  padding: 1.5rem;
  max-width: 300px;
  text-align: center;
  box-shadow: 0 10px 15px rgba(0,0,0,0.1);
}
.emoji {
  font-size: 2.5rem;
  margin-bottom: 1rem;
}
</style>
