<template>
  <section id="skills" class="py-5 bg-light">
    <div class="container">
      <div class="row">
        <div class="col-lg-10 mx-auto">
          <div class="section-header text-center mb-5" data-aos="fade-up">
            <h2 class="display-5 fw-bold mb-3">
              Meine <span class="gradient-text">Fähigkeiten</span>
            </h2>
            <p class="lead text-muted">
              Technologien und Tools, mit denen ich täglich arbeite
            </p>
          </div>

          <!-- Skills Categories -->
          <div class="skills-categories">
            <!-- Frontend Skills -->
            <div class="skill-category mb-5" data-aos="fade-up">
              <div class="category-header text-center mb-4">
                <i class="bi bi-laptop fs-1 text-primary mb-3"></i>
                <h3 class="h4 fw-bold">Frontend Entwicklung</h3>
                <p class="text-muted">Moderne Benutzeroberflächen und interaktive Webanwendungen</p>
              </div>
              
              <div class="row g-4">
                <div 
                  v-for="skill in frontendSkills" 
                  :key="skill.name"
                  class="col-lg-6"
                  data-aos="fade-up"
                  :data-aos-delay="skill.delay"
                >
                  <div class="skill-item card border-0 shadow-sm h-100">
                    <div class="card-body">
                      <div class="skill-header d-flex align-items-center mb-3">
                        <div class="skill-icon me-3">
                          <i :class="skill.icon" class="fs-3 text-primary"></i>
                        </div>
                        <div class="skill-info">
                          <h5 class="skill-name mb-1">{{ skill.name }}</h5>
                          <span class="skill-level text-muted small">{{ skill.level }}</span>
                        </div>
                      </div>
                      
                      <div class="skill-bar mb-3">
                        <div class="progress" style="height: 8px;">
                          <div 
                            class="progress-bar bg-gradient" 
                            :style="{ width: skill.percentage + '%' }"
                            :data-width="skill.percentage"
                          ></div>
                        </div>
                      </div>
                      
                      <p class="skill-description small text-muted mb-0">{{ skill.description }}</p>
                    </div>
                  </div>
                </div>
              </div>
            </div>

            <!-- Backend Skills -->
            <div class="skill-category mb-5" data-aos="fade-up">
              <div class="category-header text-center mb-4">
                <i class="bi bi-server fs-1 text-success mb-3"></i>
                <h3 class="h4 fw-bold">Backend & Tools</h3>
                <p class="text-muted">Server-seitige Entwicklung und Entwicklungstools</p>
              </div>
              
              <div class="row g-4">
                <div 
                  v-for="skill in backendSkills" 
                  :key="skill.name"
                  class="col-lg-6"
                  data-aos="fade-up"
                  :data-aos-delay="skill.delay"
                >
                  <div class="skill-item card border-0 shadow-sm h-100">
                    <div class="card-body">
                      <div class="skill-header d-flex align-items-center mb-3">
                        <div class="skill-icon me-3">
                          <i :class="skill.icon" class="fs-3 text-success"></i>
                        </div>
                        <div class="skill-info">
                          <h5 class="skill-name mb-1">{{ skill.name }}</h5>
                          <span class="skill-level text-muted small">{{ skill.level }}</span>
                        </div>
                      </div>
                      
                      <div class="skill-bar mb-3">
                        <div class="progress" style="height: 8px;">
                          <div 
                            class="progress-bar bg-gradient-success" 
                            :style="{ width: skill.percentage + '%' }"
                            :data-width="skill.percentage"
                          ></div>
                        </div>
                      </div>
                      
                      <p class="skill-description small text-muted mb-0">{{ skill.description }}</p>
                    </div>
                  </div>
                </div>
              </div>
            </div>

            <!-- Soft Skills -->
            <div class="skill-category" data-aos="fade-up">
              <div class="category-header text-center mb-4">
                <i class="bi bi-people-fill fs-1 text-warning mb-3"></i>
                <h3 class="h4 fw-bold">Soft Skills</h3>
                <p class="text-muted">Persönliche Fähigkeiten und Arbeitsweise</p>
              </div>
              
              <div class="row g-4">
                <div 
                  v-for="skill in softSkills" 
                  :key="skill.name"
                  class="col-lg-4 col-md-6"
                  data-aos="zoom-in"
                  :data-aos-delay="skill.delay"
                >
                  <div class="soft-skill-item card border-0 shadow-sm h-100 text-center">
                    <div class="card-body">
                      <div class="soft-skill-icon mb-3">
                        <i :class="skill.icon" class="fs-1 text-warning"></i>
                      </div>
                      <h5 class="card-title">{{ skill.name }}</h5>
                      <p class="card-text small text-muted">{{ skill.description }}</p>
                      
                      <!-- Skill Level Dots -->
                      <div class="skill-level-dots d-flex justify-content-center gap-1">
                        <span 
                          v-for="n in 5" 
                          :key="n"
                          class="dot"
                          :class="{ 'active': n <= skill.level }"
                        ></span>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!-- Additional Info -->
          <div class="skills-footer text-center mt-5" data-aos="fade-up">
            <div class="row g-4">
              <div class="col-md-4">
                <div class="stat-item">
                  <i class="bi bi-clock-fill text-primary fs-2 mb-2"></i>
                  <h4 class="fw-bold">3+ Jahre</h4>
                  <p class="text-muted small">Berufserfahrung</p>
                </div>
              </div>
              <div class="col-md-4">
                <div class="stat-item">
                  <i class="bi bi-code-slash text-success fs-2 mb-2"></i>
                  <h4 class="fw-bold">15+</h4>
                  <p class="text-muted small">Technologien</p>
                </div>
              </div>
              <div class="col-md-4">
                <div class="stat-item">
                  <i class="bi bi-trophy-fill text-warning fs-2 mb-2"></i>
                  <h4 class="fw-bold">50+</h4>
                  <p class="text-muted small">Projekte</p>
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
  name: 'SkillsSection',
  data() {
    return {
      frontendSkills: [
        {
          name: 'Vue.js',
          icon: 'bi bi-vue',
          level: 'Experte',
          percentage: 95,
          description: '3+ Jahre Erfahrung mit Vue 2 und Vue 3, Composition API, Pinia',
          delay: 100
        },
        {
          name: 'JavaScript',
          icon: 'bi bi-filetype-js',
          level: 'Experte',
          percentage: 90,
          description: 'ES6+, TypeScript, moderne JavaScript-Patterns',
          delay: 200
        },
        {
          name: 'HTML5 & CSS3',
          icon: 'bi bi-filetype-html',
          level: 'Experte',
          percentage: 95,
          description: 'Semantisches HTML, CSS Grid, Flexbox, SASS/SCSS',
          delay: 300
        },
        {
          name: 'Bootstrap',
          icon: 'bi bi-bootstrap-fill',
          level: 'Erfahren',
          percentage: 85,
          description: 'Responsive Design, Custom Components, Bootstrap 5',
          delay: 400
        },
        {
          name: 'React',
          icon: 'bi bi-react',
          level: 'Erfahren',
          percentage: 75,
          description: 'Hooks, Context API, Redux Toolkit',
          delay: 500
        },
        {
          name: 'Tailwind CSS',
          icon: 'bi bi-palette-fill',
          level: 'Erfahren',
          percentage: 80,
          description: 'Utility-first CSS Framework, Custom Components',
          delay: 600
        }
      ],
      backendSkills: [
        {
          name: 'Node.js',
          icon: 'bi bi-server',
          level: 'Erfahren',
          percentage: 75,
          description: 'Express.js, REST APIs, Middleware',
          delay: 100
        },
        {
          name: 'Git',
          icon: 'bi bi-git',
          level: 'Erfahren',
          percentage: 85,
          description: 'Version Control, Branching, Pull Requests',
          delay: 200
        },
        {
          name: 'Docker',
          icon: 'bi bi-box-fill',
          level: 'Mittel',
          percentage: 65,
          description: 'Containerization, Docker Compose',
          delay: 300
        },
        {
          name: 'AWS',
          icon: 'bi bi-cloud-fill',
          level: 'Mittel',
          percentage: 60,
          description: 'S3, EC2, CloudFront, Lambda',
          delay: 400
        },
        {
          name: 'MySQL',
          icon: 'bi bi-database-fill',
          level: 'Erfahren',
          percentage: 70,
          description: 'Database Design, Queries, Optimization',
          delay: 500
        },
        {
          name: 'API Design',
          icon: 'bi bi-diagram-3-fill',
          level: 'Erfahren',
          percentage: 80,
          description: 'REST APIs, GraphQL, API Documentation',
          delay: 600
        }
      ],
      softSkills: [
        {
          name: 'Teamarbeit',
          icon: 'bi bi-people-fill',
          level: 5,
          description: 'Erfahrung in agilen Teams und Projektleitung',
          delay: 100
        },
        {
          name: 'Problemlösung',
          icon: 'bi bi-lightbulb-fill',
          level: 5,
          description: 'Kreative Lösungen für komplexe technische Herausforderungen',
          delay: 200
        },
        {
          name: 'Kommunikation',
          icon: 'bi bi-chat-dots-fill',
          level: 4,
          description: 'Klare Kommunikation mit Stakeholdern und Teammitgliedern',
          delay: 300
        },
        {
          name: 'Zeitmanagement',
          icon: 'bi bi-clock-fill',
          level: 4,
          description: 'Effiziente Arbeitsorganisation und Deadlines einhalten',
          delay: 400
        },
        {
          name: 'Lernbereitschaft',
          icon: 'bi bi-book-fill',
          level: 5,
          description: 'Kontinuierliche Weiterbildung und neue Technologien',
          delay: 500
        },
        {
          name: 'Mentoring',
          icon: 'bi bi-person-badge-fill',
          level: 4,
          description: 'Unterstützung und Schulung von Junior-Entwicklern',
          delay: 600
        }
      ]
    }
  },
  mounted() {
    // Animate progress bars when section comes into view
    this.animateProgressBars()
  },
  methods: {
    animateProgressBars() {
      const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
          if (entry.isIntersecting) {
            const progressBars = entry.target.querySelectorAll('.progress-bar')
            progressBars.forEach(bar => {
              const width = bar.dataset.width
              setTimeout(() => {
                bar.style.width = width + '%'
              }, 200)
            })
          }
        })
      })
      
      const skillCategories = document.querySelectorAll('.skill-category')
      skillCategories.forEach(category => observer.observe(category))
    }
  }
}
</script>

