<template>
  <div class="container">
    <!-- Header -->
    <header class="header">
      <div class="header-content">
        <div class="header-left">
          <div class="logo-circle">
            <div class="logo-inner-circle">
              <img src="@/assets/images/Design sem nome.png" alt="" class="logo-icon" />
            </div>
          </div>
          <div class="logo-text">
            <h1>CEMN</h1>
          </div>
        </div>

        <!-- Desktop Navigation -->
        <nav class="nav-desktop">
          <a href="#infantil">Educação Infantil</a>
          <a href="#fundamental1">Ensino Fundamental I</a>
          <a href="#fundamental2">Ensino Fundamental II</a>
          <a href="#medio">Ensino Médio</a>
          <button @click="openWhatsApp" class="btn-contact">CONTATOS</button>
        </nav>

        <!-- Mobile menu button -->
        <button @click="toggleMobileMenu" class="btn-mobile-menu" aria-label="Abrir menu mobile">
          <MenuIcon v-if="!mobileMenuOpen" class="icon" />
          <XIcon v-else class="icon" />
        </button>
      </div>

      <!-- Mobile Navigation -->
      <div v-if="mobileMenuOpen" class="mobile-menu">
        <a href="#infantil">Educação Infantil</a>
        <a href="#fundamental1">Ensino Fundamental I</a>
        <a href="#fundamental2">Ensino Fundamental II</a>
        <a href="#medio">Ensino Médio</a>
        <button @click="openWhatsApp" class="btn-contact-mobile">CONTATOS</button>
      </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
      <div class="hero-content">
        <div class="hero-left">
          <div class="hero-icon-circle">
            <span class="hero-icon">🌱</span>
          </div>
          <div>
            <h1 class="hero-title">
              COLÉGIO<br />
              <span class="hero-title-highlight">MÃE NATUREZA</span>
            </h1>
          </div>
          <p class="hero-description">
            Educação de qualidade baseada em valores cristãos, estimulando o desenvolvimento
            integral através de metodologias inovadoras como STEAM, Montessori e Waldorf.
          </p>

          <div class="hero-buttons">
            <button @click="openWhatsApp" class="btn-whatsapp">
              <MessageCircleIcon class="icon-sm" />
              <span>Fale Conosco</span>
            </button>
            <button class="btn-saiba-mais">Nossa Historia</button>
          </div>
        </div>

        <div class="hero-right">
          <div class="hero-image-wrapper">
            <img
              src="../public/foto1.jpg"
              alt="Crianças aprendendo na natureza"
              class="hero-image"
            />
            <div class="heart-icon-wrapper">
              <HeartIcon class="icon-lg" />
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- About Section -->
    <section class="about">
      <div class="about-content">
        <div class="about-header">
          <h2>Nossa Missão</h2>
          <p>Proporcionar educação de qualidade centrada nos valores do amor, fé e dedicação</p>
        </div>

        <div class="about-cards">
          <div class="card">
            <div class="card-icon bg-emerald-light">
              <BookOpenIcon class="icon-md emerald" />
            </div>
            <h3>Metodologias Inovadoras</h3>
            <p>STEAM, Reggio Emilia, Maria Montessori e Pedagogia Waldorf</p>
          </div>

          <div class="card">
            <div class="card-icon bg-fuchsia-light">
              <HeartIcon class="icon-md fuchsia" />
            </div>
            <h3>Valores Cristãos</h3>
            <p>Educação baseada no amor, fé e responsabilidade</p>
          </div>

          <div class="card">
            <div class="card-icon bg-blue-light">
              <UsersIcon class="icon-md blue" />
            </div>
            <h3>Desenvolvimento Integral</h3>
            <p>Formação intelectual, emocional e social completa</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Education Levels -->
    <section class="education-levels">
      <div class="education-content">
        <div class="education-header">
          <h2>Níveis de Ensino</h2>
          <p>Da educação infantil ao Ensino Médio</p>
        </div>

        <div class="education-cards">
          <div class="edu-card">
            <div class="edu-icon">👶</div>
            <h3>Educação Infantil</h3>
            <p>Desenvolvimento através do brincar</p>
          </div>
          <div class="edu-card">
            <div class="edu-icon">📚</div>
            <h3>Fundamental I</h3>
            <p>Base sólida para o aprendizado</p>
          </div>
          <div class="edu-card">
            <div class="edu-icon">🎓</div>
            <h3>Fundamental II</h3>
            <p>Preparação para novos desafios</p>
          </div>
          <div class="edu-card">
            <div class="edu-icon">🚀</div>
            <h3>Ensino Médio</h3>
            <p>Preparação para o futuro</p>
          </div>
        </div>
      </div>
    </section>

    <!-- CTA Section -->
    <section class="cta">
      <div class="cta-content">
        <h2>Faça Parte da Nossa Família Educacional</h2>
        <p>
          Entre em contato e descubra como podemos contribuir para o desenvolvimento do seu filho
        </p>
        <button @click="openWhatsApp" class="btn-whatsapp-large">
          <MessageCircleIcon class="icon-md" />
          <span>Conversar no WhatsApp</span>
        </button>
      </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
      <div class="footer-content">
        <div class="footer-left">
          <div class="footer-logo-circle">
            <span class="logo-icon-white">🌱</span>
          </div>
          <div>
            <h3>Colégio Mãe Natureza</h3>
            <span>Educação com amor e dedicação</span>
          </div>
        </div>

        <div class="footer-menu">
          <h4>Níveis de Ensino</h4>
          <ul>
            <li>Educação Infantil</li>
            <li>Ensino Fundamental I</li>
            <li>Ensino Fundamental II</li>
            <li>Ensino Médio</li>
          </ul>
        </div>

        <div class="footer-contact">
          <h4>Contato</h4>
          <button @click="openWhatsApp" class="btn-contact-footer">
            <MessageCircleIcon class="icon-sm" />
            <span>WhatsApp</span>
          </button>
        </div>
      </div>

      <div class="footer-bottom">
        <p>© 2024 Colégio Mãe Natureza. Todos os direitos reservados.</p>
      </div>
    </footer>

    <!-- WhatsApp Float Button -->
    <div class="whatsapp-float-btn">
      <button @click="openWhatsApp" aria-label="Abrir WhatsApp" class="btn-whatsapp-float">
        <MessageCircleIcon class="icon-md" />
      </button>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import {
  MenuIcon,
  XIcon,
  MessageCircleIcon,
  BookOpenIcon,
  HeartIcon,
  UsersIcon,
} from 'lucide-vue-next'

