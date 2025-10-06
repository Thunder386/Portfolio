<template>
  <section id="about" class="py-5 bg-light">
    <div class="container">
      <div class="row align-items-center">
        <div class="col-lg-6" data-aos="fade-right">
          <div class="about-image text-center mb-5 mb-lg-0">
            <div class="image-container position-relative">
              <div class="main-image bg-primary rounded-3 shadow-lg overflow-hidden">
                <img src="/images/profile.png" alt="Andre Dingfelder" class="w-100 h-100 object-fit-cover">
              </div>
              <!-- Floating elements around image -->
              <div class="floating-icon position-absolute" style="top: -20px; right: -20px;">
                <i class="bi bi-heart-fill text-danger fs-2 pulse-element"></i>
              </div>
              <div class="floating-icon position-absolute" style="bottom: -20px; left: -20px;">
                <i class="bi bi-lightbulb-fill text-warning fs-2 floating-element"></i>
              </div>
              <div class="floating-icon position-absolute" style="top: 50%; right: -30px;">
                <i class="bi bi-rocket-takeoff-fill text-info fs-2 rotate-element"></i>
              </div>
            </div>
          </div>
        </div>
        
        <div class="col-lg-6" data-aos="fade-left">
          <div class="about-content">
            <h2 class="display-5 fw-bold mb-4">
              Über <span class="gradient-text">mich</span>
            </h2>
            
            <div class="about-text mb-4">
              <p class="lead">
                Hallo! Ich bin Andre Dingfelder, ein leidenschaftlicher Webentwickler mit über 3 Jahren Erfahrung 
                in der Entwicklung moderner Webanwendungen.
              </p>
              
              <p>
                Meine Reise begann mit der Neugier, wie Websites funktionieren. Heute entwickle ich 
                komplexe Anwendungen mit Vue.js, React und anderen modernen Technologien. Ich liebe es, 
                kreative Lösungen für technische Herausforderungen zu finden.
              </p>
              
              <p>
                Neben der Programmierung engagiere ich mich aktiv in meiner Gemeinde - bei der Feuerwehr, 
                dem Roten Kreuz und der Wasserwacht. Diese Erfahrungen haben mich gelehrt, unter Druck 
                zu arbeiten und im Team zu funktionieren.
              </p>
            </div>

            <!-- Personal Info Cards -->
            <div class="row g-3 mb-4">
              <div class="col-md-6">
                <div class="info-card card border-0 shadow-sm h-100">
                  <div class="card-body text-center">
                    <i class="bi bi-geo-alt-fill text-primary fs-3 mb-3"></i>
                    <h5 class="card-title">Standort</h5>
                    <p class="card-text text-muted">München, Deutschland</p>
                  </div>
                </div>
              </div>
              <div class="col-md-6">
                <div class="info-card card border-0 shadow-sm h-100">
                  <div class="card-body text-center">
                    <i class="bi bi-mortarboard-fill text-success fs-3 mb-3"></i>
                    <h5 class="card-title">Ausbildung</h5>
                    <p class="card-text text-muted">Informatik B.Sc.</p>
                  </div>
                </div>
              </div>
            </div>

            <!-- Values -->
            <div class="values-section">
              <h4 class="h5 fw-bold mb-3">Meine Werte</h4>
              <div class="row g-3">
                <div class="col-6 col-md-3">
                  <div class="value-item text-center">
                    <i class="bi bi-award-fill text-primary fs-4 mb-2"></i>
                    <h6 class="small fw-bold">Zuverlässigkeit</h6>
                  </div>
                </div>
                <div class="col-6 col-md-3">
                  <div class="value-item text-center">
                    <i class="bi bi-lightbulb-fill text-warning fs-4 mb-2"></i>
                    <h6 class="small fw-bold">Kreativität</h6>
                  </div>
                </div>
                <div class="col-6 col-md-3">
                  <div class="value-item text-center">
                    <i class="bi bi-people-fill text-success fs-4 mb-2"></i>
                    <h6 class="small fw-bold">Teamwork</h6>
                  </div>
                </div>
                <div class="col-6 col-md-3">
                  <div class="value-item text-center">
                    <i class="bi bi-graph-up-arrow text-info fs-4 mb-2"></i>
                    <h6 class="small fw-bold">Wachstum</h6>
                  </div>
                </div>
              </div>
            </div>

            <!-- Call to Action -->
            <div class="about-cta mt-4">
              <a href="#contact" class="btn btn-primary me-3">
                <i class="bi bi-envelope me-2"></i>Kontakt aufnehmen
              </a>
              <a href="#timeline" class="btn btn-outline-primary">
                <i class="bi bi-clock-history me-2"></i>Meine Erfahrung
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'AboutSection'
}
</script>

<style scoped>
.about-section {
  background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
}

.main-image {
  width: 300px;
  height: 300px;
  background: linear-gradient(45deg, #667eea, #764ba2);
  margin: 0 auto;
  position: relative;
}

.floating-icon {
  animation-duration: 3s;
}

.info-card {
  transition: all 0.3s ease;
  border-radius: 15px;
}

.info-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 15px 30px rgba(0,0,0,0.1) !important;
}

.value-item {
  transition: transform 0.3s ease;
}

.value-item:hover {
  transform: scale(1.1);
}

.about-text p {
  line-height: 1.8;
  margin-bottom: 1rem;
}

@media (max-width: 768px) {
  .main-image {
    width: 250px;
    height: 250px;
  }
  
  .floating-icon {
    display: none;
  }
  
  .values-section .col-md-3 {
    margin-bottom: 1rem;
  }
}
</style>
