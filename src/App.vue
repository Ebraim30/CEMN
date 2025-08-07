<template>
<div class="container">
  <!-- Header -->
  <header class="header">
    <div class="header-content">
      <div class="header-left" @click="currentPage = 'home'">
        <div class="logo-circle">
          <div class="logo-inner-circle">
            <img src="../public/logo.png" alt="" class="logo-icon" />
          </div>
        </div>
        <div class="logo-text">
          <h1>CEMN</h1>
        </div>
      </div>
      <!-- Desktop Navigation -->
      <nav class="nav-desktop">
        <a @click="currentPage = 'educainf'">Educação Infantil</a>
        <a @click="currentPage = 'ensfun1'">Ensino Fundamental I</a>
        <a @click="currentPage = 'ensfun2'">Ensino Fundamental II</a>
        <a @click="currentPage = 'ensmed'">Ensino Médio</a>
        <button @click="openWhatsApp" class="btn-contact">CONTATO</button>
      </nav>
      <!-- Mobile menu button -->
      <button @click="toggleMobileMenu" class="btn-mobile-menu" aria-label="Abrir menu mobile">
        <MenuIcon v-if="!mobileMenuOpen" class="icon" />
        <XIcon v-else class="icon" />
      </button>
    </div>
    <!-- Mobile Navigation -->
    <div v-if="mobileMenuOpen" class="mobile-menu">
      <a @click="currentPage = 'educainf'; mobileMenuOpen = false">Educação Infantil</a>
      <a @click="currentPage = 'ensfun1'; mobileMenuOpen = false">Ensino Fundamental I</a>
      <a @click="currentPage = 'ensfun2'; mobileMenuOpen = false">Ensino Fundamental II</a>
      <a @click="currentPage = 'ensmed'; mobileMenuOpen = false">Ensino Médio</a>
      <button @click="openWhatsApp" class="btn-contact-mobile">CONTATO</button>
    </div>
  </header>

  <!-- HOME PAGE -->
  <div v-if="currentPage === 'home'">
    <!-- Hero Section -->
    <section class="hero">
      <div class="hero-content">
        <div class="hero-left">
          <div class="hero-icon-circle">
            <img src="../public/logo.png" alt="Logo" class="hero-icon" />
          </div>
          <div>
            <h1 class="hero-title">
              COLÉGIO<br />
              <span class="hero-title-highlight">MÃE NATUREZA</span>
            </h1>
          </div>
          <h3>Segurança para crescer com confiança</h3>
          <p class="hero-description">
           Cuidar é parte do nosso DNA. Aqui, cada ambiente é pensado para acolher, proteger e estimular. Garantimos uma jornada de aprendizagem estruturada, com acompanhamento contínuo, tecnologia segura e equipe comprometida com o desenvolvimento integral do aluno.
          </p>
          <p class="hero-description">Mais que uma escola, somos um <strong>espaço de crescimento com valores, fé, respeito e propósito.  </strong></p>
        
          <div class="hero-buttons">
            <button @click="openWhatsApp" class="btn-whatsapp">
              <MessageCircleIcon class="icon-sm" />
              <span>Fale Conosco</span>
            </button>
            <button @click="currentPage = 'nossahistoria'" class="btn-saiba-mais">Nossa História</button>
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
          <p>Educar com princípios, inovação e acolhimento - formando seres homanos íntegros para transformar o mundo com propósito. </p>
        </div>
        <div class="about-cards">
          
          <div class="card">
            <div class="card-icon bg-fuchsia-light">
              <HeartIcon class="icon-md fuchsia" />
            </div>
            <h3>Formar com valores cristãos e caráter sólido</h3>
            <p>Promovemos uma educação fundamentada na Bíblia e nos princípios do Projeto Caráter Conta, cultivando o respeito, a responsabilidade, a cidadania, o zelo, a justiça e a sinceridade como base da convivência e da construção de um mundo melhor</p>
          </div>
          <div class="card">
            <div class="card-icon bg-emerald-light">
              <BookOpenIcon class="icon-md emerald" />
            </div>
            <h3>Ensinar com excelência pedagógica e inovação consciente</h3>
        
            <p>Unimos  metodologias ativas, STEAM, Reggio Emilia e Tecnologia Educacional para desenvolver o pensamento crítico, a criatividade, o protagonismo e o espírito investigativo - preparando nossos alunos para os desafios do século XXI, sem perder o sentido e a essência.</p>
          </div>
          <div class="card">
            <div class="card-icon bg-blue-light">
              <UsersIcon class="icon-md blue" />
            </div>
            <h3>Acolyher com amor, escuta e intencionalidade</h3>
            <p>Cuidamos do ser humano em sua totalidade - corpo, mente, emoções e espírito. Nossa Missão é criar um ambiente seguro, afetivo e inspirador, onde cada aluno se sinta visto, valorizado e desafiado a florescer com propósito.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Education Levels -->
    <section class="education-levels">
      <div class="education-content">
        <div class="education-header">
          <h2>Níveis de Ensino</h2>
          <p>Da Educação Infantil ao Ensino Médio</p>
        </div>
        <div class="education-cards">
          <div class="edu-card" @click="currentPage = 'educainf'">
            <div class="edu-icon">👶</div>
            <h3>Educação Infantil</h3>
            <p>Desenvolvimento através do brincar</p>
          </div>
          <div class="edu-card" @click="currentPage = 'ensfun1'">
            <div class="edu-icon">📚</div>
            <h3>Fundamental I</h3>
            <p>Base sólida para o aprendizado</p>
          </div>
          <div class="edu-card" @click="currentPage = 'ensfun2'">
            <div class="edu-icon">🎓</div>
            <h3>Fundamental II</h3>
            <p>Preparação para novos desafios</p>
          </div>
          <div class="edu-card" @click="currentPage = 'ensmed'">
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
  </div>

  <!-- NOSSA HISTÓRIA PAGE -->
  <div v-if="currentPage === 'nossahistoria'">
    <div class="page-header">
      <button @click="currentPage = 'home'" class="btn-back">
        <ArrowLeftIcon class="icon-sm" />
        Voltar ao Início
      </button>
    </div>
    
    <section class="page-hero">
      <div class="page-hero-content">
        <div class="page-hero-icon">📖</div>
        <h1>Nossa História</h1>
        <p>Uma jornada de dedicação à educação de qualidade</p>
      </div>
    </section>

    <section class="historia-content">
      <div class="historia-container">
        <div class="historia-grid">
          <div class="historia-text">
            <h2>Nossos Valores</h2>
            <p>
              O Centro Educacional Mãe Natureza (CEMN) é uma instituição fundamentada em perseverança, fé e dedicação, 
              centrada nos valores do amor. Priorizando Educação, Inclusão Social, Princípios Cristãos e Sustentabilidade.
            </p>
            <div class="valores-list">
              <div class="valor-item">
                <div class="valor-check">✓</div>
                <span>Educação de qualidade</span>
              </div>
              <div class="valor-item">
                <div class="valor-check">✓</div>
                <span>Valores cristãos</span>
              </div>
              <div class="valor-item">
                <div class="valor-check">✓</div>
                <span>Sustentabilidade</span>
              </div>
            </div>
          </div>
          <div class="historia-image">  
            <img src="../public/foto2.jpg" alt="História da escola" />
          </div>
        </div>

        <div class="metodologias-section">
          <h2>Metodologias Utilizadas</h2>
          <div class="metodologias-grid">
            <div class="metodologia-card">
              <div class="metodologia-icon">S</div>
              <h3>STEAM</h3>
              <p>Ciência, Tecnologia, Engenharia, Arte e Matemática</p>
            </div>
            <div class="metodologia-card">
              <div class="metodologia-icon">R</div>
              <h3>Reggio Emilia</h3>
              <p>Abordagem educacional inovadora</p>
            </div>
            <div class="metodologia-card">
              <div class="metodologia-icon">M</div>
              <h3>Montessori</h3>
              <p>Método de ensino personalizado</p>
            </div>
            
          </div>
        </div>
      </div>
    </section>
  </div>

  <!-- EDUCAÇÃO INFANTIL PAGE -->
  <div v-if="currentPage === 'educainf'">
    <div class="page-header">
      <button @click="currentPage = 'home'" class="btn-back">
        <ArrowLeftIcon class="icon-sm" />
        Voltar ao Início
      </button>
    </div>
    
    <section class="page-hero">
      <div class="page-hero-content">
        <div class="page-hero-icon">👶</div>
        <h1>Educação Infantil - Onde o aprender florece com afeto</h1>
        <p>Do brincar ao conhecer, cada detalhe é pensado para encantar</p>
      </div>
    </section>

    <section class="educainf-content">
      <div class="educainf-container">
        <div class="educainf-grid">
          <div class="educainf-image">
            <img src="../public/foto3.jpg" alt="Educação Infantil" />
          </div>
          <div class="educainf-text">
            <h2>Nossa Abordagem</h2>
            <p>
              Na Educação Infantil, priorizamos o desenvolvimento integral da criança através de atividades lúdicas, 
              respeitando o tempo e as características individuais de cada aluno.
            </p>
            <div class="abordagem-list">
              <div class="abordagem-item">
                <div class="abordagem-check">✓</div>
                <div>
                  <h3>Aprendizado através do brincar</h3>
                  <p>Atividades lúdicas que estimulam o desenvolvimento</p>
                </div>
              </div>
              <div class="abordagem-item">
                <div class="abordagem-check">✓</div>
                <div>
                  <h3>Desenvolvimento socioemocional</h3>
                  <p>Formação de valores e habilidades sociais</p>
                </div>
              </div>
              <div class="abordagem-item">
                <div class="abordagem-check">✓</div>
                <div>
                  <h3>Estímulo à criatividade</h3>
                  <p>Atividades artísticas e expressivas</p>
                </div>
              </div>
            </div>
          </div>
        </div>

        <div class="atividades-section">
          <div class="atividades-grid">
            <div class="atividade-card">
              <div class="atividade-icon">🎨</div>
              <h3>Desinvolvimento global e intencional</h3>
              <p>A Educação Infantil no Colégio Mãe Natureza é fundamentada na abordagem Reggio Emilia, no brincar como linguagem essencial da infância e em propostas baseadas nas <strong>Metodologias Ativas.</strong></p>
            <p>O ambiente é organizado para promover <strong>curiosidade, criatividade e autonomia,</strong> respeitando os ritmos individuais. Cada atividade tem um propósito pedagógico claro aliado ao desenvolvimento das funções cognitivas, motoras e socioemocionais.</p>
            </div>
            <div class="atividade-card">
              <div class="atividade-icon">🌱</div>
              <h3>Afeto e vínculos que ensinam</h3>
              <p>Aqui, cada criança é vista como única e potente. O acolhimento amoroso, o cuidadfo diário e o vínculo com os educadores criam um ambiente seguro e estimulante. As descobertqs são celebradas com entusiasmo, e a família é parceira em cada passo da jornada.</p>
            </div>
            <div class="atividade-card">
              <div class="atividade-icon">👥</div>
              <h3>Segurança, rotina e acolhimento</h3>
              <p>Ambientes planejados, alimentação supervisionada, rotina estruturada e uma equipe comprometida com o bem-estar da criança garantem tranquilidade às famílias. Formamos com amor princípios e propósitos - desde os primeiros passos.</p>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>

  <!-- ENSINO FUNDAMENTAL I PAGE -->
  <div v-if="currentPage === 'ensfun1'">
    <div class="page-header">
      <button @click="currentPage = 'home'" class="btn-back">
        <ArrowLeftIcon class="icon-sm" />
        Voltar ao Início
      </button>
    </div>
    
    <section class="page-hero">
      <div class="page-hero-content">
        <div class="page-hero-icon">📚</div>
        <h1>Ensino Fundamental I</h1>
        <p>Aprender com propósito e encantamento</p>
        <p>Conhecimento vivo, experiências reais e valores que formam.</p>
      </div>
    </section>

    <section class="ensfun1-content">
      <div class="ensfun1-container">
        <div class="ensfun1-grid">
          <div class="ensfun1-text">
            <h2>Metodologia Diferenciada</h2>
            <p>
              No Ensino Fundamental I, focamos na alfabetização e letramento, desenvolvimento do raciocínio lógico-matemático 
              e formação de valores, sempre respeitando o ritmo individual de cada criança.
            </p>
            <div class="anos-grid">
              <div class="ano-card">
                <h3>1º ao 3º ano</h3>
                <p>Alfabetização e letramento</p>
              </div>
              <div class="ano-card">
                <h3>4º ao 5º ano</h3>
                <p>Consolidação do aprendizado</p>
              </div>
            </div>
          </div>
          <div class="ensfun1-image">
            <img src="../public/foto4.jpg" alt="Ensino Fundamental I" />
          </div>
        </div>

        <div class="areas-section">
          <h2>Áreas de Conhecimento</h2>
          <div class="areas-grid">
            <div class="area-card">
              <div class="area-icon">
                <BookOpenIcon class="icon-md" />
              </div>
              <h3>Metodologias que desenvolvem habilidades</h3>
              <p>Com o material da <strong>Geekie</strong> e uma proposta pedagógica que integra <strong>Metodologias Ativas, Reggio Emilia, projetos integradores, salas temáticas e gamificação,</strong> nossos alunos desenvolvem competências como <strong>raciocínio lógico, leitura crítica e resolução de problemas,</strong> de forma significativa e conectada ao mundo atual</p>
            </div>
            <div class="area-card">
              <div class="area-icon">
                <span class="area-number">123</span>
              </div>
              <h3>Emoção e vínculo no processo de aprender</h3>
              <p>A cada nova experiência, o brilho nos olhos das crianças mostra que estão aprendendo com alegria. Com aulas de <strong>Robótica, Programação, Ciências em laboratório, dois idiomas</strong> (Inglês e Libras) e vivências cristãs, estimulamos o engajamento afetivo e a construação do conhecimento com sentido.</p>
            </div>
            <div class="area-card">
              <div class="area-icon">
                <span class="area-emoji">🌍</span>
              </div>
              <h3>Estrutura que acolhe e protege</h3>
              <p>Oferecemos uma base segura com acompanhamentop individualizado, ambientes estimulantes e valores cristãos que guiam nossa prática. Aqui, o aprendizado é construido com propósito e segurança.</p>
            </div>
          
          </div>
        </div>
      </div>
    </section>
  </div>

  <!-- ENSINO FUNDAMENTAL II PAGE -->
  <div v-if="currentPage === 'ensfun2'">
    <div class="page-header">
      <button @click="currentPage = 'home'" class="btn-back">
        <ArrowLeftIcon class="icon-sm" />
        Voltar ao Início
      </button>
    </div>
    
    <section class="page-hero">
      <div class="page-hero-content">
        <div class="page-hero-icon">🎓</div>
        <h1>Ensino Fundamental II</h1>
        <p>Protagonismo, tecnologia e construção de identidade</p>
        <p>Do conhecimento à ação, uma etapa que transforma</p>
      </div>
    </section>

    <section class="ensfun2-content">
      <div class="ensfun2-container">
        <div class="ensfun2-grid">
          <div class="ensfun2-image">
            <img src="../public/foto5.jpg" alt="Ensino Fundamental II" />
          </div>
          <div class="ensfun2-text">
            <h2>Formação Integral</h2>
            <p>
              No Ensino Fundamental II (6º ao 9º ano), aprofundamos o conhecimento em todas as áreas, 
              preparando os alunos para os desafios do Ensino Médio com autonomia e responsabilidade.
            </p>
            <div class="formacao-list">
              <div class="formacao-item">
                <div class="formacao-check">✓</div>
                <span>Aprofundamento das disciplinas</span>
              </div>
              <div class="formacao-item">
                <div class="formacao-check">✓</div>
                <span>Desenvolvimento da autonomia</span>
              </div>
              <div class="formacao-item">
                <div class="formacao-check">✓</div>
                <span>Preparação para o Ensino Médio</span>
              </div>
            </div>
          </div>
        </div>

        <div class="disciplinas-section">
          <h2>Disciplinas Principais</h2>
          <div class="disciplinas-grid">
            <div class="disciplina-card">
              <h3>Aprender com profundidade e sentido</h3>
              <p>Com o material Geekie e práticas pedagógicas qye envolvem <strong>projetos Interdisciplinares, laboratórios, aulas de campo e sala invertida,</strong> nossos alunos desenvolvem habilidades essenciais para o mundo em constante mudança. A tecnologia é integrada à rotina com o uso de <strong>CHromeBooks,</strong> promovendo a autonomia a aprendizagem personalizada.</p>
            </div>
            <div class="disciplina-card">
              <h3>Conexão com a fase e com o propósito</h3>
              <p>Essa é uma fase de mudanças e desconbertas - Por isso, nossa proposta considera as emoções, os valores e os desafios do pré-adolescente. Projetos como <strong>Empreendedorismo, Programação, Robótica e Cultura Digital</strong> despertam o interesse e promovem o engajamento com temas que fazem sentido para os alunos.</p>
            </div>
            <div class="disciplina-card">
              <h3>Apoio, limites e estrutura sólida</h3>
              <p>Odferecemos uma base segura e acolhedora, com regras claras, acompanhamento emocional e orientações constantes. Trabalhamos com a formação do caráter, a valorização da fé e o compromisso com a verdade, formando jovens preparados para fazer boas escolhas.</p>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>

  <!-- ENSINO MÉDIO PAGE -->
  <div v-if="currentPage === 'ensmed'">
    <div class="page-header">
      <button @click="currentPage = 'home'" class="btn-back">
        <ArrowLeftIcon class="icon-sm" />
        Voltar ao Início
      </button>
    </div>
    
    <section class="page-hero">
      <div class="page-hero-content">
        <div class="page-hero-icon">🚀</div>
        <h1>Ensino Médio</h1>
        <p>Excelência, autonomia e propósito de vida</p>
        <p>Preparar para o ENEM e para a vida com identidade e valores</p>
      </div>
    </section>

    <section class="ensmed-content">
      <div class="ensmed-container">
        <div class="ensmed-grid">
          <div class="ensmed-text">
            <h2>Rumo ao Futuro</h2>
            <p>
              No Ensino Médio, preparamos nossos alunos para os vestibulares e ENEM, 
              desenvolvendo competências e habilidades necessárias para o sucesso acadêmico e profissional.
            </p>
            <div class="diferenciais-card">
              <h3>Diferenciais</h3>
              <ul>
                <li>• Preparação intensiva para vestibulares</li>
                <li>• Orientação vocacional</li>
                <li>• Simulados regulares</li>
                <li>• Aulas de redação</li>
                <li>• Projetos de pesquisa</li>
              </ul>
            </div>
          </div>
          <div class="ensmed-image">
            <img src="../public/foto6.jpg" alt="Ensino Médio" />
          </div>
        </div>

        <div class="conhecimento-section">
          <h2>Áreas de Conhecimento</h2>
          <div class="conhecimento-grid">
            <div class="conhecimento-card">
              <div class="conhecimento-icon">📖</div>
              <h3>Autodesempenho e foco no futuro</h3>
              <p>No Ensino Médio, oferecemos um currículo robusto com <strong>preparação para vestibulares e ENEM,</strong> trilhas formativas personalizadas, simulados, tutorial e o usoi intensivo da plataforma <strong>Geekie One</strong> com <strong>ChromeBooks individuais.</strong> O pensamento crítico, a fluência digital e a autonomia intelectual são amplamente desenvolvidos.</p>
            </div>
            <div class="conhecimento-card">
              <div class="conhecimento-icon">🔢</div>
              <h3>Escolhas com propósito e construção de identidade</h3>
              <p>Sabemos que o Ensino Médio é decisivo. Por isso, promovemos vivÊncias que ajudam o aluno a entender <strong>quem ele é e quem deseja se tornar.</strong> Trabalhamos projetos de vida, orientação vocacional, rodas de conversa e momentos de escuta que apoiam esse processo de autoconhecimento e decisão.</p>
            </div>
            <div class="conhecimento-card">
              <div class="conhecimento-icon">🧪</div>
              <h3>Segurança emocional e espiritual para seguir em frente</h3>
              <p>Oferecemso um ambiente que equilibra exigÊncia acadêmica com suporte emocional, fé cristã e uma estrutura sólida de acompanhamento. Aqui, o aluno é preparado para ser excelente, ético e humano - em qualquer caminho que escolher. </p>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>

  <!-- Footer -->
  <footer class="footer">
    <div class="footer-content">
      <div class="footer-left">
        <div class="footer-logo-circle">
          <img src="../public/logo.png" alt="Logo" class="footer-logo-icon" />
        </div>
        <div class="footer-text">
          <h3 style="margin-bottom: 2%;">Colégio Mãe Natureza</h3>
          <span>Princípios e tecnologia na educação</span>
        </div>
      </div>
      <div class="footer-menu">
        <h4>Páginas</h4>
        <ul>
          <li><a @click="currentPage = 'nossahistoria'">Nossa História</a></li>
          <li><a @click="currentPage = 'educainf'">Educação Infantil</a></li>
          <li><a @click="currentPage = 'ensfun1'">Ensino Fundamental I</a></li>
          <li><a @click="currentPage = 'ensfun2'">Ensino Fundamental II</a></li>
          <li><a @click="currentPage = 'ensmed'">Ensino Médio</a></li>
        </ul>
      </div>
      <div class="footer-contact">
        <h4>Contato</h4>