const mobileMenuOpen = ref(false)
const toggleMobileMenu = () => {
  mobileMenuOpen.value = !mobileMenuOpen.value
}
const openWhatsApp = () => {
  const phoneNumber = '5511999999999'
  const message = 'Olá! Gostaria de saber mais informações sobre o Colégio Mãe Natureza.'
  const whatsappUrl = `https://wa.me/${phoneNumber}?text=${encodeURIComponent(message)}`
  window.open(whatsappUrl, '_blank')
}
</script>

<style scoped>
*, body, html {
  margin: 0%;
  padding: 0%;
}

/* Reset para html e body */
html,
body {
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100%;
  overflow-x: hidden;
}

/* Container */
.container {
  min-height: 100vh;
  width: 100%;
  font-family: 'Inter', sans-serif;
}

/* Header */
.header {
  background-color: #059669; /* emerald-500 */
  box-shadow:
    0 10px 15px -3px rgba(5, 150, 105, 0.4),
    0 4px 6px -4px rgba(5, 150, 105, 0.3);
  position: sticky;
  top: 0;
  z-index: 50;
  padding: 0 1rem;
}
.header-content {
  max-width: 112rem;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 4rem;
}
.header-left {
  display: flex;
  align-items: center;
  gap: 0.75rem;
}
.logo-circle {
  width: 3rem;
  height: 3rem;
  background-color: white;
  border-radius: 9999px;
  display: flex;
  justify-content: center;
  align-items: center;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}
.logo-inner-circle {
  width: 2rem;
  height: 2rem;
  background-color: #059669; /* emerald-500 */
  border-radius: 9999px;
  display: flex;
  justify-content: center;
  align-items: center;
}
.logo-icon {
  color: white;
  width: 200%;
}

