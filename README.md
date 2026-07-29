<!-- Include Font Awesome Icons Library at the Top -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">

<style>
  /* Hard override for the entire viewport background */
  html, body {
    background-color: #0d1117 !important;
    background: #0d1117 !important;
    color: #f0f6fc !important;
  }
  
  /* Hard override for Jekyll's layout container */
  .wrapper {
    background: transparent !important;
    background-color: transparent !important;
    max-width: 900px !important;
    width: 100% !important;
    margin: 0 auto !important;
    box-shadow: none !important;
    border: none !important;
  }

  /* Force headers to remain clean white against the dark theme */
  .wrapper h1, .wrapper h2, .wrapper h3, .wrapper h4, h1, h2, h3 {
    color: #ffffff !important;
  }
  
  section {
    background: transparent !important;
    width: 100% !important;
    max-width: 900px !important;
    float: none !important;
    padding: 0 !important;
  }

  header {
    display: none !important;
  }

  /* Clean, non-glowing container for the name banner */
  .hero-banner-container {
    position: relative;
    margin-top: 25px;
    margin-bottom: 15px;
    padding: 10px;
    z-index: 1;
  }

  /* Both containers share the same robust grid rules with premium card shadow depth */
  .link-container, .tab-container {
    display: grid !important;
    grid-template-columns: repeat(3, 1fr) !important;
    gap: 12px !important;
    width: 100% !important;
    max-width: 900px !important;
    box-sizing: border-box !important;
  }

  .link-container {
    margin: 20px auto 20px auto !important;
  }

  .tab-container {
    margin: 20px 0 25px 0 !important;
  }

  /* Dynamic portfolio section divider line matching highlight colors */
  .section-divider {
    height: 1px !important;
    width: 100% !important;
    max-width: 900px !important;
    margin: 10px auto !important;
    background: linear-gradient(90deg, rgba(165,71,45,0) 0%, rgba(165,71,45,0.7) 25%, rgba(165,71,45,0.7) 75%, rgba(165,71,45,0) 100%) !important;
    border: none !important;
  }

  /* Responsive adjustment for mobile viewports */
  @media (max-width: 768px) {
    .tab-container, .link-container {
      grid-template-columns: repeat(2, 1fr) !important;
    }
  }

  /* Base styling shared across ALL buttons with upgraded micro-interactions */
  .tab-btn, .custom-link-btn {
    font-size: 0.95em !important;
    font-weight: bold !important;
    border-radius: 6px !important;
    cursor: pointer !important;
    transition: transform 0.25s cubic-bezier(0.25, 1, 0.5, 1), 
                background-color 0.25s ease, 
                border-color 0.25s ease, 
                box-shadow 0.25s ease !important;
    text-decoration: none !important;
    display: inline-flex !important;
    flex-direction: column !important;
    align-items: center !important;
    justify-content: center !important;
    line-height: 1.3 !important;
    padding: 10px 8px !important;
    min-height: 64px !important;
    width: 100% !important;
    box-sizing: border-box !important;
    backface-visibility: hidden !important;
    /* Subtle internal top border highlight to simulate crisp game UI panel lighting */
    box-shadow: inset 0px 1px 0px rgba(255, 255, 255, 0.05), 0px 4px 10px rgba(0, 0, 0, 0.3) !important;
  }

  /* Project tabs icon positioning */
  .tab-btn span i {
    margin-left: 2px;
    margin-right: 2px;
  }

  /* PROJECT TABS: Dark Charcoal Palette */
  .tab-btn {
    background-color: #161b22 !important;
    color: #c9d1d9 !important;
    border: 1px solid #30363d !important;
  }

  .tab-btn:hover {
    border-color: #a5472d !important;
    background-color: #1f242c !important;
    color: #ffffff !important;
    transform: translateY(-3px) !important;
    box-shadow: inset 0px 1px 0px rgba(255, 255, 255, 0.1), 0px 8px 20px rgba(0, 0, 0, 0.45), 0px 0px 10px rgba(165, 71, 45, 0.2) !important;
  }

  .tab-btn.active-tab {
    background-color: #a5472d !important;
    color: #ffffff !important;
    border-color: #e6633e !important;
    box-shadow: 0px 0px 20px rgba(165, 71, 45, 0.6), inset 0px 1px 0px rgba(255,255,255,0.3) !important;
    transform: translateY(-1px) !important;
  }

  /* SOCIAL LINKS: Distinct Slate/Steel Blue Palette */
  .custom-link-btn {
    background-color: #1f2937 !important; 
    color: #e5e7eb !important;
    border: 1px solid #4b5563 !important;
  }

  .custom-link-btn:hover {
    background-color: #243042 !important;
    border-color: #718096 !important;
    color: #ffffff !important;
    transform: translateY(-4px) !important;
    box-shadow: inset 0px 1px 0px rgba(255, 255, 255, 0.1), 0px 10px 22px rgba(0, 0, 0, 0.5), 0px 0px 12px rgba(59, 130, 246, 0.15) !important;
  }

  /* Muted metadata labels inside buttons */
  .tab-meta, .link-meta {
    font-size: 0.82em !important;
    margin-top: 4px !important;
    font-weight: normal !important;
    letter-spacing: 0.3px !important;
  }

  .tab-meta {
    opacity: 0.60 !important;
  }

  .link-meta {
    opacity: 0.50 !important;
  }

  .active-tab .tab-meta {
    opacity: 0.85 !important;
  }

  /* Completely Static Text Blocks with sharp base presentation shadows */
  .bio-card {
    background: #161b22;
    padding: 14px 18px;
    border-radius: 8px;
    border-left: 5px solid #a5472d;
    margin-bottom: 14px;
    color: #f0f6fc;
    box-shadow: 0px 4px 15px rgba(0, 0, 0, 0.25) !important;
  }

  /* Tech Stack Icon Hover states */
  .skill-group img {
    transition: transform 0.2s cubic-bezier(0.175, 0.885, 0.32, 1.275), filter 0.2s ease !important;
    margin: 4px !important;
  }

  .skill-group img:hover {
    transform: scale(1.15) translateY(-2px) !important;
    filter: drop-shadow(0px 0px 8px rgba(165, 71, 45, 0.6)) brightness(1.1) !important;
  }

  /* Image Thumbnails & Overlays */
  .video-thumb {
    position: relative;
    display: inline-block;
  }

  .video-thumb::after {
    content: "▶";
    font-size: 60px;
    color: white;
    text-shadow: 0 0 15px rgba(0,0,0,0.8);
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    pointer-events: none;
    opacity: 0.85;
  }

  /* Coming Soon / Steam badge styling */
  .steam-badge {
    display: inline-flex !important;
    align-items: center !important;
    gap: 8px !important;
    background: #161b22 !important;
    border: 1px solid #30363d !important;
    color: #8b949e !important;
    font-weight: bold !important;
    font-size: 0.85em !important;
    padding: 8px 14px !important;
    border-radius: 20px !important;
    cursor: default !important;
    opacity: 0.9;
  }

  /* Footer */
  .site-footer {
    margin-top: 40px;
    padding-top: 25px;
    border-top: 1px solid #30363d;
    text-align: center;
    color: #8b949e;
    font-size: 0.85em;
  }

  .site-footer .link-container {
    margin: 15px auto 10px auto !important;
  }

/* Container for the characters backdrop hidden by default */
.tab-backdrop-bg {
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  z-index: -1; /* Sits perfectly behind all content panels */
  background: 
    linear-gradient(rgba(13, 17, 23, 0.88), rgba(13, 17, 23, 0.88)), 
    url('4characters.png') no-repeat;
  background-size: contain;
  background-position: center 65%;
  
  /* Initial state: Off-screen at the bottom and invisible */
  transform: translateY(100vh);
  opacity: 0;
  transition: transform 0.6s cubic-bezier(0.25, 1, 0.5, 1), opacity 0.5s ease-in-out;
  pointer-events: none;
}

/* Animate Up state: Triggered instantly when the tab parent opens */
.portfolio-tab[style*="display: block"] .tab-backdrop-bg {
  transform: translateY(0);
  opacity: 1;
}
  
</style>

<a name="top"></a>

<!-- Clean Header Container (Glow Removed) -->
<div align="center" class="hero-banner-container">
  <h1 style="font-size: 3.2em; margin-bottom: 0px; color: #ffffff !important; opacity: 1 !important; text-shadow: 0px 2px 8px rgba(0,0,0,0.8); font-weight: 800;">Tristan Anglin</h1>
  <p style="font-size: 1.2em; margin-top: 10px; margin-bottom: 6px; color: #ffffff !important; opacity: 0.9 !important; background: transparent !important; letter-spacing: 0.8px;">
    <strong style="color: #ffffff !important;">Gameplay Programmer | Systems & UI Architect</strong>
  </p>
  <p style="font-size: 0.95em; margin-top: 0px; color: #da765b !important; opacity: 0.95 !important; background: transparent !important; letter-spacing: 0.4px;">
    Actively seeking opportunities
  </p>
</div>