<div class="flex gap-4">
  <button @click="openWhatsApp" class="btn-contact-footer flex items-center gap-2">
    <MessageCircleIcon class="icon-sm" />
    <span>WhatsApp</span>
  </button>
  <br>
  <br>

  <a
    href="https://www.instagram.com/colegiomaenatureza/?hl=pt"
    target="_blank"
    rel="noopener noreferrer"
    class="btn-contact-footer flex items-center gap-2"
  >
    <InstagramIcon class="icon-sm" />
    <span>Instagram</span>
  </a>
</div>

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
InstagramIcon,
XIcon,
MessageCircleIcon,
BookOpenIcon,
HeartIcon,
UsersIcon,
ArrowLeftIcon,
} from 'lucide-vue-next'

const mobileMenuOpen = ref(false)
const currentPage = ref('home')

const toggleMobileMenu = () => {
mobileMenuOpen.value = !mobileMenuOpen.value
}

const openWhatsApp = () => {
const phoneNumber = '554734360070'
const message = 'Olá! Gostaria de saber mais informações sobre o Colégio Mãe Natureza.'
const whatsappUrl = `https://wa.me/${phoneNumber}?text=${encodeURIComponent(message)}`
window.open(whatsappUrl, '_blank')
}
</script>

<style scoped>

