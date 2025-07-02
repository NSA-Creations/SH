<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Shalom Foundation Nursery & Primary School – Kisoro, Uganda</title>
  <link href="https://fonts.googleapis.com/css?family=Montserrat:700,400&display=swap" rel="stylesheet">
  <style>
    :root {
      --primary: #2d5c2f;
      --accent: #fcb900;
      --light: #f8f8f8;
      --dark: #222;
      --border-radius: 12px;
      --overlay: rgba(44,92,47,0.55);
    }
    html, body {
      margin: 0; padding: 0;
      background: var(--light);
      color: var(--dark);
      font-family: 'Montserrat', Arial, sans-serif;
      scroll-behavior: smooth;
    }
    /* Video Background Header */
    header {
      position: relative;
      height: 60vh;
      min-height: 400px;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      overflow: hidden;
    }
    header video {
      position: absolute;
      top: 0; left: 0;
      width: 100%; height: 100%;
      object-fit: cover;
      z-index: 1;
      filter: brightness(0.7) saturate(1.2);
    }
    .header-overlay {
      position: absolute;
      top: 0; left: 0;
      width: 100%; height: 100%;
      background: var(--overlay);
      z-index: 2;
    }
    .header-content {
      position: relative;
      z-index: 3;
      color: #fff;
      text-align: center;
      animation: fadeInDown 1.5s cubic-bezier(.39,.575,.565,1) both;
    }
    @keyframes fadeInDown {
      0% { opacity: 0; transform: translateY(-60px);}
      100% { opacity: 1; transform: translateY(0);}
    }
    .logo-badge {
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 2rem;
      margin-bottom: 1rem;
      animation: slideInLeft 1.2s 0.5s both;
    }
    @keyframes slideInLeft {
      0% { opacity: 0; transform: translateX(-80px);}
      100% { opacity: 1; transform: translateX(0);}
    }
    .logo-badge img {
      width: 90px;
      height: 90px;
      object-fit: contain;
      background: #fff;
      border-radius: 50%;
      border: 3px solid var(--accent);
      box-shadow: 0 2px 8px rgba(44,92,47,0.09);
      transition: transform 0.3s;
    }
    .logo-badge img:hover {
      transform: scale(1.08) rotate(-3deg);
    }
    h1 {
      margin: 0.2em 0 0.1em 0;
      font-size: 2.5rem;
      letter-spacing: 1px;
      text-shadow: 0 2px 8px rgba(0,0,0,0.18);
      animation: fadeIn 2s 1s both;
    }
    @keyframes fadeIn {
      from { opacity: 0;}
      to { opacity: 1;}
    }
    nav {
      background: var(--accent);
      padding: 0.7rem 0;
      text-align: center;
      position: sticky;
      top: 0;
      z-index: 10;
      box-shadow: 0 2px 8px rgba(44,92,47,0.03);
      animation: fadeIn 1.2s 1.2s both;
    }
    nav a {
      color: var(--primary);
      text-decoration: none;
      font-weight: bold;
      margin: 0 1.2rem;
      font-size: 1.1rem;
      transition: color 0.3s, border-bottom 0.3s;
      border-bottom: 2px solid transparent;
      padding-bottom: 2px;
    }
    nav a:hover, nav a:focus {
      color: #fff;
      border-bottom: 2px solid #fff;
    }
    main {
      max-width: 1100px;
      margin: 2rem auto;
      background: #fff;
      border-radius: var(--border-radius);
      box-shadow: 0 2px 16px rgba(44,92,47,0.07);
      padding: 2.5rem;
      animation: fadeInUp 1.8s 0.7s both;
    }
    @keyframes fadeInUp {
      0% { opacity: 0; transform: translateY(60px);}
      100% { opacity: 1; transform: translateY(0);}
    }
    section {
      margin-bottom: 2.5rem;
      opacity: 0;
      transform: translateY(30px);
      transition: opacity 0.9s cubic-bezier(.39,.575,.565,1), transform 0.9s cubic-bezier(.39,.575,.565,1);
    }
    section.visible {
      opacity: 1;
      transform: translateY(0);
    }
    h2 {
      color: var(--primary);
      margin-top: 1.5em;
      margin-bottom: 0.5em;
      font-size: 2rem;
      position: relative;
      animation: fadeInLeft 1.2s both;
    }
    @keyframes fadeInLeft {
      0% { opacity: 0; transform: translateX(-40px);}
      100% { opacity: 1; transform: translateX(0);}
    }
    .values-list, .objectives-list, .calendar-list, .curriculum-list, .parent-tips, .resource-links, .success-stories {
      list-style: none;
      padding: 0;
      margin: 0.5em 0 0 0;
    }
    .values-list li, .objectives-list li, .calendar-list li, .curriculum-list li, .parent-tips li, .resource-links li, .success-stories li {
      background: var(--light);
      border-left: 5px solid var(--accent);
      margin-bottom: 0.5em;
      padding: 0.7em 1em;
      border-radius: 6px;
      font-size: 1.1em;
      animation: fadeInRight 1.2s both;
    }
    @keyframes fadeInRight {
      0% { opacity: 0; transform: translateX(40px);}
      100% { opacity: 1; transform: translateX(0);}
    }
    .team-grid {
      display: flex;
      flex-wrap: wrap;
      gap: 1.5rem;
      margin-top: 1em;
    }
    .team-member {
      flex: 1 1 220px;
      background: var(--light);
      border-radius: var(--border-radius);
      box-shadow: 0 1px 6px rgba(44,92,47,0.06);
      padding: 1.2em;
      text-align: center;
      transition: transform 0.3s, box-shadow 0.3s;
      animation: fadeInUp 1.2s both;
    }
    .team-member:hover {
      transform: translateY(-8px) scale(1.04);
      box-shadow: 0 4px 18px rgba(44,92,47,0.13);
    }
    .team-member img {
      width: 70px;
      height: 70px;
      border-radius: 50%;
      margin-bottom: 0.7em;
      object-fit: cover;
      border: 2px solid var(--primary);
      transition: box-shadow 0.3s;
    }
    .team-member img:hover {
      box-shadow: 0 0 0 4px var(--accent);
    }
    .contact-table {
      width: 100%;
      border-collapse: collapse;
      margin-top: 1em;
    }
    .contact-table th, .contact-table td {
      padding: 0.7em 1em;
      border-bottom: 1px solid #e0e0e0;
      text-align: left;
    }
    .contact-table th {
      background: var(--light);
      color: var(--primary);
    }
    .footer {
      background: var(--primary);
      color: #fff;
      text-align: center;
      padding: 1.2rem 0;
      margin-top: 2rem;
      border-radius: var(--border-radius) var(--border-radius) 0 0;
      font-size: 1.1rem;
      animation: fadeIn 1.2s 2s both;
    }
    .virtual-tour-img {
      width: 100%;
      max-width: 600px;
      border-radius: var(--border-radius);
      margin: 1em 0;
      box-shadow: 0 2px 10px rgba(44,92,47,0.08);
      display: block;
      margin-left: auto;
      margin-right: auto;
      animation: fadeIn 2s both;
    }
    @media (max-width: 800px) {
      main { padding: 1rem; }
      .team-grid { flex-direction: column; }
      header { height: 40vh; min-height: 220px;}
      h1 { font-size: 1.5rem;}
    }
  </style>
