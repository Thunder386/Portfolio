<template>
  <section id="hobbies" class="py-5 bg-white">
    <div class="container">
      <div class="row">
        <div class="col-lg-10 mx-auto">
          <div class="section-header text-center mb-5" data-aos="fade-up">
            <h2 class="display-5 fw-bold mb-3">
              Meine <span class="gradient-text">Engagements</span>
            </h2>
            <p class="lead text-muted">
              Ehrenamtliche Tätigkeiten, die mir wichtig sind und meinen Charakter prägen
            </p>
          </div>

          <!-- Main Hobbies Grid -->
          <div class="hobbies-grid">
            <div 
              v-for="(hobby, index) in hobbies" 
              :key="index"
              class="hobby-item"
              data-aos="fade-up"
              :data-aos-delay="index * 200"
            >
              <div class="hobby-card card border-0 shadow-lg h-100">
                <!-- Card Header -->
                <div class="hobby-header position-relative overflow-hidden">
                  <div class="hobby-icon-container">
                    <i :class="hobby.icon" class="hobby-icon"></i>
                  </div>
                  <div class="hobby-bg-pattern" :style="{ background: hobby.gradient }"></div>
                </div>
                
                <!-- Card Body -->
                <div class="card-body">
                  <h3 class="hobby-title">{{ hobby.title }}</h3>
                  <p class="hobby-description">{{ hobby.description }}</p>
                  
                  <!-- Activities -->
                  <div class="hobby-activities mb-4">
                    <h5 class="small fw-bold text-muted mb-3">Meine Aufgaben:</h5>
                    <ul class="list-unstyled">
                      <li 
                        v-for="activity in hobby.activities" 
                        :key="activity"
                        class="activity-item"
                      >
                        <i class="bi bi-check-circle-fill text-success me-2"></i>
                        {{ activity }}
                      </li>
                    </ul>
                  </div>
                  
                  <!-- Stats -->
                  <div class="hobby-stats row g-2 text-center">
                    <div class="col-4">
                      <div class="stat-number fw-bold">{{ hobby.stats.years }}</div>
                      <div class="stat-label small text-muted">Jahre</div>
                    </div>
                    <div class="col-4">
                      <div class="stat-number fw-bold">{{ hobby.stats.hours }}</div>
                      <div class="stat-label small text-muted">Std/Monat</div>
                    </div>
                    <div class="col-4">
                      <div class="stat-number fw-bold">{{ hobby.stats.events }}</div>
                      <div class="stat-label small text-muted">Einsätze</div>
                    </div>
                  </div>
                </div>
                
                <!-- Card Footer -->
                <div class="card-footer bg-transparent border-0">
                  <div class="hobby-badges">
                    <span 
                      v-for="badge in hobby.badges" 
                      :key="badge"
                      class="badge me-2 mb-2"
                      :class="badge.class"
                    >
                      {{ badge.text }}
                    </span>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!-- Impact Section -->
          <div class="impact-section mt-5" data-aos="fade-up">
            <div class="row g-4">
              <div class="col-lg-8">
                <div class="impact-content">
                  <h3 class="h4 fw-bold mb-3">Warum mir das wichtig ist</h3>
                  <p class="lead">
                    Meine ehrenamtlichen Tätigkeiten haben mich nicht nur als Person geprägt, 
                    sondern auch wertvolle Fähigkeiten für meine berufliche Entwicklung vermittelt.
                  </p>
                  
                  <div class="row g-4 mt-4">
                    <div class="col-md-6">
                      <div class="impact-item">
                        <i class="bi bi-shield-check-fill text-primary fs-3 mb-3"></i>
                        <h5 class="fw-bold">Verantwortung</h5>
                        <p class="small text-muted">
                          In kritischen Situationen schnell und besonnen handeln zu können
                        </p>
                      </div>
                    </div>
                    <div class="col-md-6">
                      <div class="impact-item">
                        <i class="bi bi-people-fill text-success fs-3 mb-3"></i>
                        <h5 class="fw-bold">Teamarbeit</h5>
                        <p class="small text-muted">
                          Vertrauen aufbauen und effektiv im Team zusammenarbeiten
                        </p>
                      </div>
                    </div>
                    <div class="col-md-6">
                      <div class="impact-item">
                        <i class="bi bi-lightning-fill text-warning fs-3 mb-3"></i>
                        <h5 class="fw-bold">Stressresistenz</h5>
                        <p class="small text-muted">
                          Unter Druck klare Entscheidungen treffen und ruhig bleiben
                        </p>
                      </div>
                    </div>
                    <div class="col-md-6">
                      <div class="impact-item">
                        <i class="bi bi-heart-fill text-danger fs-3 mb-3"></i>
                        <h5 class="fw-bold">Hilfsbereitschaft</h5>
                        <p class="small text-muted">
                          Anderen Menschen in schwierigen Situationen helfen
                        </p>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
              
              <div class="col-lg-4">
                <div class="impact-stats card border-0 shadow-sm">
                  <div class="card-body text-center">
                    <h4 class="fw-bold mb-4">Mein Beitrag</h4>
                    
                    <div class="impact-stat-item mb-4">
                      <div class="stat-circle mx-auto mb-3">
                        <i class="bi bi-clock-fill text-primary"></i>
                      </div>
                      <h3 class="fw-bold text-primary">500+</h3>
                      <p class="small text-muted">Ehrenamtliche Stunden</p>
                    </div>
                    
                    <div class="impact-stat-item mb-4">
                      <div class="stat-circle mx-auto mb-3">
                        <i class="bi bi-person-check-fill text-success"></i>
                      </div>
                      <h3 class="fw-bold text-success">50+</h3>
                      <p class="small text-muted">Menschen geholfen</p>
                    </div>
                    
                    <div class="impact-stat-item">
                      <div class="stat-circle mx-auto mb-3">
                        <i class="bi bi-award-fill text-warning"></i>
                      </div>
                      <h3 class="fw-bold text-warning">3</h3>
                      <p class="small text-muted">Organisationen</p>
                    </div>
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
  name: 'HobbiesSection',
  data() {
    return {
      hobbies: [
        {
          title: 'Freiwillige Feuerwehr',
          icon: 'bi bi-fire',
          gradient: 'linear-gradient(135deg, #ff6b6b, #ee5a24)',
          description: 'Als aktives Mitglied der Freiwilligen Feuerwehr helfe ich bei Brandschutz, technischen Hilfeleistungen und Rettungsdiensten.',
          activities: [
            'Brandbekämpfung und Rettungsdienste',
            'Technische Hilfeleistung bei Unfällen',
            'Ausbildung und Weiterbildung der Kameraden',
            'Vorbeugender Brandschutz und Aufklärung',
            'Wartung und Pflege der Ausrüstung'
          ],
          stats: {
            years: '5+',
            hours: '20',
            events: '150+'
          },
          badges: [
            { text: 'Atemschutzgeräteträger', class: 'bg-danger' },
            { text: 'Maschinist', class: 'bg-warning' },
            { text: 'Ausbilder', class: 'bg-info' }
          ]
        },
        {
          title: 'Rotes Kreuz',
          icon: 'bi bi-heart-pulse-fill',
          gradient: 'linear-gradient(135deg, #ff3838, #c44569)',
          description: 'Beim Deutschen Roten Kreuz engagiere ich mich im Sanitätsdienst und der Katastrophenhilfe.',
          activities: [
            'Sanitätsdienst bei Veranstaltungen',
            'Erste-Hilfe-Kurse leiten',
            'Katastrophenschutz und -hilfe',
            'Blutspendeaktionen unterstützen',
            'Seniorenbetreuung und Besuchsdienst'
          ],
          stats: {
            years: '4+',
            hours: '15',
            events: '80+'
          },
          badges: [
            { text: 'Sanitäter', class: 'bg-danger' },
            { text: 'Ausbilder', class: 'bg-success' },
            { text: 'Katastrophenschutz', class: 'bg-warning' }
          ]
        },
        {
          title: 'Wasserwacht',
          icon: 'bi bi-water',
          gradient: 'linear-gradient(135deg, #74b9ff, #0984e3)',
          description: 'Bei der Wasserwacht kümmere ich mich um die Sicherheit am und im Wasser.',
          activities: [
            'Wachdienst an Seen und Bädern',
            'Wasserrettung und Erste Hilfe',
            'Schwimmausbildung für Kinder',
            'Bootsführer und Rettungsschwimmer',
            'Umweltschutz und Gewässerpflege'
          ],
          stats: {
            years: '3+',
            hours: '12',
            events: '60+'
          },
          badges: [
            { text: 'Rettungsschwimmer', class: 'bg-primary' },
            { text: 'Bootsführer', class: 'bg-info' },
            { text: 'Schwimmlehrer', class: 'bg-success' }
          ]
        }
      ]
    }
  }
}
</script>

