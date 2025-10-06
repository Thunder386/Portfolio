<template>
  <section id="timeline" class="py-5 bg-white">
    <div class="container">
      <div class="row">
        <div class="col-lg-8 mx-auto">
          <div class="section-header text-center mb-5" data-aos="fade-up">
            <h2 class="display-5 fw-bold mb-3">
              Mein <span class="gradient-text">Werdegang</span>
            </h2>
            <p class="lead text-muted">
              Eine Reise durch meine berufliche Entwicklung und wichtige Meilensteine
            </p>
          </div>

          <!-- Timeline -->
          <div class="timeline-container position-relative">
            <!-- Timeline Line -->
            <div class="timeline-line position-absolute start-0 top-0 h-100"></div>
            
            <!-- Timeline Items -->
            <div 
              v-for="(item, index) in timelineItems" 
              :key="index"
              class="timeline-item mb-5"
              :data-aos="index % 2 === 0 ? 'fade-right' : 'fade-left'"
              :data-aos-delay="index * 100"
            >
              <div class="timeline-card card border-0 shadow-sm">
                <div class="card-body">
                  <div class="timeline-header d-flex justify-content-between align-items-start mb-3">
                    <div class="timeline-title">
                      <h4 class="h5 fw-bold mb-1">{{ item.title }}</h4>
                      <h5 class="h6 text-primary mb-0">{{ item.company }}</h5>
                    </div>
                    <div class="timeline-date">
                      <span class="badge bg-primary">{{ item.period }}</span>
                    </div>
                  </div>
                  
                  <p class="timeline-description mb-3">{{ item.description }}</p>
                  
                  <!-- Technologies -->
                  <div class="timeline-technologies">
                    <div class="d-flex flex-wrap gap-2">
                      <span 
                        v-for="tech in item.technologies" 
                        :key="tech"
                        class="badge bg-light text-dark border"
                      >
                        {{ tech }}
                      </span>
                    </div>
                  </div>
                  
                  <!-- Achievements -->
                  <div v-if="item.achievements" class="timeline-achievements mt-3">
                    <h6 class="small fw-bold text-muted mb-2">Wichtige Erfolge:</h6>
                    <ul class="list-unstyled small">
                      <li v-for="achievement in item.achievements" :key="achievement" class="mb-1">
                        <i class="bi bi-check-circle-fill text-success me-2"></i>{{ achievement }}
                      </li>
                    </ul>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!-- Education Section -->
          <div class="education-section mt-5" data-aos="fade-up">
            <h3 class="h4 fw-bold text-center mb-4">Ausbildung & Zertifikate</h3>
            <div class="row g-4">
              <div 
                v-for="(edu, index) in educationItems" 
                :key="index"
                class="col-md-6"
                data-aos="fade-up"
                :data-aos-delay="index * 100"
              >
                <div class="education-card card border-0 shadow-sm h-100">
                  <div class="card-body text-center">
                    <div class="education-icon mb-3">
                      <i :class="edu.icon" class="fs-1 text-primary"></i>
                    </div>
                    <h5 class="card-title">{{ edu.title }}</h5>
                    <p class="card-text text-muted">{{ edu.institution }}</p>
                    <p class="card-text small text-primary fw-bold">{{ edu.year }}</p>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'TimelineSection',
  data() {
    return {
      timelineItems: [
        {
          title: 'Senior Frontend Entwickler',
          company: 'Tech Innovations GmbH',
          period: '2023 - Heute',
          description: 'Leitung des Frontend-Teams bei der Entwicklung einer modernen E-Commerce-Plattform. Verantwortlich für Architektur-Entscheidungen und Mentoring von Junior-Entwicklern.',
          technologies: ['Vue.js 3', 'TypeScript', 'Pinia', 'Vite', 'Tailwind CSS'],
          achievements: [
            'Team von 5 auf 12 Entwickler erweitert',
            'Performance um 40% verbessert',
            'Neue Design System implementiert'
          ]
        },
        {
          title: 'Frontend Entwickler',
          company: 'Digital Solutions AG',
          period: '2021 - 2023',
          description: 'Entwicklung von benutzerfreundlichen Webanwendungen mit Vue.js und React. Zusammenarbeit mit UX/UI Designern und Backend-Teams.',
          technologies: ['Vue.js 2', 'React', 'JavaScript', 'SASS', 'Bootstrap'],
          achievements: [
            '3 große Projekte erfolgreich abgeschlossen',
            'Kundenzufriedenheit von 85% auf 95% gesteigert',
            'Code-Review Prozess eingeführt'
          ]
        },
        {
          title: 'Junior Webentwickler',
          company: 'StartUp Ventures',
          period: '2020 - 2021',
          description: 'Erste Berufserfahrung in der Webentwicklung. Entwicklung von Landing Pages und kleinen Webanwendungen. Lernen der agilen Arbeitsweise.',
          technologies: ['HTML5', 'CSS3', 'JavaScript', 'jQuery', 'PHP'],
          achievements: [
            'Erste eigene Projekte entwickelt',
            'Agile Methoden gelernt',
            'Git Version Control beherrscht'
          ]
        },
        {
          title: 'Praktikum Webentwicklung',
          company: 'Web Design Studio',
          period: '2019 - 2020',
          description: 'Praktikum während des Studiums. Erste Einblicke in die professionelle Webentwicklung und Kundenprojekte.',
          technologies: ['HTML', 'CSS', 'JavaScript', 'Photoshop'],
          achievements: [
            'Erste Kundenprojekte umgesetzt',
            'Responsive Design gelernt',
            'Design-Thinking Prozess verstanden'
          ]
        }
      ],
      educationItems: [
        {
          title: 'Bachelor Informatik',
          institution: 'Technische Universität München',
          year: '2017 - 2021',
          icon: 'bi bi-graduation-cap-fill'
        },
        {
          title: 'Vue.js Zertifikat',
          institution: 'Vue Mastery',
          year: '2022',
          icon: 'bi bi-award-fill'
        },
        {
          title: 'AWS Cloud Practitioner',
          institution: 'Amazon Web Services',
          year: '2023',
          icon: 'bi bi-cloud-fill'
        },
        {
          title: 'Scrum Master',
          institution: 'Scrum Alliance',
          year: '2022',
          icon: 'bi bi-kanban-fill'
        }
      ]
    }
  }
}
</script>

