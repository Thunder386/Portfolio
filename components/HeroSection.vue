<template>
  <section id="home" class="hero-section position-relative overflow-hidden">
    <!-- Background Pattern -->
    <div class="bg-pattern position-absolute w-100 h-100"></div>
    
    <!-- Floating Elements -->
    <div class="floating-elements position-absolute w-100 h-100">
      <!-- Floating Code Icons -->
      <div class="floating-element position-absolute" style="top: 10%; left: 10%; animation-delay: 0s;">
        <i class="bi bi-code-slash fs-1 text-primary opacity-25"></i>
      </div>
      <div class="floating-element position-absolute" style="top: 20%; right: 15%; animation-delay: 1s;">
        <i class="bi bi-gear-fill fs-2 text-secondary opacity-25"></i>
      </div>
      <div class="floating-element position-absolute" style="bottom: 30%; left: 20%; animation-delay: 2s;">
        <i class="bi bi-laptop fs-1 text-info opacity-25"></i>
      </div>
      <div class="floating-element position-absolute" style="top: 60%; right: 10%; animation-delay: 0.5s;">
        <i class="bi bi-phone fs-2 text-warning opacity-25"></i>
      </div>
      <div class="floating-element position-absolute" style="bottom: 20%; right: 30%; animation-delay: 1.5s;">
        <i class="bi bi-database fs-1 text-success opacity-25"></i>
      </div>
      
      <!-- Rotating Elements -->
      <div class="rotate-element position-absolute" style="top: 15%; left: 80%; animation-delay: 0s;">
        <i class="bi bi-hexagon fs-3 text-primary opacity-20"></i>
      </div>
      <div class="rotate-element position-absolute" style="bottom: 40%; left: 5%; animation-delay: 2s;">
        <i class="bi bi-circle fs-4 text-secondary opacity-20"></i>
      </div>
      
      <!-- Pulse Elements -->
      <div class="pulse-element position-absolute" style="top: 40%; left: 70%; animation-delay: 1s;">
        <i class="bi bi-star-fill fs-2 text-warning opacity-30"></i>
      </div>
      <div class="pulse-element position-absolute" style="bottom: 60%; right: 20%; animation-delay: 0.8s;">
        <i class="bi bi-lightning-fill fs-3 text-info opacity-30"></i>
      </div>
    </div>

    <!-- Main Content -->
    <div class="container position-relative" style="z-index: 10;">
      <div class="row min-vh-100 align-items-center">
        <div class="col-lg-6" data-aos="fade-right">
          <div class="hero-content">
            <h1 class="display-3 fw-bold mb-4">
              Hallo, ich bin
              <span class="gradient-text">Andre Dingfelder</span>
            </h1>
            <h2 class="h3 mb-4 text-muted">
              <span class="typing-text">{{ currentText }}</span>
              <span class="cursor">|</span>
            </h2>
            <p class="lead mb-4">
              Leidenschaftlicher Entwickler mit Fokus auf moderne Webtechnologien. 
              Ich erstelle digitale Lösungen, die begeistern und funktionieren.
            </p>
            <div class="hero-buttons">
              <a href="#contact" class="btn btn-primary btn-lg me-3 mb-3">
                <i class="bi bi-envelope me-2"></i>Kontakt aufnehmen
              </a>
              <a href="#timeline" class="btn btn-outline-primary btn-lg mb-3">
                <i class="bi bi-person-badge me-2"></i>Mehr erfahren
              </a>
            </div>
            
            <!-- Buy Me a Coffee Button -->
            <div class="mt-4">
              <a href="https://buymeacoffee.com/thunder386" target="_blank" class="btn btn-warning btn-lg">
                <i class="bi bi-cup-hot-fill me-2"></i>Buy me a Coffee
              </a>
            </div>
          </div>
        </div>
        
        <div class="col-lg-6" data-aos="fade-left">
          <div class="hero-image text-center">
            <div class="profile-card position-relative">
              <!-- Profile Image -->
              <div class="profile-img-container mx-auto mb-4">
                <div class="profile-img rounded-circle overflow-hidden shadow-lg">
                  <img src="/images/profile.png" alt="Andre Dingfelder" class="w-100 h-100 object-fit-cover">
                </div>
                <!-- Floating badges around profile -->
                <div class="floating-badge position-absolute" style="top: 10%; right: 10%;">
                  <span class="badge bg-success fs-6 pulse-element">
                    <i class="bi bi-check-circle me-1"></i>Online
                  </span>
                </div>
                <div class="floating-badge position-absolute" style="bottom: 20%; left: 5%;">
                  <span class="badge bg-info fs-6 floating-element">
                    <i class="bi bi-code me-1"></i>Vue.js
                  </span>
                </div>
                <div class="floating-badge position-absolute" style="top: 50%; right: -10%;">
                  <span class="badge bg-warning fs-6 floating-element" style="animation-delay: 1s;">
                    <i class="bi bi-bootstrap me-1"></i>Bootstrap
                  </span>
                </div>
              </div>
              
              <!-- Stats Cards -->
              <div class="row g-3">
                <div class="col-4">
                  <div class="stat-card card border-0 shadow-sm">
                    <div class="card-body text-center">
                      <h3 class="text-primary fw-bold">50+</h3>
                      <small class="text-muted">Projekte</small>
                    </div>
                  </div>
                </div>
                <div class="col-4">
                  <div class="stat-card card border-0 shadow-sm">
                    <div class="card-body text-center">
                      <h3 class="text-success fw-bold">3+</h3>
                      <small class="text-muted">Jahre</small>
                    </div>
                  </div>
                </div>
                <div class="col-4">
                  <div class="stat-card card border-0 shadow-sm">
                    <div class="card-body text-center">
                      <h3 class="text-warning fw-bold">100%</h3>
                      <small class="text-muted">Leidenschaft</small>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Scroll Indicator -->
    <div class="scroll-indicator position-absolute bottom-0 start-50 translate-middle-x mb-4">
      <div class="scroll-down-wrapper text-center">
        <div class="scroll-icon-container mb-2">
          <div class="mouse-icon">
            <div class="mouse-wheel"></div>
          </div>
        </div>
        <p class="scroll-text mb-0">Scrollen für mehr</p>
        <i class="bi bi-chevron-double-down scroll-arrow"></i>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'HeroSection',
  data() {
    return {
      texts: [
        'Frontend Entwickler',
        'Vue.js Spezialist',
        'UI/UX Designer',
        'Problem Löser',
        'Team Player'
      ],
      currentText: '',
      textIndex: 0,
      charIndex: 0,
      isDeleting: false
    }
  },
  mounted() {
    this.startTyping()
  },
  methods: {
    startTyping() {
      const fullText = this.texts[this.textIndex]
      
      if (this.isDeleting) {
        this.currentText = fullText.substring(0, this.charIndex - 1)
        this.charIndex--
      } else {
        this.currentText = fullText.substring(0, this.charIndex + 1)
        this.charIndex++
      }
      
      let typeSpeed = this.isDeleting ? 100 : 150
      
      if (!this.isDeleting && this.charIndex === fullText.length) {
        typeSpeed = 2000
        this.isDeleting = true
      } else if (this.isDeleting && this.charIndex === 0) {
        this.isDeleting = false
        this.textIndex = (this.textIndex + 1) % this.texts.length
        typeSpeed = 500
      }
      
      setTimeout(() => this.startTyping(), typeSpeed)
    }
  }
}
</script>