<style scoped>
.hobbies-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  gap: 2rem;
}

.hobby-card {
  transition: all 0.3s ease;
  border-radius: 20px;
  overflow: hidden;
}

.hobby-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 25px 50px rgba(0,0,0,0.15) !important;
}

.hobby-header {
  height: 120px;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
}

.hobby-icon {
  font-size: 3rem;
  color: white;
  z-index: 2;
  position: relative;
  text-shadow: 0 2px 4px rgba(0,0,0,0.3);
}

.hobby-icon-container {
  position: relative;
  z-index: 2;
}

.hobby-bg-pattern {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  opacity: 0.9;
}

.hobby-bg-pattern::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><pattern id="grain" width="100" height="100" patternUnits="userSpaceOnUse"><circle cx="50" cy="50" r="1" fill="white" opacity="0.1"/></pattern></defs><rect width="100" height="100" fill="url(%23grain)"/></svg>');
}

.hobby-title {
  font-size: 1.5rem;
  font-weight: 700;
  margin-bottom: 1rem;
  color: #2c3e50;
}

.hobby-description {
  color: #6c757d;
  line-height: 1.6;
  margin-bottom: 1.5rem;
}

.activity-item {
  margin-bottom: 0.5rem;
  font-size: 0.9rem;
}

.hobby-stats {
  background: #f8f9fa;
  border-radius: 10px;
  padding: 1rem;
  margin-top: 1rem;
}

