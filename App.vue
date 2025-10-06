<template>
  <div id="app">
    <!-- Navigation -->
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark fixed-top">
      <div class="container">
        <a class="navbar-brand fw-bold" href="#home">
          <i class="bi bi-code-slash me-2"></i>ANDRE DINGFELDER
        </a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav ms-auto">
            <li class="nav-item">
              <a class="nav-link" href="#home">Home</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#about">Über mich</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#timeline">Erfahrung</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#skills">Skills</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#hobbies">Hobbys</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#contact">Kontakt</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>

    <!-- Hero Section -->
    <HeroSection />

    <!-- About Section -->
    <AboutSection />

    <!-- Timeline Section -->
    <TimelineSection />

    <!-- Skills Section -->
    <SkillsSection />

    <!-- Hobbies Section -->
    <HobbiesSection />

    <!-- Contact Section -->
    <ContactSection />

    <!-- Footer -->
    <footer class="bg-dark text-light py-4">
      <div class="container text-center">
        <p>&copy; 2024 Mein Portfolio. Alle Rechte vorbehalten.</p>
        <div class="social-links mt-3">
          <a href="#" class="text-light me-3"><i class="bi bi-linkedin fs-4"></i></a>
          <a href="#" class="text-light me-3"><i class="bi bi-github fs-4"></i></a>
          <a href="#" class="text-light me-3"><i class="bi bi-twitter fs-4"></i></a>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
import HeroSection from './components/HeroSection.vue'
import AboutSection from './components/AboutSection.vue'
import TimelineSection from './components/TimelineSection.vue'
import SkillsSection from './components/SkillsSection.vue'
import HobbiesSection from './components/HobbiesSection.vue'
import ContactSection from './components/ContactSection.vue'

export default {
  name: 'App',
  components: {
    HeroSection,
    AboutSection,
    TimelineSection,
    SkillsSection,
    HobbiesSection,
    ContactSection
  }
}
</script>