<!-- Global External Link Grid Container -->
<div class="link-container">
  <a class="custom-link-btn" href="https://tristananglin.github.io/RESUME - GAME DEVELOPMENT.pdf" target="_blank">
    <span>Resume</span>
    <span class="link-meta">PDF</span>
  </a>
  <a class="custom-link-btn" href="https://linkedin.com/in/TristanAnglin" target="_blank">
    <span>LinkedIn</span>
    <span class="link-meta">Professional Network</span>
  </a>
  <a class="custom-link-btn" href="mailto:tmanglin00@gmail.com">
    <span>Email</span>
    <span class="link-meta">Reach out</span>
  </a>
  <a class="custom-link-btn" href="https://github.com/TristanAnglin" target="_blank">
    <span>GitHub</span>
    <span class="link-meta">Source Code</span>
  </a>
  <a class="custom-link-btn" href="https://www.instagram.com/tristananglin_" target="_blank">
    <span>Instagram</span>
    <span class="link-meta">Dev Logs</span>
  </a>
  <a class="custom-link-btn" href="https://www.youtube.com/@TristanAnglin" target="_blank">
    <span>YouTube</span>
    <span class="link-meta">Gameplay Showcases</span>
  </a>
</div>

<!-- Clean Visual Divisor Break -->
<div style="width: 100%; height: 2px; background: linear-gradient(90deg, transparent 5%, #bd4c2a 50%, transparent 95%); margin: 25px 0; opacity: 0.7;"></div>

<!-- Unified Grid Layout Wrapper with Full-Width Overview -->
<div class="tab-container">
  <!-- Full-Width Overview Tab (Spans all 3 columns) -->
  <button class="tab-btn active-tab" onclick="switchTab(event, 'about-tab')" style="grid-column: 1 / -1 !important;">
    <span style="display: inline-flex; align-items: center; line-height: 1; font-size: 1.1em;">
      Overview & Skills
    </span>
    <span class="tab-meta">Core Profile</span>
  </button>
  
  <!-- Project Tabs (Perfectly distributed 3x2 grid underneath) -->
  <button class="tab-btn" onclick="switchTab(event, 'round-based-survival')">
    <span style="display: inline-flex; align-items: center; line-height: 1;">
      Round Based Survival 
      <i class="fa-brands fa-steam" style="color: #66c0f4; font-size: 0.95em; margin-left: 6px; margin-right: 6px; margin-top: -1px;" title="Planned Steam Release"></i>
      <img src="https://skillicons.dev/icons?i=unity&theme=dark" height="18" style="margin-top: -2px;" alt="Unity" />
    </span>
    <span class="tab-meta">In Development</span>
  </button>

  <button class="tab-btn" onclick="switchTab(event, 'blood-lineage')">
    <span style="display: inline-flex; align-items: center; line-height: 1;">
      Blood & Lineage 
      <i class="fa-brands fa-steam" style="color: #66c0f4; font-size: 0.95em; margin-left: 6px; margin-right: 6px; margin-top: -1px;" title="Coming to Steam"></i>
      <img src="https://skillicons.dev/icons?i=unreal&theme=dark" height="18" style="margin-top: -2px;" alt="UE5" />
    </span>
    <span class="tab-meta">Sept 2025 - April 2026</span>
  </button>
  
  <button class="tab-btn" onclick="switchTab(event, 'tower-defense')">
    <span style="display: inline-flex; align-items: center; line-height: 1;">
      Tower Defense 
      <img src="https://skillicons.dev/icons?i=cpp&theme=dark" height="18" style="margin-left: 6px; margin-top: -2px;" alt="C++" />
    </span>
    <span class="tab-meta">Dec 2024</span>
  </button>
  
  <button class="tab-btn" onclick="switchTab(event, 'darkside')">
    <span style="display: inline-flex; align-items: center; line-height: 1;">
      Your Dark Side 
      <img src="https://skillicons.dev/icons?i=java&theme=dark" height="18" style="margin-left: 6px; margin-top: -2px;" alt="Java" />
    </span>
    <span class="tab-meta">2023</span>
  </button>
  
  <button class="tab-btn" onclick="switchTab(event, 'dungeon')">
    <span style="display: inline-flex; align-items: center; line-height: 1;">
      Dungeon Crawler 
      <img src="https://skillicons.dev/icons?i=py&theme=dark" height="18" style="margin-left: 6px; margin-top: -2px;" alt="Python" />
    </span>
    <span class="tab-meta">2017</span>
  </button>
  
  <button class="tab-btn" onclick="switchTab(event, 'hit-run')">
    <span style="display: inline-flex; align-items: center; line-height: 1;">
      Hit & Run 
      <img src="https://skillicons.dev/icons?i=py&theme=dark" height="18" style="margin-left: 6px; margin-top: -2px;" alt="Python" />
    </span>
    <span class="tab-meta">2016</span>
  </button>
</div>

<div style="width: 100%; height: 2px; background: linear-gradient(90deg, transparent 5%, #bd4c2a 50%, transparent 95%); margin: 25px 0; opacity: 0.7;"></div>

<div id="about-tab" class="portfolio-tab" style="display: block;">
  <table border="0" style="width: 100%; border-collapse: collapse; border: none;">
    <tr style="border: none;">
      <td width="55%" valign="top" style="border: none; background: transparent; padding-right: 15px;">
        <div class="bio-card">
          Growing up in a household with a 300+ board game collection gave me an intuitive grasp of game balance and systems design long before I wrote my first line of code.
        </div>
        <div class="bio-card">
          My programming journey began in 2016 with Python, but my curiosity quickly outpaced the classroom. This drive led me to self-teach Java to develop "Your Dark Side." I soon realized my true calling was in the technical architecture and creative heart of game design.
        </div>
        <div class="bio-card">
          A 2026 Honors Graduate in Game Development, I have maintained a 3.86 GPA while dedicating myself to building a portfolio of modular core systems and dynamic user interfaces.
        </div>
      </td>

      <td class="skill-group" width="45%" valign="top" align="center" style="border: none; background: transparent; line-height: 1.8;">
        <div style="margin-bottom: 15px;">
          <b style="color: #ffffff;">Programming</b><br/>
          <img src="https://skillicons.dev/icons?i=cpp&theme=dark" height="40" alt="C++" title="C++" />
          <img src="https://skillicons.dev/icons?i=cs&theme=dark" height="40" alt="C#" title="C#" />
          <img src="https://skillicons.dev/icons?i=py&theme=dark" height="40" alt="Python" title="Python" />
          <img src="https://skillicons.dev/icons?i=java&theme=dark" height="40" alt="Java" title="Java" />
          <img src="https://skillicons.dev/icons?i=html&theme=dark" height="40" alt="HTML5" title="HTML5" />
          <img src="https://skillicons.dev/icons?i=js&theme=dark" height="40" alt="JavaScript" title="JavaScript" />
        </div>

        <div style="margin-bottom: 15px;">
          <b style="color: #ffffff;">Workflow & Version Control</b><br/>
          <img src="assets/Icons/JiraIcon.png" height="40" style="vertical-align: middle; border-radius: 5px;" alt="Jira" title="Jira" />
          <img src="https://skillicons.dev/icons?i=git&theme=dark" height="40" style="vertical-align: middle;" alt="Git" title="Git" />
          <img src="https://skillicons.dev/icons?i=mysql&theme=dark" height="40" style="vertical-align: middle;" alt="MySQL" title="MySQL" />
          <img src="https://skillicons.dev/icons?i=nodejs&theme=dark" height="40" style="vertical-align: middle;" alt="Node.js" title="Node.js" />
          <img src="https://skillicons.dev/icons?i=cmake&theme=dark" height="40" style="vertical-align: middle;" alt="CMake" title="CMake" />
        </div>

        <div style="margin-bottom: 15px;">
          <b style="color: #ffffff;">Development Environments & Engines</b><br/>
          <img src="https://skillicons.dev/icons?i=visualstudio&theme=dark" height="40" alt="Visual Studio" title="Visual Studio" />
          <img src="https://skillicons.dev/icons?i=vscode&theme=dark" height="40" alt="VS Code" title="VS Code" />
          <img src="https://skillicons.dev/icons?i=eclipse&theme=dark" height="40" alt="Eclipse" title="Eclipse" />
          <img src="https://skillicons.dev/icons?i=unreal&theme=dark" height="40" alt="Unreal Engine" title="Unreal Engine" />
          <img src="https://skillicons.dev/icons?i=unity&theme=dark" height="40" alt="Unity" title="Unity" />
        </div>

        <div style="margin-bottom: 15px;">
          <b style="color: #ffffff;">Art, Audio & UI Design</b><br/>
          <img src="assets/Icons/3dsmaxIcon.png" height="40" style="vertical-align: middle; border-radius: 5px;" alt="3ds Max" title="3ds Max" />
          <img src="https://skillicons.dev/icons?i=blender&theme=dark" height="40" style="vertical-align: middle;" alt="Blender" title="Blender" />
          <img src="https://skillicons.dev/icons?i=photoshop&theme=dark" height="40" style="vertical-align: middle;" alt="Adobe Photoshop" title="Adobe Photoshop" />
          <img src="https://skillicons.dev/icons?i=illustrator&theme=dark" height="40" style="vertical-align: middle;" alt="Adobe Illustrator" title="Adobe Illustrator" />
          <img src="https://skillicons.dev/icons?i=pr&theme=dark" height="40" style="vertical-align: middle;" alt="Adobe Premiere Pro" title="Adobe Premiere Pro" />
          <img src="https://skillicons.dev/icons?i=au&theme=dark" height="40" style="vertical-align: middle;" alt="Adobe Audition" title="Adobe Audition" />
        </div>
      </td>
    </tr>
  </table>

  <div style="width: 100%; height: 2px; background: linear-gradient(90deg, transparent 5%, #bd4c2a 50%, transparent 95%); margin: 25px 0; opacity: 0.7;"></div>

  <!-- Presentation Frame for Showcase Photo -->
  <div align="center" style="width: 100%; padding-bottom: 30px; padding-top: 5px;">
    <img src="myselfLevelup.jpg" 
         alt="Tristan Anglin - Level Up Showcase" 
         loading="lazy"
         style="width: 100%; height: auto; border-radius: 12px; border: 1px solid rgba(165, 71, 45, 0.4); box-shadow: 0px 15px 35px rgba(0,0,0,0.6), 0px 0px 20px rgba(165, 71, 45, 0.15); transition: all 0.4s ease;"
         onmouseover="this.style.borderColor='rgba(230, 99, 62, 0.7)'; this.style.boxShadow='0px 20px 45px rgba(0,0,0,0.7), 0px 0px 25px rgba(165, 71, 45, 0.35)';"
         onmouseout="this.style.borderColor='rgba(165, 71, 45, 0.4)'; this.style.boxShadow='0px 15px 35px rgba(0,0,0,0.6), 0px 0px 20px rgba(165, 71, 45, 0.15)';" />
  </div>