.stat-number {
  font-size: 1.5rem;
  color: #2c3e50;
}

.stat-label {
  font-size: 0.75rem;
  text-transform: uppercase;
  letter-spacing: 0.5px;
}

.hobby-badges .badge {
  font-size: 0.75rem;
  padding: 0.5rem 0.75rem;
  border-radius: 15px;
}

.impact-item {
  text-align: center;
  padding: 1rem;
  transition: transform 0.3s ease;
}

.impact-item:hover {
  transform: translateY(-5px);
}

.impact-stats {
  border-radius: 20px;
  background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
}

.stat-circle {
  width: 60px;
  height: 60px;
  border-radius: 50%;
  background: white;
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: 0 5px 15px rgba(0,0,0,0.1);
}

.impact-stat-item {
  transition: transform 0.3s ease;
}

.impact-stat-item:hover {
  transform: scale(1.05);
}

/* Responsive Design */
@media (max-width: 768px) {
  .hobbies-grid {
    grid-template-columns: 1fr;
    gap: 1.5rem;
  }
  
  .hobby-header {
    height: 100px;
  }
  
  .hobby-icon {
    font-size: 2.5rem;
  }
  
  .hobby-stats {
    padding: 0.75rem;
  }
  
  .stat-number {
    font-size: 1.25rem;
  }
}

/* Animation for hobby cards */
@keyframes slideInUp {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.hobby-item {
  animation: slideInUp 0.6s ease-out;
}

/* Hover effects for impact items */
.impact-item i {
  transition: transform 0.3s ease;
}

.impact-item:hover i {
  transform: scale(1.2);
}
</style>