<style scoped>
.timeline-container {
  position: relative;
}

.timeline-line {
  width: 3px;
  background: linear-gradient(to bottom, #667eea, #764ba2);
  left: 2rem;
  z-index: 1;
}

.timeline-item {
  position: relative;
  padding-left: 5rem;
}

.timeline-item::before {
  content: '';
  position: absolute;
  left: 1.5rem;
  top: 1.5rem;
  width: 15px;
  height: 15px;
  border-radius: 50%;
  background: white;
  border: 3px solid #667eea;
  z-index: 2;
  box-shadow: 0 0 0 4px white;
}

.timeline-card {
  transition: all 0.3s ease;
  border-radius: 15px;
}

.timeline-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 20px 40px rgba(0,0,0,0.1) !important;
}

.timeline-technologies .badge {
  transition: all 0.3s ease;
}

.timeline-technologies .badge:hover {
  transform: scale(1.05);
  background: #667eea !important;
  color: white !important;
}

.education-card {
  transition: all 0.3s ease;
  border-radius: 15px;
}

.education-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 15px 30px rgba(0,0,0,0.1) !important;
}

.education-icon {
  transition: transform 0.3s ease;
}

.education-card:hover .education-icon {
  transform: scale(1.2);
}

/* Responsive Design */
@media (max-width: 768px) {
  .timeline-item {
    padding-left: 3rem;
  }
  
  .timeline-line {
    left: 1.5rem;
  }
  
  .timeline-item::before {
    left: 1rem;
  }
  
  .timeline-header {
    flex-direction: column;
    align-items: flex-start !important;
  }
  
  .timeline-date {
    margin-top: 0.5rem;
  }
}

/* Animation for timeline items */
@keyframes slideInFromLeft {
  from {
    opacity: 0;
    transform: translateX(-50px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes slideInFromRight {
  from {
    opacity: 0;
    transform: translateX(50px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

.timeline-item:nth-child(even) {
  animation: slideInFromRight 0.6s ease-out;
}

.timeline-item:nth-child(odd) {
  animation: slideInFromLeft 0.6s ease-out;
}
</style>