</div>

<div id="round-based-survival" class="portfolio-tab" style="display: none; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif; color: #c9d1d9;">
  
  <div style="display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 10px;">
    <!-- Left Side: Title Badge + Unity Logo -->
    <div style="display: flex; align-items: center; gap: 8px;">
      <img src="https://img.shields.io/badge/Round%20Based%20Survival-a5472d?style=for-the-badge" height="35" alt="Round Based Survival"/>
      <img src="https://skillicons.dev/icons?i=unity" height="30" style="display: block;" alt="Unity Engine" />
    </div>
    
    <!-- Middle: Steam Release Badge -->
    <div>
      <span class="steam-badge" style="padding: 6px 14px; background: #161b22; border: 1px solid #333; border-radius: 20px; font-size: 0.85em; color: #8b949e; display: inline-flex; align-items: center; gap: 8px; font-weight: bold;">
        <i class="fa-brands fa-steam" style="color: #66c0f4; font-size: 1.5em; margin-left: 6px; margin-right: 6px; margin-top: -1px;" title="Planned Steam Release"></i>
        Planned Steam Release
      </span>
    </div>
    
    <!-- Right Side: Status Badge -->
    <img src="https://img.shields.io/badge/Status--In%20Development-333333?style=for-the-badge" height="35" alt="In Development"/>
  </div>

  <!-- Sub-Header Metadata Line -->
  <div style="display: flex; justify-content: space-between; margin-top: 12px; padding-bottom: 4px; flex-wrap: wrap; gap: 5px;">
    <b style="color: #f0f6fc; font-size: 1.1em;">3D Action Survival Loop</b>
    <b style="color: #da765b; font-size: 1.1em;">Solo Systems & Gameplay Programmer</b>
  </div>

  <!-- Summary Box and Metric Display Split Grid -->
  <div style="display: grid; grid-template-columns: 2fr 1fr; gap: 15px; margin: 20px 0; align-items: center;">
    <div style="background: #161b22; padding: 16px; border-radius: 8px; border-left: 5px solid #a5472d; color: #f0f6fc; line-height: 1.5;">
      Architecting a modular and scalable round-based survival loop framework from scratch using <b>Unity</b> and decoupled <b>C#</b> architecture. Engineering finite state machines for wave progression, dynamic enemy spawning algorithms, and fluid weapon/inventory management profiles configured for a commercial desktop deployment.
    </div>
    <div style="background: #0d1117; border: 1px solid #30363d; padding: 12px; border-radius: 8px; text-align: center;">
      <div style="font-size: 1.8em; font-weight: bold; color: #f0f6fc; margin-bottom: 2px;">C#</div>
      <div style="font-size: 0.75em; color: #8b949e; text-transform: uppercase; letter-spacing: 0.5px; margin-bottom: 10px;">OOP Architecture</div>
      <div style="font-size: 1.8em; font-weight: bold; color: #f0f6fc; margin-bottom: 2px;">Unity</div>
      <div style="font-size: 0.75em; color: #8b949e; text-transform: uppercase; letter-spacing: 0.5px;">Input System / UIElements</div>
    </div>
  </div>

  <h3 style="margin-bottom: 5px; color: #ffffff; font-size: 1.3em;">Technical Features</h3>
  <div style="width: 100%; height: 2px; background: linear-gradient(90deg, transparent 0%, #bd4c2a 50%, transparent 100%); margin: 10px 0 25px 0; opacity: 0.7;"></div>

  <!-- Detailed Contributions Card -->
  <div style="background: #161b22; padding: 18px; border-radius: 8px; border-left: 5px solid #a5472d; margin-bottom: 25px; color: #f0f6fc;">
    <div style="display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 5px; margin-bottom: 10px;">
      <b style="color: #ffffff; font-size: 1.1em;">Gameplay Framework & Core State Machines</b>
      <span style="font-size: 0.75em; background: #21262d; border: 1px solid #30363d; padding: 3px 8px; border-radius: 20px; color: #8b949e; font-weight: bold;">C# Scripting / State Architecture</span>
    </div>
    
    <ul style="margin: 0; padding-left: 20px; line-height: 1.6; color: #c9d1d9;">
      <li><b>Round Transition Automation:</b> Programmed a centralized Game Director manager using an state-driven architecture to dynamically control round scaling curves, grace periods, and clear conditions.</li>
      <li><b>Decoupled ScriptableObject Databases:</b> Created data-driven configuration arrays for items, enemy scaling variations, and progressive round modifiers to maximize code reusability.</li>
      <li><b>Robust Input Management:</b> Implemented smooth mechanics built natively around the updated Unity Input System for modular control handling profiles.</li>
    </ul>
  </div>
</div>

<div id="blood-lineage" class="portfolio-tab" style="display: none; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif; color: #c9d1d9;">
  
  <div id="image-zoom-modal" onclick="this.style.display='none'" style="display: none; position: fixed; z-index: 99999; left: 0; top: 0; width: 100%; height: 100%; background-color: rgba(13, 17, 23, 0.95); align-items: center; justify-content: center; cursor: zoom-out;">
    <img id="modal-target-img" style="max-width: 90%; max-height: 90%; border-radius: 8px; border: 2px solid #a5472d; box-shadow: 0 0 30px rgba(165, 71, 45, 0.4);">
  </div>

  <script>
    function zoomImage(imgElement) {
      const modal = document.getElementById('image-zoom-modal');
      const modalImg = document.getElementById('modal-target-img');
      modal.style.display = "flex";
      modalImg.src = imgElement.src;
    }
  </script>

<div style="display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 10px;">
  <!-- Left Side: Title Badge + Unreal Logo -->
  <div style="display: flex; align-items: center; gap: 8px;">
    <img src="https://img.shields.io/badge/Blood%20%26%20Lineage-a5472d?style=for-the-badge" height="35" alt="Blood & Lineage"/>
    <img src="https://skillicons.dev/icons?i=unreal" height="30" style="display: block;" alt="Unreal Engine" />
  </div>
  
  <!-- Middle: Centered Steam Status with Steam Icon -->
  <div>
    <span class="steam-badge" style="padding: 6px 14px; background: #161b22; border: 1px solid #333; border-radius: 20px; font-size: 0.85em; color: #8b949e; display: inline-flex; align-items: center; gap: 8px; font-weight: bold;">
      <i class="fa-brands fa-steam" style="color: #66c0f4; font-size: 1.5em; margin-left: 6px; margin-right: 6px; margin-top: -1px;" title="Coming to Steam"></i>
      Coming soon
    </span>
  </div>
  
  <!-- Right Side: Year/Date Badge -->
  <img src="https://img.shields.io/badge/Sept%202025%20--%20April%202026-333333?style=for-the-badge" height="35" alt="Sept 2025 - April 2026"/>
</div>

<!-- Metadata block renders perfectly right below it -->
<div style="display: flex; justify-content: space-between; margin-top: 12px; padding-bottom: 4px; flex-wrap: wrap; gap: 5px;">
  <b style="color: #f0f6fc; font-size: 1.1em;">3D Co-op Musou RPG (Capstone Project)</b>
  <b style="color: #da765b; font-size: 1.1em;">Lead Systems Architect & UI Programmer</b>
