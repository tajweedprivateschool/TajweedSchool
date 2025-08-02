# Quick Reference Guide - Tajweed School Website

## JavaScript Functions

### Chat System
| Function | Purpose | Usage |
|----------|---------|-------|
| `openChat()` | Opens chat popup | `onclick="openChat()"` |
| `closeChat()` | Closes chat popup | `onclick="closeChat()"` |
| `sendMessage()` | Processes chat messages | `onclick="sendMessage()"` |

### Animation
| Function | Purpose | Parameters |
|----------|---------|------------|
| `AOS.init()` | Initialize scroll animations | `{duration, once, easing}` |

## CSS Classes

### Layout Components
| Class | Purpose | Usage |
|-------|---------|-------|
| `.glass-container` | Glass-morphism container | `<div class="glass-container">` |
| `.section-title` | Section headers | `<h2 class="section-title">` |
| `.header` | Sticky navigation | `<header class="header">` |

### Interactive Components
| Class | Purpose | Usage |
|-------|---------|-------|
| `.btn-primary` | Primary buttons | `<button class="btn-primary">` |
| `.chatbot-icon` | Chat trigger | `<div class="chatbot-icon">` |
| `.chat-popup` | Chat interface | `<div class="chat-popup">` |
| `.mobile-menu-btn` | Mobile menu toggle | `<div class="mobile-menu-btn">` |

### Form Components
| Class | Purpose | Usage |
|-------|---------|-------|
| `.form-tabs` | Tab container | `<div class="form-tabs">` |
| `.form-tab` | Individual tabs | `<div class="form-tab">` |
| `.form-container` | Form content | `<div class="form-container">` |

## HTML Structure

### Required Elements
```html
<!-- Chat System -->
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

<!-- Form Tabs -->
<div class="form-tabs">
  <div class="form-tab active" data-tab="registration">ثبت‌نام</div>
  <div class="form-tab" data-tab="contact">تماس</div>
</div>

<div class="form-container active" id="registration">
  <!-- Registration form -->
</div>

<div class="form-container" id="contact">
  <!-- Contact form -->
</div>
```

## CSS Variables

### Color Palette
```css
:root {
  --primary-bg: #1e1d1b;      /* Dark background */
  --accent-gold: #d6bd8a;     /* Primary gold */
  --dark-gold: #a48550;       /* Darker gold */
  --light-gold: #f0e6d2;      /* Light gold */
  --text: #ffffff;             /* White text */
  --beige: #c4b998;           /* Beige accent */
}
```

### Background Colors
```css
:root {
  --light-bg: rgba(255, 255, 255, 0.05);    /* Light overlay */
  --card-bg: rgba(30, 29, 27, 0.8);         /* Card background */
}
```

## Event Listeners

### Automatic Setup
The following event listeners are automatically configured:

1. **Chat System**
   - Click outside to close
   - Enter key to send message

2. **Mobile Menu**
   - Toggle on button click
   - Close on link click
   - Responsive behavior

3. **Form Tabs**
   - Tab switching
   - Active state management

4. **Window Resize**
   - Mobile menu responsiveness

## Animation Attributes

### AOS (Animate On Scroll)
```html
<!-- Basic usage -->
<div data-aos="fade-up">Content</div>

<!-- With options -->
<div data-aos="fade-up" 
     data-aos-duration="1000" 
     data-aos-delay="200">
  Content
</div>
```

### Available Animations
- `fade-up`, `fade-down`, `fade-left`, `fade-right`
- `zoom-in`, `zoom-out`
- `slide-up`, `slide-down`

## Chat Keywords

### Supported Persian Keywords
| Keyword | Response Type |
|---------|---------------|
| `ثبت نام` / `ثبت‌نام` | Registration info |
| `شهریه` / `هزینه` | Tuition fees |
| `کانکور` / `کنکور` | Exam preparation |
| `سلام` / `درود` | Greeting |
| `واتساپ` / `واتس اپ` | WhatsApp contact |
| `ساعت کاری` / `زمان` | Working hours |
| `آدرس` / `مکان` | Address info |

## Responsive Breakpoints

### CSS Media Queries
```css
/* Mobile */
@media (max-width: 768px) { }

/* Tablet */
@media (max-width: 992px) { }

/* Desktop */
@media (min-width: 993px) { }
```

## External Dependencies

### CDN Resources
```html
<!-- Font Awesome -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

<!-- AOS Animation -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.css">
<script src="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.js"></script>

<!-- Google Fonts -->
<link href="https://fonts.googleapis.com/css2?family=Vazirmatn:wght@300;400;500;600;700&display=swap" rel="stylesheet">
```

## Common Issues & Solutions

### Chat Not Working
- Check if JavaScript is enabled
- Verify chat elements exist in DOM
- Ensure proper event listeners are attached

### Animations Not Working
- Verify AOS library is loaded
- Check for JavaScript errors
- Ensure elements have proper data attributes

### Mobile Menu Issues
- Check viewport meta tag
- Verify CSS media queries
- Test on actual mobile devices

### Form Submission
- Ensure server-side handling is configured
- Check form action and method attributes
- Verify required fields are filled

## Performance Tips

### CSS Optimization
- Use CSS custom properties for theming
- Minimize specificity conflicts
- Use hardware-accelerated animations

### JavaScript Optimization
- Cache DOM queries
- Use event delegation
- Debounce resize handlers

### Loading Optimization
- Use CDN resources
- Minimize inline styles
- Optimize font loading

## Browser Support

### Modern Features
- **backdrop-filter**: Chrome 76+, Safari 9+, Firefox 103+
- **CSS Grid**: All modern browsers
- **Flexbox**: All modern browsers
- **CSS Custom Properties**: All modern browsers

### Fallbacks
- Provide fallbacks for backdrop-filter
- Test on older browsers
- Use polyfills when necessary

---

*This quick reference provides essential information for developers working with the Tajweed School website. For detailed documentation, refer to `API_DOCUMENTATION.md` and `COMPONENT_DOCUMENTATION.md`.*