<style scoped>
.skill-item {
  transition: all 0.3s ease;
  border-radius: 15px;
}

.skill-item:hover {
  transform: translateY(-5px);
  box-shadow: 0 15px 30px rgba(0,0,0,0.1) !important;
}

.progress-bar {
  transition: width 1s ease-in-out;
  background: linear-gradient(45deg, #667eea, #764ba2) !important;
}

.progress-bar.bg-gradient-success {
  background: linear-gradient(45deg, #28a745, #20c997) !important;
}

.soft-skill-item {
  transition: all 0.3s ease;
  border-radius: 15px;
}

.soft-skill-item:hover {
  transform: translateY(-10px);
  box-shadow: 0 20px 40px rgba(0,0,0,0.1) !important;
}

.skill-level-dots {
  margin-top: 1rem;
}

.dot {
  width: 8px;
  height: 8px;
  border-radius: 50%;
  background: #e9ecef;
  transition: all 0.3s ease;
}

.dot.active {
  background: linear-gradient(45deg, #ffc107, #fd7e14);
  transform: scale(1.2);
}

.stat-item {
  padding: 1rem;
  transition: transform 0.3s ease;
}

.stat-item:hover {
  transform: scale(1.05);
}

.skill-icon {
  transition: transform 0.3s ease;
}

.skill-item:hover .skill-icon {
  transform: scale(1.2);
}

.soft-skill-icon {
  transition: transform 0.3s ease;
}

.soft-skill-item:hover .soft-skill-icon {
  transform: scale(1.2);
}

/* Gradient backgrounds for skill categories */
.skill-category:nth-child(1) {
  background: linear-gradient(135deg, rgba(102, 126, 234, 0.05) 0%, rgba(118, 75, 162, 0.05) 100%);
  padding: 2rem;
  border-radius: 20px;
}

.skill-category:nth-child(2) {
  background: linear-gradient(135deg, rgba(40, 167, 69, 0.05) 0%, rgba(32, 201, 151, 0.05) 100%);
  padding: 2rem;
  border-radius: 20px;
}

.skill-category:nth-child(3) {
  background: linear-gradient(135deg, rgba(255, 193, 7, 0.05) 0%, rgba(253, 126, 20, 0.05) 100%);
  padding: 2rem;
  border-radius: 20px;
}

@media (max-width: 768px) {
  .skill-category {
    padding: 1rem !important;
  }
  
  .skill-header {
    flex-direction: column;
    text-align: center;
  }
  
  .skill-icon {
    margin-bottom: 0.5rem;
  }
}
</style>
