<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>لیسه عالی خصوصی تجوید | آموزش با کیفیت</title>
  <link href="https://fonts.googleapis.com/css2?family=Vazirmatn:wght@300;400;500;600;700&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Vazirmatn', sans-serif;
    }
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
    body {
      background-color: var(--primary-bg);
      color: var(--text);
      line-height: 1.8;
      overflow-x: hidden;
      background: radial-gradient(circle at top, #2d2c29, #1a1917);
    }
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
    .header {
      padding: 20px 5%;
      display: flex;
      justify-content: space-between;
      align-items: center;
      position: sticky;
      top: 0;
      z-index: 1000;
      background: rgba(30, 29, 27, 0.95);
      backdrop-filter: blur(10px);
      border-bottom: 1px solid rgba(214, 189, 138, 0.1);
    }
    .logo {
      display: flex;
      align-items: center;
      gap: 15px;
      transition: transform 0.3s ease;
    }
    .logo:hover {
      transform: scale(1.05);
    }
    .logo img {
      height: 70px;
      width: auto;
      border-radius: 50%;
      border: 2px solid var(--accent-gold);
      padding: 5px;
    }
    .logo-text {
      font-size: 28px;
      font-weight: 700;
      color: var(--accent-gold);
      text-shadow: 0 0 10px rgba(214, 189, 138, 0.3);
    }
    .nav-links {
      display: flex;
      gap: 30px;
    }
    .nav-links a {
      color: var(--text);
      text-decoration: none;
      font-weight: 500;
      position: relative;
      padding: 8px 0;
      transition: color 0.3s ease;
    }
    .nav-links a::after {
      content: '';
      position: absolute;
      width: 0;
      height: 3px;
      bottom: 0;
      left: 0;
      background-color: var(--accent-gold);
      transition: width 0.3s ease;
    }
    .nav-links a:hover {
      color: var(--accent-gold);
    }
    .nav-links a:hover::after {
      width: 100%;
    }
    .hero {
      height: 90vh;
      background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url('https://page.genspark.site/v1/base64_upload/9d6045ae80360a0ebc1d17d829dc2d24') no-repeat center center/cover;
      display: flex;
      align-items: center;
      position: relative;
      overflow: hidden;
    }
    .hero::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: linear-gradient(45deg, rgba(30, 29, 27, 0.3), rgba(214, 189, 138, 0.1));
    }
    .hero-content {
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 5%;
      position: relative;
      z-index: 1;
      text-align: center;
    }
    .hero h1 {
      font-size: 52px;
      margin-bottom: 20px;
      color: var(--accent-gold);
      text-shadow: 0 2px 10px rgba(0, 0, 0, 0.5);
      line-height: 1.3;
    }
    .hero p {
      font-size: 22px;
      margin-bottom: 40px;
      max-width: 800px;
      color: var(--light-gold);
      margin-left: auto;
      margin-right: auto;
    }
    .about {
      padding: 100px 5%;
      display: flex;
      align-items: center;
      gap: 50px;
      max-width: 1400px;
      margin: 0 auto;
    }
    .about-image {
      flex: 1;
      border-radius: 16px;
      overflow: hidden;
      box-shadow: 0 15px 30px rgba(0, 0, 0, 0.4);
    }
    .about-image img {
      width: 100%;
      height: auto;
      display: block;
      transition: transform 0.5s ease;
    }
    .about-image:hover img {
      transform: scale(1.05);
    }
    .about-content {
      flex: 1;
    }
    .about-content h2 {
      font-size: 36px;
      color: var(--accent-gold);
      margin-bottom: 30px;
    }
    .about-content p {
      font-size: 18px;
      line-height: 1.8;
      color: var(--light-gold);
      margin-bottom: 20px;
    }
    .mission-vision {
      padding: 80px 5%;
      background: linear-gradient(rgba(30, 29, 27, 0.9), rgba(30, 29, 27, 0.9)), url('https://page.genspark.site/v1/base64_upload/5f9a8b12c91c286ebd6f5ff8dea3eaa5') center/cover;
      position: relative;
    }
    .mission-vision::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.6);
    }
    .mission-vision-content {
      position: relative;
      z-index: 1;
      max-width: 1200px;
      margin: 0 auto;
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
      gap: 50px;
    }
    .mission-card, .vision-card {
      padding: 40px;
    }
    .mission-card h3, .vision-card h3 {
      font-size: 28px;
      color: var(--accent-gold);
      margin-bottom: 25px;
      position: relative;
      padding-bottom: 15px;
    }
    .mission-card h3::after, .vision-card h3::after {
      content: '';
      position: absolute;
      bottom: 0;
      right: 0;
      width: 60px;
      height: 3px;
      background: var(--accent-gold);
    }
    .mission-card p, .vision-card p {
      font-size: 18px;
      line-height: 1.8;
      color: var(--light-gold);
    }
    .programs {
      padding: 100px 5%;
      max-width: 1400px;
      margin: 0 auto;
    }
    .programs-container {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
      gap: 40px;
      margin-top: 50px;
    }
    .program-card {
      padding: 40px 30px;
      position: relative;
      overflow: hidden;
    }
    .program-card::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 5px;
      background: linear-gradient(90deg, var(--accent-gold), var(--dark-gold));
    }
    .program-icon {
      font-size: 50px;
      color: var(--accent-gold);
      margin-bottom: 25px;
      transition: transform 0.3s ease;
    }
    .program-card:hover .program-icon {
      transform: scale(1.1);
    }
    .program-card h3 {
      font-size: 26px;
      margin-bottom: 20px;
      color: var(--accent-gold);
    }
    .program-card p {
      color: var(--light-gold);
      font-size: 18px;
      margin-bottom: 25px;
    }
    .program-details {
      margin-top: 20px;
    }
    .program-details li {
      margin-bottom: 10px;
      color: var(--light-gold);
      display: flex;
      align-items: center;
      gap: 10px;
    }
    .program-details li i {
      color: var(--accent-gold);
    }
    .facilities {
      padding: 100px 5%;
      background: var(--primary-bg);
    }
    .facilities-container {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 30px;
      margin-top: 50px;
    }
    .facility-card {
      position: relative;
      border-radius: 16px;
      overflow: hidden;
      height: 250px;
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
    }
    .facility-card img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: transform 0.5s ease;
    }
    .facility-card:hover img {
      transform: scale(1.1);
    }
    .facility-overlay {
      position: absolute;
      bottom: 0;
      left: 0;
      width: 100%;
      padding: 20px;
      background: linear-gradient(to top, rgba(0, 0, 0, 0.8), transparent);
    }
    .facility-overlay h3 {
      color: var(--accent-gold);
      font-size: 22px;
      margin-bottom: 10px;
    }
    .facility-overlay p {
      color: var(--light-gold);
      font-size: 16px;
    }
    .stats {
      padding: 80px 5%;
      background: linear-gradient(rgba(30, 29, 27, 0.9), rgba(30, 29, 27, 0.9)), url('https://page.genspark.site/v1/base64_upload/9207bf7d2bfa35e12c59069c6d10fa46') center/cover;
      position: relative;
    }
    .stats::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.6);
    }
    .stats-content {
      position: relative;
      z-index: 1;
      max-width: 1400px;
      margin: 0 auto;
    }
    .stats-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 40px;
    }
    .stat-card {
      text-align: center;
      padding: 40px 30px;
    }
    .stat-number {
      font-size: 56px;
      font-weight: 700;
      color: var(--accent-gold);
      margin-bottom: 15px;
      font-family: 'Vazirmatn', sans-serif;
      text-shadow: 0 0 15px rgba(214, 189, 138, 0.4);
    }
    .stat-label {
      font-size: 22px;
      color: var(--light-gold);
      font-weight: 500;
    }
    .testimonials {
      padding: 100px 5%;
      max-width: 1400px;
      margin: 0 auto;
    }
    .testimonial-container {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
      gap: 40px;
      margin-top: 50px;
    }
    .testimonial-card {
      padding: 35px;
      position: relative;
    }
    .testimonial-card::before {
      content: '"';
      position: absolute;
      top: 20px;
      left: 25px;
      font-size: 100px;
      color: rgba(214, 189, 138, 0.1);
      font-family: serif;
      line-height: 1;
    }
    .testimonial-text {
      font-size: 18px;
      margin-bottom: 25px;
      color: var(--light-gold);
      font-style: italic;
      position: relative;
      z-index: 1;
    }
    .testimonial-author {
      display: flex;
      align-items: center;
      gap: 15px;
    }
    .author-avatar {
      width: 60px;
      height: 60px;
      border-radius: 50%;
      border: 2px solid var(--accent-gold);
      overflow: hidden;
    }
    .author-avatar img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
    .author-info h4 {
      color: var(--accent-gold);
      font-size: 20px;
      margin-bottom: 5px;
    }
    .author-info p {
      color: var(--light-gold);
      font-size: 16px;
    }
    .gallery {
      padding: 80px 5%;
      background: var(--primary-bg);
    }
    .gallery-container {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 20px;
      margin-top: 50px;
    }
    .gallery-item {
      position: relative;
      border-radius: 10px;
      overflow: hidden;
      height: 250px;
      box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
    }
    .gallery-item img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: transform 0.5s ease;
    }
    .gallery-item:hover img {
      transform: scale(1.1);
    }
    .gallery-overlay {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.5);
      display: flex;
      align-items: center;
      justify-content: center;
      opacity: 0;
      transition: opacity 0.3s ease;
    }
    .gallery-item:hover .gallery-overlay {
      opacity: 1;
    }
    .gallery-overlay i {
      color: white;
      font-size: 40px;
    }
    .contact {
      padding: 100px 5%;
      background: linear-gradient(rgba(30, 29, 27, 0.9), rgba(30, 29, 27, 0.9)), url('https://page.genspark.site/v1/base64_upload/1c62826e13efca63ce1054f93cad362a') center/cover;
      position: relative;
    }
    .contact::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.7);
    }
    .contact-container {
      position: relative;
      z-index: 1;
      max-width: 1200px;
      margin: 0 auto;
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
      gap: 50px;
    }
    .contact-info {
      display: flex;
      flex-direction: column;
      gap: 30px;
    }
    .contact-item {
      display: flex;
      align-items: center;
      gap: 20px;
    }
    .contact-icon {
      width: 60px;
      height: 60px;
      background: rgba(214, 189, 138, 0.1);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      color: var(--accent-gold);
      font-size: 24px;
    }
    .contact-text h3 {
      color: var(--accent-gold);
      font-size: 22px;
      margin-bottom: 10px;
    }
    .contact-text p, .contact-text a {
      color: var(--light-gold);
      font-size: 18px;
      text-decoration: none;
      transition: color 0.3s ease;
    }
    .contact-text a:hover {
      color: var(--accent-gold);
    }
    .map-container {
      height: 100%;
      min-height: 400px;
      border-radius: 16px;
      overflow: hidden;
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.4);
    }
    .map-container iframe {
      width: 100%;
      height: 100%;
      border: none;
    }
    .footer {
      background: linear-gradient(to top, #1a1917, #0f0e0d);
      padding: 60px 5% 30px;
      border-top: 1px solid rgba(214, 189, 138, 0.1);
    }
    .footer-content {
      max-width: 1400px;
      margin: 0 auto;
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 50px;
    }
    .footer-section h3 {
      color: var(--accent-gold);
      font-size: 24px;
      margin-bottom: 25px;
      position: relative;
      padding-bottom: 15px;
    }
    .footer-section h3::after {
      content: '';
      position: absolute;
      bottom: 0;
      right: 0;
      width: 60px;
      height: 3px;
      background: var(--accent-gold);
    }
    .footer-links {
      list-style: none;
    }
    .footer-links li {
      margin-bottom: 15px;
    }
    .footer-links a {
      color: var(--light-gold);
      text-decoration: none;
      transition: color 0.3s ease;
      display: flex;
      align-items: center;
      gap: 10px;
    }
    .footer-links a:hover {
      color: var(--accent-gold);
    }
    .social-links {
      display: flex;
      gap: 20px;
      margin-top: 30px;
    }
    .social-links a {
      width: 50px;
      height: 50px;
      background: rgba(214, 189, 138, 0.1);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      color: var(--accent-gold);
      font-size: 20px;
      transition: all 0.3s ease;
    }
    .social-links a:hover {
      background: var(--accent-gold);
      color: var(--primary-bg);
      transform: translateY(-5px);
    }
    .copyright {
      text-align: center;
      padding-top: 40px;
      margin-top: 40px;
      border-top: 1px solid rgba(255, 255, 255, 0.05);
      color: var(--light-gold);
      font-size: 16px;
    }
    .whatsapp-chat {
      position: fixed;
      bottom: 20px;
      right: 20px;
      z-index: 1000;
      display: flex;
      flex-direction: column;
      gap: 15px;
    }
    .whatsapp-icon {
      width: 65px;
      height: 65px;
      background: #25D366;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      color: white;
      font-size: 34px;
      box-shadow: 0 4px 15px rgba(37, 211, 102, 0.4);
      cursor: pointer;
      transition: all 0.3s ease;
      animation: pulse 2s infinite;
    }
    .whatsapp-icon:hover {
      transform: scale(1.1);
      box-shadow: 0 6px 20px rgba(37, 211, 102, 0.6);
      animation: none;
    }
    .chatbot-icon {
      width: 65px;
      height: 65px;
      background: linear-gradient(145deg, var(--accent-gold), var(--dark-gold));
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      color: var(--primary-bg);
      font-size: 32px;
      box-shadow: 0 4px 15px rgba(214, 189, 138, 0.4);
      cursor: pointer;
      transition: all 0.3s ease;
      animation: float 3s ease-in-out infinite;
    }
    .chatbot-icon:hover {
      transform: scale(1.1);
      box-shadow: 0 6px 20px rgba(214, 189, 138, 0.6);
      animation: none;
    }
    .chat-popup {
      position: fixed;
      bottom: 100px;
      right: 20px;
      width: 380px;
      height: 500px;
      border-radius: 20px;
      box-shadow: 0 10px 40px rgba(0, 0, 0, 0.6);
      overflow: hidden;
      display: none;
      z-index: 999;
      border: 1px solid rgba(214, 189, 138, 0.3);
    }
    .chat-header {
      background: linear-gradient(90deg, var(--primary-bg), #2a2926);
      color: var(--accent-gold);
      padding: 18px;
      display: flex;
      align-items: center;
      gap: 12px;
      border-bottom: 1px solid rgba(214, 189, 138, 0.2);
      font-weight: 600;
      font-size: 18px;
    }
    .chat-messages {
      background: var(--primary-bg);
      height: 380px;
      padding: 20px;
      overflow-y: auto;
      display: flex;
      flex-direction: column;
      gap: 15px;
    }
    .user-msg, .bot-msg {
      max-width: 85%;
      padding: 14px 18px;
      border-radius: 18px;
      line-height: 1.6;
      position: relative;
      animation: fadeIn 0.3s ease;
    }
    .user-msg {
      background: linear-gradient(135deg, var(--accent-gold), var(--dark-gold));
      color: var(--primary-bg);
      margin-left: auto;
      border-top-right-radius: 5px;
      box-shadow: 0 4px 10px rgba(214, 189, 138, 0.3);
    }
    .bot-msg {
      background: var(--light-bg);
      color: var(--text);
      margin-right: auto;
      border-top-left-radius: 5px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
    }
    .chat-input {
      display: flex;
      background: var(--primary-bg);
      padding: 12px;
      border-top: 1px solid rgba(255, 255, 255, 0.1);
    }
    .chat-input input {
      flex: 1;
      background: rgba(255, 255, 255, 0.1);
      border: 1px solid rgba(214, 189, 138, 0.2);
      padding: 14px 18px;
      border-radius: 30px;
      color: white;
      margin-right: 10px;
      outline: none;
      transition: all 0.3s ease;
      font-size: 16px;
    }
    .chat-input input:focus {
      border-color: var(--accent-gold);
      box-shadow: 0 0 0 2px rgba(214, 189, 138, 0.3);
    }
    .chat-input button {
      background: var(--accent-gold);
      color: var(--primary-bg);
      border: none;
      width: 50px;
      height: 50px;
      border-radius: 50%;
      cursor: pointer;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 20px;
      transition: all 0.3s ease;
    }
    .chat-input button:hover {
      transform: scale(1.1);
      background: var(--dark-gold);
    }
    /* استایل‌های جدید برای فرم‌ها */
    .forms-section {
      padding: 100px 5%;
      max-width: 1400px;
      margin: 0 auto;
    }
    .form-container {
      display: none;
      max-width: 800px;
      margin: 0 auto;
      padding: 40px;
    }
    .form-container.active {
      display: block;
    }
    .form-tabs {
      display: flex;
      justify-content: center;
      margin-bottom: 40px;
      gap: 20px;
    }
    .form-tab {
      padding: 15px 30px;
      background: rgba(214, 189, 138, 0.1);
      border-radius: 10px;
      cursor: pointer;
      transition: all 0.3s ease;
      font-weight: 600;
      color: var(--light-gold);
      border: 1px solid rgba(214, 189, 138, 0.3);
    }
    .form-tab.active {
      background: linear-gradient(145deg, var(--accent-gold), var(--dark-gold));
      color: var(--primary-bg);
      box-shadow: 0 4px 15px rgba(214, 189, 138, 0.3);
    }
    .form-tab:hover:not(.active) {
      background: rgba(214, 189, 138, 0.2);
    }
    .form-group {
      margin-bottom: 25px;
    }
    .form-group label {
      display: block;
      margin-bottom: 10px;
      color: var(--accent-gold);
      font-weight: 500;
    }
    .form-group .required {
      color: #e74c3c;
      margin-right: 5px;
    }
    .form-control {
      width: 100%;
      padding: 14px 20px;
      background: rgba(255, 255, 255, 0.05);
      border: 1px solid rgba(214, 189, 138, 0.3);
      border-radius: 10px;
      color: var(--text);
      font-size: 16px;
      transition: all 0.3s ease;
    }
    .form-control:focus {
      outline: none;
      border-color: var(--accent-gold);
      box-shadow: 0 0 0 3px rgba(214, 189, 138, 0.2);
    }
    textarea.form-control {
      min-height: 120px;
      resize: vertical;
    }
    .form-submit {
      background: linear-gradient(145deg, var(--accent-gold), var(--dark-gold));
      color: var(--primary-bg);
      border: none;
      padding: 16px 40px;
      border-radius: 10px;
      font-weight: 600;
      font-size: 18px;
      cursor: pointer;
      transition: all 0.3s ease;
      box-shadow: 0 4px 15px rgba(214, 189, 138, 0.3);
      display: inline-flex;
      align-items: center;
      gap: 12px;
      margin-top: 20px;
      width: 100%;
      justify-content: center;
    }
    .form-submit:hover {
      transform: translateY(-3px);
      box-shadow: 0 8px 25px rgba(214, 189, 138, 0.5);
      background: linear-gradient(145deg, var(--dark-gold), var(--accent-gold));
    }
    .form-row {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
    }
    .form-success {
      display: none;
      text-align: center;
      padding: 40px;
    }
    .form-success i {
      font-size: 60px;
      color: #27ae60;
      margin-bottom: 20px;
    }
    .form-success h3 {
      font-size: 28px;
      color: var(--accent-gold);
      margin-bottom: 15px;
    }
    .form-success p {
      color: var(--light-gold);
      font-size: 18px;
      line-height: 1.8;
    }
    /* Animations */
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(10px); }
      to { opacity: 1; transform: translateY(0); }
    }
    @keyframes pulse {
      0% { transform: scale(1); }
      50% { transform: scale(1.05); }
      100% { transform: scale(1); }
    }
    @keyframes float {
      0% { transform: translateY(0px); }
      50% { transform: translateY(-10px); }
      100% { transform: translateY(0px); }
    }
    /* Mobile Menu Button */
    .mobile-menu-btn {
      display: none;
      background: transparent;
      border: none;
      color: var(--accent-gold);
      font-size: 28px;
      cursor: pointer;
    }
    /* Responsive Styles */
    @media (max-width: 1200px) {
      .about {
        flex-direction: column;
      }
      .about-image, .about-content {
        flex: none;
        width: 100%;
      }
    }
    @media (max-width: 992px) {
      .hero h1 {
        font-size: 42px;
      }
      .hero p {
        font-size: 20px;
      }
      .nav-links {
        display: none;
      }
      .mobile-menu-btn {
        display: block;
      }
      .section-title {
        font-size: 32px;
      }
    }
    @media (max-width: 768px) {
      .hero {
        height: 80vh;
      }
      .hero h1 {
        font-size: 36px;
      }
      .hero p {
        font-size: 18px;
      }
      .section-title {
        font-size: 30px;
      }
      .stat-number {
        font-size: 46px;
      }
      .chat-popup {
        width: 320px;
        height: 450px;
        bottom: 90px;
        right: 10px;
      }
      .whatsapp-chat {
        flex-direction: row;
        bottom: 20px;
        right: 20px;
      }
    }
    @media (max-width: 480px) {
      .hero h1 {
        font-size: 30px;
      }
      .logo-text {
        font-size: 22px;
      }
      .logo img {
        height: 50px;
      }
      .program-card, .testimonial-card {
        padding: 30px 20px;
      }
      .chat-popup {
        width: 300px;
        height: 420px;
        bottom: 80px;
      }
      .gallery-container {
        grid-template-columns: 1fr;
      }
    }
    /* Scrollbar */
    ::-webkit-scrollbar {
      width: 8px;
    }
    ::-webkit-scrollbar-track {
      background: rgba(30, 29, 27, 0.8);
    }
    ::-webkit-scrollbar-thumb {
      background: var(--accent-gold);
      border-radius: 4px;
    }
    ::-webkit-scrollbar-thumb:hover {
      background: var(--dark-gold);
    }
  </style>