</div>

  <div style="display: grid; grid-template-columns: 2fr 1fr; gap: 15px; margin: 20px 0; align-items: center;">
    <div style="background: #161b22; padding: 16px; border-radius: 8px; border-left: 5px solid #a5472d; color: #f0f6fc; line-height: 1.5;">
      Led the technical roadmap and framework development for an 11-person team. Personally architected the core gameplay loops, server-sided multiplayer infrastructure, and a comprehensive suite of UI/UX systems. Managed cross-department stability and build delivery utilizing <b>Jira</b> and <b>GitHub</b>.
    </div>
    <div style="background: #0d1117; border: 1px solid #30363d; padding: 12px; border-radius: 8px; text-align: center;">
      <div style="font-size: 1.8em; font-weight: bold; color: #f0f6fc; margin-bottom: 2px;">20+</div>
      <div style="font-size: 0.75em; color: #8b949e; text-transform: uppercase; letter-spacing: 0.5px; margin-bottom: 10px;">Networked Systems</div>
      <div style="font-size: 1.8em; font-weight: bold; color: #f0f6fc; margin-bottom: 2px;">50+</div>
      <div style="font-size: 0.75em; color: #8b949e; text-transform: uppercase; letter-spacing: 0.5px;">Vector UI Assets</div>
    </div>
  </div>

  <div align="center" style="margin: 25px 0;">
    <div style="position: relative; width: 100%; max-width: 850px; aspect-ratio: 16 / 9; border-radius: 12px; border: 2px solid #a5472d; box-shadow: 0px 0px 20px rgba(165, 71, 45, 0.2); overflow: hidden;">
      <iframe 
        src="https://www.youtube.com/embed/tgr0kjX5Q0Q?autoplay=1&mute=1&loop=1&playlist=tgr0kjX5Q0Q&controls=1&modestbranding=1" 
        title="Blood & Lineage Gameplay"
        loading="lazy"
        style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: none;"
        allow="autoplay; encrypted-media; picture-in-picture" 
        allowfullscreen>
      </iframe>
    </div>
  </div>

  <div style="background: #161b22; padding: 12px 15px; border-radius: 8px; border-left: 5px solid #6e7681; margin-bottom: 35px; font-style: italic; font-size: 0.9em; color: #c9d1d9; line-height: 1.5;">
    "My workflow prioritizes networking and system state first. I engineer structural foundations and client/server validation profiles before implementing vector aesthetics, custom animations, and responsive motion graphics."
  </div>

  <h3 style="margin-bottom: 5px; color: #ffffff; font-size: 1.3em;">Core Contributions</h3>
  <div style="width: 100%; height: 2px; background: linear-gradient(90deg, transparent 0%, #bd4c2a 50%, transparent 100%); margin: 10px 0 25px 0; opacity: 0.7;"></div>

  <div style="background: #161b22; padding: 18px; border-radius: 8px; border-left: 5px solid #a5472d; margin-bottom: 25px; color: #f0f6fc;">
    <div style="display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 5px; margin-bottom: 10px;">
      <b style="color: #ffffff; font-size: 1.1em;">Multiplayer Architecture & Systems Framework</b>
      <span style="font-size: 0.75em; background: #21262d; border: 1px solid #30363d; padding: 3px 8px; border-radius: 20px; color: #8b949e; font-weight: bold;">C++ / Blueprints / Replication</span>
    </div>
    
    <ul style="margin: 0 0 20px 0; padding-left: 20px; line-height: 1.6; color: #c9d1d9;">
      <li><b>Architected Core Separation:</b> Refactored codebase into a clean model splitting logic across <i>Character</i> (combat/movement), <i>Player Controller</i> (UI/Inputs), and <i>Player State</i> (persistent multiplayer variables).</li>
      <li><b>Engineered Seamless Travel Persistence:</b> Designed a deep state copying system carrying player data (stats, inventory, meta-progression) across multiplayer level transitions safely.</li>
      <li><b>Implemented Networking:</b> Developed server-sided logic for synchronized loot drops, currency accumulation, and player interactions for up to 4 concurrent clients.</li>
      <li><b>Prevented Design Soft-locks:</b> Built an automated, scaling Class-Locked Signature Weapon system ensuring players remain continuously viable without the risk of destroying primary weapon items.</li>
    </ul>

    <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(340px, 1fr)); gap: 15px; margin-top: 15px;">
      <div style="background: #0d1117; border: 1px solid #30363d; border-radius: 6px; padding: 12px; display: flex; flex-direction: column; justify-content: space-between;">
        <div>
          <b style="color: #ffffff; font-size: 0.95em; display: block; margin-bottom: 4px;">PlayerState Data</b>
          <p style="font-size: 0.85em; color: #8b949e; line-height: 1.4; margin-bottom: 12px;">
            During seamless travel transitions, the engine destroys and regenerates Actor states. To prevent loss of progress, `CopyProperties` intercepts the tear-down to manually pass player statistics, currencies, and deeply copied inventory outer arrays over to the newly instantiated world state.
          </p>
        </div>
        <div style="text-align: center; background: #161b22; padding: 6px; border-radius: 4px; border: 1px solid #21262d;">
          <img src="Copy Properties.PNG" alt="Player State Data Serialization Code" loading="lazy" onclick="zoomImage(this)" style="max-width: 100%; max-height: 220px; width: auto; height: auto; object-fit: contain; border-radius: 4px; cursor: zoom-in; transition: transform 0.2s;" onmouseover="this.style.transform='scale(1.01)'" onmouseout="this.style.transform='scale(1)'">
          <span style="font-size: 0.75em; color: #da765b; display: block; margin-top: 6px; font-weight: bold;">🔍 Click to expand</span>
        </div>
      </div>

      <div style="background: #0d1117; border: 1px solid #30363d; border-radius: 6px; padding: 12px; display: flex; flex-direction: column; justify-content: space-between;">
        <div>
          <b style="color: #ffffff; font-size: 0.95em; display: block; margin-bottom: 4px;">UI Culling</b>
          <p style="font-size: 0.85em; color: #8b949e; line-height: 1.4; margin-bottom: 12px;">
            World destruction without proactive UI tracking results in fatal engine null-pointer references. This architectural cleanup routine systematically unbinds input frames, culls active viewports, and marks non-viewport/3D widgets directly for clean garbage collection before map streams clear.
          </p>
        </div>
        <div style="text-align: center; background: #161b22; padding: 6px; border-radius: 4px; border: 1px solid #21262d;">
          <img src="Clean UI.PNG" alt="UI Culling" loading="lazy" onclick="zoomImage(this)" style="max-width: 100%; max-height: 220px; width: auto; height: auto; object-fit: contain; border-radius: 4px; cursor: zoom-in; transition: transform 0.2s;" onmouseover="this.style.transform='scale(1.01)'" onmouseout="this.style.transform='scale(1)'">
          <span style="font-size: 0.75em; color: #da765b; display: block; margin-top: 6px; font-weight: bold;">🔍 Click to expand</span>
        </div>
      </div>
    </div>
  </div>

  <div style="background: #161b22; padding: 18px; border-radius: 8px; border-left: 5px solid #a5472d; margin-bottom: 25px; color: #f0f6fc;">
    <div style="display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 5px; margin-bottom: 10px;">
      <b style="color: #ffffff; font-size: 1.1em;">Full-Stack UI/UX Engineering & Unified Drag-and-Drop</b>
      <span style="font-size: 0.75em; background: #21262d; border: 1px solid #30363d; padding: 3px 8px; border-radius: 20px; color: #8b949e; font-weight: bold;">UMG / Slate / Motion Design</span>
    </div>
    
    <ul style="margin: 0 0 20px 0; padding-left: 20px; line-height: 1.6; color: #c9d1d9;">
      <li><b>Interface Suite Development:</b> Programmed over 20+ intricate screens including a networked 4-Player Match Lobby, interactive Keybind Remappers, Save Management Profiles, and specialized Armory systems.</li>
      <li><b>Engineered Custom Visual Payloads:</b> Programmed a unified `UDragDropOperation` subclass passing full `FItemData` memory frames to let user drag actions seamlessly bridge across the distinct Inventory, Forge, and Armory UI panels natively.</li>
      <li><b>Dynamic HUD & State Feedback:</b> Built a responsive player HUD factoring formula-based calculations (e.g., Intelligence stats dynamically adjusting displayed mana costs in real-time) and low-health UI vignettes.</li>
      <li><b>Graphic Asset Production:</b> Hand-crafted and vectorized a cohesive library of 50+ custom flat-design icons spanning difficulty tiers, classes, stats, and equipment matrices.</li>
    </ul>

    <b style="color: #ffffff; font-size: 0.95em; display: block; margin-bottom: 10px; padding-left: 5px;">Visual Breakdown: System Prototyping to Production Assets</b>
    <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(240px, 1fr)); gap: 12px;">
      <div style="text-align: center; background: #0d1117; padding: 10px; border-radius: 6px; border: 1px solid #30363d;">
        <img src="InventoryWireframe.png" alt="UX Wireframe Layout" loading="lazy" onclick="zoomImage(this)" style="width: 100%; height: auto; aspect-ratio: 16/10; object-fit: contain; background: #161b22; border-radius: 4px; cursor: zoom-in; transition: transform 0.2s;" onmouseover="this.style.transform='scale(1.02)'" onmouseout="this.style.transform='scale(1)'">
        <p style="font-size: 0.8em; color: #8b949e; margin-top: 8px; margin-bottom: 0;"><b>Phase 1:</b> Screen Wireframe & Core Functional Grid</p>
      </div>
      <div style="text-align: center; background: #0d1117; padding: 10px; border-radius: 6px; border: 1px solid #30363d;">
        <img src="InventoryFinal.PNG" alt="Inventory Layout Art Integration" loading="lazy" onclick="zoomImage(this)" style="width: 100%; height: auto; aspect-ratio: 16/10; object-fit: contain; background: #161b22; border-radius: 4px; cursor: zoom-in; transition: transform 0.2s;" onmouseover="this.style.transform='scale(1.02)'" onmouseout="this.style.transform='scale(1)'">
        <p style="font-size: 0.8em; color: #8b949e; margin-top: 8px; margin-bottom: 0;"><b>Phase 2:</b> Vector Asset Pipeline Integration</p>
      </div>
      <div style="text-align: center; background: #0d1117; padding: 10px; border-radius: 6px; border: 1px solid #30363d;">
        <img src="HUDFinal.PNG" alt="Final Tactical HUD Layout" loading="lazy" onclick="zoomImage(this)" style="width: 100%; height: auto; aspect-ratio: 16/10; object-fit: contain; background: #161b22; border-radius: 4px; cursor: zoom-in; transition: transform 0.2s;" onmouseover="this.style.transform='scale(1.02)'" onmouseout="this.style.transform='scale(1)'">
        <p style="font-size: 0.8em; color: #8b949e; margin-top: 8px; margin-bottom: 0;"><b>Phase 3:</b> Responsive HUD State & Drag Contexts</p>
      </div>
    </div>
  </div>

  <div style="background: #161b22; padding: 18px; border-radius: 8px; border-left: 5px solid #a5472d; margin-bottom: 25px; color: #f0f6fc;">
    <div style="display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 5px; margin-bottom: 10px;">
      <b style="color: #ffffff; font-size: 1.1em;">Advanced Economy Mechanics (Forge & Armory)</b>
      <span style="font-size: 0.75em; background: #21262d; border: 1px solid #30363d; padding: 3px 8px; border-radius: 20px; color: #8b949e; font-weight: bold;">Data Structures / Math Logic</span>
    </div>
    
    <div style="display: grid; grid-template-columns: 1fr; gap: 15px;">
      <div>
        <ul style="margin: 0; padding-left: 20px; line-height: 1.6; color: #c9d1d9;">
          <li><b>Modular Optimization:</b> Programmed a highly decoupled <i>Inventory Component</i> separating item processing into a light, flat replication struct data block (`FItemData`) inside a single `UItemObject` interface shell to protect network limits.</li>
          <li><b>Cross-Item Forging Logic:</b> Created an algebraic upgrading suite handling dual-input asset compression that handles custom rarity distributions using secure, server-side weighted tables.</li>
          <li><b>Secure Transaction Loop:</b> Enforced strict server validation across all Armory global vendor shops, protecting inventory state changes and bulk item clearances.</li>
          <li><b>QoL Algorithms:</b> Wrote item parsing automation enabling one-click optimal "Auto-Equip" sweeps alongside an unexamined inventory tracker engine.</li>
        </ul>
      </div>
      
      <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(340px, 1fr)); gap: 15px; margin-top: 5px;">
        <div style="background: #0d1117; border: 1px solid #30363d; border-radius: 6px; padding: 12px; display: flex; flex-direction: column; justify-content: space-between;">
          <div>
            <b style="color: #ffffff; font-size: 0.95em; display: block; margin-bottom: 4px;">Optimized Memory Layout</b>
            <p style="font-size: 0.85em; color: #8b949e; line-height: 1.4; margin-bottom: 12px;">
              By separating the lightweight primitive data array matrix (`FItemData`) from the higher-level network-supported wrapper (`UItemObject`), the architecture minimizes RPC signature size during bulk trades.
            </p>
          </div>
          <div style="text-align: center; background: #161b22; padding: 6px; border-radius: 4px; border: 1px solid #21262d;">
            <img src="ItemObject.PNG" alt="Replicated Struct and UItemObject" loading="lazy" onclick="zoomImage(this)" style="max-width: 100%; max-height: 220px; width: auto; height: auto; object-fit: contain; border-radius: 4px; cursor: zoom-in; transition: transform 0.2s;" onmouseover="this.style.transform='scale(1.01)'" onmouseout="this.style.transform='scale(1)'">
            <span style="font-size: 0.75em; color: #da765b; display: block; margin-top: 6px; font-weight: bold;">🔍 Click to expand</span>
          </div>
        </div>

        <div style="background: #0d1117; border: 1px solid #30363d; border-radius: 6px; padding: 12px; display: flex; flex-direction: column; justify-content: space-between;">
          <div>
            <b style="color: #ffffff; font-size: 0.95em; display: block; margin-bottom: 4px;">Server-Side Probability Math</b>
            <p style="font-size: 0.85em; color: #8b949e; line-height: 1.4; margin-bottom: 12px;">
              The item combination system compresses dual items down to singular upward-tier elements. All logic resolves deterministically via random probability weighting algorithms locked behind authority barriers.
            </p>
          </div>
          <div style="text-align: center; background: #161b22; padding: 6px; border-radius: 4px; border: 1px solid #21262d;">
            <img src="ForgeCalculation.PNG" alt="Forge Fusion" loading="lazy" onclick="zoomImage(this)" style="max-width: 100%; max-height: 220px; width: auto; height: auto; object-fit: contain; border-radius: 4px; cursor: zoom-in;" onerror="this.style.display='none'">
            <span style="font-size: 0.75em; color: #da765b; display: block; margin-top: 6px; font-weight: bold;">🔍 Click to expand</span>
          </div>
        </div>
      </div>
    </div>
  </div>

  <div style="background: #161b22; padding: 18px; border-radius: 8px; border-left: 5px solid #a5472d; margin-bottom: 25px; color: #f0f6fc;">
    <div style="display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 5px; margin-bottom: 10px;">
      <b style="color: #ffffff; font-size: 1.1em;">Boss AI & Networked Encounter Design (Hades)</b>
      <span style="font-size: 0.75em; background: #21262d; border: 1px solid #30363d; padding: 3px 8px; border-radius: 20px; color: #8b949e; font-weight: bold;">AI Behavior / Gameplay Scripting</span>
    </div>
    
    <div style="display: grid; grid-template-columns: 1fr; gap: 15px;">
      <div>
        <ul style="margin: 0; padding-left: 20px; line-height: 1.6; color: #c9d1d9;">
          <li><b>Multi-Phase State Machinery:</b> Programmed the complex, multi-tiered Hades encounter sequencing behaviors, custom animation blends, and phase transition logic.</li>
          <li><b>Network Prediction Meshes:</b> Engineered an original approach generating synchronized visual telegraph projections locally across clients instantly, keeping gameplay tight under latency.</li>
          <li><b>Adaptive Combat Scaling:</b> Constructed real-time algorithmic triggers adapting sweep speeds, rotation frequencies, and projectile volume attributes tied directly to lobby-wide chosen difficulty settings.</li>
          <li><b>Cinematic Integrations:</b> Synchronized camera blends linking cinematic entryways directly into actionable combat frames to organically telegraph impending mechanical threats.</li>
        </ul>
      </div>
    </div>
  </div>

  <h3 style="margin-top: 30px; margin-bottom: 5px; color: #ffffff; font-size: 1.3em;">Technical Post-Mortem</h3>
  <div style="width: 100%; height: 2px; background: linear-gradient(90deg, transparent 0%, #bd4c2a 50%, transparent 100%); margin: 10px 0 25px 0; opacity: 0.7;"></div>

  <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 15px; margin-bottom: 15px;">
    <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #bd4c2a;">
      <b style="color: #ffffff;">The Challenge: Network Synchronization</b>
      <p style="margin-top: 5px; margin-bottom: 0; font-size: 0.9em; line-height: 1.5; color: #c9d1d9;">
        Architecting a 4-player co-op Musou game introduced severe replication challenges. Systems that performed flawlessly in standalone environments suffered from client-side race conditions and severe tracking variance during high-density enemy swarms.
      </p>
    </div>
    <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #28a745;">
      <b style="color: #ffffff;">The Resolution: Server-sided Logic</b>
      <p style="margin-top: 5px; margin-bottom: 0; font-size: 0.9em; line-height: 1.5; color: #c9d1d9;">
        Enforced strict server-sided logic. Implemented networking for vital systems (loot states, spell tracking) and decoupled local client-side UI visual execution completely from back-end replicated states to secure stability.
      </p>
    </div>
  </div>
  
  <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #4285F4; margin-bottom: 20px;">
    <b style="color: #ffffff;">Architectural Blueprint & Deliverables</b>
    <p style="margin-top: 5px; margin-bottom: 0; font-size: 0.9em; line-height: 1.5; color: #c9d1d9;">
      In future multiplayer titles, I adopt a network-first prototyping rule. No gameplay component profile is built in isolation; systems are integrated with replication parameters and network emulation layers from day one to neutralize latency margins.
    </p>
  </div>
