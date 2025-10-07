<template>
  <section id="contact" class="py-5 bg-light">
    <div class="container">
      <div class="row">
        <div class="col-lg-10 mx-auto">
          <div class="section-header text-center mb-5" data-aos="fade-up">
            <h2 class="display-5 fw-bold mb-3">
              Lass uns <span class="gradient-text">in Kontakt</span> bleiben
            </h2>
            <p class="lead text-muted">
              Haben Sie ein Projekt im Kopf? Lassen Sie uns darüber sprechen!
            </p>
          </div>

          <div class="row g-5">
            <!-- Contact Form -->
            <div class="col-lg-8" data-aos="fade-right">
              <div class="contact-form-container">
                <div class="card border-0 shadow-lg">
                  <div class="card-body p-4">
                    <h3 class="h4 fw-bold mb-4">
                      <i class="bi bi-envelope-fill text-primary me-2"></i>
                      Nachricht senden
                    </h3>
                    
                    <form @submit.prevent="sendEmail" class="contact-form">
                      <div class="row g-3">
                        <div class="col-md-6">
                          <label for="name" class="form-label">Name *</label>
                          <input 
                            type="text" 
                            class="form-control" 
                            id="name" 
                            v-model="form.name"
                            required
                            :class="{ 'is-invalid': errors.name }"
                          >
                          <div v-if="errors.name" class="invalid-feedback">
                            {{ errors.name }}
                          </div>
                        </div>
                        
                        <div class="col-md-6">
                          <label for="email" class="form-label">E-Mail *</label>
                          <input 
                            type="email" 
                            class="form-control" 
                            id="email" 
                            v-model="form.email"
                            required
                            :class="{ 'is-invalid': errors.email }"
                          >
                          <div v-if="errors.email" class="invalid-feedback">
                            {{ errors.email }}
                          </div>
                        </div>
                        
                        <div class="col-12">
                          <label for="subject" class="form-label">Betreff *</label>
                          <input 
                            type="text" 
                            class="form-control" 
                            id="subject" 
                            v-model="form.subject"
                            required
                            :class="{ 'is-invalid': errors.subject }"
                          >
                          <div v-if="errors.subject" class="invalid-feedback">
                            {{ errors.subject }}
                          </div>
                        </div>
                        
                        <div class="col-12">
                          <label for="message" class="form-label">Nachricht *</label>
                          <textarea 
                            class="form-control" 
                            id="message" 
                            rows="5" 
                            v-model="form.message"
                            required
                            :class="{ 'is-invalid': errors.message }"
                            placeholder="Erzählen Sie mir von Ihrem Projekt..."
                          ></textarea>
                          <div v-if="errors.message" class="invalid-feedback">
                            {{ errors.message }}
                          </div>
                        </div>
                        
                        <!-- Buy Me a Coffee Button -->
                        <div class="col-12">
                          <div class="coffee-section p-3 bg-warning bg-opacity-10 rounded-3 mb-3">
                            <div class="d-flex align-items-center justify-content-between">
                              <div>
                                <h6 class="mb-1 fw-bold">
                                  <i class="bi bi-cup-hot-fill text-warning me-2"></i>
                                  Gefällt Ihnen meine Arbeit?
                                </h6>
                                <p class="small text-muted mb-0">
                                  Unterstützen Sie mich mit einem Kaffee! ☕
                                </p>
                              </div>
                              <a 
                                href="https://buymeacoffee.com/thunder386" 
                                target="_blank" 
                                class="btn btn-warning btn-sm"
                              >
                                <i class="bi bi-cup-hot-fill me-1"></i>
                                Buy me a Coffee
                              </a>
                            </div>
                          </div>
                        </div>
                        
                        <div class="col-12">
                          <button 
                            type="submit" 
                            class="btn btn-primary btn-lg w-100"
                            :disabled="isSubmitting"
                          >
                            <span v-if="isSubmitting" class="spinner-border spinner-border-sm me-2"></span>
                            <i v-else class="bi bi-send-fill me-2"></i>
                            {{ isSubmitting ? 'Wird gesendet...' : 'Nachricht senden' }}
                          </button>
                        </div>
                      </div>
                    </form>
                    
                    <!-- Success/Error Messages -->
                    <div v-if="message" class="alert mt-4" :class="messageClass">
                      <i :class="messageIcon" class="me-2"></i>
                      {{ message }}
                    </div>
                  </div>
                </div>
              </div>
            </div>
            
            <!-- Contact Info -->
            <div class="col-lg-4" data-aos="fade-left">
              <div class="contact-info">
                <div class="contact-info-card card border-0 shadow-sm mb-4">
                  <div class="card-body text-center">
                    <div class="contact-avatar mb-3">
                      <div class="avatar-circle mx-auto">
                        <i class="bi bi-person-fill text-white fs-3"></i>
                      </div>
                    </div>
                    <h4 class="fw-bold">Andre Dingfelder</h4>
                    <p class="text-muted">Full Stack Entwickler</p>
                    <div class="contact-social mt-3">
                      <a href="https://www.linkedin.com/in/andre-dingfelder-528367228" class="btn btn-outline-primary btn-sm me-2">
                        <i class="bi bi-linkedin"></i>
                      </a>
                      <a href="https://github.com/Thunder386" class="btn btn-outline-dark btn-sm me-2">
                        <i class="bi bi-github"></i>
                      </a>
                      <a href="https://x.com/386Thunder" class="btn btn-outline-info btn-sm">
                        <i class="bi bi-twitter"></i>
                      </a>
                    </div>
                  </div>
                </div>
                
                <!-- Contact Details -->
                <div class="contact-details">
                  <div class="contact-item card border-0 shadow-sm mb-3">
                    <div class="card-body">
                      <div class="d-flex align-items-center">
                        <div class="contact-icon me-3">
                          <i class="bi bi-envelope-fill text-primary fs-4"></i>
                        </div>
                        <div>
                          <h6 class="mb-1 fw-bold">E-Mail</h6>
                          <p class="mb-0 text-muted small">info@andredingfelder.de</p>
                        </div>
                      </div>
                    </div>
                  </div>
                  
                  <div class="contact-item card border-0 shadow-sm mb-3">
                    <div class="card-body">
                      <div class="d-flex align-items-center">
                        <div class="contact-icon me-3">
                          <i class="bi bi-geo-alt-fill text-danger fs-4"></i>
                        </div>
                        <div>
                          <h6 class="mb-1 fw-bold">Standort</h6>
                          <p class="mb-0 text-muted small">Würzburg, Deutschland</p>
                        </div>
                      </div>
                    </div>
                  </div>
                  
                  <div class="contact-item card border-0 shadow-sm">
                    <div class="card-body">
                      <div class="d-flex align-items-center">
                        <div class="contact-icon me-3">
                          <i class="bi bi-clock-fill text-warning fs-4"></i>
                        </div>
                        <div>
                          <h6 class="mb-1 fw-bold">Antwortzeit</h6>
                          <p class="mb-0 text-muted small">Innerhalb von 24 Stunden</p>
                        </div>
                      </div>
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
  name: 'ContactSection',
  data() {
    return {
      form: {
        name: '',
        email: '',
        subject: '',
        message: ''
      },
      errors: {},
      isSubmitting: false,
      message: '',
      messageClass: '',
      messageIcon: ''
    }
  },
  methods: {
    async sendEmail() {
      this.errors = {}
      this.isSubmitting = true
      this.message = ''
      
      // Validate form
      if (!this.validateForm()) {
        this.isSubmitting = false
        return
      }
      
      try {
        // Simulate email sending (replace with actual email service)
        await this.simulateEmailSending()
        
        this.message = 'Vielen Dank! Ihre Nachricht wurde erfolgreich gesendet. Ich werde mich schnellstmöglich bei Ihnen melden.'
        this.messageClass = 'alert-success'
        this.messageIcon = 'bi bi-check-circle-fill'
        
        // Reset form
        this.form = {
          name: '',
          email: '',
          subject: '',
          message: ''
        }
        
      } catch (error) {
        this.message = 'Es ist ein Fehler aufgetreten. Bitte versuchen Sie es später erneut oder kontaktieren Sie mich direkt per E-Mail.'
        this.messageClass = 'alert-danger'
        this.messageIcon = 'bi bi-exclamation-triangle-fill'
      } finally {
        this.isSubmitting = false
      }
    },
    
    validateForm() {
      const errors = {}
      
      if (!this.form.name.trim()) {
        errors.name = 'Bitte geben Sie Ihren Namen ein.'
      }
      
      if (!this.form.email.trim()) {
        errors.email = 'Bitte geben Sie Ihre E-Mail-Adresse ein.'
      } else if (!this.isValidEmail(this.form.email)) {
        errors.email = 'Bitte geben Sie eine gültige E-Mail-Adresse ein.'
      }
      
      if (!this.form.subject.trim()) {
        errors.subject = 'Bitte geben Sie einen Betreff ein.'
      }
      
      if (!this.form.message.trim()) {
        errors.message = 'Bitte geben Sie eine Nachricht ein.'
      } else if (this.form.message.trim().length < 10) {
        errors.message = 'Die Nachricht sollte mindestens 10 Zeichen lang sein.'
      }
      
      this.errors = errors
      return Object.keys(errors).length === 0
    },
    
    isValidEmail(email) {
      const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/
      return emailRegex.test(email)
    },
    
    simulateEmailSending() {
      return new Promise((resolve) => {
        setTimeout(() => {
          resolve()
        }, 2000)
      })
    }
  }
}
</script>