</head>
<body>
  <header class="header">
    <div class="logo">
      <img src="https://page.genspark.site/v1/base64_upload/e15ea70c0aad1c22b030e48b82f093ae" alt="لوگوی مکتب خصوصی تجوید">
      <div class="logo-text">لیسه عالی خصوصی تجوید</div>
    </div>
    <nav class="nav-links">
      <a href="#">خانه</a>
      <a href="#about">درباره ما</a>
      <a href="#programs">برنامه‌های آموزشی</a>
      <a href="#facilities">امکانات</a>
      <a href="#contact">تماس با ما</a>
      <a href="#register">ثبت‌نام</a>
    </nav>
    <button class="mobile-menu-btn">
      <i class="fas fa-bars"></i>
    </button>
  </header>
  <section class="hero">
    <div class="hero-content">
      <h1 data-aos="fade-up">یک دانش‌آموز، یک ملت</h1>
      <p data-aos="fade-up" data-aos-delay="100">مکتب خصوصی تجوید با بیش از 15 سال سابقه درخشان در تربیت نسلی آگاه، متخصص و متعهد</p>
      <button class="btn-primary" data-aos="fade-up" data-aos-delay="200">
        <i class="fas fa-user-graduate"></i>
        ثبت‌نام در دوره‌ها
      </button>
    </div>
  </section>
  <section class="about" id="about">
    <div class="about-image" data-aos="fade-right">
      <img src="https://page.genspark.site/v1/base64_upload/5f0cbe53f17abfa326cc30ac4cb470a0" alt="مراسم در مکتب تجوید">
    </div>
    <div class="about-content" data-aos="fade-left">
      <h2>درباره مکتب خصوصی تجوید</h2>
      <p>لیسه عالی خصوصی تجوید در سال 1388 هجری شمسی با هدف ارائه آموزش‌های با کیفیت و پرورش دانش‌آموزان متعهد تأسیس شد. ما با بهره‌گیری از کادر آموزشی مجرب و امکانات مدرن، محیطی ایده‌آل برای یادگیری فراهم کرده‌ایم.</p>
      <p>مکتب ما با شعار "یک دانش‌آموز، یک ملت" به پرورش نسلی می‌پردازد که بتواند نقش مؤثری در پیشرفت جامعه داشته باشد. نرخ قبولی دانش‌آموزان ما در کانکور بیش از 95% است که نشان‌دهنده کیفیت بالای آموزشی ما می‌باشد.</p>
      <button class="btn-primary">
        <i class="fas fa-info-circle"></i>
        بیشتر بدانید
      </button>
    </div>
  </section>
  <section class="mission-vision">
    <div class="mission-vision-content">
      <div class="mission-card glass-container" data-aos="fade-up">
        <h3>مأموریت ما</h3>
        <p>تربیت نسلی آگاه، متخصص و متعهد که بتوانند نقش موثری در پیشرفت جامعه داشته باشند. ما با ارائه آموزش‌های علمی، دینی و مهارت‌های زندگی، دانش‌آموزان را برای چالش‌های آینده آماده می‌کنیم.</p>
      </div>
      <div class="vision-card glass-container" data-aos="fade-up" data-aos-delay="100">
        <h3>چشم‌انداز ما</h3>
        <p>تبدیل شدن به مرجع برتر آموزشی در کشور و پرورش دانش‌آموزانی که نه تنها از نظر علمی، بلکه از لحاظ اخلاقی و اجتماعی نیز سرآمد باشند. ما به دنبال ایجاد تحول در نظام آموزشی کشور هستیم.</p>
      </div>
    </div>
  </section>
  <section class="programs" id="programs">
    <h2 class="section-title" data-aos="fade-up">برنامه‌های آموزشی</h2>
    <div class="programs-container">
      <div class="program-card glass-container" data-aos="fade-up">
        <div class="program-icon">
          <i class="fas fa-quran"></i>
        </div>
        <h3>تجوید و علوم قرآنی</h3>
        <p>دوره‌های تخصصی تجوید، تفسیر و علوم قرآنی با بهره‌گیری از اساتید مجرب و روش‌های نوین آموزشی.</p>
        <ul class="program-details">
          <li><i class="fas fa-clock"></i> مدت: 3 ماه</li>
          <li><i class="fas fa-user-graduate"></i> مقاطع: ابتدایی تا لیسه</li>
          <li><i class="fas fa-certificate"></i> گواهینامه معتبر</li>
        </ul>
      </div>
      <div class="program-card glass-container" data-aos="fade-up" data-aos-delay="100">
        <div class="program-icon">
          <i class="fas fa-university"></i>
        </div>
        <h3>آمادگی کانکور</h3>
        <p>دوره فشرده آمادگی برای آزمون کانکور با نرخ قبولی بیش از 95% در سال‌های اخیر.</p>
        <ul class="program-details">
          <li><i class="fas fa-clock"></i> مدت: 6 ماه</li>
          <li><i class="fas fa-book"></i> دروس: ریاضی، فیزیک، کیمیا، بیولوژی</li>
          <li><i class="fas fa-chart-line"></i> موفقیت تضمینی</li>
        </ul>
      </div>
      <div class="program-card glass-container" data-aos="fade-up" data-aos-delay="200">
        <div class="program-icon">
          <i class="fas fa-hands-helping"></i>
        </div>
        <h3>مهارت‌های زندگی</h3>
        <p>آموزش مهارت‌های ضروری زندگی از جمله مدیریت زمان، ارتباط مؤثر، حل مسئله و کار تیمی.</p>
        <ul class="program-details">
          <li><i class="fas fa-clock"></i> مدت: 2 ماه</li>
          <li><i class="fas fa-users"></i> گروه‌های سنی: 12 تا 18 سال</li>
          <li><i class="fas fa-brain"></i> تقویت هوش هیجانی</li>
        </ul>
      </div>
    </div>
  </section>
  <section class="facilities" id="facilities">
    <h2 class="section-title" data-aos="fade-up">امکانات و تسهیلات</h2>
    <div class="facilities-container">
      <div class="facility-card" data-aos="fade-up">
        <img src="https://page.genspark.site/v1/base64_upload/5f9a8b12c91c286ebd6f5ff8dea3eaa5" alt="فضای آموزشی">
        <div class="facility-overlay">
          <h3>فضای آموزشی استاندارد</h3>
          <p>کلاس‌های مجهز به آخرین امکانات آموزشی</p>
        </div>
      </div>
      <div class="facility-card" data-aos="fade-up" data-aos-delay="100">
        <img src="https://page.genspark.site/v1/base64_upload/409db47d4584f4ad4a27559cdb6313e6" alt="فضای امتحانات">
        <div class="facility-overlay">
          <h3>فضای مناسب امتحانات</h3>
          <p>سالن‌های مجزا برای برگزاری آزمون‌ها</p>
        </div>
      </div>
      <div class="facility-card" data-aos="fade-up" data-aos-delay="200">
        <img src="https://page.genspark.site/v1/base64_upload/ba56fff8e99aec7a1ef413d255f82893" alt="امکانات ورزشی">
        <div class="facility-overlay">
          <h3>امکانات ورزشی</h3>
          <p>سالن ورزشی و زمین فوتبال</p>
        </div>
      </div>
      <div class="facility-card" data-aos="fade-up">
        <img src="https://page.genspark.site/v1/base64_upload/5b88e649849185e2681010f3d988739e" alt="فضای فرهنگی">
        <div class="facility-overlay">
          <h3>فضای فرهنگی</h3>
          <p>کتابخانه و سالن مطالعه</p>
        </div>
      </div>
      <div class="facility-card" data-aos="fade-up" data-aos-delay="100">
        <img src="https://page.genspark.site/v1/base64_upload/9207bf7d2bfa35e12c59069c6d10fa46" alt="سالن اجتماعات">
        <div class="facility-overlay">
          <h3>سالن اجتماعات</h3>
          <p>ظرفیت 200 نفر برای مراسم و همایش‌ها</p>
        </div>
      </div>
      <div class="facility-card" data-aos="fade-up" data-aos-delay="200">
        <img src="https://page.genspark.site/v1/base64_upload/1c62826e13efca63ce1054f93cad362a" alt="سالن سخنرانی">
        <div class="facility-overlay">
          <h3>سالن سخنرانی</h3>
          <p>مجهز به سیستم صوتی و تصویری پیشرفته</p>
        </div>
      </div>
    </div>
  </section>
  <section class="stats">
    <h2 class="section-title" data-aos="fade-up">دستاوردهای ما</h2>
    <div class="stats-content">
      <div class="stats-grid">
        <div class="stat-card" data-aos="fade-up" data-aos-delay="0">
          <div class="stat-number">15+</div>
          <div class="stat-label">سال سابقه آموزشی</div>
        </div>
        <div class="stat-card" data-aos="fade-up" data-aos-delay="100">
          <div class="stat-number">2500+</div>
          <div class="stat-label">دانش‌آموز فعال</div>
        </div>
        <div class="stat-card" data-aos="fade-up" data-aos-delay="200">
          <div class="stat-number">35+</div>
          <div class="stat-label">استاد مجرب</div>
        </div>
        <div class="stat-card" data-aos="fade-up" data-aos-delay="300">
          <div class="stat-number">95%</div>
          <div class="stat-label">نرخ قبولی کانکور</div>
        </div>
      </div>
    </div>
  </section>
  <section class="testimonials">
    <h2 class="section-title" data-aos="fade-up">نظرات دانش‌آموزان و والدین</h2>
    <div class="testimonial-container">
      <div class="testimonial-card glass-container" data-aos="fade-up">
        <div class="testimonial-text">
          مکتب خصوصی تجوید علاوه بر ارائه آموزش‌های علمی با کیفیت، در پرورش شخصیت و مهارت‌های اجتماعی فرزندم نیز نقش بسزایی داشته است.
        </div>
        <div class="testimonial-author">
          <div class="author-avatar">
            <img src="https://randomuser.me/api/portraits/men/32.jpg" alt="محمد امینی">
          </div>
          <div class="author-info">
            <h4>محمد امینی</h4>
            <p>والد یکی از دانش‌آموزان</p>
          </div>
        </div>
      </div>
      <div class="testimonial-card glass-container" data-aos="fade-up" data-aos-delay="100">
        <div class="testimonial-text">
          استادان با تجربه و محیط آموزشی مناسب مکتب تجوید، من را در مسیر موفقیت قرار داد و توانستم در کانکور با رتبه عالی پذیرفته شوم.
        </div>
        <div class="testimonial-author">
          <div class="author-avatar">
            <img src="https://randomuser.me/api/portraits/men/54.jpg" alt="احمد رضایی">
          </div>
          <div class="author-info">
            <h4>احمد رضایی</h4>
            <p>فارغ‌التحصیل سال 1400</p>
          </div>
        </div>
      </div>
      <div class="testimonial-card glass-container" data-aos="fade-up" data-aos-delay="200">
        <div class="testimonial-text">
          دوره‌های مهارت‌های زندگی مکتب تجوید به من کمک کرد تا اعتماد به نفس بیشتری داشته باشم و بهتر بتوانم با چالش‌های زندگی مواجه شوم.
        </div>
        <div class="testimonial-author">
          <div class="author-avatar">
            <img src="https://randomuser.me/api/portraits/women/67.jpg" alt="فاطمه حسینی">
          </div>
          <div class="author-info">
            <h4>فاطمه حسینی</h4>
            <p>دانش‌آموز دوره مهارت‌های زندگی</p>
          </div>
        </div>
      </div>
    </div>
  </section>
  <section class="gallery">
    <h2 class="section-title" data-aos="fade-up">گالری تصاویر</h2>
    <div class="gallery-container">
      <div class="gallery-item" data-aos="fade-up">
        <img src="https://page.genspark.site/v1/base64_upload/506d20892a2e161b37d33dca048415da" alt="جشن فارغ‌التحصیلی">
        <div class="gallery-overlay">
          <i class="fas fa-search-plus"></i>
        </div>
      </div>
      <div class="gallery-item" data-aos="fade-up" data-aos-delay="100">
        <img src="https://page.genspark.site/v1/base64_upload/d134a7c39ff0000a8681ebab2fb9b468" alt="سمینار آموزشی">
        <div class="gallery-overlay">
          <i class="fas fa-search-plus"></i>
        </div>
      </div>
      <div class="gallery-item" data-aos="fade-up" data-aos-delay="200">
        <img src="https://page.genspark.site/v1/base64_upload/5f0cbe53f17abfa326cc30ac4cb470a0" alt="جشنواره فرهنگی">
        <div class="gallery-overlay">
          <i class="fas fa-search-plus"></i>
        </div>
      </div>
      <div class="gallery-item" data-aos="fade-up">
        <img src="https://page.genspark.site/v1/base64_upload/ba56fff8e99aec7a1ef413d255f82893" alt="تیم ورزشی">
        <div class="gallery-overlay">
          <i class="fas fa-search-plus"></i>
        </div>
      </div>
      <div class="gallery-item" data-aos="fade-up" data-aos-delay="100">
        <img src="https://page.genspark.site/v1/base64_upload/4052f88082d5587a159bd1bf4644f99a" alt="اهدای گواهینامه">
        <div class="gallery-overlay">
          <i class="fas fa-search-plus"></i>
        </div>
      </div>
      <div class="gallery-item" data-aos="fade-up" data-aos-delay="200">
        <img src="https://page.genspark.site/v1/base64_upload/409db47d4584f4ad4a27559cdb6313e6" alt="فضای امتحانات">
        <div class="gallery-overlay">
          <i class="fas fa-search-plus"></i>
        </div>
      </div>
    </div>
  </section>
  <section class="forms-section" id="register">
    <h2 class="section-title" data-aos="fade-up">ثبت‌نام و تماس</h2>
    <div class="form-tabs">
      <div class="form-tab active" data-tab="register-form">فرم ثبت‌نام</div>
      <div class="form-tab" data-tab="contact-form">درخواست تماس</div>
    </div>
    <!-- فرم ثبت‌نام -->
    <div class="form-container glass-container active" id="register-form">
      <form id="registrationForm">
        <div class="form-row">
          <div class="form-group">
            <label for="fullname"><span class="required">*</span> نام کامل</label>
            <input type="text" id="fullname" name="fullname" class="form-control" required>
          </div>
          <div class="form-group">
            <label for="age"><span class="required">*</span> سن</label>
            <input type="number" id="age" name="age" class="form-control" required min="5" max="80">
          </div>
        </div>
        <div class="form-row">
          <div class="form-group">
            <label for="gender"><span class="required">*</span> جنسیت</label>
            <select id="gender" name="gender" class="form-control" required>
              <option value="">انتخاب کنید</option>
              <option value="مرد">مرد</option>
              <option value="زن">زن</option>
            </select>
          </div>
          <div class="form-group">
            <label for="phone"><span class="required">*</span> شماره تماس</label>
            <input type="tel" id="phone" name="phone" class="form-control" required>
          </div>
        </div>
        <div class="form-row">
          <div class="form-group">
            <label for="email">آدرس ایمیل</label>
            <input type="email" id="email" name="email" class="form-control">
          </div>
          <div class="form-group">
            <label for="level"><span class="required">*</span> سطح فعلی تجوید</label>
            <select id="level" name="level" class="form-control" required>
              <option value="">انتخاب کنید</option>
              <option value="مبتدی">مبتدی (تازه کار)</option>
              <option value="متوسط">متوسط</option>
              <option value="پیشرفته">پیشرفته</option>
            </select>
          </div>
        </div>
        <div class="form-group">
          <label for="time"><span class="required">*</span> زمان‌های پیشنهادی برای کلاس</label>
          <textarea id="time" name="time" class="form-control" required></textarea>
        </div>
        <div class="form-group">
          <label for="goals">اهداف شما از یادگیری تجوید</label>
          <textarea id="goals" name="goals" class="form-control"></textarea>
        </div>
        <div class="form-group">
          <label for="notes">ملاحظات یا سوالات خاص</label>
          <textarea id="notes" name="notes" class="form-control"></textarea>
        </div>
        <button type="submit" class="form-submit">
          <i class="fas fa-paper-plane"></i>
          ارسال درخواست ثبت‌نام
        </button>
      </form>
      <div class="form-success" id="register-success">
        <i class="fas fa-check-circle"></i>
        <h3>درخواست ثبت‌نام شما با موفقیت ارسال شد</h3>
        <p>کارشناسان ما به زودی با شما تماس خواهند گرفت. برای اطلاعات بیشتر می‌توانید با شماره ۰۷۹۴۸۲۹۰۹۰ تماس بگیرید.</p>
      </div>
    </div>
    <!-- فرم درخواست تماس -->
    <div class="form-container glass-container" id="contact-form">
      <form id="contactForm">
        <div class="form-row">
          <div class="form-group">
            <label for="contact-name"><span class="required">*</span> نام شما</label>
            <input type="text" id="contact-name" name="name" class="form-control" required>
          </div>
          <div class="form-group">
            <label for="contact-phone"><span class="required">*</span> شماره تماس</label>
            <input type="tel" id="contact-phone" name="phone" class="form-control" required>
          </div>
        </div>
        <div class="form-group">
          <label for="contact-email">آدرس ایمیل</label>
          <input type="email" id="contact-email" name="email" class="form-control">
        </div>
        <div class="form-group">
          <label for="subject"><span class="required">*</span> موضوع درخواست</label>
          <select id="subject" name="subject" class="form-control" required>
            <option value="">انتخاب کنید</option>
            <option value="ثبت‌نام در دوره">ثبت‌نام در دوره</option>
            <option value="سوال درباره دوره‌ها">سوال درباره دوره‌ها</option>
            <option value="مشاوره رایگان">مشاوره رایگان</option>
            <option value="همکاری با مکتب">همکاری با مکتب</option>
            <option value="سایر">سایر</option>
          </select>
        </div>
        <div class="form-group">
          <label for="message"><span class="required">*</span> پیام شما</label>
          <textarea id="message" name="message" class="form-control" required></textarea>
        </div>
        <div class="form-group">
          <label for="best-time">بهترین زمان برای تماس</label>
          <input type="text" id="best-time" name="best-time" class="form-control" placeholder="مثلاً: بین ساعت 14 تا 18">
        </div>
        <button type="submit" class="form-submit">
          <i class="fas fa-headset"></i>
          ارسال درخواست تماس
        </button>
      </form>
      <div class="form-success" id="contact-success">
        <i class="fas fa-check-circle"></i>
        <h3>درخواست تماس شما با موفقیت ارسال شد</h3>
        <p>کارشناسان ما در اسرع وقت با شما تماس خواهند گرفت. برای ارتباط فوری می‌توانید با شماره ۰۷۹۴۸۲۹۰۹۰ تماس بگیرید.</p>
      </div>
    </div>
  </section>
  <section class="contact" id="contact">
    <h2 class="section-title" data-aos="fade-up">تماس با ما</h2>
    <div class="contact-container">
      <div class="contact-info" data-aos="fade-right">
        <div class="contact-item">
          <div class="contact-icon">
            <i class="fas fa-map-marker-alt"></i>
          </div>
          <div class="contact-text">
            <h3>آدرس مکتب</h3>
            <p>کابل افغانستان، جاده شهید مزاری، ایستگاه تانک تیل، بعد از اولین سه‌راهی به سمت راست، کوچه سوم</p>
          </div>
        </div>
        <div class="contact-item">
          <div class="contact-icon">
            <i class="fas fa-phone"></i>
          </div>
          <div class="contact-text">
            <h3>تلفن تماس</h3>
            <a href="tel:+93794829090">0093794829090</a>
          </div>
        </div>
        <div class="contact-item">
          <div class="contact-icon">
            <i class="fas fa-envelope"></i>
          </div>
          <div class="contact-text">
            <h3>ایمیل</h3>
            <a href="mailto:info.tajweedprivatehighschool@gmail.com">info.tajweedprivatehighschool@gmail.com</a>
          </div>
        </div>
        <div class="contact-item">
          <div class="contact-icon">
            <i class="fas fa-clock"></i>
          </div>
          <div class="contact-text">
            <h3>ساعات کاری</h3>
            <p>شنبه تا پنجشنبه: 7:00 صبح تا 4:00 بعد از ظهر</p>
          </div>
        </div>
      </div>
      <div class="map-container" data-aos="fade-left">
        <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3289.1234567890123!2d69.12345678901234!3d34.12345678901234!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2zMzTCsDA3JzI0LjQiTiA2OcKwMDcnMjQuNCJF!5e0!3m2!1sen!2saf!4v1234567890123!5m2!1sen!2saf" allowfullscreen="" loading="lazy"></iframe>
      </div>
    </div>
  </section>
  <footer class="footer">
    <div class="footer-content">
      <div class="footer-section">
        <h3>درباره مکتب تجوید</h3>
        <p style="color: #d6bd8a; margin-bottom: 20px; line-height: 1.8;">
          لیسه عالی خصوصی تجوید با بیش از ۱۵ سال سابقه درخشان در زمینه آموزش و پرورش، با بهره‌گیری از اساتید مجرب و روش‌های نوین آموزشی، محیطی مناسب برای یادگیری عمیق فراهم کرده است.
        </p>
        <div class="social-links">
          <a href="#"><i class="fab fa-facebook-f"></i></a>
          <a href="#"><i class="fab fa-instagram"></i></a>
          <a href="#"><i class="fab fa-telegram"></i></a>
          <a href="#"><i class="fab fa-youtube"></i></a>
        </div>
      </div>
      <div class="footer-section">
        <h3>لینک‌های سریع</h3>
        <ul class="footer-links">
          <li><a href="#"><i class="fas fa-angle-left"></i> خانه</a></li>
          <li><a href="#about"><i class="fas fa-angle-left"></i> درباره ما</a></li>
          <li><a href="#programs"><i class="fas fa-angle-left"></i> برنامه‌های آموزشی</a></li>
          <li><a href="#facilities"><i class="fas fa-angle-left"></i> امکانات</a></li>
          <li><a href="#contact"><i class="fas fa-angle-left"></i> تماس با ما</a></li>
        </ul>
      </div>
      <div class="footer-section">
        <h3>ثبت‌نام</h3>
        <ul class="footer-links">
          <li><a href="#"><i class="fas fa-angle-left"></i> شرایط ثبت‌نام</a></li>
          <li><a href="#"><i class="fas fa-angle-left"></i> مدارک مورد نیاز</a></li>
          <li><a href="#"><i class="fas fa-angle-left"></i> شهریه و هزینه‌ها</a></li>
          <li><a href="#"><i class="fas fa-angle-left"></i> فرم درخواست ثبت‌نام</a></li>
          <li><a href="#"><i class="fas fa-angle-left"></i> برنامه زمان‌بندی آزمون‌ها</a></li>
        </ul>
      </div>
    </div>
    <div class="copyright">
      © ۱۴۰۲ لیسه عالی خصوصی تجوید. تمامی حقوق محفوظ است.
    </div>
  </footer>
  <div class="whatsapp-chat">
    <div class="chatbot-icon" onclick="openChat()">
      <i class="fas fa-robot"></i>
    </div>
    <a href="https://wa.me/93794829090" target="_blank" class="whatsapp-icon">
      <i class="fab fa-whatsapp"></i>
    </a>
  </div>
  <div class="chat-popup" id="chat-popup">
    <div class="chat-header">
      <i class="fas fa-robot"></i>
      <span>تجوید هوشمند</span>
    </div>
    <div class="chat-messages" id="chat-messages">
      <div class="bot-msg">
        خوش آمدید به مکتب خصوصی تجوید 🌟<br>
        من تجوید هوشمند هستم. چگونه می‌توانم کمکتان کنم؟
      </div>
    </div>
    <div class="chat-input">
      <input type="text" id="chat-input" placeholder="پیام خود را بنویسید...">
      <button onclick="sendMessage()"><i class="fas fa-paper-plane"></i></button>
    </div>
  </div>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.js"></script>
  <script>
    // Initialize AOS for animations
    AOS.init({
      duration: 1000,
      once: true,
      easing: 'ease-out'
    });
    function openChat() {
      document.getElementById("chat-popup").style.display = "block";
    }
    function closeChat() {
      document.getElementById("chat-popup").style.display = "none";
    }
    function sendMessage() {
      const input = document.getElementById("chat-input");
      const messages = document.getElementById("chat-messages");
      const userMsg = input.value;
      if (userMsg.trim() === "") return;
      messages.innerHTML += `<div class="user-msg">${userMsg}</div>`;
      const lowerMsg = userMsg.toLowerCase();
      let reply = "متوجه نشدم. لطفاً واضح‌تر بپرسید.";
      if (lowerMsg.includes("ثبت نام") || lowerMsg.includes("ثبت‌نام")) {
        reply = "برای ثبت‌نام به صفحه ثبت‌نام مراجعه کنید یا با ۰۷۹۴۸۲۹۰۹۰ تماس بگیرید. همچنین می‌توانید از طریق لینک زیر اقدام کنید:<br><a href='#' style='color: #d6bd8a; text-decoration: underline;'>صفحه ثبت‌نام</a>";
      } else if (lowerMsg.includes("شهریه") || lowerMsg.includes("هزینه")) {
        reply = "شهریه بسته به مقاطع متفاوت است. در صفحه ثبت‌نام ماشین‌حساب هزینه موجود است. هزینه دوره‌های مقدماتی از ۱۵۰۰ افغانی شروع می‌شود.";
      } else if (lowerMsg.includes("کانکور") || lowerMsg.includes("کنکور")) {
        reply = "دوره آمادگی کانکور ما ۶ ماهه است و با بهترین اساتید برگزار می‌شود. این دوره شامل دروس تجوید، تفسیر و فقه می‌باشد.";
      } else if (lowerMsg.includes("سلام") || lowerMsg.includes("درود")) {
        reply = "سلام دوست عزیز! 🌙<br>خوش آمدید. چگونه می‌توانم کمکتان کنم؟";
      } else if (lowerMsg.includes("واتساپ") || lowerMsg.includes("واتس اپ")) {
        reply = "برای چت با پشتیبانی ما در واتساپ روی آیکون واتساپ کلیک کنید یا مستقیماً با شماره ۰۷۹۴۸۲۹۰۹۰ تماس بگیرید.";
      } else if (lowerMsg.includes("ساعت کاری") || lowerMsg.includes("زمان")) {
        reply = "مکتب از شنبه تا پنجشنبه از ساعت ۸ صبح تا ۸ شب فعال است. روزهای جمعه تعطیل می‌باشد.";
      } else if (lowerMsg.includes("آدرس") || lowerMsg.includes("مکان")) {
        reply = "آدرس مکتب: کابل افغانستان، جاده شهید مزاری، ایستگاه تانک تیل، بعد از اولین سه‌راهی به سمت راست، کوچه سوم<br>همچنین می‌توانید از طریق نقشه زیر موقعیت ما را مشاهده کنید.";
      }
      setTimeout(() => {
        messages.innerHTML += `<div class="bot-msg">${reply}</div>`;
        messages.scrollTop = messages.scrollHeight;
      }, 800);
      input.value = "";
    }
    // Close chat when clicking outside
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
    // Send message on Enter key
    document.getElementById('chat-input').addEventListener('keypress', function(e) {
      if (e.key === 'Enter') {
        sendMessage();
      }
    });
    // Mobile menu toggle
    const mobileMenuBtn = document.querySelector('.mobile-menu-btn');
    const navLinks = document.querySelector('.nav-links');
    mobileMenuBtn.addEventListener('click', function() {
      navLinks.style.display = navLinks.style.display === 'flex' ? 'none' : 'flex';
    });
    // Close mobile menu when clicking on a link
    document.querySelectorAll('.nav-links a').forEach(link => {
      link.addEventListener('click', function() {
        if (window.innerWidth <= 992) {
          navLinks.style.display = 'none';
        }
      });
    });
    // Responsive menu on resize
    window.addEventListener('resize', function() {
      if (window.innerWidth > 992) {
        navLinks.style.display = 'flex';
      } else {
        navLinks.style.display = 'none';
      }
    });
    // تغییر بین تب‌های فرم
    document.querySelectorAll('.form-tab').forEach(tab => {
      tab.addEventListener('click', function() {
        // حذف کلاس active از همه تب‌ها
        document.querySelectorAll('.form-tab').forEach(t => t.classList.remove('active'));
        document.querySelectorAll('.form-container').forEach(c => c.classList.remove('active'));
        // اضافه کردن کلاس active به تب انتخاب شده
        this.classList.add('active');
        document.getElementById(this.dataset.tab).classList.add('active');
      });
    });
    // ارسال فرم ثبت‌نام
    document.getElementById('registrationForm').addEventListener('submit', function(e) {
      e.preventDefault();
      // در اینجا کد ارسال به سرور قرار می‌گیرد
      // برای نمونه فقط پیام موفقیت را نمایش می‌دهیم
      this.style.display = 'none';
      document.getElementById('register-success').style.display = 'block';
      // ارسال ایمیل (این بخش نیاز به پیکربندی سرور دارد)
      // برای راه‌اندازی واقعی نیاز به استفاده از PHP یا دیگر زبان‌های سمت سرور دارید
      // یا می‌توانید از سرویس‌هایی مانند FormSubmit.co استفاده کنید
    });
    // ارسال فرم تماس
    document.getElementById('contactForm').addEventListener('submit', function(e) {
      e.preventDefault();
      // در اینجا کد ارسال به سرور قرار می‌گیرد
      // برای نمونه فقط پیام موفقیت را نمایش می‌دهیم
      this.style.display = 'none';
      document.getElementById('contact-success').style.display = 'block';
      // ارسال ایمیل (این بخش نیاز به پیکربندی سرور دارد)
      // برای راه‌اندازی واقعی نیاز به استفاده از PHP یا دیگر زبان‌های سمت سرور دارید
      // یا می‌توانید از سرویس‌هایی مانند FormSubmit.co استفاده کنید
    });
    // برای راه‌اندازی واقعی، یکی از این روش‌ها را انتخاب کنید:
    // روش 1: استفاده از mailto (ساده)
    // در تگ فرم این خط را قرار دهید:
    // <form action="mailto:contact.tajweedschool@gmail.com" method="post" enctype="text/plain">
    // روش 2: استفاده از PHP (پیشنهادی)
    // یک فایل با نام send_email.php ایجاد کنید با محتوای زیر:
    /*
    <?php
    $to = "contact.tajweedschool@gmail.com";
    $subject = "درخواست جدید - مکتب تجوید";
    $message = "نام: " . $_POST['name'] . "
";
    $message .= "تلفن: " . $_POST['phone'] . "
";
    // بقیه فیلدها...
    $headers = "From: " . $_POST['email'] . "\r
" .
               "Reply-To: " . $_POST['email'] . "\r
" .
               "X-Mailer: PHP/" . phpversion();
    mail($to, $subject, $message, $headers);
    header('Location: thank-you.html'); // صفحه تشکر پس از ارسال
    ?>
    */
    // سپس در تگ فرم این خط را قرار دهید:
    // <form action="send_email.php" method="post">
    // روش 3: استفاده از سرویس‌های فرم آنلاین
    // می‌توانید از سرویس‌هایی مانند FormSubmit.co استفاده کنید:
    // <form action="https://formsubmit.co/contact.tajweedschool@gmail.com" method="POST">
  </script>
</body>
</html>