</div>

<div id="tower-defense" class="portfolio-tab" style="display: none;">
<div style="display: flex; justify-content: space-between; align-items: center;">
  <!-- Left Side: Title Badge + C++ Logo -->
  <div style="display: flex; align-items: center; gap: 8px;">
    <img src="https://img.shields.io/badge/Tower%20Defense-a5472d?style=for-the-badge" height="35" alt="Tower Defense"/>
    <img src="https://skillicons.dev/icons?i=cpp" height="30" style="display: block;" alt="C++" />
  </div>
  
  <!-- Right Side: Year/Date Badge -->
  <img src="https://img.shields.io/badge/Dec%202024-333333?style=for-the-badge" height="35" alt="Dec 2024"/>
</div>
  
  <div style="display: flex; justify-content: space-between; margin-top: 12px; padding-bottom: 4px; flex-wrap: wrap; gap: 5px;">
    <b style="color: #f0f6fc; font-size: 1.1em;">2D Tile-Based Strategy TD</b>
    <b style="color: #da765b; font-size: 1.1em;">Solo Developer</b>
  </div>
  
  <div style="background: #161b22; padding: 12px; border-radius: 8px; border-left: 5px solid #a5472d; margin-bottom: 15px; margin-top: 15px; color: #f0f6fc;">
    A technical exercise in engine-level programming, built from the ground up using C++ and OpenGL. The project focused on efficient spatial partitioning and real-time path manipulation within a custom rendering pipeline.
  </div>
  <div align="center" style="margin: 25px 0;">
    <div style="position: relative; width: 100%; max-width: 850px; aspect-ratio: 16 / 9; border-radius: 12px; border: 2px solid #a5472d; box-shadow: 0px 0px 20px rgba(165, 71, 45, 0.2); overflow: hidden;">
      <iframe 
        src="https://www.youtube.com/embed/cCLGPVTF1Aw?autoplay=1&mute=1&loop=1&playlist=cCLGPVTF1Aw&controls=1&modestbranding=1&rel=0" 
        title="Tower Defense Gameplay"
        loading="lazy"
        style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: none;"
        allow="autoplay; encrypted-media; picture-in-picture" 
        allowfullscreen>
      </iframe>
    </div>
  </div>

  <h3 style="margin-bottom: 5px; color: #ffffff;">Core Contributions</h3>
  <div style="width: 100%; height: 2px; background: linear-gradient(90deg, transparent 0%, #bd4c2a 50%, transparent 100%); margin: 15px 0 25px 0; opacity: 0.7;"></div>

  <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #a5472d; margin-bottom: 12px; color: #f0f6fc;">
    <b style="color: #ffffff;">Custom OpenGL Engine & Y-Sorting</b>
    <ul style="margin-top: 5px; margin-bottom: 0; padding-left: 20px;">
      <li><b>Developed</b> a lightweight 2D rendering engine from the ground up using Modern C++ and OpenGL.</li>
      <li><b>Implemented</b> a dynamic Top-Down Depth Sorting (Y-sorting) system to manage draw call ordering.</li>
      <li><b>Optimized</b> visual layering to ensure foreground structures naturally overlap background entities.</li>
    </ul>
  </div>

  <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #a5472d; margin-bottom: 12px; color: #f0f6fc;">
    <b style="color: #ffffff;">Dynamic Pathfinding</b>
    <ul style="margin-top: 5px; margin-bottom: 0; padding-left: 20px;">
      <li><b>Engineered</b> a tile-based grid system utilizing the A* Search Algorithm for enemy navigation.</li>
      <li><b>Implemented</b> real-time path recalculation, allowing AI to adapt instantly as players place walls.</li>
      <li><b>Integrated</b> validation logic to ensure a valid path to the objective is maintained at all times.</li>
    </ul>
  </div>

  <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #a5472d; margin-bottom: 12px; color: #f0f6fc;">
    <b style="color: #ffffff;">Tower Mechanics & Evolution</b>
    <ul style="margin-top: 5px; margin-bottom: 0; padding-left: 20px;">
      <li><b>Created</b> a hover-state system for real-time range visualization and player feedback.</li>
      <li><b>Built</b> a kill-based progression system that triggers dynamic stat scaling for towers.</li>
      <li><b>Programmed</b> visual transformations via automated sprite swaps to reflect tower "level up" states.</li>
    </ul>
  </div>

  <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #a5472d; margin-bottom: 12px; color: #f0f6fc;">
    <b style="color: #ffffff;">Grid & Placement Logic</b>
    <ul style="margin-top: 5px; margin-bottom: 0; padding-left: 20px;">
      <li><b>Developed</b> a robust snapping and validation system for tile-based structure placement.</li>
      <li><b>Architected</b> interaction logic between player-built obstacles and the underlying navigation mesh.</li>
      <li><b>Managed</b> collision detection to ensure accurate interactions with enemy hitboxes.</li>
    </ul>
  </div>
  <h3 style="margin-top: 30px; margin-bottom: 5px; color: #ffffff;">Technical Post-Mortem</h3>
  <div style="width: 100%; height: 2px; background: linear-gradient(90deg, transparent 0%, #bd4c2a 50%, transparent 100%); margin: 15px 0 25px 0; opacity: 0.7;"></div>

  <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 15px; margin-bottom: 20px;">
    <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #bd4c2a;">
      <b style="color: #ffffff;">The Challenge: Math Shaders & Pathing Depth</b>
      <p style="margin-top: 5px; margin-bottom: 0; font-size: 0.95em; line-height: 1.5; color: #c9d1d9;">
        Building an engine from scratch meant handling raw matrices. I encountered geometric complications getting vertex shaders to accurately rotate projectiles toward target headings, alongside performance bottlenecks when multiple active entities computed A* path calculations on a mutable grid simultaneously.
      </p>
    </div>
    <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #28a745;">
      <b style="color: #ffffff;">The Resolution: Matrix Transforms & Caching</b>
      <p style="margin-top: 5px; margin-bottom: 0; font-size: 0.95em; line-height: 1.5; color: #c9d1d9;">
        Resolved sprite transformation defects by normalizing directional vectors and feeding precise arctangent orientations directly into the shader pipeline. Optimized navigation data by caching computed paths, only forcing an A* re-evaluation when structural map changes invalidated the current grid node layout.
      </p>
    </div>
  </div>
  <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #4285F4; margin-bottom: 10px;">
    <b style="color: #ffffff;">Future Approach & Architectural Evolution</b>
    <p style="margin-top: 5px; margin-bottom: 0; font-size: 0.95em; line-height: 1.5; color: #c9d1d9;">
      To maximize lower-level execution efficiency, I would swap out standard pathfinding references for a <b>Flow Field / Vector Field navigation model</b>. This would allow an infinite number of swarm entities to share a single directional vector grid, completely eliminating per-unit CPU overhead.
    </p>
  </div>
