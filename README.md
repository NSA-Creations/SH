<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Shalom Foundation Nursery & Primary School – Kisoro, Uganda</title>
  <link href="https://fonts.googleapis.com/css?family=Montserrat:700,400&display=swap" rel="stylesheet" />
  <style>
    :root {
      --primary: #2d5c2f;
      --accent: #fcb900;
      --light: #f8f8f8;
      --dark: #222;
      --border-radius: 12px;
      --overlay: rgba(44, 92, 47, 0.55);
      --transition: 0.3s ease;
    }
    html, body {
      margin: 0; padding: 0;
      background: var(--light);
      color: var(--dark);
      font-family: 'Montserrat', Arial, sans-serif;
      scroll-behavior: smooth;
      line-height: 1.6;
    }
    /* Header with video background */
    header {
      position: relative;
      height: 60vh;
      min-height: 400px;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      overflow: hidden;
      text-align: center;
      color: white;
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
      max-width: 900px;
      padding: 0 1rem;
      animation: fadeInDown 1.5s cubic-bezier(.39,.575,.565,1) both;
    }
    .logo-badge {
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 2rem;
      margin-bottom: 1rem;
      animation: slideInLeft 1.2s 0.5s both;
    }
    .logo-badge img {
      width: 90px;
      height: 90px;
      object-fit: contain;
      background: #fff;
      border-radius: 50%;
      border: 3px solid var(--accent);
      box-shadow: 0 2px 8px rgba(44, 92, 47, 0.09);
      transition: transform 0.3s;
    }
    .logo-badge img:hover {
      transform: scale(1.08) rotate(-3deg);
    }
    h1 {
      margin: 0.2em 0 0.1em 0;
      font-size: 2.8rem;
      letter-spacing: 1px;
      text-shadow: 0 2px 8px rgba(0,0,0,0.3);
      animation: fadeIn 2s 1s both;
    }
    p.motto {
      font-style: italic;
      font-weight: 500;
      font-size: 1.2rem;
      margin-top: 0.2em;
      text-shadow: 0 1px 6px rgba(0,0,0,0.3);
    }
    @keyframes fadeInDown {
      0% { opacity: 0; transform: translateY(-60px);}
      100% { opacity: 1; transform: translateY(0);}
    }
    @keyframes slideInLeft {
      0% { opacity: 0; transform: translateX(-80px);}
      100% { opacity: 1; transform: translateX(0);}
    }
    @keyframes fadeIn {
      from { opacity: 0;}
      to { opacity: 1;}
    }
    /* Navigation */
    nav {
      background: var(--accent);
      padding: 0.7rem 0;
      text-align: center;
      position: sticky;
      top: 0;
      z-index: 10;
      box-shadow: 0 2px 8px rgba(44, 92, 47, 0.03);
      animation: fadeIn 1.2s 1.2s both;
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 0.8rem 1.2rem;
    }
    nav a {
      color: var(--primary);
      text-decoration: none;
      font-weight: 700;
      font-size: 1.1rem;
      border-bottom: 2px solid transparent;
      padding-bottom: 2px;
      transition: color 0.3s, border-bottom 0.3s;
      white-space: nowrap;
    }
    nav a:hover,
    nav a:focus {
      color: #fff;
      border-bottom: 2px solid #fff;
      outline: none;
    }
    /* Search bar in nav */
    .nav-search {
      margin-left: 1rem;
      flex-grow: 1;
      max-width: 300px;
      position: relative;
    }
    .nav-search input[type="search"] {
      width: 100%;
      padding: 0.4rem 1rem;
      border-radius: var(--border-radius);
      border: none;
      font-size: 1rem;
      outline: none;
      transition: box-shadow 0.3s;
    }
    .nav-search input[type="search"]:focus {
      box-shadow: 0 0 6px var(--primary);
    }
    /* Main content */
    main {
      max-width: 1100px;
      margin: 2rem auto;
      background: #fff;
      border-radius: var(--border-radius);
      box-shadow: 0 2px 16px rgba(44, 92, 47, 0.07);
      padding: 2.5rem 3rem;
      animation: fadeInUp 1.8s 0.7s both;
    }
    @keyframes fadeInUp {
      0% { opacity: 0; transform: translateY(60px);}
      100% { opacity: 1; transform: translateY(0);}
    }
    section {
      margin-bottom: 3rem;
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
      margin-bottom: 0.8em;
      font-size: 2.2rem;
      position: relative;
      animation: fadeInLeft 1.2s both;
      border-bottom: 3px solid var(--accent);
      padding-bottom: 0.3em;
      max-width: max-content;
    }
    @keyframes fadeInLeft {
      0% { opacity: 0; transform: translateX(-40px);}
      100% { opacity: 1; transform: translateX(0);}
    }
    ul {
      list-style: none;
      padding-left: 0;
    }
    li {
      background: var(--light);
      border-left: 5px solid var(--accent);
      margin-bottom: 0.7em;
      padding: 0.8em 1.2em;
      border-radius: 6px;
      font-size: 1.15em;
      animation: fadeInRight 1.2s both;
    }
    @keyframes fadeInRight {
      0% { opacity: 0; transform: translateX(40px);}
      100% { opacity: 1; transform: translateX(0);}
    }
    /* Staff directory */
    .staff-grid {
      display: flex;
      flex-wrap: wrap;
      gap: 1.5rem;
      margin-top: 1em;
      justify-content: center;
    }
    .staff-member {
      flex: 1 1 220px;
      background: var(--light);
      border-radius: var(--border-radius);
      box-shadow: 0 1px 6px rgba(44, 92, 47, 0.06);
      padding: 1.2em;
      text-align: center;
      transition: transform 0.3s, box-shadow 0.3s;
      animation: fadeInUp 1.2s both;
      cursor: default;
    }
    .staff-member:hover {
      transform: translateY(-8px) scale(1.04);
      box-shadow: 0 4px 18px rgba(44, 92, 47, 0.13);
    }
    .staff-member img {
      width: 80px;
      height: 80px;
      border-radius: 50%;
      margin-bottom: 0.7em;
      object-fit: cover;
      border: 2px solid var(--primary);
      transition: box-shadow 0.3s;
    }
    .staff-member img:hover {
      box-shadow: 0 0 0 4px var(--accent);
    }
    .staff-member h3 {
      margin: 0.3em 0 0.1em 0;
      font-size: 1.2rem;
      color: var(--primary);
    }
    .staff-member p {
      margin: 0.1em 0 0.3em 0;
      font-size: 1rem;
      font-weight: 600;
      color: #444;
    }
    .staff-member a {
      color: var(--accent);
      text-decoration: none;
      font-weight: 700;
      font-size: 0.95rem;
      transition: color 0.3s;
    }
    .staff-member a:hover {
      color: var(--primary);
      text-decoration: underline;
    }
    /* Calendar */
    .calendar-list li {
      display: flex;
      justify-content: space-between;
      font-weight: 600;
    }
    .calendar-list li span.date {
      color: var(--primary);
      font-style: italic;
      font-weight: 400;
    }
    /* Multimedia gallery */
    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 1rem;
      margin-top: 1rem;
    }
    .gallery img, .gallery video {
      width: 100%;
      border-radius: var(--border-radius);
      box-shadow: 0 2px 10px rgba(44, 92, 47, 0.08);
      cursor: pointer;
      transition: transform 0.3s ease;
    }
    .gallery img:hover, .gallery video:hover {
      transform: scale(1.05);
    }
    /* Forms */
    form {
      max-width: 600px;
      margin: 1rem auto;
      background: var(--light);
      padding: 2rem;
      border-radius: var(--border-radius);
      box-shadow: 0 2px 12px rgba(44, 92, 47, 0.1);
    }
    form label {
      display: block;
      margin-bottom: 0.5rem;
      font-weight: 600;
      color: var(--primary);
    }
    form input[type="text"],
    form input[type="email"],
    form input[type="tel"],
    form select,
    form textarea {
      width: 100%;
      padding: 0.6rem 1rem;
      margin-bottom: 1rem;
      border-radius: var(--border-radius);
      border: 1px solid #ccc;
      font-size: 1rem;
      font-family: 'Montserrat', Arial, sans-serif;
      transition: border-color 0.3s;
    }
    form input[type="text"]:focus,
    form input[type="email"]:focus,
    form input[type="tel"]:focus,
    form select:focus,
    form textarea:focus {
      border-color: var(--primary);
      outline: none;
    }
    form button {
      background: var(--primary);
      color: white;
      border: none;
      padding: 0.8rem 2rem;
      font-size: 1.1rem;
      border-radius: var(--border-radius);
      cursor: pointer;
      font-weight: 700;
      transition: background-color 0.3s;
    }
    form button:hover {
      background: var(--accent);
      color: var(--primary);
    }
    /* Contact info table */
    .contact-table {
      width: 100%;
      border-collapse: collapse;
      margin-top: 1em;
      font-size: 1.1rem;
    }
    .contact-table th, .contact-table td {
      padding: 0.7em 1em;
      border-bottom: 1px solid #e0e0e0;
      text-align: left;
    }
    .contact-table th {
      background: var(--light);
      color: var(--primary);
      font-weight: 700;
    }
    /* Footer */
    .footer {
      background: var(--primary);
      color: #fff;
      text-align: center;
      padding: 1.2rem 1rem;
      margin-top: 2rem;
      border-radius: var(--border-radius) var(--border-radius) 0 0;
      font-size: 1.1rem;
      animation: fadeIn 1.2s 2s both;
      user-select: none;
    }
    /* Responsive */
    @media (max-width: 800px) {
      main {
        padding: 1rem 1.5rem;
      }
      .staff-grid {
        flex-direction: column;
        gap: 1.5rem;
      }
      header {
        height: 40vh;
        min-height: 220px;
      }
      h1 {
        font-size: 1.8rem;
      }
      nav {
        flex-direction: column;
        gap: 0.6rem;
      }
      .nav-search {
        max-width: 100%;
        margin-left: 0;
        margin-top: 0.5rem;
      }
    }
  </style>