/* Logo text */
.logo-text h1 {
  font-size: 1.25rem;
  font-weight: 700;
  color: white;
}
.subtitle {
  color: #d1fae5; /* emerald-100 */
  font-size: 0.875rem;
  font-weight: 500;
}

/* Navigation desktop */
.nav-desktop {
  display: none;
  align-items: center;
  gap: 2rem;
}
.nav-desktop a {
  color: white;
  font-size: 0.875rem;
  font-weight: 500;
  text-decoration: none;
  transition: color 0.3s;
}
.nav-desktop a:hover {
  color: #d1fae5; /* emerald-100 */
}
.btn-contact {
  background-color: #963266; /* fuchsia-600 */
  color: white;
  padding: 0.5rem 1.5rem;
  border-radius: 9999px;
  font-size: 0.875rem;
  font-weight: 600;
  cursor: pointer;
  border: none;
  transition:
    background-color 0.3s,
    transform 0.3s;
}
.btn-contact:hover {
  background-color: #812b58; /* fuchsia-700 */
  transform: scale(1.05);
}

/* Mobile menu button */
.btn-mobile-menu {
  display: inline-flex;
  padding: 0.5rem;
  color: white;
  background: none;
  border: none;
  cursor: pointer;
}

/* Icons */
.icon {
  height: 1.5rem;
  width: 1.5rem;
}

/* Mobile menu */
.mobile-menu {
  display: flex;
  flex-direction: column;
  gap: 0.75rem;
  padding: 1rem 0;
  border-top: 1px solid #059669; /* emerald-400 */
}
.mobile-menu a {
  color: white;
  font-size: 0.875rem;
  font-weight: 500;
  text-decoration: none;
}
.btn-contact-mobile {
  background-color: #963266;
  color: white;
  padding: 0.5rem 1rem;
  border-radius: 9999px;
  font-size: 0.875rem;
  font-weight: 600;
  cursor: pointer;
  border: none;
  width: fit-content;
}