</div>

<div id="darkside" class="portfolio-tab" style="display: none;">
<div style="display: flex; justify-content: space-between; align-items: center;">

  <div style="display: flex; align-items: center; gap: 8px;">
    <img src="https://img.shields.io/badge/Your%20Dark%20Side-a5472d?style=for-the-badge" height="35" alt="Your Dark Side"/>
    <img src="https://skillicons.dev/icons?i=java&theme=dark" height="30" style="display: block;" alt="Java" />
  </div>
  
  <img src="https://img.shields.io/badge/2023-333333?style=for-the-badge" height="35" alt="2023"/>
</div>
  <div style="display: flex; justify-content: space-between; margin-top: 12px; padding-bottom: 4px; flex-wrap: wrap; gap: 5px;">
    <b style="color: #f0f6fc; font-size: 1.1em;">2D Tile-Based Fantasy RPG</b>
    <b style="color: #da765b; font-size: 1.1em;">Solo Developer</b>
  </div>
  <div style="background: #161b22; padding: 12px; border-radius: 8px; border-left: 5px solid #a5472d; margin-bottom: 15px; margin-top: 15px; color: #f0f6fc;">
    Built entirely from the ground up in Java, Your Dark Side represents my final major project before transitioning into formal game development studies. Driven by pure passion and self-teaching, it served as a technical playground for implementing the core pillars of the RPG genre—including complex state management, A* pathfinding, and integrated merchant economies.
  </div>
  <div align="center" style="margin: 25px 0;">
    <div style="position: relative; width: 100%; max-width: 850px; aspect-ratio: 16 / 9; border-radius: 12px; border: 2px solid #a5472d; box-shadow: 0px 0px 20px rgba(165, 71, 45, 0.2); overflow: hidden;">
      <iframe 
        src="https://www.youtube.com/embed/8z6vDdhrYUA?autoplay=1&mute=1&loop=1&playlist=8z6vDdhrYUA&controls=1&modestbranding=1&rel=0" 
        title="Your Dark Side Gameplay"
        loading="lazy"
        style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: none;"
        allow="autoplay; encrypted-media; picture-in-picture" 
        allowfullscreen>
      </iframe>
    </div>
  </div>

  <h3 style="margin-bottom: 5px; color: #ffffff;">Core Contributions</h3>
  <div style="width: 100%; height: 2px; background: linear-gradient(90deg, transparent 0%, #bd4c2a 50%, transparent 100%); margin: 15px 0 25px 0; opacity: 0.7;"></div>

  <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #a5472d; margin-bottom: 12px; color: #f0f6fc;">
    <b style="color: #ffffff;">Modular Class Framework</b>
    <ul style="margin-top: 5px; margin-bottom: 0; padding-left: 20px;">
      <li><b>Engineered</b> a multi-class selection system as the foundation for character state management.</li>
      <li><b>Implemented</b> attribute scaling logic to handle unique progression paths for different classes.</li>
    </ul>
  </div>

  <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #a5472d; margin-bottom: 12px; color: #f0f6fc;">
    <b style="color: #ffffff;">Inventory & Economy Logic</b>
    <ul style="margin-top: 5px; margin-bottom: 0; padding-left: 20px;">
      <li><b>Developed</b> a robust inventory system and NPC interaction framework for merchant economies.</li>
      <li><b>Programmed</b> complex item valuation and transactional logic for buying/selling mechanics.</li>
    </ul>
  </div>

  <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #a5472d; margin-bottom: 12px; color: #f0f6fc;">
    <b style="color: #ffffff;">A* Pathfinding Implementation</b>
    <ul style="margin-top: 5px; margin-bottom: 0; padding-left: 20px;">
      <li><b>Integrated</b> advanced A* pathfinding algorithms to ensure intelligent enemy AI navigation.</li>
      <li><b>Optimized</b> path calculation for complex, tile-based fantasy environments.</li>
    </ul>
  </div>

  <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #a5472d; margin-bottom: 12px; color: #f0f6fc;">
    <b style="color: #ffffff;">Spell Framework & Minimap</b>
    <ul style="margin-top: 5px; margin-bottom: 0; padding-left: 20px;">
      <li><b>Designed</b> an extensible spell architecture for easy integration of new combat mechanics and effects.</li>
      <li><b>Developed</b> a real-time minimap system featuring entity tracking and dynamic zoom capabilities.</li>
    </ul>
  </div>
  <h3 style="margin-top: 30px; margin-bottom: 5px; color: #ffffff;">Technical Post-Mortem</h3>
  <div style="width: 100%; height: 2px; background: linear-gradient(90deg, transparent 0%, #bd4c2a 50%, transparent 100%); margin: 15px 0 25px 0; opacity: 0.7;"></div>

  <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 15px; margin-bottom: 20px;">
    <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #bd4c2a;">
      <b style="color: #ffffff;">The Challenge: The Scope Creep Trap</b>
      <p style="margin-top: 5px; margin-bottom: 0; font-size: 0.95em; line-height: 1.5; color: #c9d1d9;">
        As an early project, the initial vision over-scoped heavily on content scale. Trying to build multiple sweeping features simultaneously without a concrete framework threatened to leave the project completely unplayable and fractured.
      </p>
    </div>
    <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #28a745;">
      <b style="color: #ffffff;">The Resolution: Pivoting to System Foundations</b>
      <p style="margin-top: 5px; margin-bottom: 0; font-size: 0.95em; line-height: 1.5; color: #c9d1d9;">
        Halted wide-scale asset development and shifted focus to isolating core modular data. Successfully targeted and polished the underlying mechanics: creating an extensible inventory loop, working out class selection persistence, and stabilizing the mathematical equations governing RPG stat scaling.
      </p>
    </div>
  </div>
  <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #4285F4; margin-bottom: 10px;">
    <b style="color: #ffffff;">Future Approach & Architectural Evolution</b>
    <p style="margin-top: 5px; margin-bottom: 0; font-size: 0.95em; line-height: 1.5; color: #c9d1d9;">
      This project taught me the vital importance of producing a **Minimum Viable Product (MVP)**. I would now implement a strict milestone pipeline, ensuring the core transactional loop and gameplay states are rock-solid before mapping out extensive horizontal mechanics or game content blocks.
    </p>
  </div>