</head>
<body>
  <header>
    <video autoplay muted loop playsinline poster="header-fallback.jpg" aria-label="Video showing happy children learning and playing at Shalom Foundation School">
      <source src="school-video.mp4" type="video/mp4" />
      Your browser does not support the video tag.
    </video>
    <div class="header-overlay"></div>
    <div class="header-content" role="banner">
      <div class="logo-badge" aria-label="School logos">
        <img src="logo-placeholder.png" alt="Shalom Foundation School Logo" />
        <img src="badge-placeholder.png" alt="School Badge" />
      </div>
      <h1>Shalom Foundation Nursery & Primary School</h1>
      <p><strong>Kisoro District, Uganda</strong></p>
      <p class="motto">Motto: God is Love</p>
    </div>
  </header>

  <nav role="navigation" aria-label="Primary navigation">
    <a href="#about">About</a>
    <a href="#vision">Vision &amp; Mission</a>
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
    <div class="nav-search">
      <label for="site-search" class="visually-hidden">Search the site</label>
      <input type="search" id="site-search" name="site-search" placeholder="Search..." aria-label="Search the website" />
    </div>
  </nav>

  <main>
    <!-- About -->
    <section id="about" tabindex="0" aria-labelledby="about-title">
      <h2 id="about-title">About Shalom Foundation</h2>
      <p>Established in the heart of Kisoro District, Shalom Foundation Nursery & Primary School is committed to nurturing young minds through holistic education rooted in Christian values. Our school blends academic excellence with character development, preparing students to thrive in a rapidly changing world.</p>
      <p>Our campus is designed to be safe, welcoming, and inspiring, equipped with modern classrooms, play areas, and learning resources.</p>
    </section>

    <!-- Vision & Mission -->
    <section id="vision" tabindex="0" aria-labelledby="vision-title">
      <h2 id="vision-title">Vision &amp; Mission</h2>
      <p><strong>Vision:</strong> To be a leading institution in Kisoro that fosters academic excellence, spiritual growth, and social responsibility.</p>
      <p><strong>Mission:</strong> To provide quality education that empowers children to become responsible citizens guided by Christian principles and equipped with skills for lifelong success.</p>
    </section>

    <!-- Objectives -->
    <section id="objectives" tabindex="0" aria-labelledby="objectives-title">
      <h2 id="objectives-title">Objectives</h2>
      <ul>
        <li>Deliver a balanced curriculum that promotes intellectual, physical, and spiritual development.</li>
        <li>Encourage creativity, critical thinking, and problem-solving skills.</li>
        <li>Foster a safe and inclusive environment for all students.</li>
        <li>Engage parents and the community in the educational process.</li>
        <li>Promote environmental stewardship and social responsibility.</li>
      </ul>
    </section>

    <!-- Core Values -->
    <section id="values" tabindex="0" aria-labelledby="values-title">
      <h2 id="values-title">Core Values</h2>
      <ul>
        <li><strong>Faith:</strong> Upholding Christian beliefs as the foundation of our community.</li>
        <li><strong>Integrity:</strong> Acting with honesty and fairness in all we do.</li>
        <li><strong>Respect:</strong> Valuing each individual and embracing diversity.</li>
        <li><strong>Excellence:</strong> Striving for the highest standards academically and morally.</li>
        <li><strong>Compassion:</strong> Caring for others and fostering kindness.</li>
      </ul>
    </section>

    <!-- Integrated Calendar -->
    <section id="calendar" tabindex="0" aria-labelledby="calendar-title">
      <h2 id="calendar-title">School Calendar &amp; Events</h2>
      <ul class="calendar-list" aria-live="polite">
        <li><span class="date">Jan 7</span> – First Day of Term 1</li>
        <li><span class="date">Feb 15</span> – Parents’ Evening</li>
        <li><span class="date">Mar 20</span> – Sports Day</li>
        <li><span class="date">Apr 10</span> – End of Term 1</li>
        <li><span class="date">May 5</span> – Term 2 Begins</li>
        <li><span class="date">Jun 25</span> – Mid-Year Exams</li>
        <li><span class="date">Jul 15</span> – Cultural Festival</li>
        <li><span class="date">Sep 30</span> – End of Term 3</li>
        <li><span class="date">Oct 10</span> – Term 4 Begins</li>
        <li><span class="date">Dec 15</span> – Graduation &amp; Closing Ceremony</li>
      </ul>
      <p>Sync our calendar with your personal calendar using <a href="#" aria-label="Download calendar in iCal format">iCal</a> or <a href="#" aria-label="Download calendar in Google Calendar format">Google Calendar</a>.</p>
    </section>

    <!-- Admissions -->
    <section id="admissions" tabindex="0" aria-labelledby="admissions-title">
      <h2 id="admissions-title">Admissions</h2>
      <p>We welcome applications from parents seeking a nurturing and academically rigorous environment for their children. Our admissions process is transparent and designed to help families understand our values and expectations.</p>
      <form aria-label="Admissions application form" novalidate>
        <label for="applicant-name">Child's Full Name</label>
        <input type="text" id="applicant-name" name="applicant-name" required placeholder="Enter full name" />

        <label for="dob">Date of Birth</label>
        <input type="date" id="dob" name="dob" required />

        <label for="parent-name">Parent/Guardian Name</label>
        <input type="text" id="parent-name" name="parent-name" required placeholder="Enter your name" />

        <label for="contact-email">Email Address</label>
        <input type="email" id="contact-email" name="contact-email" required placeholder="example@mail.com" />

        <label for="contact-phone">Phone Number</label>
        <input type="tel" id="contact-phone" name="contact-phone" required placeholder="+256 7XX XXX XXX" />

        <label for="grade-level">Preferred Grade Level</label>
        <select id="grade-level" name="grade-level" required>
          <option value="" disabled selected>Select grade</option>
          <option value="nursery">Nursery</option>
          <option value="primary1">Primary 1</option>
          <option value="primary2">Primary 2</option>
          <option value="primary3">Primary 3</option>
          <option value="primary4">Primary 4</option>
          <option value="primary5">Primary 5</option>
          <option value="primary6">Primary 6</option>
          <option value="primary7">Primary 7</option>
        </select>

        <button type="submit">Submit Application</button>
      </form>
    </section>

    <!-- Curriculum -->
    <section id="curriculum" tabindex="0" aria-labelledby="curriculum-title">
      <h2 id="curriculum-title">Curriculum</h2>
      <p>Our curriculum follows the Uganda National Education Standards, enriched with Christian teachings and life skills. We emphasize:</p>
      <ul>
        <li>Core subjects: English, Mathematics, Science, Social Studies</li>
        <li>Religious Education and Moral Development</li>
        <li>Physical Education and Sports</li>
        <li>Arts, Music, and Drama</li>
        <li>ICT and Digital Literacy</li>
        <li>Environmental Awareness and Community Service</li>
      </ul>
    </section>

    <!-- Christian Life -->
    <section id="christian" tabindex="0" aria-labelledby="christian-title">
      <h2 id="christian-title">Christian Life at Shalom</h2>
      <p>Faith is central to our school life. We provide daily devotionals, weekly chapel services, and opportunities for spiritual growth. Our students learn to live out Christian values in their daily interactions and community involvement.</p>
    </section>

    <!-- Student Life -->
    <section id="studentlife" tabindex="0" aria-labelledby="studentlife-title">
      <h2 id="studentlife-title">Student Life</h2>
      <p>Beyond academics, students enjoy a vibrant life filled with clubs, sports, and cultural activities. We encourage leadership, teamwork, and creativity through:</p>
      <ul>
        <li>Sports teams and competitions</li>
        <li>Music and drama clubs</li>
        <li>Environmental and social clubs</li>
        <li>Student council and leadership programs</li>
      </ul>
    </section>

    <!-- Parents -->
    <section id="parent" tabindex="0" aria-labelledby="parent-title">
      <h2 id="parent-title">For Parents</h2>
      <p>We value strong partnerships with parents. Our secure parent portal allows you to:</p>
      <ul>
        <li>Monitor your child's academic progress and attendance</li>
        <li>Communicate directly with teachers and staff</li>
        <li>Access school announcements and newsletters</li>
        <li>Submit feedback and forms online</li>
      </ul>
      <p><a href="#" aria-label="Access Parent Portal">Access the Parent Portal</a></p>
    </section>

    <!-- Our Team -->
    <section id="team" tabindex="0" aria-labelledby="team-title">
      <h2 id="team-title">Our Dedicated Team</h2>
      <div class="staff-grid" role="list">
        <article class="staff-member" role="listitem" aria-label="Headteacher: Mrs. Grace Namusisi">
          <img src="staff-grace.jpg" alt="Mrs. Grace Namusisi, Headteacher" />
          <h3>Mrs. Grace Namusisi</h3>
          <p>Headteacher</p>
          <a href="mailto:grace.namusisi@shalomschool.ug" aria-label="Email Mrs. Grace Namusisi">grace.namusisi@shalomschool.ug</a>
        </article>
        <article class="staff-member" role="listitem" aria-label="Deputy Headteacher: Mr. John Kato">
          <img src="staff-john.jpg" alt="Mr. John Kato, Deputy Headteacher" />
          <h3>Mr. John Kato</h3>
          <p>Deputy Headteacher</p>
          <a href="mailto:john.kato@shalomschool.ug" aria-label="Email Mr. John Kato">john.kato@shalomschool.ug</a>
        </article>
        <article class="staff-member" role="listitem" aria-label="Admissions Officer: Ms. Sarah Achieng">
          <img src="staff-sarah.jpg" alt="Ms. Sarah Achieng, Admissions Officer" />
          <h3>Ms. Sarah Achieng</h3>
          <p>Admissions Officer</p>
          <a href="mailto:sarah.achieng@shalomschool.ug" aria-label="Email Ms. Sarah Achieng">sarah.achieng@shalomschool.ug</a>
        </article>
        <!-- Add more staff as needed -->
      </div>
    </section>

    <!-- Virtual Tour -->
    <section id="virtualtour" tabindex="0" aria-labelledby="virtualtour-title">
      <h2 id="virtualtour-title">Virtual Tour</h2>
      <p>Explore our beautiful campus from the comfort of your home. Our virtual tour showcases classrooms, play areas, and facilities that make Shalom Foundation a special place to learn and grow.</p>
      <img src="virtual-tour.jpg" alt="Virtual tour image showing the school campus and facilities" class="virtual-tour-img" />
      <p><a href="virtual-tour.html" aria-label="Start the full virtual tour">Start the full virtual tour</a></p>
    </section>

    <!-- News and Announcements -->
    <section id="news" tabindex="0" aria-labelledby="news-title">
      <h2 id="news-title">News &amp; Announcements</h2>
      <ul>
        <li><strong>June 20, 2025:</strong> Congratulations to our Primary 7 students for excellent results in national exams!</li>
        <li><strong>May 10, 2025:</strong> New ICT lab inaugurated to enhance digital learning.</li>
        <li><strong>April 5, 2025:</strong> Join us for the upcoming Cultural Festival on July 15.</li>
      </ul>
    </section>

    <!-- Multimedia Gallery -->
    <section id="gallery" tabindex="0" aria-labelledby="gallery-title">
      <h2 id="gallery-title">Photo &amp; Video Gallery</h2>
      <div class="gallery" role="list">
        <img src="gallery1.jpg" alt="Students participating in a science experiment" role="listitem" />
        <img src="gallery2.jpg" alt="Children playing football during sports day" role="listitem" />
        <video controls role="listitem" aria-label="Video of school choir performing at chapel service">
          <source src="choir-performance.mp4" type="video/mp4" />
          Your browser does not support the video tag.
        </video>
        <img src="gallery3.jpg" alt="Art and craft activities in the classroom" role="listitem" />
      </div>
    </section>

    <!-- Contact -->
    <section id="contact" tabindex="0" aria-labelledby="contact-title">
      <h2 id="contact-title">Contact Us</h2>
      <p>We welcome your questions and feedback. Reach out to us via phone, email, or the form below.</p>
      <table class="contact-table" role="presentation" aria-label="School contact information">
        <tbody>
          <tr>
            <th scope="row">Phone</th>
            <td>+256 789 123 456</td>
          </tr>
          <tr>
            <th scope="row">Email</th>
            <td>info@shalomschool.ug</td>
          </tr>
          <tr>
            <th scope="row">Address</th>
            <td>P.O. Box 1234, Kisoro District, Uganda</td>
          </tr>
        </tbody>
      </table>
      <form aria-label="Contact form" novalidate>
        <label for="contact-name">Your Name</label>
        <input type="text" id="contact-name" name="contact-name" required placeholder="Enter your name" />

        <label for="contact-email-form">Your Email</label>
        <input type="email" id="contact-email-form" name="contact-email-form" required placeholder="example@mail.com" />

        <label for="contact-message">Message</label>
        <textarea id="contact-message" name="contact-message" rows="5" required placeholder="Write your message here..."></textarea>

        <button type="submit">Send Message</button>
      </form>
    </section>
  </main>

  <div class="footer" role="contentinfo">
    &copy; 2025 Shalom Foundation Nursery & Primary School, Kisoro District, Uganda. All rights reserved.
  </div>

  <script>
    // Section fade-in on scroll
    function revealSections() {
      const sections = document.querySelectorAll('main section');
      const trigger = window.innerHeight * 0.92;
      sections.forEach(sec => {
        const top = sec.getBoundingClientRect().top;
        if (top < trigger) sec.classList.add('visible');
      });
    }
    window.addEventListener('scroll', revealSections);
    window.addEventListener('DOMContentLoaded', revealSections);

    // Simple form validation and alert for demonstration (can be replaced with real backend)
    document.querySelectorAll('form').forEach(form => {
      form.addEventListener('submit', e => {
        e.preventDefault();
        alert('Thank you for your submission! We will get back to you shortly.');
        form.reset();
      });
    });
  </script>

  <style>
    /* Accessibility helper class */
    .visually-hidden {
      position: absolute !important;
      height: 1px; width: 1px;
      overflow: hidden;
      clip: rect(1px, 1px, 1px, 1px);
      white-space: nowrap;
    }
  </style>
</body>
</html>