<style scoped>
.contact-form-container .card {
  border-radius: 20px;
}

.contact-form .form-control {
  border-radius: 10px;
  border: 2px solid #e9ecef;
  transition: all 0.3s ease;
  padding: 0.75rem 1rem;
}

.contact-form .form-control:focus {
  border-color: #667eea;
  box-shadow: 0 0 0 0.2rem rgba(102, 126, 234, 0.25);
}

.contact-form .form-label {
  font-weight: 600;
  color: #2c3e50;
  margin-bottom: 0.5rem;
}

.contact-info-card {
  border-radius: 20px;
}

.avatar-circle {
  width: 80px;
  height: 80px;
  border-radius: 50%;
  background: linear-gradient(45deg, #667eea, #764ba2);
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: 0 10px 30px rgba(102, 126, 234, 0.3);
}

.contact-item {
  border-radius: 15px;
  transition: all 0.3s ease;
}

.contact-item:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 25px rgba(0,0,0,0.1) !important;
}

.contact-icon {
  width: 50px;
  height: 50px;
  border-radius: 50%;
  background: rgba(102, 126, 234, 0.1);
  display: flex;
  align-items: center;
  justify-content: center;
  transition: transform 0.3s ease;
}

.contact-item:hover .contact-icon {
  transform: scale(1.1);
}