<style scoped>
.hero-section {
  min-height: 100vh;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  position: relative;
}

.hero-section::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: rgba(0, 0, 0, 0.3);
  z-index: 1;
}

.hero-content {
  color: white;
  z-index: 10;
  position: relative;
}

.typing-text {
  color: #ffd700;
  font-weight: 600;
}

.cursor {
  animation: blink 1s infinite;
}

@keyframes blink {
  0%, 50% { opacity: 1; }
  51%, 100% { opacity: 0; }
}

.profile-img {
  width: 200px;
  height: 200px;
  background: linear-gradient(45deg, #667eea, #764ba2);
  position: relative;
}

.floating-badge {
  animation: float 3s ease-in-out infinite;
}

.stat-card {
  transition: transform 0.3s ease;
}

.stat-card:hover {
  transform: translateY(-5px);
}

.scroll-indicator {
  z-index: 20;
  animation: scrollBounce 2s ease-in-out infinite;
}

.scroll-down-wrapper {
  background: rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(10px);
  padding: 20px 30px;
  border-radius: 50px;
  border: 2px solid rgba(255, 255, 255, 0.2);
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
  transition: all 0.3s ease;
}

.scroll-down-wrapper:hover {
  background: rgba(255, 255, 255, 0.15);
  border-color: rgba(255, 255, 255, 0.4);
  transform: translateY(-5px);
  box-shadow: 0 12px 40px rgba(0, 0, 0, 0.2);
}

.mouse-icon {
  width: 30px;
  height: 45px;
  border: 3px solid rgba(255, 255, 255, 0.8);
  border-radius: 15px;
  position: relative;
  margin: 0 auto;
  background: rgba(255, 255, 255, 0.1);
}

.mouse-wheel {
  width: 4px;
  height: 10px;
  background: rgba(255, 255, 255, 0.8);
  border-radius: 2px;
  position: absolute;
  top: 8px;
  left: 50%;
  transform: translateX(-50%);
  animation: scrollWheel 1.5s ease-in-out infinite;
}

.scroll-text {
  color: rgba(255, 255, 255, 0.9);
  font-size: 0.9rem;
  font-weight: 500;
  letter-spacing: 0.5px;
  text-transform: uppercase;
  text-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
  margin-top: 8px;
}

.scroll-arrow {
  color: rgba(255, 255, 255, 0.8);
  font-size: 1.2rem;
  animation: arrowBounce 1.5s ease-in-out infinite;
  display: block;
  margin-top: 5px;
}

@keyframes scrollBounce {
  0%, 100% {
    transform: translateY(0) translateX(-50%);
  }
  50% {
    transform: translateY(-15px) translateX(-50%);
  }
}

@keyframes scrollWheel {
  0% {
    opacity: 1;
    transform: translateX(-50%) translateY(0);
  }
  100% {
    opacity: 0;
    transform: translateX(-50%) translateY(15px);
  }
}

@keyframes arrowBounce {
  0%, 100% {
    transform: translateY(0);
    opacity: 0.8;
  }
  50% {
    transform: translateY(5px);
    opacity: 1;
  }
}

@media (max-width: 768px) {
  .hero-section h1 {
    font-size: 2.5rem !important;
  }
  
  .profile-img {
    width: 150px;
    height: 150px;
  }
  
  .floating-badge {
    font-size: 0.75rem !important;
  }
  
  .scroll-down-wrapper {
    padding: 15px 20px;
    border-radius: 40px;
  }
  
  .mouse-icon {
    width: 25px;
    height: 38px;
  }
  
  .scroll-text {
    font-size: 0.75rem;
  }
  
  .scroll-arrow {
    font-size: 1rem;
  }
}
</style>
