<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>StyleMate - Your Personal AI Stylist</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }
    
    body {
      background-color: #f5f5f5;
    }
    
    .container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 20px;
    }
    
    header {
      background-color: white;
      padding: 20px 0;
      box-shadow: 0 2px 10px rgba(0,0,0,0.1);
    }
    
    nav {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    
    .logo {
      display: flex;
      align-items: center;
      font-size: 24px;
      font-weight: bold;
      color: #333;
    }
    
    .logo img {
      width: 30px;
      margin-right: 10px;
    }
    
    .nav-links {
      display: flex;
      gap: 30px;
    }
    
    .nav-links a {
      text-decoration: none;
      color: #333;
    }
    
    .auth-buttons {
      display: flex;
      gap: 15px;
    }
    
    .btn {
      padding: 10px 20px;
      border-radius: 50px;
      font-weight: 500;
      cursor: pointer;
      transition: all 0.3s ease;
    }
    
    .btn-primary {
      background-color: #ff7f50;
      color: white;
      border: none;
    }
    
    .btn-outline {
      background-color: transparent;
      border: 1px solid #ff7f50;
      color: #ff7f50;
    }
    
    .hero {
      padding: 60px 0;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }
    
    .hero-content {
      max-width: 500px;
    }
    
    .hero-title {
      font-size: 48px;
      font-weight: bold;
      line-height: 1.2;
      margin-bottom: 20px;
      color: #222;
    }
    
    .hero-text {
      font-size: 18px;
      color: #555;
      margin-bottom: 30px;
    }
    
    .hero-image {
      width: 45%;
      border-radius: 10px;
      overflow: hidden;
    }
    
    .hero-image img {
      width: 100%;
      height: auto;
    }
    
    .features {
      padding: 60px 0;
      background-color: white;
    }
    
    .section-title {
      font-size: 36px;
      font-weight: bold;
      margin-bottom: 40px;
      text-align: center;
    }
    
    .steps {
      display: flex;
      justify-content: space-between;
      gap: 30px;
      margin-bottom: 60px;
    }
    
    .step-card {
      background-color: white;
      padding: 30px;
      border-radius: 10px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.1);
      flex: 1;
    }
    
    .step-number {
      font-size: 20px;
      font-weight: bold;
      margin-bottom: 15px;
    }
    
    .step-text {
      color: #555;
      line-height: 1.6;
    }
    
    .features-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 30px;
    }
    
    .feature-card {
      background-color: #f9f9f9;
      padding: 30px;
      border-radius: 10px;
      transition: transform 0.3s ease;
    }
    
    .feature-card:hover {
      transform: translateY(-5px);
    }
    
    .feature-title {
      font-size: 20px;
      font-weight: bold;
      margin-bottom: 15px;
    }
    
    .feature-text {
      color: #555;
      line-height: 1.6;
    }
    
    .testimonials {
      padding: 60px 0;
    }
    
    .testimonial-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 30px;
    }
    
    .testimonial-card {
      background-color: white;
      padding: 30px;
      border-radius: 10px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.1);
    }
    
    .testimonial-avatar {
      width: 80px;
      height: 80px;
      border-radius: 50%;
      overflow: hidden;
      margin-bottom: 20px;
    }
    
    .testimonial-avatar img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
    
    .testimonial-text {
      font-style: italic;
      color: #555;
      margin-bottom: 15px;
      line-height: 1.6;
    }
    
    .testimonial-author {
      font-weight: bold;
    }
    
    .upload-section {
      padding: 60px 0;
      background-color: #f0f8ff;
      text-align: center;
    }
    
    .upload-container {
      max-width: 600px;
      margin: 0 auto;
      background-color: white;
      padding: 40px;
      border-radius: 10px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.1);
    }
    
    .upload-title {
      font-size: 24px;
      font-weight: bold;
      margin-bottom: 20px;
    }
    
    .upload-text {
      color: #555;
      margin-bottom: 30px;
    }
    
    .upload-area {
      border: 2px dashed #ddd;
      padding: 40px;
      border-radius: 10px;
      margin-bottom: 30px;
      cursor: pointer;
    }
    
    .upload-icon {
      font-size: 48px;
      color: #ddd;
      margin-bottom: 15px;
    }
    
    .outfit-suggestion {
      padding: 60px 0;
    }
    
    .suggestion-container {
      display: grid;
      grid-template-columns: 1fr 2fr;
      gap: 30px;
    }
    
    .wardrobe-preview {
      background-color: white;
      padding: 30px;
      border-radius: 10px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.1);
    }
    
    .wardrobe-title {
      font-size: 20px;
      font-weight: bold;
      margin-bottom: 20px;
    }
    
    .wardrobe-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(80px, 1fr));
      gap: 15px;
    }
    
    .wardrobe-item {
      border: 1px solid #ddd;
      border-radius: 5px;
      overflow: hidden;
      aspect-ratio: 1;
    }
    
    .wardrobe-item img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
    
    .outfit-results {
      background-color: white;
      padding: 30px;
      border-radius: 10px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.1);
    }
    
    .results-title {
      font-size: 20px;
      font-weight: bold;
      margin-bottom: 20px;
    }
    
    .outfit-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
      gap: 20px;
    }
    
    .outfit-card {
      border: 1px solid #ddd;
      border-radius: 5px;
      overflow: hidden;
    }
    
    .outfit-image {
      width: 100%;
      aspect-ratio: 3/4;
      background-color: #f9f9f9;
    }
    
    .outfit-image img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
    
    .outfit-info {
      padding: 15px;
    }
    
    .outfit-occasion {
      font-weight: bold;
      margin-bottom: 5px;
    }
    
    .outfit-description {
      font-size: 14px;
      color: #555;
    }
    
    footer {
      background-color: #333;
      color: white;
      padding: 40px 0;
    }
    
    .footer-content {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    
    .footer-links {
      display: flex;
      gap: 20px;
    }
    
    .footer-links a {
      color: white;
      text-decoration: none;
    }
    
    .social-links {
      display: flex;
      gap: 15px;
    }
    
    .social-links a {
      color: white;
      font-size: 20px;
    }
    
    @media (max-width: 768px) {
      .hero {
        flex-direction: column;
        text-align: center;
      }
      
      .hero-content {
        max-width: 100%;
        margin-bottom: 40px;
      }
      
      .hero-image {
        width: 80%;
      }
      
      .steps {
        flex-direction: column;
      }
      
      .suggestion-container {
        grid-template-columns: 1fr;
      }
    }
  </style>
</head>
<body>
  <header>
    <div class="container">
      <nav>
        <div class="logo">
          <img src="/api/placeholder/30/30" alt="StyleMate Logo">
          StyleMate
        </div>
        <div class="nav-links">
          <a href="#">Home</a>
          <a href="#">Features</a>
          <a href="#">Virtual Try-On</a>
          <a href="#">Style Guide</a>
          <a href="#">Profile</a>
        </div>
        <div class="auth-buttons">
          <button class="btn btn-outline">Log In</button>
          <button class="btn btn-primary">Sign Up</button>
        </div>
      </nav>
    </div>
  </header>

  <section class="hero">
    <div class="container">
      <div class="hero-content">
        <h1 class="hero-title">Your Personal AI Stylist - Effortless Outfits, Every Day!</h1>
        <p class="hero-text">Get AI-powered outfit recommendations based on your style, occasion, and weather.</p>
        <button class="btn btn-primary">Get Started for Free</button>
      </div>
      <div class="hero-image">
        <img src="/api/placeholder/500/500" alt="StyleMate Outfit Collection">
      </div>
    </div>
  </section>

  <section class="features">
    <div class="container">
      <h2 class="section-title">How It Works</h2>
      <div class="steps">
        <div class="step-card">
          <h3 class="step-number">Step 1</h3>
          <p class="step-text">Upload photos of your wardrobe (or sync from online stores).</p>
        </div>
        <div class="step-card">
          <h3 class="step-number">Step 2</h3>
          <p class="step-text">AI suggests outfit combinations for any occasion.</p>
        </div>
        <div class="step-card">
          <h3 class="step-number">Step 3</h3>
          <p class="step-text">Try them on virtually or shop missing items.</p>
        </div>
      </div>

      <h2 class="section-title">AI-Powered Features</h2>
      <div class="features-grid">
        <div class="feature-card">
          <h3 class="feature-title">Smart Outfit Generator</h3>
          <p class="feature-text">Get daily outfit suggestions tailored to your preferences.</p>
        </div>
        <div class="feature-card">
          <h3 class="feature-title">Weather-Based Styling</h3>
          <p class="feature-text">Adapts your outfits to the weather forecast.</p>
        </div>
        <div class="feature-card">
          <h3 class="feature-title">Virtual Try-On</h3>
          <p class="feature-text">Experience an augmented reality dressing room.</p>
        </div>
        <div class="feature-card">
          <h3 class="feature-title">Personalized Shopping</h3>
          <p class="feature-text">AI suggests missing pieces for a complete wardrobe.</p>
        </div>
      </div>
    </div>
  </section>

  <section class="upload-section">
    <div class="container">
      <div class="upload-container">
        <h2 class="upload-title">Upload Your Wardrobe</h2>
        <p class="upload-text">Let our AI analyze your clothes and create personalized outfit suggestions.</p>
        <div class="upload-area">
          <div class="upload-icon">📁</div>
          <p>Drag and drop your photos here, or click to browse</p>
        </div>
        <button class="btn btn-primary">Continue</button>
      </div>
    </div>
  </section>

  <section class="outfit-suggestion">
    <div class="container">
      <h2 class="section-title">Personalized Outfit Suggestions</h2>
      <div class="suggestion-container">
        <div class="wardrobe-preview">
          <h3 class="wardrobe-title">Your Wardrobe</h3>
          <div class="wardrobe-grid">
            <div class="wardrobe-item">
              <img src="/api/placeholder/80/80" alt="Wardrobe Item">
            </div>
            <div class="wardrobe-item">
              <img src="/api/placeholder/80/80" alt="Wardrobe Item">
            </div>
            <div class="wardrobe-item">