</div>

<div id="dungeon" class="portfolio-tab" style="display: none;">
<div style="display: flex; justify-content: space-between; align-items: center;">
  <!-- Left Side: Title Badge + Python Logo -->
  <div style="display: flex; align-items: center; gap: 8px;">
    <img src="https://img.shields.io/badge/Dungeon%20Crawler-a5472d?style=for-the-badge" height="35" alt="Dungeon Crawler"/>
    <img src="https://skillicons.dev/icons?i=python" height="30" style="display: block;" alt="Python" />
  </div>
  
  <!-- Right Side: Year Badge -->
  <img src="https://img.shields.io/badge/2017-333333?style=for-the-badge" height="35" alt="2017"/>
</div>
  <div style="display: flex; justify-content: space-between; margin-top: 12px; padding-bottom: 4px; flex-wrap: wrap; gap: 5px;">
    <b style="color: #f0f6fc; font-size: 1.1em;">2D Dungeon Crawler RPG</b>
    <b style="color: #da765b; font-size: 1.1em;">Solo Developer</b>
  </div>
  <div style="background: #161b22; padding: 12px; border-radius: 8px; border-left: 5px solid #a5472d; margin-bottom: 15px; margin-top: 15px; color: #f0f6fc;">
    This project represents my first deep dive into the RPG genre and complex system architecture. Developed entirely on an iPad, this was an ambitious leap from previous work, driven by a passion for dungeon crawlers. It stands as a milestone where I successfully implemented interlocking systems like inventory management, class-based stats, and enemy AI.
  </div>
  <div align="center" style="margin: 25px 0;">
    <div style="position: relative; width: 100%; max-width: 850px; aspect-ratio: 16 / 9; border-radius: 12px; border: 2px solid #a5472d; box-shadow: 0px 0px 20px rgba(165, 71, 45, 0.2); overflow: hidden;">
      <iframe 
        src="https://www.youtube.com/embed/HNQjJI9nPDQ?autoplay=1&mute=1&loop=1&playlist=HNQjJI9nPDQ&controls=1&modestbranding=1&rel=0" 
        title="Dungeon Crawler Gameplay"
        loading="lazy"
        style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: none;"
        allow="autoplay; encrypted-media; picture-in-picture" 
        allowfullscreen>
      </iframe>
    </div>
  </div>

  <h3 style="margin-bottom: 5px; color: #ffffff;">Core Contributions</h3>
  <div style="width: 100%; height: 2px; background: linear-gradient(90deg, transparent 0%, #bd4c2a 50%, transparent 100%); margin: 15px 0 25px 0; opacity: 0.7;"></div>

  <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #a5472d; margin-bottom: 12px; color: #f0f6fc;">
    <b style="color: #ffffff;">RPG Systems Architecture</b>
    <ul style="margin-top: 5px; margin-bottom: 0; padding-left: 20px;">
      <li><b>Designed</b> a multi-class selection system featuring 8 unique character classes.</li>
      <li><b>Implemented</b> discrete starting attribute sets to differentiate class-based gameplay.</li>
    </ul>
  </div>

  <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #a5472d; margin-bottom: 12px; color: #f0f6fc;">
    <b style="color: #ffffff;">Combat & Enemy AI</b>
    <ul style="margin-top: 5px; margin-bottom: 0; padding-left: 20px;">
      <li><b>Developed</b> a real-time combat engine supporting 8-directional movement and hit detection.</li>
      <li><b>Programmed</b> enemy homing logic to dynamically track and engage the player.</li>
    </ul>
  </div>

  <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #a5472d; margin-bottom: 12px; color: #f0f6fc;">
    <b style="color: #ffffff;">Loot & Progression Logic</b>
    <ul style="margin-top: 5px; margin-bottom: 0; padding-left: 20px;">
      <li><b>Scripted</b> a dynamic reward system that triggers randomized XP, gold, and item drops upon enemy defeat.</li>
      <li><b>Engineered</b> a persistent inventory and leveling framework to track character progression.</li>
    </ul>
  </div>

  <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #a5472d; margin-bottom: 12px; color: #f0f6fc;">
    <b style="color: #ffffff;">UI/UX Prototyping</b>
    <ul style="margin-top: 5px; margin-bottom: 0; padding-left: 20px;">
      <li><b>Architected</b> a multi-scene menu flow, including dungeon selection and inventory management interfaces.</li>
      <li><b>Integrated</b> functional UI elements to bridge technical systems with user feedback.</li>
    </ul>
  </div>
  <h3 style="margin-top: 30px; margin-bottom: 5px; color: #ffffff;">Technical Post-Mortem</h3>
  <div style="width: 100%; height: 2px; background: linear-gradient(90deg, transparent 0%, #bd4c2a 50%, transparent 100%); margin: 15px 0 25px 0; opacity: 0.7;"></div>

  <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 15px; margin-bottom: 20px;">
    <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #bd4c2a;">
      <b style="color: #ffffff;">The Challenge: Platform Limits & Over-scoping</b>
      <p style="margin-top: 5px; margin-bottom: 0; font-size: 0.95em; line-height: 1.5; color: #c9d1d9;">
        Attempting a sprawling, feature-heavy classic RPG while coding entirely on an iPad environment led to immediate scope management and technical hurdles. The feature set grew faster than the architectural framework could support.
      </p>
    </div>
    <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #28a745;">
      <b style="color: #ffffff;">The Resolution: Mechanics-First Isolation</b>
      <p style="margin-top: 5px; margin-bottom: 0; font-size: 0.95em; line-height: 1.5; color: #c9d1d9;">
        Stripped out secondary systemic systems to safeguard production. Focused purely on establishing working architectural baselines: locking down the database structures for player inventories, debugging enemy AI detection states, and deploying a functional numerical prototype.
      </p>
    </div>
  </div>
  <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #4285F4; margin-bottom: 10px;">
    <b style="color: #ffffff;">Future Approach & Architectural Evolution</b>
    <p style="margin-top: 5px; margin-bottom: 0; font-size: 0.95em; line-height: 1.5; color: #c9d1d9;">
      This project served as my early wake-up call regarding design constraints. Today, I approach pre-production by establishing a formal **Technical Design Document (TDD)**, using functional mockups to isolate systemic bottlenecks and protect scope limits before writing execution code.
    </p>
  </div>
