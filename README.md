<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>R.I.V.E.R – Environmental Robotics Initiative</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap" rel="stylesheet">
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      font-family: 'Poppins', sans-serif;
      background: linear-gradient(to bottom, #001d3d, #003566, #0077b6, #00b4d8, #90e0ef);
      color: #fff;
      overflow-x: hidden;
    }
    a { color: inherit; text-decoration: none; }
    h1, h2, h3 { margin-bottom: 20px; }

    nav {
      position: fixed;
      top: 0;
      width: 100%;
      background: rgba(0, 0, 0, 0.7);
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 20px 50px;
      z-index: 1000;
      backdrop-filter: blur(10px);
    }
    nav .logo {
      font-weight: 700;
      font-size: 28px;
      color: #00b4d8;
      letter-spacing: 2px;
    }
    nav ul { display: flex; list-style: none; }
    nav ul li { margin-left: 25px; }
    nav ul li a:hover { color: #90e0ef; }

    section {
      padding: 100px 10%;
      text-align: center;
    }

    .hero {
      height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      background: url('https://images.unsplash.com/photo-1507525428034-b723cf961d3e?fit=crop&w=1600&q=80') center/cover no-repeat;
      position: relative;
    }
    .hero::after {
      content: '';
      position: absolute;
      top: 0; left: 0;
      width: 100%; height: 100%;
      background: rgba(0, 0, 0, 0.55);
    }
    .hero-content {
      position: relative;
      z-index: 1;
      max-width: 800px;
      text-align: center;
      color: #fff;
      animation: fadeIn 2s ease;
    }
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(30px); }
      to { opacity: 1; transform: translateY(0); }
    }
    .hero h1 {
      font-size: 60px;
      background: linear-gradient(90deg, #00b4d8, #90e0ef);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }
    .hero p { font-size: 22px; margin-top: 20px; }
    .hero button {
      margin-top: 30px;
      padding: 15px 40px;
      border: none;
      border-radius: 40px;
      background: linear-gradient(90deg, #00b4d8, #90e0ef);
      color: #001d3d;
      font-weight: bold;
      cursor: pointer;
      transition: 0.3s;
    }
    .hero button:hover { background: #0077b6; color: white; }

    .content {
      background: rgba(255, 255, 255, 0.1);
      border-radius: 15px;
      padding: 40px;
      box-shadow: 0 0 20px rgba(0, 0, 0, 0.2);
      margin-top: 40px;
      text-align: left;
    }

    .fun-fact {
      background: rgba(0, 0, 0, 0.3);
      border-left: 5px solid #90e0ef;
      padding: 30px;
      margin-top: 40px;
      border-radius: 10px;
      text-align: left;
      color: #dff6ff;
    }

    footer {
      background: rgba(0, 0, 0, 0.85);
      text-align: center;
      padding: 30px 0;
      color: #90e0ef;
      font-size: 14px;
    }

    .project-title {
      font-size: 38px;
      background: linear-gradient(90deg, #90e0ef, #00b4d8);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      margin-bottom: 10px;
    }

    .project-section {
      margin-top: 50px;
      background: rgba(255, 255, 255, 0.08);
      border-radius: 15px;
      padding: 40px;
    }

    ul { list-style: disc; margin: 15px 0 0 40px; text-align: left; }
  </style>
</head>
<body>
  <nav>
    <div class="logo">R.I.V.E.R</div>
    <ul>
      <li><a href="#about">About</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#funfacts">Fun Facts</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>

  <section class="hero">
    <div class="hero-content">
      <h1>R.I.V.E.R</h1>
      <p>Robotic Intelligent Vessel for Environmental Restoration</p>
      <button onclick="document.getElementById('about').scrollIntoView({behavior: 'smooth'})">Explore</button>
    </div>
  </section>

  <section id="about">
    <h2 class="project-title">About the Initiative</h2>
    <div class="content">
      <p><strong>R.I.V.E.R</strong> is an advanced autonomous robot designed to restore and protect aquatic ecosystems. It navigates rivers and lakes using AI, GPS, and LiDAR to identify and remove trash clusters, all while avoiding harm to wildlife.</p>
      <p>Its collection barriers guide waste to onboard conveyors for sorting. Recyclables are separated from non-recyclables automatically. When full, a collection boat docks to replace containers — enabling 24/7 cleanup operations.</p>

      <h3>Microplastic Filtration & Ecosystem Restoration</h3>
      <p>R.I.V.E.R doesn’t stop at visible waste — it combats <strong>microplastics</strong> using natural filtration systems. The robot deploys floating wood chips and clay pieces coated with biofilm — a living layer of microorganisms that trap and degrade microplastics. Combined with aquatic plants like cattails and duckweed, it creates a mini-ecosystem that cleans and revives water naturally.</p>
      <p>The ROV (Remotely Operated Vehicle) assists underwater, scanning the environment with sensors, collecting submerged debris, and analyzing ecosystem health in real-time.</p>
    </div>
  </section>

  <section id="projects">
    <h2 class="project-title">Other Projects in Development</h2>

    <div class="project-section">
      <h3>Solution 2: Robotic Fishnet Ver. 1</h3>
      <p>This version of the robotic fishnet is a square metal frame equipped with sensors and cameras at each corner. It detects trash automatically and maneuvers the net to capture it efficiently, reducing the need for manual cleanup. Designed for use in both calm and flowing water, it provides precision waste collection and protection for aquatic life.</p>
    </div>

    <div class="project-section">
      <h3>Solution 3: Robotic Fishnet Ver. 2</h3>
      <p>The upgraded version introduces integrated AI and heat vision technology. This allows the net to distinguish between waste and live creatures, ensuring ethical operation. The system connects to an app — inspired by the Ellipsis AI platform — enabling users to monitor activity through the robots’ cameras. If the net cannot capture certain debris, the AI notifies the app to optimize future missions.</p>
    </div>
  </section>

  <section id="funfacts">
    <h2 class="project-title">Fun Facts</h2>
    <div class="fun-fact">
      <p>🌿 A single gram of biofilm can contain over 10 billion microorganisms working together — nature’s own cleanup crew!</p>
    </div>
    <div class="fun-fact">
      <p>🌊 Duckweed can absorb microplastics smaller than 5 micrometers — invisible to the human eye — while producing oxygen and supporting aquatic life.</p>
    </div>
    <div class="fun-fact">
      <p>🤖 R.I.V.E.R’s AI uses the same navigation logic as autonomous vehicles, adapted for unpredictable river currents and floating debris.</p>
    </div>
    <div class="fun-fact">
      <p>🔬 Microplastics take up to 500 years to break down, but biofilm-coated materials can start degrading them within months.</p>
    </div>
  </section>

  <section id="contact">
    <h2 class="project-title">Get in Touch</h2>
    <div class="content">
      <p>Interested in collaborating or learning more about our environmental robotics? Reach out to our team for partnerships, research, or support opportunities.</p>
      <form style="display:flex;flex-direction:column;gap:15px;margin-top:20px;">
        <input type="text" placeholder="Your Name" required style="padding:12px;border:none;border-radius:8px;">
        <input type="email" placeholder="Your Email" required style="padding:12px;border:none;border-radius:8px;">
        <textarea placeholder="Your Message" rows="5" required style="padding:12px;border:none;border-radius:8px;"></textarea>
        <button type="submit" style="padding:15px;border:none;border-radius:8px;background:#00b4d8;color:#001d3d;font-weight:bold;cursor:pointer;">Send Message</button>
      </form>
    </div>
  </section>

  <footer>
    &copy; 2025 R.I.V.E.R Project | Environmental Robotics Initiative | All Rights Reserved
  </footer>
</body>
</html>