html,
body {
margin: 0;
padding: 0;
width: 100%;
height: 100%;
overflow-x: hidden;
}


.footer-logo-icon{
  width:auto;
  height: auto;
  display: block;
  max-width: 150px;
}
.container {
min-height: 100vh;
width: 100%;
font-family: 'Inter', sans-serif;
}

.header {
background-color: #059669;
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
cursor: pointer;
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
background-color: #ffffff;
border-radius: 9999px;
display: flex;
justify-content:center;
text-align: center;
align-items: center;
}

.logo-icon {
color: white;
width: 65px;
height: 65px;
display: block;
}

.logo-text h1 {
font-size: 1.25rem;
font-weight: 700;
color: white;
}

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
cursor: pointer;
}

.nav-desktop a:hover {
color: #d1fae5;
}

.btn-contact {
background-color: #812b58;
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
background-color: #6b2347;
transform: scale(1.05);
}

.btn-mobile-menu {
display: inline-flex;
padding: 0.5rem;
color: white;
background: none;
border: none;
cursor: pointer;
}

.icon {
height: 1.5rem;
width: 1.5rem;
}

.mobile-menu {
display: flex;
flex-direction: column;
gap: 0.75rem;
padding: 1rem 0;
border-top: 1px solid #059669;
}

.mobile-menu a {
color: white;
font-size: 0.875rem;
font-weight: 500;
text-decoration: none;
cursor: pointer;
}