</div>

<div id="hit-run" class="portfolio-tab" style="display: none;">
<div style="display: flex; justify-content: space-between; align-items: center;">
  <!-- Left Side: Title Badge + Python Logo -->
  <div style="display: flex; align-items: center; gap: 8px;">
    <img src="https://img.shields.io/badge/Hit%20%26%20Run-a5472d?style=for-the-badge" height="35" alt="Hit & Run"/>
    <img src="https://skillicons.dev/icons?i=python" height="30" style="display: block;" alt="Python" />
  </div>
  
  <!-- Right Side: Year Badge -->
  <img src="https://img.shields.io/badge/2016-333333?style=for-the-badge" height="35" alt="2016"/>
</div>
  <div style="display: flex; justify-content: space-between; margin-top: 12px; padding-bottom: 4px; flex-wrap: wrap; gap: 5px;">
    <b style="color: #f0f6fc; font-size: 1.1em;">2D Endless Survival</b>
    <b style="color: #da765b; font-size: 1.1em;">Solo Developer</b>
  </div>
  <div style="background: #161b22; padding: 12px; border-radius: 8px; border-left: 5px solid #a5472d; margin-bottom: 15px; margin-top: 15px; color: #f0f6fc;">
    As my first step into game development, Hit & Run was a crucial layout experiment parsing 2D hit detection logic and continuous speed scaling.
  </div>
  <div align="center" style="margin: 25px 0;">
    <div style="position: relative; width: 100%; max-width: 850px; aspect-ratio: 16 / 9; border-radius: 12px; border: 2px solid #a5472d; box-shadow: 0px 0px 20px rgba(165, 71, 45, 0.2); overflow: hidden;">
      <iframe 
        src="https://www.youtube.com/embed/FSjgXKFcKIo?autoplay=1&mute=1&loop=1&playlist=FSjgXKFcKIo&controls=1&modestbranding=1&rel=0" 
        title="Hit & Run Gameplay"
        loading="lazy"
        style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: none;"
        allow="autoplay; encrypted-media; picture-in-picture" 
        allowfullscreen>
      </iframe>
    </div>
  </div>
<h3 style="margin-bottom: 5px; color: #ffffff;">Core Contributions</h3>
  <div style="width: 100%; height: 2px; background: linear-gradient(90deg, transparent 0%, #bd4c2a 50%, transparent 100%); margin: 15px 0 25px 0; opacity: 0.7;"></div>
  <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #a5472d; margin-bottom: 12px; color: #f0f6fc;">
    <b style="color: #ffffff;">Progression Economy & Multi-Currency Shops</b>
    <ul style="margin-top: 5px; margin-bottom: 0; padding-left: 20px;">
      <li><b>Engineered</b> an integrated economy system featuring a Stat Shop and a Spell Shop for mid-run power scaling.</li>
      <li><b>Implemented</b> transactional logic for purchasing new magical abilities and upgrading multi-tier spell profiles.</li>
      <li><b>Programmed</b> attribute modification systems that dynamically recalculate core player stats, including Haste (attack speed), Armor (flat flat damage reduction), and Dodge (percentage-based avoidance).</li>
    </ul>
  </div>

  <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #a5472d; margin-bottom: 12px; color: #f0f6fc;">
    <b style="color: #ffffff;">Resource Management & Spell Architecture</b>
    <ul style="margin-top: 5px; margin-bottom: 0; padding-left: 20px;">
      <li><b>Developed</b> a dynamic Mana resource loop to regulate spell casting, complete with passive regeneration states and casting thresholds.</li>
      <li><b>Designed</b> an extensible framework for diverse spell behaviors, linking ability cooldowns, area-of-effect parameters, and damage logic directly to player stats.</li>
    </ul>
  </div>

  <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #a5472d; margin-bottom: 12px; color: #f0f6fc;">
    <b style="color: #ffffff;">Round-Based Enemy Scaling & Swarm AI</b>
    <ul style="margin-top: 5px; margin-bottom: 0; padding-left: 20px;">
      <li><b>Architected</b> a round-based survival system with automated wave progression and escalating difficulty curves.</li>
      <li><b>Scripted</b> dynamic AI spawning algorithms that increase enemy crowd density, scale base movement speed, and augment health pools as rounds progress to create intense "swarm" scenarios.</li>
      <li><b>Optimized</b> 2D collision handling to smoothly process a high volume of simultaneous enemy hitboxes overlapping the player viewport.</li>
    </ul>
  </div>
  <h3 style="margin-top: 30px; margin-bottom: 5px; color: #ffffff;">Technical Post-Mortem</h3>
  <div style="width: 100%; height: 2px; background: linear-gradient(90deg, transparent 0%, #bd4c2a 50%, transparent 100%); margin: 15px 0 25px 0; opacity: 0.7;"></div>

  <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 15px; margin-bottom: 20px;">
    <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #bd4c2a;">
      <b style="color: #ffffff;">The Challenge: Coordinate & Rendering Failures</b>
      <p style="margin-top: 5px; margin-bottom: 0; font-size: 0.95em; line-height: 1.5; color: #c9d1d9;">
        The prototype was initially structured around a traditional side-scrolling engine with a moving ground plane. This architecture generated persistent visual artifacting, tracking tearing, and logic bugs where collision boundaries routinely misaligned during high-velocity updates.
      </p>
    </div>
    <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #28a745;">
      <b style="color: #ffffff;">The Resolution: Clever Paradigm Reversal</b>
      <p style="margin-top: 5px; margin-bottom: 0; font-size: 0.95em; line-height: 1.5; color: #c9d1d9;">
        Instead of getting bogged down in cosmetic background scrolling, I flipped the layout vector. I clamped the player viewport to a clean, stationary backdrop and transferred the kinetic motion logic directly onto the incoming enemy swarm objects—preserving the intended gameplay feel while erasing the bugs.
      </p>
    </div>
  </div>
  <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #4285F4; margin-bottom: 10px;">
    <b style="color: #ffffff;">Future Approach & Architectural Evolution</b>
    <p style="margin-top: 5px; margin-bottom: 0; font-size: 0.95em; line-height: 1.5; color: #c9d1d9;">
      This taught me that player perception dictates mechanical design. Knowing what I know now about rendering loops, I would solve the original problem by running a <b>parallax texture shader offset</b> on a single static quad mesh, giving the perfect optical illusion of distance travel at zero performance or collision cost.
    </p>
  </div>
</div>

<script>
function switchTab(event, tabId) {
  // Hide all active tab containers safely
  var tabs = document.getElementsByClassName("portfolio-tab");
  for (var i = 0; i < tabs.length; i++) {
    tabs[i].style.display = "none";
    tabs[i].classList.remove("active-content");
  }
  
  // Clear the active class flag from all layout buttons
  var buttons = document.getElementsByClassName("tab-btn");
  for (var j = 0; j < buttons.length; j++) {
    buttons[j].classList.remove("active-tab");
  }
  
  // Show target selection layout and activate target button item
  var targetTab = document.getElementById(tabId);
  if (targetTab) {
    targetTab.style.display = "block";
    targetTab.classList.add("active-content");
  }
  
  if (event && event.currentTarget) {
    event.currentTarget.classList.add("active-tab");
  }
}
</script>

<script>
  const canvas = document.getElementById('particle-canvas');
  const ctx = canvas.getContext('2d');

  let particlesArray = [];
  const numberOfParticles = 45; // Keeps it clean and optimized

  // Set sizing
  function setCanvasSize() {
    canvas.width = window.innerWidth;
    canvas.height = window.innerHeight;
  }
  setCanvasSize();
  window.addEventListener('resize', setCanvasSize);
</script>
