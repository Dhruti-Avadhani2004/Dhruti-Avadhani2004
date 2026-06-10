<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>⚡ DHRUTI AVADHANI ⚡ // CYBERPUNK 2077 // PINK NEON DREAM</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: linear-gradient(135deg, #0a0a1a 0%, #1a0a2a 50%, #0a0a1a 100%);
      font-family: 'Courier New', 'Fira Code', monospace;
      overflow-x: hidden;
      position: relative;
    }

    /* PINK NEON GLOW EFFECTS */
    @keyframes neonPulse {
      0%, 100% { text-shadow: 0 0 5px #ff69b4, 0 0 10px #ff69b4, 0 0 20px #ff1493, 0 0 40px #ff69b4; }
      50% { text-shadow: 0 0 10px #ff69b4, 0 0 20px #ff1493, 0 0 40px #ff69b4, 0 0 80px #ff1493; }
    }

    @keyframes cyanPulse {
      0%, 100% { text-shadow: 0 0 5px #00ffff, 0 0 10px #00ffff, 0 0 20px #00bfff; }
      50% { text-shadow: 0 0 10px #00ffff, 0 0 20px #00bfff, 0 0 40px #00ffff; }
    }

    @keyframes float {
      0%, 100% { transform: translateY(0px); }
      50% { transform: translateY(-20px); }
    }

    @keyframes spinSlow {
      from { transform: rotate(0deg); }
      to { transform: rotate(360deg); }
    }

    @keyframes glitch {
      0%, 100% { transform: translate(0); opacity: 1; }
      20% { transform: translate(-2px, 2px); }
      40% { transform: translate(-2px, -2px); }
      60% { transform: translate(2px, 2px); }
      80% { transform: translate(2px, -2px); }
    }

    @keyframes scanline {
      0% { transform: translateY(-100%); }
      100% { transform: translateY(100%); }
    }

    .glitch-text {
      animation: glitch 0.3s infinite;
    }

    /* SCANLINE EFFECT */
    .scanline {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: linear-gradient(to bottom, transparent 50%, rgba(255, 105, 180, 0.03) 50%);
      background-size: 100% 4px;
      pointer-events: none;
      z-index: 999;
      animation: scanline 10s linear infinite;
    }

    /* NEON BORDERS */
    .neon-border {
      border: 2px solid #ff69b4;
      box-shadow: 0 0 15px #ff69b4, inset 0 0 15px #ff69b4;
      border-radius: 15px;
      backdrop-filter: blur(5px);
    }

    /* PARTICLES BACKGROUND */
    #particles {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: 0;
      pointer-events: none;
    }

    .particle {
      position: absolute;
      background: radial-gradient(circle, #ff69b4, #00ffff);
      border-radius: 50%;
      opacity: 0.6;
      animation: float 3s infinite ease-in-out;
      pointer-events: none;
    }

    /* MAIN CONTAINER */
    .container {
      position: relative;
      z-index: 2;
      max-width: 1400px;
      margin: 0 auto;
      padding: 20px;
    }

    /* HACKER TYPING EFFECT */
    .typing {
      overflow: hidden;
      white-space: nowrap;
      border-right: 3px solid #ff69b4;
      animation: typing 3.5s steps(40, end), blink-caret 0.75s step-end infinite;
    }

    @keyframes typing {
      from { width: 0; }
      to { width: 100%; }
    }

    @keyframes blink-caret {
      from, to { border-color: transparent; }
      50% { border-color: #ff69b4; }
    }

    /* CARDS */
    .card {
      background: rgba(10, 10, 30, 0.7);
      backdrop-filter: blur(10px);
      border-radius: 20px;
      padding: 25px;
      margin: 20px 0;
      transition: all 0.3s ease;
      border: 1px solid rgba(255, 105, 180, 0.3);
    }

    .card:hover {
      transform: translateY(-10px) scale(1.02);
      border-color: #ff69b4;
      box-shadow: 0 0 30px rgba(255, 105, 180, 0.3);
    }

    /* SKILL BARS */
    .skill-bar {
      width: 100%;
      height: 30px;
      background: rgba(0, 255, 255, 0.1);
      border-radius: 15px;
      overflow: hidden;
      margin: 10px 0;
    }

    .skill-fill {
      height: 100%;
      background: linear-gradient(90deg, #ff69b4, #00ffff);
      border-radius: 15px;
      animation: fillBar 2s ease-out;
      display: flex;
      align-items: center;
      justify-content: flex-end;
      padding-right: 10px;
      color: white;
      font-weight: bold;
    }

    @keyframes fillBar {
      from { width: 0; }
      to { width: var(--width); }
    }

    /* GLASS MORPHISM */
    .glass {
      background: rgba(255, 255, 255, 0.05);
      backdrop-filter: blur(10px);
      border-radius: 20px;
      border: 1px solid rgba(255, 105, 180, 0.2);
    }

    /* FLOATING ELEMENTS */
    .floating {
      animation: float 6s ease-in-out infinite;
    }

    /* ROTATING ICON */
    .rotating {
      animation: spinSlow 20s linear infinite;
    }

    /* RESPONSIVE GRID */
    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 20px;
      margin: 20px 0;
    }

    h1, h2, h3 {
      background: linear-gradient(135deg, #ff69b4, #00ffff);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      margin-bottom: 15px;
    }

    h1 {
      font-size: 4rem;
      animation: neonPulse 1.5s ease-in-out infinite;
    }

    .badge {
      display: inline-block;
      padding: 8px 16px;
      margin: 5px;
      background: linear-gradient(135deg, #ff69b4, #ff1493);
      border-radius: 20px;
      color: white;
      font-weight: bold;
      transition: all 0.3s ease;
    }

    .badge:hover {
      transform: scale(1.1);
      box-shadow: 0 0 20px #ff69b4;
    }

    /* TERMINAL WINDOW */
    .terminal {
      background: #0a0a0a;
      border-radius: 10px;
      overflow: hidden;
      border: 1px solid #ff69b4;
      box-shadow: 0 0 20px rgba(255, 105, 180, 0.3);
    }

    .terminal-header {
      background: #1a1a1a;
      padding: 10px;
      display: flex;
      gap: 8px;
      border-bottom: 1px solid #ff69b4;
    }

    .terminal-dot {
      width: 12px;
      height: 12px;
      border-radius: 50%;
    }

    .terminal-dot.red { background: #ff5f56; }
    .terminal-dot.yellow { background: #ffbd2e; }
    .terminal-dot.green { background: #27c93f; }

    .terminal-content {
      padding: 20px;
      font-family: monospace;
      color: #00ffff;
    }

    /* SOCIAL ICONS */
    .social-icon {
      display: inline-block;
      width: 60px;
      height: 60px;
      margin: 10px;
      transition: all 0.3s ease;
      cursor: pointer;
    }

    .social-icon:hover {
      transform: scale(1.2) rotate(360deg);
      filter: drop-shadow(0 0 10px #ff69b4);
    }

    /* RESPONSIVE */
    @media (max-width: 768px) {
      h1 { font-size: 2rem; }
      .grid { grid-template-columns: 1fr; }
    }
  </style>
</head>
<body>

<div id="particles"></div>
<div class="scanline"></div>

<div class="container">
  
  <!-- HEADER WITH GIFS -->
  <div align="center" style="margin: 50px 0;">
    <img src="https://media.giphy.com/media/3o7abB06u9bNzA8LC8/giphy.gif" width="80" style="display: inline-block;">
    <img src="https://media.giphy.com/media/26AHONQ79FdWZhAI0/giphy.gif" width="80" style="display: inline-block;">
    <img src="https://media.giphy.com/media/xT9IgzoKnwFNmISR8I/giphy.gif" width="80" style="display: inline-block;">
    
    <h1 class="glitch-text">⚡ DHRUTI AVADHANI ⚡</h1>
    
    <div class="typing" style="font-size: 1.5rem; color: #00ffff; margin: 20px 0;">
      >_ CYBERSECURITY ARCHITECT // PINK NEON DREAMER // CHAOS ENGINEER
    </div>
    
    <img src="https://media.giphy.com/media/26tn33aiTi1jkl6H6/giphy.gif" width="200">
    <img src="https://media.giphy.com/media/3o7abB06u9bNzA8LC8/giphy.gif" width="80">
  </div>

  <!-- STATS GRID -->
  <div class="grid">
    <div class="card">
      <h2>💗 CURRENT STATUS</h2>
      <div class="terminal">
        <div class="terminal-header">
          <div class="terminal-dot red"></div>
          <div class="terminal-dot yellow"></div>
          <div class="terminal-dot green"></div>
        </div>
        <div class="terminal-content">
          $ whoami<br>
          > FINAL YEAR CYBERSECURITY STUDENT<br>
          $ pwd<br>
          > /IIT_KANPUR/BOSCH/RV_UNIVERSITY<br>
          $ ps aux | grep dhruti<br>
          > 1337 0.0 0.1 hacking the mainframe...<br>
          $ 🎯 MISSION: BREAK EVERYTHING, FIX EVERYTHING
        </div>
      </div>
    </div>

    <div class="card">
      <h2>🔮 SKILL MATRIX</h2>
      <div class="skill-bar">
        <div class="skill-fill" style="--width: 95%; width: 95%">PENTESTING 95%</div>
      </div>
      <div class="skill-bar">
        <div class="skill-fill" style="--width: 90%; width: 90%">SOC ANALYTICS 90%</div>
      </div>
      <div class="skill-bar">
        <div class="skill-fill" style="--width: 88%; width: 88%">AI SECURITY 88%</div>
      </div>
      <div class="skill-bar">
        <div class="skill-fill" style="--width: 92%; width: 92%">CLOUD SECURITY 92%</div>
      </div>
      <div class="skill-bar">
        <div class="skill-fill" style="--width: 85%; width: 85%">DFIR 85%</div>
      </div>
    </div>
  </div>

  <!-- ACHIEVEMENTS WITH ANIMATIONS -->
  <div class="card">
    <h2>🏆 ACHIEVEMENT UNLOCKED</h2>
    <div class="grid">
      <div class="floating" style="text-align: center;">
        <img src="https://media.giphy.com/media/3o6Zt481isNVuQI1l6/giphy.gif" width="100">
        <h3>CTF CHAMPION</h3>
        <p>1st PLACE | Magnovite 2024</p>
      </div>
      <div class="floating" style="text-align: center; animation-delay: 1s;">
        <img src="https://media.giphy.com/media/l0MYt5jH6gkTWtCZG/giphy.gif" width="100">
        <h3>IEEE XPLORE</h3>
        <p>Paper Accepted @ AIDE 2026</p>
      </div>
      <div class="floating" style="text-align: center; animation-delay: 2s;">
        <img src="https://media.giphy.com/media/26BRv0ThflBHCx4uU/giphy.gif" width="100">
        <h3>BERTELSMANN SCHOLAR</h3>
        <p>Top 1% Global</p>
      </div>
    </div>
  </div>

  <!-- PROJECTS WITH GLOW -->
  <div class="card">
    <h2>🚀 WILD PROJECTS</h2>
    <div class="grid">
      <div class="glass" style="padding: 20px;">
        <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExeGZ1a2hnd3U4ZzBqM2V0d2R6cGgwamU1bHZ6aXY0aXc5dWp2bWJpdyZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/3o7abB06u9bNzA8LC8/giphy.gif" width="50">
        <h3>🤖 GENAI PENTESTING AGENT</h3>
        <p>46 vulns discovered • Autonomous chaos • Bug bounty validated</p>
        <div class="badge">AI-POWERED</div>
        <div class="badge">46 EXPLOITS</div>
      </div>
      <div class="glass" style="padding: 20px;">
        <img src="https://media.giphy.com/media/xT9IgzoKnwFNmISR8I/giphy.gif" width="50">
        <h3>🛡️ SGC-GATEKEEPER</h3>
        <p>SAST/SCA Platform • Real-time vuln dashboard • CVSS scoring</p>
        <div class="badge">DEVSECOPS</div>
        <div class="badge">AUTOMATED</div>
      </div>
      <div class="glass" style="padding: 20px;">
        <img src="https://media.giphy.com/media/l0MYt5jH6gkTWtCZG/giphy.gif" width="50">
        <h3>🔍 XAI JS DETECTOR</h3>
        <p>Chrome extension • DOM XSS blocker • Cryptojacking stopper</p>
        <div class="badge">XAI</div>
        <div class="badge">REAL-TIME</div>
      </div>
    </div>
  </div>

  <!-- TOOLS CAROUSEL -->
  <div class="card">
    <h2>💀 WEAPON ARSENAL</h2>
    <div align="center" style="margin: 20px 0;">
      <img src="https://img.shields.io/badge/-WIRESHARK-1679A7?style=for-the-badge&logo=wireshark&logoColor=white&labelColor=ff69b4">
      <img src="https://img.shields.io/badge/-BURP_SUITE-FF6633?style=for-the-badge&logo=burpsuite&logoColor=white&labelColor=00ffff">
      <img src="https://img.shields.io/badge/-METASPLOIT-008C8C?style=for-the-badge&logo=metasploit&logoColor=white&labelColor=ff69b4">
      <img src="https://img.shields.io/badge/-KALI_LINUX-557C94?style=for-the-badge&logo=kalilinux&logoColor=white&labelColor=00ffff">
      <img src="https://img.shields.io/badge/-PYTHON-3776AB?style=for-the-badge&logo=python&logoColor=white&labelColor=ff69b4">
      <img src="https://img.shields.io/badge/-AWS-232F3E?style=for-the-badge&logo=amazonaws&logoColor=white&labelColor=00ffff">
      <img src="https://img.shields.io/badge/-NESSUS-00C8FF?style=for-the-badge&logo=nessus&logoColor=white&labelColor=ff69b4">
      <img src="https://img.shields.io/badge/-NAMP-004BFF?style=for-the-badge&logo=nmap&logoColor=white&labelColor=00ffff">
    </div>
  </div>

  <!-- LIVE GITHUB STATS WITH ANIMATION -->
  <div class="card">
    <h2>📊 LIVE HACKER STATS</h2>
    <div align="center">
      <img src="https://github-readme-stats.vercel.app/api?username=Dhruti-Avadhani2004&show_icons=true&theme=radical&bg_color=0a0a2a&title_color=ff69b4&icon_color=00ffff&text_color=ffffff&border_color=ff69b4&border_radius=15" width="48%">
      <img src="https://github-readme-streak-stats.herokuapp.com/?user=Dhruti-Avadhani2004&theme=radical&background=0a0a2a&stroke=ff69b4&ring=ff69b4&fire=00ffff&currStreakNum=ffffff&sideNums=ff69b4&currStreakLabel=00ffff&sideLabels=ff69b4&dates=ffffff&border=ff69b4" width="48%">
    </div>
  </div>

  <!-- MUSIC VISUALIZER VIBE -->
  <div class="card">
    <h2>🎧 CURRENTLY HACKING TO</h2>
    <div align="center">
      <img src="https://spotify-github-profile.vercel.app/api/view?uid=YOUR_SPOTIFY_ID&cover_image=true&theme=compact&bar_color=ff69b4&bar_color_cover=true" width="60%">
      <br>
      <img src="https://media.giphy.com/media/26n6WywJyh39n1pBu/giphy.gif" width="100">
      <img src="https://media.giphy.com/media/3o7abB06u9bNzA8LC8/giphy.gif" width="100">
    </div>
  </div>

  <!-- SOCIAL LINKS WITH CRAZY ANIMATIONS -->
  <div class="card">
    <h2>🌐 CONNECT OR ELSE</h2>
    <div align="center">
      <a href="https://www.linkedin.com/in/dhruti-avadhani-456758280/">
        <img class="social-icon" src="https://cdn-icons-png.flaticon.com/512/174/174857.png" alt="LinkedIn">
      </a>
      <a href="https://github.com/Dhruti-Avadhani2004/">
        <img class="social-icon" src="https://cdn-icons-png.flaticon.com/512/25/25231.png" alt="GitHub">
      </a>
      <a href="mailto:dhruti.avadhani2004@gmail.com">
        <img class="social-icon" src="https://cdn-icons-png.flaticon.com/512/732/732200.png" alt="Email">
      </a>
    </div>
  </div>

  <!-- RESUME BUTTON WITH EXPLOSION -->
  <div align="center" style="margin: 40px 0;">
    <div class="badge" style="font-size: 1.5rem; padding: 15px 30px; cursor: pointer;" onclick="window.open('YOUR_RESUME_LINK', '_blank')">
      💾 DOWNLOAD RESUME → 💥
    </div>
  </div>

  <!-- FOOTER -->
  <div align="center">
    <img src="https://capsule-render.vercel.app/api?type=waving&color=ff69b4&height=120&section=footer&fontColor=00ffff"/>
    <br>
    <img src="https://komarev.com/ghpvc/?username=Dhruti-Avadhani2004&color=ff69b4&style=for-the-badge&label=PROFILE+VIEWS">
    <br><br>
    <p style="color: #ff69b4;">⚡ made with pink neon, 4am energy, and questionable life choices ⚡</p>
    <p style="color: #00ffff;">// hack the planet // stay pink // stay glitchy //</p>
  </div>

</div>

<script>
  // PARTICLE SYSTEM
  function createParticles() {
    const container = document.getElementById('particles');
    const particleCount = 100;
    
    for (let i = 0; i < particleCount; i++) {
      const particle = document.createElement('div');
      particle.classList.add('particle');
      const size = Math.random() * 5 + 2;
      particle.style.width = size + 'px';
      particle.style.height = size + 'px';
      particle.style.left = Math.random() * 100 + '%';
      particle.style.top = Math.random() * 100 + '%';
      particle.style.animationDelay = Math.random() * 5 + 's';
      particle.style.animationDuration = Math.random() * 3 + 2 + 's';
      container.appendChild(particle);
    }
  }
  
  // GLITCH EFFECT ON HOVER
  const glitchElements = document.querySelectorAll('.card');
  glitchElements.forEach(el => {
    el.addEventListener('mouseenter', () => {
      el.style.animation = 'glitch 0.2s infinite';
    });
    el.addEventListener('mouseleave', () => {
      el.style.animation = '';
    });
  });
  
  createParticles();
  
  // RANDOM COLOR FLICKER
  setInterval(() => {
    const badges = document.querySelectorAll('.badge');
    badges.forEach(badge => {
      if (Math.random() > 0.9) {
        badge.style.transform = 'scale(1.1)';
        setTimeout(() => {
          badge.style.transform = '';
        }, 200);
      }
    });
  }, 2000);
</script>

</body>
</html>