/* Hero Section */
.hero {
  background: linear-gradient(135deg, #34d399 0%, #10b981 50%, #047857 100%);
  padding: 5rem 1rem;
  color: white;
}
.hero-content {
  max-width: 112rem;
  margin: 0 auto;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 3rem;
  align-items: center;
}
.hero-left {
  max-width: 40rem;
}
.hero-icon-circle {
  width: 4rem;
  height: 4rem;
  background: white;
  border-radius: 9999px;
  display: flex;
  justify-content: center;
  align-items: center;
  box-shadow: 0 10px 15px rgba(0, 0, 0, 0.15);
  margin-bottom: 1.5rem;
}
.hero-icon {
  color: #059669;
  font-size: 2rem;
}
.hero-title {
  font-size: 3rem;
  font-weight: 800;
  line-height: 1.1;
  margin-bottom: 1rem;
}
.hero-title-highlight {
  color: #d1fae5;
}
.hero-description {
  font-size: 1.125rem;
  line-height: 1.6;
  margin-bottom: 2rem;
  max-width: 28rem;
}
.hero-buttons {
  display: flex;
  gap: 1rem;
  flex-wrap: wrap;
}
.btn-whatsapp {
  background-color: white;
  color: #059669;
  padding: 1rem 2rem;
  border-radius: 9999px;
  font-weight: 700;
  display: flex;
  align-items: center;
  gap: 0.5rem;
  box-shadow: 0 10px 15px rgba(0, 0, 0, 0.15);
  cursor: pointer;
  border: none;
  transition:
    background-color 0.3s,
    transform 0.3s;
}
.btn-whatsapp:hover {
  background-color: #ecfdf5;
  transform: scale(1.05);
}
.btn-saiba-mais {
  border: 2px solid white;
  background: none;
  color: white;
  padding: 1rem 2rem;
  border-radius: 9999px;
  font-weight: 700;
  cursor: pointer;
  transition:
    background-color 0.3s,
    color 0.3s;
}
.btn-saiba-mais:hover {
  background-color: white;
  color: #059669;
}

/* Hero image */
.hero-right {
  display: flex;
  justify-content: flex-end;
}
.hero-image-wrapper {
  position: relative;
  width: 24rem;
  height: 24rem;
  border-radius: 9999px;
  overflow: hidden;
  box-shadow: 0 25px 50px rgba(0, 0, 0, 0.25);
  border: 8px solid rgba(255 255 255 / 0.2);
}
.hero-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
.heart-icon-wrapper {
  position: absolute;
  bottom: -1rem;
  right: -1rem;
  width: 6rem;
  height: 6rem;
  background-color: #963266;
  border-radius: 9999px;
  display: flex;
  justify-content: center;
  align-items: center;
  box-shadow: 0 10px 25px #963266b9;
}
.icon-lg {
  color: white;
  width: 3rem;
  height: 3rem;
}

/* About Section */
.about {
  padding: 5rem 1rem;
  background-color: #f9fafb;
  margin: 0  !important;
}
.about-content {
  max-width: 112rem;
  margin: 0 auto;
}
.about-header {
  text-align: center;
  margin-bottom: 4rem;
}
.about-header h2 {
  font-size: 2.5rem;
  font-weight: 700;
  color: #111827;
  margin-bottom: 1rem;
}
.about-header p {
  font-size: 1.25rem;
  color: #4b5563;
  max-width: 48rem;
  margin-left: auto;
  margin-right: auto;
}
.about-cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
}
.card {
  background-color: white;
  padding: 2rem;
  border-radius: 1rem;
  box-shadow: 0 10px 15px rgba(0, 0, 0, 0.1);
  text-align: center;
  transition: box-shadow 0.3s;
  cursor: default;
}
.card:hover {
  box-shadow: 0 20px 30px rgba(0, 0, 0, 0.15);
}
.card-icon {
  width: 4rem;
  height: 4rem;
  margin-bottom: 1.5rem;
  border-radius: 9999px;
  display: flex;
  justify-content: center;
  align-items: center;
  margin-left: auto;
  margin-right: auto;
}
.bg-emerald-light {
  background-color: #d1fae5;
}
.bg-fuchsia-light {
  background-color: #9632665d;
}
.bg-blue-light {
  background-color: #dbeafe;
}
.icon-md {
  width: 2rem;
  height: 2rem;
}
.emerald {
  color: #059669;
}
.fuchsia {
  color: #963266;
}
.blue {
  color: #2563eb;
}
.card h3 {
  font-size: 1.25rem;
  font-weight: 700;
  color: #111827;
  margin-bottom: 0.75rem;
}
.card p {
  color: #4b5563;
  font-size: 1rem;
}

/* Education Levels Section */
.education-levels {
  padding: 5rem 1rem;
  background-color: #963266; /* fuchsia-600 */
  color: white;
}
.education-content {
  max-width: 112rem;
  margin: 0 auto;
}
.education-header {
  text-align: center;
  margin-bottom: 4rem;
}
.education-header h2 {
  font-size: 2.5rem;
  font-weight: 700;
  margin-bottom: 0.75rem;
}
.education-header p {
  font-size: 1.25rem;
  color: #f5d0fe; /* fuchsia-100 */
}

/* Education cards grid */
.education-cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
  gap: 1.5rem;
}
.edu-card {
  background-color: rgba(255 255 255 / 0.1);
  backdrop-filter: blur(8px);
  padding: 1.5rem;
  border-radius: 1rem;
  text-align: center;
  cursor: pointer;
  transition: background-color 0.3s;
}
.edu-card:hover {
  background-color: rgba(255 255 255 / 0.2);
}
.edu-icon {
  font-size: 2.5rem;
  margin-bottom: 1rem;
  user-select: none;
}
.edu-card h3 {
  font-weight: 700;
  font-size: 1.25rem;
  margin-bottom: 0.5rem;
}
.edu-card p {
  font-size: 0.875rem;
  color: #f5d0fe;
}

