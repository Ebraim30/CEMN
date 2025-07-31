<template>
  <section class="section animate-fadeInUp">
    <div class="container text-center">
      <h1 class="title mb-2">Ensino Médio</h1>
      <p class="text mb-4">Preparação completa para o ENEM e a vida.</p>

      <ul class="checklist">
        <li>🎯 Aulas interativas e com foco em resolução de problemas</li>
        <li>📝 Simulados e preparação intensiva</li>
        <li>💡 Apoio emocional e orientação vocacional</li>
      </ul>

      <div class="mt-6 flex justify-center">
        <button class="btn-primary">Conheça o Ensino Médio</button>
      </div>
    </div>
  </section>
</template>

<style scoped>
@import './styles/shared.css';

.checklist {
  margin-top: 2rem;
  text-align: left;
  list-style: none;
  padding-left: 0;
  color: #4b5563;
  font-size: 1.125rem;
  max-width: 700px;
  margin-left: auto;
  margin-right: auto;
}

.checklist li {
  margin-bottom: 1rem;
  background: #ffffff;
  padding: 0.75rem 1rem;
  border-left: 4px solid #059669;
  border-radius: 0.5rem;
  box-shadow: 0 5px 10px rgba(0, 0, 0, 0.05);
  transition: all 0.3s ease;
}
.checklist li:hover {
  background-color: #ecfdf5;
  transform: translateX(4px);
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
