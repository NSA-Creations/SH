```html



  
  
  Shalom Foundation Nursery & Primary School – Kisoro, Uganda
  
  
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
  


  
    
      
      Your browser does not support the video tag.
    
    
    
      
        
        
      
      Shalom Foundation Nursery & Primary School
      Kisoro District, Uganda
      Motto: God is Love
    
  

  
    About
    Vision &amp; Mission
    Objectives
    Core Values
    Calendar
    Admissions
    Curriculum
    Christian Life
    Student Life
    Parents
    Our Team
    Virtual Tour
    Contact
    
      Search the site
      
    
  

  
    
    
      About Shalom Foundation
      Established in the heart of Kisoro District, Shalom Foundation Nursery & Primary School is committed to nurturing young minds through holistic education rooted in Christian values. Our school blends academic excellence with character development, preparing students to thrive in a rapidly changing world.
      Our campus is designed to be safe, welcoming, and inspiring, equipped with modern classrooms, play areas, and learning resources.
    

    
    
      Vision &amp; Mission
      Vision: To be a leading institution in Kisoro that fosters academic excellence, spiritual growth, and social responsibility.
      Mission: To provide quality education that empowers children to become responsible citizens guided by Christian principles and equipped with skills for lifelong success.
    

    
    
      Objectives
      
        Deliver a balanced curriculum that promotes intellectual, physical, and spiritual development.
        Encourage creativity, critical thinking, and problem-solving skills.
        Foster a safe and inclusive environment for all students.
        Engage parents and the community in the educational process.
        Promote environmental stewardship and social responsibility.
      
    

    
    
      Core Values
      
        Faith: Upholding Christian beliefs as the foundation of our community.
        Integrity: Acting with honesty and fairness in all we do.
        Respect: Valuing each individual and embracing diversity.
        Excellence: Striving for the highest standards academically and morally.
        Compassion: Caring for others and fostering kindness.
      
    

    
    
      School Calendar &amp; Events
      
        Jan 7 – First Day of Term 1
        Feb 15 – Parents’ Evening
        Mar 20 – Sports Day
        Apr 10 – End of Term 1
        May 5 – Term 2 Begins
        Jun 25 – Mid-Year Exams
        Jul 15 – Cultural Festival
        Sep 30 – End of Term 3
        Oct 10 – Term 4 Begins
        Dec 15 – Graduation &amp; Closing Ceremony
      
      Sync our calendar with your personal calendar using iCal or Google Calendar.
    

    
    
      Admissions
      We welcome applications from parents seeking a nurturing and academically rigorous environment for their children. Our admissions process is transparent and designed to help families understand our values and expectations.
      
        Child's Full Name
        

        Date of Birth
        

        Parent/Guardian Name
        

        Email Address
        

        Phone Number
        

        Preferred Grade Level
        
          Select grade
          Nursery
          Primary 1
          Primary 2
          Primary 3
          Primary 4
          Primary 5
          Primary 6
          Primary 7
        

        Submit Application
      
    

    
    
      Curriculum
      Our curriculum follows the Uganda National Education Standards, enriched with Christian teachings and life skills. We emphasize:
      
        Core subjects: English, Mathematics, Science, Social Studies
        Religious Education and Moral Development
        Physical Education and Sports
        Arts, Music, and Drama
        ICT and Digital Literacy
        Environmental Awareness and Community Service
      
    

    
    
      Christian Life at Shalom
      Faith is central to our school life. We provide daily devotionals, weekly chapel services, and opportunities for spiritual growth. Our students learn to live out Christian values in their daily interactions and community involvement.
    

    
    
      Student Life
      Beyond academics, students enjoy a vibrant life filled with clubs, sports, and cultural activities. We encourage leadership, teamwork, and creativity through:
      
        Sports teams and competitions
        Music and drama clubs
        Environmental and social clubs
        Student council and leadership programs
      
    

    
    
      For Parents
      We value strong partnerships with parents. Our secure parent portal allows you to:
      
        Monitor your child's academic progress and attendance
        Communicate directly with teachers and staff
        Access school announcements and newsletters
        Submit feedback and forms online
      
      Access the Parent Portal
    

    
    
      Our Dedicated Team
      
        
          
          Mrs. Grace Namusisi
          Headteacher
          grace.namusisi@shalomschool.ug
        
        
          
          Mr. John Kato
          Deputy Headteacher
          john.kato@shalomschool.ug
        
        
          
          Ms. Sarah Achieng
          Admissions Officer
          sarah.achieng@shalomschool.ug
        
        
      
    

    
    
      Virtual Tour
      Explore our beautiful campus from the comfort of your home. Our virtual tour showcases classrooms, play areas, and facilities that make Shalom Foundation a special place to learn and grow.
      
      Start the full virtual tour
    

    
    
      News &amp; Announcements
      
        June 20, 2025: Congratulations to our Primary 7 students for excellent results in national exams!
        May 10, 2025: New ICT lab inaugurated to enhance digital learning.
        April 5, 2025: Join us for the upcoming Cultural Festival on July 15.
      
    

    
    
      Photo &amp; Video Gallery
      
        
        
        
          
          Your browser does not support the video tag.
        
        
      
    

    
    
      Contact Us
      We welcome your questions and feedback. Reach out to us via phone, email, or the form below.
      
        
          
            Phone
            +256 789 123 456
          
          
            Email
            info@shalomschool.ug
          
          
            Address
            P.O. Box 1234, Kisoro District, Uganda
          
        
      
      
        Your Name
        

        Your Email
        

        Message
        

        Send Message
      
    
  

  
    &copy; 2025 Shalom Foundation Nursery & Primary School, Kisoro District, Uganda. All rights reserved.
  

  
    // Section fade-in on scroll
    function revealSections() {
      const sections = document.querySelectorAll('main section');
      const trigger = window.innerHeight * 0.92;
      sections.forEach(sec => {
        const top = sec.getBoundingClientRect().top;
        if (top  {
      form.addEventListener('submit', e => {
        e.preventDefault();
        alert('Thank you for your submission! We will get back to you shortly.');
        form.reset();
      });
    });
  

  
    /* Accessibility helper class */
    .visually-hidden {
      position: absolute !important;
      height: 1px; width: 1px;
      overflow: hidden;
      clip: rect(1px, 1px, 1px, 1px);
      white-space: nowrap;
    }
  


```

## Explanation

This updated HTML page reflects the best practices and requested content for a top-tier school website:

- **Responsive Design:** The CSS uses flexible layouts, media queries, and fluid grids to ensure usability on all devices.
- **User-Friendly Navigation:** Clear navigation with a sticky menu and a prominent search bar for quick access.
- **Secure Parent and Student Portals:** Links and descriptions for secure portals (mocked here with a link placeholder).
- **Integrated Calendar:** A well-structured calendar with key dates and options to sync with personal calendars.
- **News and Announcements:** A dedicated section with latest news to keep the community informed.
- **Staff Directory:** Organized staff profiles with photos, roles, and contact emails to foster transparency.
- **Online Forms and Applications:** Admissions and contact forms with accessible labels and validation.
- **Multimedia Gallery:** Photo and video gallery showcasing school life and activities.
- **SEO and Accessibility:** Semantic HTML, ARIA roles, alt attributes, keyboard focus management, and visually hidden labels for screen readers.
- **Contact Information and Feedback:** Clear contact details and a feedback form to encourage communication.

This structure and content will present Shalom Foundation Nursery & Primary School as a modern, caring, and professional educational institution.

[1] https://fonts.googleapis.com/css?family=Monts