/* CTA Section */
.cta {
  padding: 5rem 1rem;
  background-color: #059669; /* emerald-500 */
  color: white;
  text-align: center;
}
.cta-content {
  max-width: 64rem;
  margin: 0 auto;
}
.cta h2 {
  font-size: 2.5rem;
  font-weight: 700;
  margin-bottom: 1.5rem;
}
.cta p {
  font-size: 1.25rem;
  margin-bottom: 2.5rem;
  color: #d1fae5;
}
.btn-whatsapp-large {
  background-color: white;
  color: #059669;
  padding: 1.25rem 2.5rem;
  border-radius: 9999px;
  font-weight: 700;
  display: inline-flex;
  align-items: center;
  gap: 0.75rem;
  box-shadow: 0 10px 15px rgba(0, 0, 0, 0.15);
  cursor: pointer;
  border: none;
  transition:
    background-color 0.3s,
    transform 0.3s;
}
.btn-whatsapp-large:hover {
  background-color: #ecfdf5;
  transform: scale(1.05);
}

/* Footer */
.footer {
  background-color: #111827; /* gray-900 */
  color: white;
  padding: 4rem 1rem;
}
.footer-content {
  max-width: 112rem;
  margin: 0 auto;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 2rem;
}
.footer-left {
  display: flex;
  gap: 1rem;
  align-items: center;
}
.footer-logo-circle {
  width: 3rem;
  height: 3rem;
  background-color: #059669; /* emerald-500 */
  border-radius: 9999px;
  display: flex;
  justify-content: center;
  align-items: center;
}
.logo-icon-white {
  color: white;
  font-size: 1.125rem;
  font-weight: 700;
}
.footer-left h3 {
  font-size: 1.25rem;
  font-weight: 700;
}
.footer-left span {
  color: #9ca3af; /* gray-400 */
}
.footer-menu h4,
.footer-contact h4 {
  font-size: 1.125rem;
  font-weight: 600;
  margin-bottom: 1rem;
}
.footer-menu ul {
  list-style: none;
  padding: 0;
  margin: 0;
  color: #9ca3af;
}
.footer-menu li {
  margin-bottom: 0.5rem;
}
.btn-contact-footer {
  background-color: #059669;
  padding: 0.75rem 1.5rem;
  border-radius: 9999px;
  font-weight: 600;
  color: white;
  cursor: pointer;
  border: none;
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  transition: background-color 0.3s;
}
.btn-contact-footer:hover {
  background-color: #047857;
}

/* Footer bottom */
.footer-bottom {
  border-top: 1px solid #1f2937; /* gray-800 */
  margin-top: 3rem;
  padding-top: 2rem;
  text-align: center;
  color: #9ca3af;
}

/* WhatsApp Float Button */
.whatsapp-float-btn {
  position: fixed;
  bottom: 1.5rem;
  right: 1.5rem;
  z-index: 50;
}
.btn-whatsapp-float {
  background-color: #22c55e; /* green-500 */
  color: white;
  padding: 1rem;
  border-radius: 9999px;
  box-shadow: 0 25px 50px rgba(34, 197, 94, 0.7);
  cursor: pointer;
  border: none;
  transition:
    background-color 0.3s,
    transform 0.3s;
  animation: pulse 2s infinite;
  display: flex;
  align-items: center;
  justify-content: center;
}
.btn-whatsapp-float:hover {
  background-color: #16a34a; /* green-600 */
  transform: scale(1.1);
}

/* Icon sizes */
.icon-sm {
  width: 1.25rem;
  height: 1.25rem;
}
.icon-md {
  width: 1.5rem;
  height: 1.5rem;
}

/* Scroll suave */
html {
  scroll-behavior: smooth;
}

/* Animações personalizadas */
@keyframes pulse {
  0%,
  100% {
    opacity: 1;
    transform: scale(1);
  }
  50% {
    opacity: 0.75;
    transform: scale(1.1);
  }
}
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
.animate-fadeInUp {
  animation: fadeInUp 0.6s ease-out;
}

/* Gradientes personalizados */
.bg-gradient-custom {
  background: linear-gradient(135deg, #10b981 0%, #059669 100%);
}

/* Media queries para mostrar nav desktop e esconder mobile em telas maiores */
@media (min-width: 1024px) {
  .nav-desktop {
    display: flex;
  }
  .btn-mobile-menu,
  .mobile-menu {
    display: none !important;
  }
}
</style>