</head>
<body>
  <header>
    <video autoplay muted loop playsinline poster="header-fallback.jpg">
      <source src="school-video.mp4" type="video/mp4">
      <!-- Add WebM/OGG sources for broader support if available -->
      Your browser does not support the video tag.
    </video>
    <div class="header-overlay"></div>
    <div class="header-content">
      <div class="logo-badge">
        <img src="logo-placeholder.png" alt="Shalom School Logo">
        <img src="badge-placeholder.png" alt="Shalom School Badge">
      </div>
      <h1>Shalom Foundation Nursery & Primary School</h1>
      <p><strong>Kisoro District, Uganda</strong></p>
      <p><em>Motto: God is Love</em></p>
    </div>
  </header>
  <nav>
    <a href="#about">About</a>
    <a href="#vision">Vision & Mission</a>
    <a href="#objectives">Objectives</a>
    <a href="#values">Core Values</a>
    <a href="#calendar">Calendar</a>
    <a href="#admissions">Admissions</a>
    <a href="#curriculum">Curriculum</a>
    <a href="#christian">Christian Life</a>
    <a href="#studentlife">Student Life</a>
    <a href="#parent">Parents</a>
    <a href="#team">Our Team</a>
    <a href="#virtualtour">Virtual Tour</a>
    <a href="#contact">Contact</a>
  </nav>
  <main>
    <!-- All your previous sections go here -->
    <!-- ... (copy the previously provided HTML sections here) ... -->
    <!-- For brevity, not repeating all sections; use the expanded content from previous answer -->
  </main>
  <div class="footer">
    &copy; 2025 Shalom Foundation Nursery & Primary School, Kisoro District, Uganda. All rights reserved.
  </div>
  <script>
    // Section fade-in on scroll
    function revealSections() {
      const sections = document.querySelectorAll('main section');
      const trigger = window.innerHeight * 0.92;
      sections.forEach(sec => {
        const top = sec.getBoundingClientRect().top;
        if(top < trigger) sec.classList.add('visible');
      });
    }
    window.addEventListener('scroll', revealSections);
    window.addEventListener('DOMContentLoaded', revealSections);
  </script>
</body>
</html>
