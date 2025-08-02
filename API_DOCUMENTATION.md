# API Documentation - Tajweed School Website

## Overview
This documentation covers all public APIs, functions, and components in the Tajweed School website. The project is a single-page application built with HTML, CSS, and JavaScript, featuring a Persian/Farsi interface for a religious school.

## Table of Contents
1. [JavaScript Functions](#javascript-functions)
2. [CSS Components](#css-components)
3. [HTML Structure](#html-structure)
4. [Event Listeners](#event-listeners)
5. [Usage Examples](#usage-examples)

---

## JavaScript Functions

### Animation Functions

#### `AOS.init(configuration)`
Initializes the AOS (Animate On Scroll) library for scroll-based animations.

**Parameters:**
- `configuration` (Object): Configuration object for AOS
  - `duration` (Number): Animation duration in milliseconds (default: 1000)
  - `once` (Boolean): Whether animation should occur only once (default: true)
  - `easing` (String): Easing function for animations (default: 'ease-out')

**Example:**
```javascript
AOS.init({
  duration: 1000,
  once: true,
  easing: 'ease-out'
});
```

### Chat System Functions

#### `openChat()`
Opens the chat popup interface.

**Returns:** `undefined`

**Example:**
```javascript
// Call when user clicks chat icon
openChat();
```

#### `closeChat()`
Closes the chat popup interface.

**Returns:** `undefined`

**Example:**
```javascript
// Call when user clicks close button
closeChat();
```

#### `sendMessage()`
Processes and sends user messages in the chat interface. Handles user input, generates automated responses based on keywords, and updates the chat display.

**Functionality:**
- Retrieves user input from chat input field
- Validates input (prevents empty messages)
- Displays user message in chat
- Generates automated responses based on Persian keywords
- Displays bot response with delay
- Scrolls chat to bottom
- Clears input field

**Supported Keywords and Responses:**
- `ثبت نام` / `ثبت‌نام` → Registration information
- `شهریه` / `هزینه` → Tuition fee information
- `کانکور` / `کنکور` → Exam preparation course details
- `سلام` / `درود` → Greeting response
- `واتساپ` / `واتس اپ` → WhatsApp contact information
- `ساعت کاری` / `زمان` → Working hours
- `آدرس` / `مکان` → Address and location information

**Returns:** `undefined`

**Example:**
```javascript
// Called when user clicks send button or presses Enter
sendMessage();
```

### Form Handling Functions

#### Form Submission Handlers
The website includes form submission handlers for registration and contact forms.

**Registration Form Handler:**
```javascript
document.getElementById('registrationForm').addEventListener('submit', function(e) {
  e.preventDefault();
  // Form processing logic
  this.style.display = 'none';
  document.getElementById('register-success').style.display = 'block';
});
```

**Contact Form Handler:**
```javascript
document.getElementById('contactForm').addEventListener('submit', function(e) {
  e.preventDefault();
  // Form processing logic
  this.style.display = 'none';
  document.getElementById('contact-success').style.display = 'block';
});
```

---

## CSS Components

### Design System Variables
The website uses CSS custom properties for consistent theming:

```css
:root {
  --primary-bg: #1e1d1b;
  --accent-gold: #d6bd8a;
  --dark-gold: #a48550;
  --light-gold: #f0e6d2;
  --light-bg: rgba(255, 255, 255, 0.05);
  --card-bg: rgba(30, 29, 27, 0.8);
  --text: #ffffff;
  --beige: #c4b998;
}
```

### Glass Container Component
Reusable glass-morphism container with hover effects:

```css
.glass-container {
  background: var(--card-bg);
  backdrop-filter: blur(10px);
  -webkit-backdrop-filter: blur(10px);
  border: 1px solid rgba(214, 189, 138, 0.2);
  border-radius: 16px;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.glass-container:hover {
  transform: translateY(-5px);
  box-shadow: 0 12px 40px rgba(0, 0, 0, 0.4);
}
```

### Button Components

#### Primary Button
```css
.btn-primary {
  background: linear-gradient(145deg, var(--accent-gold), var(--dark-gold));
  color: var(--primary-bg);
  border: none;
  padding: 14px 32px;
  border-radius: 10px;
  font-weight: 600;
  font-size: 18px;
  cursor: pointer;
  transition: all 0.3s ease;
  box-shadow: 0 4px 15px rgba(214, 189, 138, 0.3);
  display: inline-flex;
  align-items: center;
  gap: 10px;
}

.btn-primary:hover {
  transform: translateY(-3px);
  box-shadow: 0 8px 25px rgba(214, 189, 138, 0.5);
  background: linear-gradient(145deg, var(--dark-gold), var(--accent-gold));
}
```

### Section Title Component
```css
.section-title {
  text-align: center;
  font-size: 36px;
  margin-bottom: 60px;
  position: relative;
  color: var(--accent-gold);
}

.section-title::after {
  content: '';
  position: absolute;
  bottom: -15px;
  left: 50%;
  transform: translateX(-50%);
  width: 80px;
  height: 4px;
  background: var(--accent-gold);
  border-radius: 2px;
}
```

---

## HTML Structure

### Main Sections
1. **Header** - Navigation and logo
2. **Hero Section** - Main banner with call-to-action
3. **About Section** - School information
4. **Services Section** - Course offerings
5. **Contact Section** - Contact forms and information
6. **Footer** - Additional links and information

### Key HTML Elements

#### Chat System
```html
<div class="chatbot-icon" onclick="openChat()">
  <i class="fas fa-comments"></i>
</div>

<div id="chat-popup" class="chat-popup">
  <div class="chat-header">
    <h3>پشتیبانی آنلاین</h3>
    <button onclick="closeChat()"><i class="fas fa-times"></i></button>
  </div>
  <div id="chat-messages" class="chat-messages"></div>
  <div class="chat-input">
    <input type="text" id="chat-input" placeholder="پیام خود را بنویسید...">
    <button onclick="sendMessage()"><i class="fas fa-paper-plane"></i></button>
  </div>
</div>
```

#### Form Tabs
```html
<div class="form-tabs">
  <div class="form-tab active" data-tab="registration">ثبت‌نام</div>
  <div class="form-tab" data-tab="contact">تماس</div>
</div>
```

---

## Event Listeners

### Document-Level Events

#### Click Outside Chat
```javascript
document.addEventListener('click', function(event) {
  const chatPopup = document.getElementById('chat-popup');
  const chatIcon = document.querySelector('.chatbot-icon');
  if (chatPopup.style.display === 'block' && 
      !chatPopup.contains(event.target) && 
      event.target !== chatIcon && 
      !chatIcon.contains(event.target)) {
    chatPopup.style.display = 'none';
  }
});
```

#### Enter Key for Chat
```javascript
document.getElementById('chat-input').addEventListener('keypress', function(e) {
  if (e.key === 'Enter') {
    sendMessage();
  }
});
```

### Mobile Menu Events

#### Menu Toggle
```javascript
const mobileMenuBtn = document.querySelector('.mobile-menu-btn');
const navLinks = document.querySelector('.nav-links');
mobileMenuBtn.addEventListener('click', function() {
  navLinks.style.display = navLinks.style.display === 'flex' ? 'none' : 'flex';
});
```

#### Mobile Menu Link Click
```javascript
document.querySelectorAll('.nav-links a').forEach(link => {
  link.addEventListener('click', function() {
    if (window.innerWidth <= 992) {
      navLinks.style.display = 'none';
    }
  });
});
```

#### Window Resize Handler
```javascript
window.addEventListener('resize', function() {
  if (window.innerWidth > 992) {
    navLinks.style.display = 'flex';
  } else {
    navLinks.style.display = 'none';
  }
});
```

### Form Tab Events
```javascript
document.querySelectorAll('.form-tab').forEach(tab => {
  tab.addEventListener('click', function() {
    document.querySelectorAll('.form-tab').forEach(t => t.classList.remove('active'));
    document.querySelectorAll('.form-container').forEach(c => c.classList.remove('active'));
    this.classList.add('active');
    document.getElementById(this.dataset.tab).classList.add('active');
  });
});
```

---

## Usage Examples

### Implementing Chat System
```html
<!-- Add chat icon to your page -->
<div class="chatbot-icon" onclick="openChat()">
  <i class="fas fa-comments"></i>
</div>

<!-- Add chat popup -->
<div id="chat-popup" class="chat-popup">
  <!-- Chat content -->
</div>
```

### Using Glass Container Component
```html
<div class="glass-container">
  <h2>Your Content</h2>
  <p>This will have the glass-morphism effect</p>
</div>
```

### Creating Form Tabs
```html
<div class="form-tabs">
  <div class="form-tab active" data-tab="form1">Tab 1</div>
  <div class="form-tab" data-tab="form2">Tab 2</div>
</div>

<div class="form-container active" id="form1">
  <!-- Form 1 content -->
</div>

<div class="form-container" id="form2">
  <!-- Form 2 content -->
</div>
```

### Adding AOS Animations
```html
<div data-aos="fade-up" data-aos-duration="1000">
  <!-- This element will animate on scroll -->
</div>
```

---

## Browser Compatibility

### CSS Features
- **backdrop-filter**: Modern browsers (Chrome 76+, Safari 9+, Firefox 103+)
- **CSS Grid**: All modern browsers
- **Flexbox**: All modern browsers
- **CSS Custom Properties**: All modern browsers

### JavaScript Features
- **ES6+**: All modern browsers
- **addEventListener**: All modern browsers
- **querySelector/querySelectorAll**: All modern browsers

### External Dependencies
- **Font Awesome 6.4.0**: Icon library
- **AOS 2.3.4**: Animation library
- **Google Fonts (Vazirmatn)**: Persian font

---

## Performance Considerations

### CSS Optimizations
- Use of CSS custom properties for consistent theming
- Efficient selectors and minimal specificity conflicts
- Hardware-accelerated animations (transform, opacity)

### JavaScript Optimizations
- Event delegation for dynamic elements
- Debounced resize handlers
- Efficient DOM queries with caching

### Loading Optimizations
- External CDN resources for faster loading
- Minimal inline styles
- Optimized font loading with display=swap

---

## Security Considerations

### Form Handling
- Client-side validation for user experience
- Server-side validation required for production
- CSRF protection recommended for form submissions

### Content Security
- Sanitize user inputs in chat system
- Validate form data before processing
- Implement rate limiting for chat functionality

---

## Deployment Notes

### File Structure
```
/
├── README.md (main HTML file)
├── LICENSE
├── .gitignore
└── API_DOCUMENTATION.md (this file)
```

### Production Considerations
1. Minify CSS and JavaScript
2. Optimize images and assets
3. Implement proper form handling on server
4. Add analytics and monitoring
5. Configure proper caching headers
6. Implement error handling and logging

---

## Support and Maintenance

### Common Issues
1. **Chat not working**: Check if JavaScript is enabled
2. **Animations not working**: Verify AOS library is loaded
3. **Forms not submitting**: Ensure server-side handling is configured
4. **Mobile menu issues**: Check viewport meta tag

### Future Enhancements
1. Add more sophisticated chat responses
2. Implement real-time chat functionality
3. Add form validation feedback
4. Implement progressive web app features
5. Add multi-language support
6. Implement analytics tracking

---

*This documentation covers all public APIs, functions, and components in the Tajweed School website. For additional support or questions, refer to the main README.md file or contact the development team.*