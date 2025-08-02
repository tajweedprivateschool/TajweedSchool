# Component Documentation - Tajweed School Website

## Overview
This document provides detailed documentation for all reusable UI components in the Tajweed School website. Each component includes usage examples, customization options, and best practices.

## Table of Contents
1. [Layout Components](#layout-components)
2. [Interactive Components](#interactive-components)
3. [Form Components](#form-components)
4. [Animation Components](#animation-components)
5. [Utility Components](#utility-components)

---

## Layout Components

### Glass Container
A reusable container with glass-morphism effect and hover animations.

**CSS Class:** `.glass-container`

**Features:**
- Backdrop blur effect
- Subtle border with gold accent
- Hover animation with lift effect
- Responsive design
- Consistent with design system

**Usage:**
```html
<div class="glass-container">
  <h2>Section Title</h2>
  <p>Your content goes here</p>
</div>
```

**Customization:**
```css
/* Custom glass container */
.custom-glass {
  background: rgba(30, 29, 27, 0.9);
  backdrop-filter: blur(15px);
  border: 2px solid rgba(214, 189, 138, 0.3);
  border-radius: 20px;
}
```

**Best Practices:**
- Use for content sections that need visual separation
- Avoid nesting multiple glass containers
- Ensure sufficient contrast with text content
- Test on devices with limited backdrop-filter support

### Section Title
Consistent section headers with decorative underline.

**CSS Class:** `.section-title`

**Features:**
- Centered alignment
- Gold accent color
- Decorative underline
- Responsive typography
- Consistent spacing

**Usage:**
```html
<h2 class="section-title">عنوان بخش</h2>
```

**Customization:**
```css
/* Custom section title */
.custom-section-title {
  font-size: 42px;
  color: var(--accent-gold);
  margin-bottom: 80px;
}

.custom-section-title::after {
  width: 100px;
  height: 6px;
  background: linear-gradient(90deg, var(--accent-gold), var(--dark-gold));
}
```

### Header Component
Sticky navigation header with glass effect.

**CSS Class:** `.header`

**Features:**
- Sticky positioning
- Backdrop blur
- Responsive navigation
- Mobile menu toggle
- Logo and navigation links

**Structure:**
```html
<header class="header">
  <div class="logo">
    <img src="logo.png" alt="Logo">
    <span>مکتب تجوید</span>
  </div>
  <nav class="nav-links">
    <a href="#home">خانه</a>
    <a href="#about">درباره ما</a>
    <a href="#services">خدمات</a>
    <a href="#contact">تماس</a>
  </nav>
  <div class="mobile-menu-btn">
    <i class="fas fa-bars"></i>
  </div>
</header>
```

---

## Interactive Components

### Primary Button
Gradient button with hover effects and icon support.

**CSS Class:** `.btn-primary`

**Features:**
- Gold gradient background
- Hover animation with lift effect
- Icon support with gap spacing
- Consistent padding and typography
- Shadow effects

**Usage:**
```html
<button class="btn-primary">
  <i class="fas fa-user"></i>
  ثبت‌نام کنید
</button>
```

**Variants:**
```css
/* Secondary button variant */
.btn-secondary {
  background: transparent;
  border: 2px solid var(--accent-gold);
  color: var(--accent-gold);
}

.btn-secondary:hover {
  background: var(--accent-gold);
  color: var(--primary-bg);
}
```

**Best Practices:**
- Use for primary call-to-action buttons
- Include descriptive text with icons
- Ensure sufficient contrast ratios
- Test hover states on touch devices

### Chat System
Interactive chat interface with automated responses.

**Components:**
- Chat icon (`.chatbot-icon`)
- Chat popup (`.chat-popup`)
- Chat messages (`.chat-messages`)
- Chat input (`.chat-input`)

**Usage:**
```html
<!-- Chat Icon -->
<div class="chatbot-icon" onclick="openChat()">
  <i class="fas fa-comments"></i>
</div>

<!-- Chat Popup -->
<div id="chat-popup" class="chat-popup">
  <div class="chat-header">
    <h3>پشتیبانی آنلاین</h3>
    <button onclick="closeChat()">
      <i class="fas fa-times"></i>
    </button>
  </div>
  <div id="chat-messages" class="chat-messages"></div>
  <div class="chat-input">
    <input type="text" id="chat-input" placeholder="پیام خود را بنویسید...">
    <button onclick="sendMessage()">
      <i class="fas fa-paper-plane"></i>
    </button>
  </div>
</div>
```

**JavaScript Functions:**
```javascript
// Open chat
function openChat() {
  document.getElementById("chat-popup").style.display = "block";
}

// Close chat
function closeChat() {
  document.getElementById("chat-popup").style.display = "none";
}

// Send message
function sendMessage() {
  const input = document.getElementById("chat-input");
  const messages = document.getElementById("chat-messages");
  const userMsg = input.value;
  
  if (userMsg.trim() === "") return;
  
  messages.innerHTML += `<div class="user-msg">${userMsg}</div>`;
  
  // Generate response based on keywords
  const response = generateResponse(userMsg);
  
  setTimeout(() => {
    messages.innerHTML += `<div class="bot-msg">${response}</div>`;
    messages.scrollTop = messages.scrollHeight;
  }, 800);
  
  input.value = "";
}
```

**Customization:**
```css
/* Custom chat styles */
.custom-chat-popup {
  max-width: 400px;
  border-radius: 20px;
  box-shadow: 0 20px 60px rgba(0, 0, 0, 0.5);
}

.custom-chat-messages {
  max-height: 300px;
  overflow-y: auto;
}
```

### Mobile Menu
Responsive navigation menu for mobile devices.

**Components:**
- Mobile menu button (`.mobile-menu-btn`)
- Navigation links (`.nav-links`)

**Usage:**
```html
<div class="mobile-menu-btn">
  <i class="fas fa-bars"></i>
</div>

<nav class="nav-links">
  <a href="#home">خانه</a>
  <a href="#about">درباره ما</a>
  <a href="#services">خدمات</a>
  <a href="#contact">تماس</a>
</nav>
```

**JavaScript:**
```javascript
const mobileMenuBtn = document.querySelector('.mobile-menu-btn');
const navLinks = document.querySelector('.nav-links');

mobileMenuBtn.addEventListener('click', function() {
  navLinks.style.display = navLinks.style.display === 'flex' ? 'none' : 'flex';
});

// Close menu when clicking on links
document.querySelectorAll('.nav-links a').forEach(link => {
  link.addEventListener('click', function() {
    if (window.innerWidth <= 992) {
      navLinks.style.display = 'none';
    }
  });
});
```

---

## Form Components

### Form Tabs
Tabbed interface for switching between different forms.

**Components:**
- Form tabs container (`.form-tabs`)
- Individual tabs (`.form-tab`)
- Form containers (`.form-container`)

**Usage:**
```html
<div class="form-tabs">
  <div class="form-tab active" data-tab="registration">ثبت‌نام</div>
  <div class="form-tab" data-tab="contact">تماس</div>
</div>

<div class="form-container active" id="registration">
  <!-- Registration form content -->
</div>

<div class="form-container" id="contact">
  <!-- Contact form content -->
</div>
```

**JavaScript:**
```javascript
document.querySelectorAll('.form-tab').forEach(tab => {
  tab.addEventListener('click', function() {
    // Remove active class from all tabs and containers
    document.querySelectorAll('.form-tab').forEach(t => t.classList.remove('active'));
    document.querySelectorAll('.form-container').forEach(c => c.classList.remove('active'));
    
    // Add active class to clicked tab and corresponding container
    this.classList.add('active');
    document.getElementById(this.dataset.tab).classList.add('active');
  });
});
```

**Customization:**
```css
/* Custom tab styles */
.custom-form-tab {
  background: var(--card-bg);
  border: 1px solid var(--accent-gold);
  border-radius: 10px;
  padding: 15px 25px;
  margin: 0 10px;
  cursor: pointer;
  transition: all 0.3s ease;
}

.custom-form-tab.active {
  background: var(--accent-gold);
  color: var(--primary-bg);
  transform: translateY(-2px);
}
```

### Form Input
Styled form inputs with consistent design.

**Usage:**
```html
<div class="form-group">
  <label for="name">نام</label>
  <input type="text" id="name" name="name" required>
</div>

<div class="form-group">
  <label for="email">ایمیل</label>
  <input type="email" id="email" name="email" required>
</div>

<div class="form-group">
  <label for="phone">شماره تلفن</label>
  <input type="tel" id="phone" name="phone" required>
</div>
```

**Customization:**
```css
/* Custom form input styles */
.custom-input {
  background: var(--card-bg);
  border: 1px solid rgba(214, 189, 138, 0.3);
  border-radius: 8px;
  padding: 12px 16px;
  color: var(--text);
  font-size: 16px;
  transition: border-color 0.3s ease;
}

.custom-input:focus {
  outline: none;
  border-color: var(--accent-gold);
  box-shadow: 0 0 0 2px rgba(214, 189, 138, 0.2);
}
```

---

## Animation Components

### AOS Animations
Scroll-triggered animations using AOS library.

**Setup:**
```html
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.css">
<script src="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.js"></script>
```

**Initialization:**
```javascript
AOS.init({
  duration: 1000,
  once: true,
  easing: 'ease-out'
});
```

**Usage:**
```html
<!-- Fade up animation -->
<div data-aos="fade-up" data-aos-duration="1000">
  <h2>Animated Title</h2>
  <p>This content will fade up when scrolled into view.</p>
</div>

<!-- Slide in from left -->
<div data-aos="fade-right" data-aos-delay="200">
  <p>This content will slide in from the left with a delay.</p>
</div>

<!-- Zoom in effect -->
<div data-aos="zoom-in" data-aos-duration="800">
  <img src="image.jpg" alt="Animated image">
</div>
```

**Available Animations:**
- `fade-up` - Fade in from bottom
- `fade-down` - Fade in from top
- `fade-left` - Fade in from right
- `fade-right` - Fade in from left
- `zoom-in` - Zoom in effect
- `zoom-out` - Zoom out effect
- `slide-up` - Slide up from bottom
- `slide-down` - Slide down from top

**Customization:**
```html
<!-- Custom animation with all options -->
<div data-aos="fade-up"
     data-aos-duration="1200"
     data-aos-delay="300"
     data-aos-easing="ease-in-out"
     data-aos-once="true"
     data-aos-anchor-placement="top-center">
  Custom animated content
</div>
```

### Hover Animations
CSS-based hover effects for interactive elements.

**Button Hover:**
```css
.btn-primary:hover {
  transform: translateY(-3px);
  box-shadow: 0 8px 25px rgba(214, 189, 138, 0.5);
  background: linear-gradient(145deg, var(--dark-gold), var(--accent-gold));
}
```

**Card Hover:**
```css
.glass-container:hover {
  transform: translateY(-5px);
  box-shadow: 0 12px 40px rgba(0, 0, 0, 0.4);
}
```

**Link Hover:**
```css
.nav-links a:hover {
  color: var(--accent-gold);
  transform: translateY(-2px);
}
```

---

## Utility Components

### Loading Spinner
Simple loading indicator for async operations.

**CSS:**
```css
.loading-spinner {
  width: 40px;
  height: 40px;
  border: 4px solid rgba(214, 189, 138, 0.3);
  border-top: 4px solid var(--accent-gold);
  border-radius: 50%;
  animation: spin 1s linear infinite;
}

@keyframes spin {
  0% { transform: rotate(0deg); }
  100% { transform: rotate(360deg); }
}
```

**Usage:**
```html
<div class="loading-spinner"></div>
```

### Success Message
Styled success notification component.

**CSS:**
```css
.success-message {
  background: rgba(76, 175, 80, 0.1);
  border: 1px solid #4caf50;
  border-radius: 8px;
  padding: 16px;
  color: #4caf50;
  text-align: center;
  margin: 20px 0;
}
```

**Usage:**
```html
<div class="success-message">
  <i class="fas fa-check-circle"></i>
  فرم با موفقیت ارسال شد!
</div>
```

### Error Message
Styled error notification component.

**CSS:**
```css
.error-message {
  background: rgba(244, 67, 54, 0.1);
  border: 1px solid #f44336;
  border-radius: 8px;
  padding: 16px;
  color: #f44336;
  text-align: center;
  margin: 20px 0;
}
```

**Usage:**
```html
<div class="error-message">
  <i class="fas fa-exclamation-circle"></i>
  خطا در ارسال فرم. لطفاً دوباره تلاش کنید.
</div>
```

### Responsive Grid
Flexible grid system for responsive layouts.

**CSS:**
```css
.responsive-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 30px;
  padding: 20px;
}

@media (max-width: 768px) {
  .responsive-grid {
    grid-template-columns: 1fr;
    gap: 20px;
  }
}
```

**Usage:**
```html
<div class="responsive-grid">
  <div class="glass-container">
    <h3>Card 1</h3>
    <p>Content for card 1</p>
  </div>
  <div class="glass-container">
    <h3>Card 2</h3>
    <p>Content for card 2</p>
  </div>
  <div class="glass-container">
    <h3>Card 3</h3>
    <p>Content for card 3</p>
  </div>
</div>
```

---

## Best Practices

### Accessibility
- Use semantic HTML elements
- Provide alt text for images
- Ensure sufficient color contrast
- Add focus indicators for interactive elements
- Test with screen readers

### Performance
- Minimize CSS and JavaScript
- Use efficient selectors
- Optimize images and assets
- Implement lazy loading where appropriate
- Cache static resources

### Responsive Design
- Use relative units (rem, em, %)
- Test on multiple screen sizes
- Implement mobile-first approach
- Optimize touch targets for mobile
- Consider loading times on slow connections

### Browser Compatibility
- Test on multiple browsers
- Provide fallbacks for modern CSS features
- Use polyfills when necessary
- Consider progressive enhancement

---

## Component Testing

### Manual Testing Checklist
- [ ] Components render correctly
- [ ] Interactive elements respond to user input
- [ ] Animations work as expected
- [ ] Responsive behavior on different screen sizes
- [ ] Accessibility features work properly
- [ ] Performance is acceptable

### Automated Testing
Consider implementing automated tests for:
- Component rendering
- User interactions
- Form validation
- Animation triggers
- Responsive breakpoints

---

*This component documentation provides comprehensive guidance for using and customizing all UI components in the Tajweed School website. For additional support, refer to the main API documentation or contact the development team.*