.coffee-section {
  border: 2px dashed #ffc107;
  transition: all 0.3s ease;
}

.coffee-section:hover {
  background: rgba(255, 193, 7, 0.2) !important;
  transform: scale(1.02);
}

.btn-primary {
  background: linear-gradient(45deg, #667eea, #764ba2);
  border: none;
  border-radius: 10px;
  padding: 0.75rem 2rem;
  font-weight: 600;
  transition: all 0.3s ease;
}

.btn-primary:hover {
  transform: translateY(-2px);
  box-shadow: 0 10px 20px rgba(102, 126, 234, 0.3);
}

.btn-primary:disabled {
  opacity: 0.7;
  transform: none;
}

.alert {
  border-radius: 10px;
  border: none;
  padding: 1rem 1.5rem;
}

.contact-social .btn {
  border-radius: 50%;
  width: 40px;
  height: 40px;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  transition: all 0.3s ease;
}

.contact-social .btn:hover {
  transform: translateY(-3px);
  box-shadow: 0 5px 15px rgba(0,0,0,0.2);
}

/* Animation for form elements */
.contact-form .form-control {
  animation: slideInUp 0.6s ease-out;
}

@keyframes slideInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* Responsive Design */
@media (max-width: 768px) {
  .contact-form-container .card-body {
    padding: 1.5rem !important;
  }
  
  .contact-item .d-flex {
    flex-direction: column;
    text-align: center;
  }
  
  .contact-icon {
    margin-bottom: 1rem;
  }
  
  .coffee-section .d-flex {
    flex-direction: column;
    text-align: center;
  }
  
  .coffee-section .btn {
    margin-top: 1rem;
  }
}

/* Loading animation */
.spinner-border-sm {
  width: 1rem;
  height: 1rem;
}

/* Success/Error message styling */
.alert-success {
  background: linear-gradient(135deg, rgba(40, 167, 69, 0.1), rgba(32, 201, 151, 0.1));
  border-left: 4px solid #28a745;
  color: #155724;
}

.alert-danger {
  background: linear-gradient(135deg, rgba(220, 53, 69, 0.1), rgba(255, 99, 132, 0.1));
  border-left: 4px solid #dc3545;
  color: #721c24;
}
</style>
