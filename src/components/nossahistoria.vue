<template>
  <section class="section animate-fadeInUp">
    <div class="container">
      <h1 class="title">Nossa História</h1>
      <p class="text mb-8">
        O Colégio Mãe Natureza nasceu com a missão de transformar vidas por meio de uma educação
        baseada em amor, fé e dedicação.
      </p>
      <div class="timeline">
        <div class="timeline-item">
          <span class="year">2010</span>
          <p>Fundação da escola com turmas de Educação Infantil.</p>
        </div>
        <div class="timeline-item">
          <span class="year">2015</span>
          <p>Ampliação para o Ensino Fundamental I e implementação do método Montessori.</p>
        </div>
        <div class="timeline-item">
          <span class="year">2020</span>
          <p>Início do Ensino Médio com foco em ENEM e cidadania.</p>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.section {
  padding: 4rem 1rem;
  background-color: #f9fafb;
}
.container {
  max-width: 800px;
  margin: 0 auto;
  text-align: center;
}
.title {
  font-size: 2.5rem;
  font-weight: 700;
  margin-bottom: 2rem;
  color: #059669;
}
.text {
  font-size: 1.125rem;
  line-height: 1.8;
  color: #4b5563;
}
.timeline {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
  text-align: left;
  margin-top: 2rem;
}
.timeline-item {
  background: white;
  padding: 1rem;
  border-left: 4px solid #059669;
  border-radius: 0.5rem;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
}
.year {
  font-weight: 700;
  color: #059669;
}
</style>