.btn-contact-mobile {
background-color: #812b58;
color: white;
padding: 0.5rem 1rem;
border-radius: 9999px;
font-size: 0.875rem;
font-weight: 600;
cursor: pointer;
border: none;
width: fit-content;
}

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
height: 4rem;
display: flex;
justify-content: left;
align-items: center;
box-shadow: 0 10px 15px rgba(0, 0, 0, 0);
margin-bottom: 1.5rem;
}

.hero-icon {
color: #059669;
width: 170px;
display: block;
height: auto;
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
background-color: #d1fae5;
}

.heart-icon-wrapper {
position: absolute;
bottom: -1rem;
right: -1rem;
width: 6rem;
height: 6rem;
background-color: #812b58;
border-radius: 9999px;
display: flex;
justify-content: center;
align-items: center;
box-shadow: 0 10px 25px rgba(129, 43, 88, 0.7);
}

.icon-lg {
color: white;
width: 3rem;
height: 3rem;
}

.about {
padding: 5rem 1rem;
background-color: #f9fafb;
margin: 0 !important;
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
background-color: rgba(129, 43, 88, 0.1);
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
color: #812b58;
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

.education-levels {
padding: 5rem 1rem;
background-color: #812b58;
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
color: rgba(255, 255, 255, 0.8);
}

.education-cards {
display: grid;
grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
gap: 1.5rem;
}
.footer-text{
  margin-left: 15%;
}
.edu-card {
background-color: rgba(255 255 255 / 0.1);
backdrop-filter: blur(8px);
padding: 1.5rem;
border-radius: 1rem;
text-align: center;
cursor: pointer;
transition: background-color 0.3s, transform 0.3s;
}

.edu-card:hover {
background-color: rgba(255 255 255 / 0.2);
transform: scale(1.05);
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
color: rgba(255, 255, 255, 0.8);
}

.cta {
padding: 5rem 1rem;
background-color: #059669;
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

.page-header {
background-color: #059669;
padding: 1rem;
}

.btn-back {
color: white;
background: none;
border: none;
display: flex;
align-items: center;
gap: 0.5rem;
cursor: pointer;
font-size: 0.875rem;
transition: color 0.3s;
}

.btn-back:hover {
color: #d1fae5;
}

.page-hero {
background: linear-gradient(135deg, #34d399 0%, #10b981 50%, #047857 100%);
padding: 5rem 1rem;
color: white;
text-align: center;
}

.page-hero-content {
max-width: 48rem;
margin: 0 auto;
}

.page-hero-icon {
font-size: 4rem;
margin-bottom: 1.5rem;
}

.page-hero h1 {
font-size: 3rem;
font-weight: 700;
margin-bottom: 1rem;
}

.page-hero p {
font-size: 1.25rem;
color: #d1fae5;
}

.historia-content {
padding: 5rem 1rem;
background-color: #f9fafb;
}

.historia-container {
max-width: 112rem;
margin: 0 auto;
}

.historia-grid {
display: grid;
grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
gap: 3rem;
align-items: center;
margin-bottom: 4rem;
}

.historia-text h2 {
font-size: 2rem;
font-weight: 700;
color: #111827;
margin-bottom: 1.5rem;
}

.historia-text p {
color: #4b5563;
margin-bottom: 1.5rem;
line-height: 1.6;
}

.valores-list {
display: flex;
flex-direction: column;
gap: 1rem;
}

.valor-item {
display: flex;
align-items: center;
gap: 0.75rem;
}

.valor-check {
width: 2rem;
height: 2rem;
background-color: #812b58;
border-radius: 9999px;
display: flex;
align-items: center;
justify-content: center;
color: white;
font-weight: 700;
}

.historia-image {
border-radius: 1rem;
overflow: hidden;
box-shadow: 0 0px 0px rgba(0, 0, 0, 0.15);
}

.historia-image img {
width: 100%;
height: 24rem;
object-fit: cover;
background-color: #d1fae5;
}


.metodologias-section {
background-color: white;
padding: 3rem;
border-radius: 1rem;
box-shadow: 0 10px 15px rgba(0, 0, 0, 0.1);
}

.metodologias-section h2 {
font-size: 2rem;
font-weight: 700;
color: #111827;
text-align: center;
margin-bottom: 2rem;
}

.metodologias-grid {
display: grid;
grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
gap: 1.5rem;
}

.metodologia-card {
text-align: center;
}

.metodologia-icon {
width: 4rem;
height: 4rem;
background-color: #d1fae5;
border-radius: 9999px;
display: flex;
align-items: center;
justify-content: center;
margin: 0 auto 1rem;
font-weight: 700;
color: #059669;
font-size: 1.5rem;
}

.metodologia-card h3 {
font-weight: 600;
color: #111827;
margin-bottom: 0.5rem;
}

.metodologia-card p {
font-size: 0.875rem;
color: #4b5563;
}

.educainf-content {
padding: 5rem 1rem;
background-color: #f9fafb;
}

.educainf-container {
max-width: 112rem;
margin: 0 auto;
}

.educainf-grid {
display: grid;
grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
gap: 3rem;
align-items: center;
margin-bottom: 4rem;
}

.educainf-image {
border-radius: 1rem;
overflow: hidden;
box-shadow: 0 20px 30px rgba(0, 0, 0, 0.15);
}

.educainf-image img {
width: 100%;
height: 28rem;
object-fit: cover;
background-color: #d1fae5;
}

.educainf-text h2 {
font-size: 2rem;
font-weight: 700;
color: #111827;
margin-bottom: 1.5rem;
}

.educainf-text p {
color: #4b5563;
margin-bottom: 1.5rem;
line-height: 1.6;
}

.abordagem-list {
display: flex;
flex-direction: column;
gap: 1rem;
}

.abordagem-item {
display: flex;
align-items: flex-start;
gap: 0.75rem;
}

.abordagem-check {
width: 1.5rem;
height: 1.5rem;
background-color: #812b58;
border-radius: 9999px;
display: flex;
align-items: center;
justify-content: center;
color: white;
font-size: 0.75rem;
font-weight: 700;
flex-shrink: 0;
margin-top: 0.25rem;
}

.abordagem-item h3 {
font-weight: 600;
color: #111827;
margin-bottom: 0.25rem;
}

.abordagem-item p {
font-size: 0.875rem;
color: #4b5563;
margin: 0;
}

.atividades-section {
margin-top: 3rem;
}

.atividades-grid {
display: grid;
grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
gap: 2rem;
}

.atividade-card {
background-color: white;
padding: 2rem;
border-radius: 1rem;
box-shadow: 0 10px 15px rgba(0, 0, 0, 0.1);
text-align: center;
transition: box-shadow 0.3s;
}

.atividade-card:hover {
box-shadow: 0 20px 30px rgba(0, 0, 0, 0.15);
}

.atividade-icon {
font-size: 2.5rem;
margin-bottom: 1rem;
}

.atividade-card h3 {
font-size: 1.25rem;
font-weight: 700;
color: #111827;
margin-bottom: 0.75rem;
}

.atividade-card p {
color: #4b5563;
}

.ensfun1-content {
padding: 5rem 1rem;
background-color: #f9fafb;
}

.ensfun1-container {
max-width: 112rem;
margin: 0 auto;
}

.ensfun1-grid {
display: grid;
grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
gap: 3rem;
align-items: center;
margin-bottom: 4rem;
}

.ensfun1-text h2 {
font-size: 2rem;
font-weight: 700;
color: #111827;
margin-bottom: 1.5rem;
}

.ensfun1-text p {
color: #4b5563;
margin-bottom: 1.5rem;
line-height: 1.6;
}

.anos-grid {
display: grid;
grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
gap: 1rem;
}

.ano-card {
background-color: #d1fae5;
padding: 1rem;
border-radius: 0.75rem;
}

.ano-card h3 {
font-weight: 600;
color: #047857;
margin-bottom: 0.5rem;
}

.ano-card p {
font-size: 0.875rem;
color: #065f46;
margin: 0;
}

.ensfun1-image {
border-radius: 1rem;
overflow: hidden;
box-shadow: 0 20px 30px rgba(0, 0, 0, 0.15);
}

.ensfun1-image img {
width: 100%;
height: 28rem;
object-fit: cover;
background-color: #dbeafe;
}

.areas-section {
background-color: rgba(129, 43, 88, 0.05);
padding: 3rem;
border-radius: 1rem;
}

.areas-section h2 {
font-size: 2rem;
font-weight: 700;
color: #111827;
text-align: center;
margin-bottom: 2rem;
}

.areas-grid {
display: grid;
grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
gap: 1.5rem;
}

.area-card {
text-align: center;
}

.area-icon {
width: 4rem;
height: 4rem;
background-color: #812b58;
border-radius: 9999px;
display: flex;
align-items: center;
justify-content: center;
margin: 0 auto 1rem;
color: white;
}

.area-number,
.area-emoji {
font-weight: 700;
}

.area-card h3 {
font-weight: 600;
color: #111827;
margin-bottom: 0.5rem;
}

.area-card p {
font-size: 0.875rem;
color: #4b5563;
}

.ensfun2-content {
padding: 5rem 1rem;
background-color: #f9fafb;
}

.ensfun2-container {
max-width: 112rem;
margin: 0 auto;
}

.ensfun2-grid {
display: grid;
grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
gap: 3rem;
align-items: center;
margin-bottom: 4rem;
}

.ensfun2-image {
border-radius: 1rem;
overflow: hidden;
box-shadow: 0 20px 30px rgba(0, 0, 0, 0.15);
}

.ensfun2-image img {
width: 100%;
height: 24rem;
object-fit: cover;
background-color: #e0e7ff;
}

.ensfun2-text h2 {
font-size: 2rem;
font-weight: 700;
color: #111827;
margin-bottom: 1.5rem;
}

.ensfun2-text p {
color: #4b5563;
margin-bottom: 1.5rem;
line-height: 1.6;
}

.formacao-list {
display: flex;
flex-direction: column;
gap: 1rem;
}

.formacao-item {
display: flex;
align-items: center;
gap: 0.75rem;
}

.formacao-check {
width: 2rem;
height: 2rem;
background-color: #812b58;
border-radius: 9999px;
display: flex;
align-items: center;
justify-content: center;
color: white;
font-weight: 700;
}

.disciplinas-section {
background-color: white;
padding: 3rem;
border-radius: 1rem;
box-shadow: 0 10px 15px rgba(0, 0, 0, 0.1);
}

.disciplinas-section h2 {
font-size: 2rem;
font-weight: 700;
color: #111827;
text-align: center;
margin-bottom: 2rem;
}

.disciplinas-grid {
display: grid;
grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
gap: 1.5rem;
}

.disciplina-card {
background-color: #f9fafb;
padding: 1.5rem;
border-radius: 0.75rem;
box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05);
}

.disciplina-card h3 {
font-weight: 700;
color: #111827;
margin-bottom: 0.5rem;
}

.disciplina-card p {
font-size: 0.875rem;
color: #4b5563;
margin: 0;
}

.ensmed-content {
padding: 5rem 1rem;
background-color: #f9fafb;
}

.ensmed-container {
max-width: 112rem;
margin: 0 auto;
}

.ensmed-grid {
display: grid;
grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
gap: 3rem;
align-items: center;
margin-bottom: 4rem;
}

.ensmed-text h2 {
font-size: 2rem;
font-weight: 700;
color: #111827;
margin-bottom: 1.5rem;
}

.ensmed-text p {
color: #4b5563;
margin-bottom: 1.5rem;
line-height: 1.6;
}

.diferenciais-card {
background-color: #d1fae5;
padding: 1.5rem;
border-radius: 0.75rem;
}

.diferenciais-card h3 {
font-weight: 700;
color: #047857;
margin-bottom: 1rem;
}

.diferenciais-card ul {
list-style: none;
padding: 0;
margin: 0;
color: #065f46;
}

.diferenciais-card li {
margin-bottom: 0.5rem;
}

.ensmed-image {
border-radius: 1rem;
overflow: hidden;
box-shadow: 0 20px 30px rgba(0, 0, 0, 0.15);
}

.ensmed-image img {
width: 100%;
height: 28rem;
object-fit: cover;
background-color: #fef3c7;
}

.conhecimento-section {
background: linear-gradient(135deg, #10b981 0%, #059669 100%);
padding: 3rem;
border-radius: 1rem;
color: white;
}

.conhecimento-section h2 {
font-size: 2rem;
font-weight: 700;
text-align: center;
margin-bottom: 2rem;
}

.conhecimento-grid {
display: grid;
grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
gap: 1.5rem;
}

.conhecimento-card {
background-color: rgba(255, 255, 255, 0.1);
backdrop-filter: blur(8px);
padding: 1.5rem;
border-radius: 0.75rem;
text-align: center;
}

.conhecimento-icon {
font-size: 2rem;
margin-bottom: 1rem;
}

.conhecimento-card h3 {
font-weight: 600;
margin-bottom: 0.5rem;
}

.conhecimento-card p {
font-size: 0.875rem;
color: rgba(255, 255, 255, 0.8);
}

.footer {
background-color: #111827;
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
height: 3rem;
background-color: #05966800;
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
color: #9ca3af;
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

.footer-menu a {
color: #9ca3af;
cursor: pointer;
transition: color 0.3s;
}

.footer-menu a:hover {
color: white;
}

.btn-contact-footer {
background-color: #059669;
padding: 0.75rem 1.5rem;
border-radius: 9999px;
font-weight: 400;
color: white;
cursor: pointer;
border: none;
display: inline-flex;
align-items: center;
gap: 0.5rem;
transition: background-color 0.3s;
text-decoration: none;
font-size:medium;}

.btn-contact-footer:hover {
background-color: #047857;
}

.footer-bottom {
border-top: 1px solid #1f2937;
margin-top: 3rem;
padding-top: 2rem;
text-align: center;
color: #9ca3af;
}

.whatsapp-float-btn {
position: fixed;
bottom: 1.5rem;
right: 1.5rem;
z-index: 50;
}

.btn-whatsapp-float {
background-color: #22c55e;
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
background-color: #16a34a;
transform: scale(1.1);
}

.icon-sm {
width: 1.25rem;
height: 1.25rem;
}

.icon-md {
width: 1.5rem;
height: 1.5rem;
}

html {
scroll-behavior: smooth;
}

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

@media (min-width: 1024px) {
.nav-desktop {
  display: flex;
}
.btn-mobile-menu,
.mobile-menu {
  display: none !important;
}
}

@media (max-width: 768px) {
.hero-title {
  font-size: 2.5rem;
}

.page-hero h1 {
  font-size: 2.5rem;
}

.about-header h2,
.education-header h2,
.cta h2 {
  font-size: 2rem;
}

.hero-image-wrapper {
  width: 20rem;
  height: 20rem;
}

.heart-icon-wrapper {
  width: 5rem;
  height: 5rem;
}

.icon-lg {
  width: 2.5rem;
  height: 2.5rem;
}
}

@media (max-width: 480px) {
.hero-buttons {
  flex-direction: column;
}

.btn-whatsapp,
.btn-saiba-mais {
  width: 100%;
  justify-content: center;
}

.hero-image-wrapper {
  width: 18rem;
  height: 18rem;
}
}
</style>