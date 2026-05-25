<style>
  /* Hard override for the entire viewport background */
  html, body {
    background-color: #0d1117 !important;
    background: #0d1117 !important;
    color: #f0f6fc !important;
  }
  
  /* Hard override for Jekyll's layout container */
  .wrapper {
    background-color: #0d1117 !important;
    background: #0d1117 !important;
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
    background-color: #0d1117 !important;
    background: #0d1117 !important;
    width: 100% !important;
    max-width: 900px !important;
    float: none !important;
    padding: 0 !important;
  }

  header {
    display: none !important;
  }

  /* Center alignment layout for the portfolio tabs */
  .tab-container {
    display: flex !important;
    justify-content: center !important;
    gap: 10px !important;
    margin: 20px 0 !important;
    flex-wrap: wrap !important;
    background-color: transparent !important;
  }

  .tab-btn {
    background-color: #161b22 !important;
    color: #c9d1d9 !important;
    border: 1px solid #30363d !important;
    padding: 8px 16px !important;
    font-size: 0.95em !important;
    font-weight: bold !important;
    border-radius: 6px !important;
    cursor: pointer !important;
    transition: all 0.2s ease !important;
    text-decoration: none !important;
  }

  .tab-btn:hover {
    border-color: #a5472d !important;
    background-color: #1f242c !important;
    color: #ffffff !important;
  }

  .tab-btn.active-tab {
    background-color: #a5472d !important;
    color: #ffffff !important;
    border-color: #a5472d !important;
    box-shadow: 0px 0px 10px rgba(165, 71, 45, 0.4) !important;
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
</style>

<a name="top"></a>
<div align="center">
<h1 style="font-size: 3em; margin-bottom: 0px; color: #ffffff !important; opacity: 1 !important;">Tristan Anglin</h1>
<p style="font-size: 1.2em; margin-top: 15px; color: #ffffff !important; opacity: 1 !important; background: transparent !important;">
  <strong style="color: #ffffff !important; opacity: 1 !important;">Game Developer | Systems Architect & UI Designer</strong>
</p>
</div>

<p align="center">
  <a href="https://tristananglin.github.io/Tristan Anglin FULL 2026.pdf" target="_blank"><img src="https://img.shields.io/badge/RESUME-28a745?style=for-the-badge&logo=googledocs&logoColor=white" height="30" /></a>&nbsp;
  <a href="https://linkedin.com/in/TristanAnglin" target="_blank"><img src="https://img.shields.io/badge/linkedin-0077B5?style=for-the-badge&logo=LINKEDIN&logoColor=white" height="30" /></a>&nbsp;
  <a href="mailto:tmanglin00@gmail.com"><img src="https://img.shields.io/badge/EMAIL-4285F4?style=for-the-badge&logo=gmail&logoColor=white" height="30" /></a>
  <br />
  <a href="https://github.com/TristanAnglin" target="_blank"><img src="https://img.shields.io/badge/GITHUB-333333?style=for-the-badge&logo=github&logoColor=white" height="30" /></a>&nbsp;
  <a href="https://www.instagram.com/tristananglin_" target="_blank"><img src="https://img.shields.io/badge/INSTAGRAM-833AB4?style=for-the-badge&logo=instagram&logoColor=white" height="30" /></a>&nbsp;
  <a href="https://www.youtube.com/@TristanAnglin" target="_blank"><img src="https://img.shields.io/badge/YOUTUBE-CD201F?style=for-the-badge&logo=youtube&logoColor=white" height="30" /></a>
</p>

<div class="tab-container" style="display: flex; justify-content: center; flex-wrap: wrap; gap: 10px; align-items: stretch;">
  
  <style>
    .tab-btn {
      display: inline-flex !important;
      flex-direction: column !important;
      align-items: center !important;
      justify-content: center !important;
      line-height: 1.2 !important;
      padding: 8px 16px !important;
      min-height: 54px !important;
    }
    .tab-meta {
      font-size: 0.9em;
      opacity: 0.65;
      margin-top: 4px;
      font-weight: normal;
      letter-spacing: 0.5px;
    }
    .active-tab .tab-meta {
      opacity: 0.85;
    }
  </style>

  <button class="tab-btn active-tab" onclick="switchTab(event, 'about-tab')">
    <span>Overview & Skills</span>
    <span class="tab-meta">Core Profile</span>
  </button>
  
  <button class="tab-btn" onclick="switchTab(event, 'blood-lineage')">
    <span>Blood & Lineage</span>
    <span class="tab-meta">2026 • UE5</span>
  </button>
  
  <button class="tab-btn" onclick="switchTab(event, 'tower-defense')">
    <span>Tower Defense</span>
    <span class="tab-meta">2024 • C++</span>
  </button>
  
  <button class="tab-btn" onclick="switchTab(event, 'darkside')">
    <span>Your Dark Side</span>
    <span class="tab-meta">2023 • Java</span>
  </button>
  
  <button class="tab-btn" onclick="switchTab(event, 'dungeon')">
    <span>Dungeon Crawler</span>
    <span class="tab-meta">2017 • Python</span>
  </button>
  
  <button class="tab-btn" onclick="switchTab(event, 'hit-run')">
    <span>Hit & Run</span>
    <span class="tab-meta">2016 • Python</span>
  </button>
</div>

<hr />

<div id="about-tab" class="portfolio-tab active-content" style="display: block;">
  <table border="0" style="width: 100%; border-collapse: collapse; border: none;">
    <tr style="border: none;">
      <td width="55%" valign="top" style="border: none; background: transparent; padding-right: 15px;">
        <div style="background: #161b22; padding: 12px 15px; border-radius: 8px; border-left: 5px solid #a5472d; margin-bottom: 12px; color: #f0f6fc;">
          Growing up in a household with a 300+ board game collection gave me an intuitive grasp of game balance and systems design long before I wrote my first line of code.
        </div>
        <div style="background: #161b22; padding: 12px 15px; border-radius: 8px; border-left: 5px solid #a5472d; margin-bottom: 12px; color: #f0f6fc;">
          My programming journey began in 2016 with Python, but my curiosity quickly outpaced the classroom. This drive led me to self-teach Java to develop "Your Dark Side." I soon realized my true calling was in the technical architecture and creative heart of game design.
        </div>
        <div style="background: #161b22; padding: 12px 15px; border-radius: 8px; border-left: 5px solid #a5472d; margin-bottom: 12px; color: #f0f6fc;">
          Since specializing in Game Development in 2023, I have maintained a 3.86 GPA and dedicated myself to building a portfolio of modular core systems and dynamic user interfaces.
        </div>
      </td>

      <td width="45%" valign="top" align="center" style="border: none; background: transparent; line-height: 1.8;">
        <div style="margin-bottom: 15px;">
          <b style="color: #ffffff;">Programming & Engines</b><br/>
          <img src="https://skillicons.dev/icons?i=cpp&theme=dark" height="40" />
          <img src="https://skillicons.dev/icons?i=cs&theme=dark" height="40" />
          <img src="https://skillicons.dev/icons?i=py&theme=dark" height="40" />
          <img src="https://skillicons.dev/icons?i=java&theme=dark" height="40" />
          <img src="https://skillicons.dev/icons?i=unreal&theme=dark" height="40" />
          <img src="https://skillicons.dev/icons?i=unity&theme=dark" height="40" />
        </div>

        <div style="margin-bottom: 15px;">
          <b style="color: #ffffff;">Workflow & Version Control</b><br/>
          <img src="assets/Icons/JiraIcon.png" height="40" style="vertical-align: middle; border-radius: 5px;" />
          <img src="https://skillicons.dev/icons?i=git&theme=dark" height="40" style="vertical-align: middle;" />
          <img src="https://skillicons.dev/icons?i=mysql&theme=dark" height="40" style="vertical-align: middle;" />
          <img src="https://skillicons.dev/icons?i=nodejs&theme=dark" height="40" style="vertical-align: middle;" />
          <img src="https://skillicons.dev/icons?i=cmake&theme=dark" height="40" style="vertical-align: middle;" />
        </div>

        <div style="margin-bottom: 15px;">
          <b style="color: #ffffff;">Development Environments</b><br/>
          <img src="https://skillicons.dev/icons?i=visualstudio&theme=dark" height="40" />
          <img src="https://skillicons.dev/icons?i=vscode&theme=dark" height="40" />
          <img src="https://skillicons.dev/icons?i=eclipse&theme=dark" height="40" />
        </div>

        <div style="margin-bottom: 15px;">
          <b style="color: #ffffff;">Art, Audio & UI Design</b><br/>
          <img src="assets/Icons/3dsmaxIcon.png" height="40" style="vertical-align: middle; border-radius: 5px;" />
          <img src="https://skillicons.dev/icons?i=blender&theme=dark" height="40" style="vertical-align: middle;" />
          <img src="https://skillicons.dev/icons?i=photoshop&theme=dark" height="40" style="vertical-align: middle;" />
          <img src="https://skillicons.dev/icons?i=illustrator&theme=dark" height="40" style="vertical-align: middle;" />
          <img src="https://skillicons.dev/icons?i=pr&theme=dark" height="40" style="vertical-align: middle;" />
          <img src="https://skillicons.dev/icons?i=au&theme=dark" height="40" style="vertical-align: middle;" />
        </div>
      </td>
    </tr>
  </table>

  <div align="center" style="width: 100%; padding-bottom: 30px; border-top: 1px solid #30363d; padding-top: 25px;">
  
  <img src="myselfLevelup.jpg" alt="Tristan Anglin - Level Up Showcase" style="width: 100%; height: auto; border-radius: 12px; border: 2px solid #a5472d; box-shadow: 0px 0px 15px rgba(165, 71, 45, 0.15);" />
  
</div>
</div>

<div id="blood-lineage" class="portfolio-tab" style="display: none;">
  <div style="display: flex; justify-content: space-between; align-items: center;">
    <img src="https://img.shields.io/badge/Blood%20%26%20Lineage-a5472d?style=for-the-badge&logo=unrealengine&logoColor=white" height="35"/>
    <img src="https://img.shields.io/badge/2026-333333?style=for-the-badge" height="35"/>
  </div>
  <div style="display: flex; justify-content: space-between; margin-top: 8px;">
    <b style="color: #f0f6fc;">3D Co-op Musou RPG</b>
    <b style="color: #f0f6fc;">Lead Systems Architect & UI Programmer</b>
  </div>
  <div style="background: #161b22; padding: 12px; border-radius: 8px; border-left: 5px solid #a5472d; margin-bottom: 15px; margin-top: 15px; color: #f0f6fc;">
    A high-action capstone project developed by an 11-person team. I architected the core gameplay framework and led the development of 20+ interconnected systems, managing the technical roadmap via <b>Jira</b> and <b>GitHub</b> to ensure cross-department stability.
</div>
  <div align="center" style="margin: 25px 0;">
    
    <video 
      src="assets/videos/Blood & Lineage.mp4" 
      autoplay 
      muted 
      loop 
      playsinline
      style="width: 100%; max-width: 850px; aspect-ratio: 16 / 9; border-radius: 12px; border: 2px solid #a5472d; box-shadow: 0px 0px 20px rgba(165, 71, 45, 0.2); object-fit: cover; pointer-events: none;">
    </video>

  </div>

  <h3 style="margin-bottom: 5px; color: #ffffff;">Process:</h3>
  <div style="height: 2px; background: #a5472d; margin-bottom: 20px; border-radius: 2px;"></div>

  <div style="display: grid; grid-template-columns: 1.6fr 1fr; gap: 20px; align-items: start; margin-bottom: 25px;">
    <div style="display: flex; flex-direction: column; gap: 20px;">
      <div style="text-align: center;">
        <img src="InventoryWireframe.png" alt="Step 1" style="width: 100%; border-radius: 8px; border: 1px solid #30363d;">
        <p style="font-size: 0.85em; color: #8b949e; margin-top: 10px;"><b>Step 1:</b> Functional Layout & UX Blockout</p>
      </div>
      <div style="text-align: center;">
        <img src="HUDFinal.PNG" alt="Step 3" style="width: 100%; max-width: 320px; margin: 0 auto; border-radius: 8px; border: 2px solid #a5472d;">
        <p style="font-size: 0.85em; color: #8b949e; margin-top: 10px;"><b>Step 3:</b> Real-time HUD & Feedback Loop</p>
      </div>
    </div>
    <div style="text-align: center;">
      <img src="InventoryFinal.PNG" alt="Step 2" style="max-height: 550px; width: auto; max-width: 100%; border-radius: 8px; border: 2px solid #a5472d;">
      <p style="font-size: 0.85em; color: #8b949e; margin-top: 10px;"><b>Step 2:</b> Final Asset Integration</p>
    </div>
  </div>

  <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #6e7681; margin-bottom: 30px; font-style: italic; font-size: 0.95em; color: #c9d1d9; line-height: 1.5;">
    "My workflow prioritizes systems first. I begin with functional blockouts and networked state before integrating final art assets, custom iconography, and motion graphics."
  </div>

  <h3 style="margin-bottom: 5px; color: #ffffff;">Core Contributions: Blood & Lineage</h3>
  <div style="height: 2px; background: #a5472d; margin-bottom: 20px; border-radius: 2px;"></div>

  <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #a5472d; margin-bottom: 12px; color: #f0f6fc;">
    <b style="color: #ffffff;">Technical Architecture & Networked Framework</b>
    <ul style="margin-top: 5px; margin-bottom: 0; padding-left: 20px;">
      <li><b>Refactored</b> the core engine architecture to a <b>Character/Controller/State</b> model, ensuring clean separation of movement, UI management, and persistent networked data.</li>
      <li><b>Architected</b> a persistent progression system utilizing <b>Seamless Travel</b>, allowing PlayerState data (stats, inventory, meta-progression) to carry over between game zones.</li>
      <li><b>Engineered</b> a Class-Locked Signature Weapon System with dynamic scaling to prevent gameplay soft-locks while maintaining combat viability across difficulty tiers.</li>
      <li><b>Implemented</b> server-authoritative logic for loot rarity, item drops, and currency transactions to ensure synchronized state across all 4 clients.</li>
    </ul>
  </div>

  <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #a5472d; margin-bottom: 12px; color: #f0f6fc;">
    <b style="color: #ffffff;">Full-Stack UI/UX Engineering & Iconography</b>
    <ul style="margin-top: 5px; margin-bottom: 0; padding-left: 20px;">
      <li><b>Developed</b> a comprehensive suite of 20+ networked interfaces, including a 4-player Lobby with real-time updates and a dynamic 3D <b>Preview</b>.</li>
      <li><b>Designed and Vectorized</b> a custom library of 50+ icons for classes, attributes, equipment, and difficulty tiers to establish a cohesive visual identity.</li>
      <li><b>Programmed</b> complex UI logic for the <b>Forge and Armory</b>, including a weighted probability engine for cross-item merging and bulk-sell functionality by rarity tier.</li>
      <li><b>Integrated</b> dynamic HUD feedback, such as real-time mana cost scaling based on Intelligence stats and low-health post-process vignettes.</li>
    </ul>
  </div>

  <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #a5472d; margin-bottom: 12px; color: #f0f6fc;">
    <b style="color: #ffffff;">Boss Encounter Design & AI (Hades)</b>
    <ul style="margin-top: 5px; margin-bottom: 0; padding-left: 20px;">
      <li><b>Architected</b> the multi-phase Hades encounter, managing complex state transitions, multi-spin sweep logic, and fireball barrage sequences.</li>
      <li><b>Engineered</b> a <b>Networked Prediction Mesh</b> system that generates visual telegraphs on all clients before attacks execute, ensuring fair dodge-windows in high-latency environments.</li>
      <li><b>Developed</b> a dynamic difficulty scaling system that adjusts boss damage, attack frequency, and rotation counts based on the global difficulty tier and boss health.</li>
      <li><b>Implemented</b> cinematic-to-gameplay transitions, including an opening sequence that teaches mechanical cues for the "Obelisk Slam" phase.</li>
    </ul>
  </div>

  <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #a5472d; margin-bottom: 12px; color: #f0f6fc;">
    <b style="color: #ffffff;">Advanced Systems & UX Optimization</b>
    <ul style="margin-top: 5px; margin-bottom: 0; padding-left: 20px;">
      <li><b>Created</b> a modular <b>Inventory Actor Component</b> for clean replication of item data via replicated structs, optimizing network bandwidth.</li>
      <li><b>Developed</b> "Quality of Life" systems, including a "New Item" exclamation state that clears on hover and an <b>Auto-Equip</b> algorithm that parses inventory for highest-value stats.</li>
      <li><b>Implemented</b> an interactive, multi-section tutorial scene with custom camera logic to guide new players through complex RPG mechanics.</li>
    </ul>
  </div>

  <h3 style="margin-top: 30px; margin-bottom: 5px; color: #ffffff;">Process & Individual Impact</h3>
  <div style="height: 2px; background: #a5472d; margin-bottom: 20px; border-radius: 2px;"></div>

  <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #a5472d; margin-bottom: 10px; color: #f0f6fc;">
    <b style="color: #ffffff;">Individual Contribution & Leadership</b>
    <p style="margin-top: 5px; margin-bottom: 0; line-height: 1.6;">
      As the Lead Systems Architect, I personally implemented the highest volume of game systems, ranging from the core networking handshake to the final post-game statistics screen. I managed the technical roadmap via <b>Jira</b>, directed the integration of assets from the art department, and led the final sprint to resolve technical debt and ensure launch-day stability for the technology showcase.
    </p>
  </div>
</div>


<div id="tower-defense" class="portfolio-tab" style="display: none;">
  <div style="display: flex; justify-content: space-between; align-items: center;">
    <img src="https://img.shields.io/badge/Tower%20Defense-a5472d?style=for-the-badge&logo=cplusplus&logoColor=white" height="35"/>
    <img src="https://img.shields.io/badge/2024-333333?style=for-the-badge" height="35"/>
  </div>
  <div style="display: flex; justify-content: space-between; margin-top: 8px;">
    <b style="color: #f0f6fc;">2D Tile-Based Strategy TD</b>
    <b style="color: #f0f6fc;">Solo Developer</b>
  </div>
  <div style="background: #161b22; padding: 12px; border-radius: 8px; border-left: 5px solid #a5472d; margin-bottom: 15px; margin-top: 15px; color: #f0f6fc;">
    A technical exercise in engine-level programming, built from the ground up using C++ and OpenGL. The project focused on efficient spatial partitioning and real-time path manipulation within a custom rendering pipeline.
  </div>
  <div align="center" style="margin: 25px 0;">
    <a href="https://youtu.be/cCLGPVTF1Aw" target="_blank" class="video-thumb">
      <img src="https://img.youtube.com/vi/cCLGPVTF1Aw/maxresdefault.jpg" alt="Tower Defense Gameplay" style="width: 100%; max-width: 850px; aspect-ratio: 16 / 9; object-fit: cover; border-radius: 12px; border: 2px solid #a5472d; box-shadow: 0px 0px 20px rgba(165, 71, 45, 0.2);">
    </a>
  </div>

  <h3 style="margin-bottom: 5px; color: #ffffff;">Core Contributions</h3>
  <div style="height: 2px; background: #a5472d; margin-bottom: 20px; border-radius: 2px;"></div>

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
</div>


<div id="darkside" class="portfolio-tab" style="display: none;">
  <div style="display: flex; justify-content: space-between; align-items: center;">
    <img src="https://img.shields.io/badge/Your%20Dark%20Side-a5472d?style=for-the-badge&logo=openjdk&logoColor=white" height="35"/>
    <img src="https://img.shields.io/badge/2023-333333?style=for-the-badge" height="35"/>
  </div>
  <div style="display: flex; justify-content: space-between; margin-top: 8px;">
    <b style="color: #f0f6fc;">2D Tile-Based Fantasy RPG</b>
    <b style="color: #f0f6fc;">Solo Developer</b>
  </div>
  <div style="background: #161b22; padding: 12px; border-radius: 8px; border-left: 5px solid #a5472d; margin-bottom: 15px; margin-top: 15px; color: #f0f6fc;">
    Built entirely from the ground up in Java, Your Dark Side represents my final major project before transitioning into formal game development studies. Driven by pure passion and self-teaching, it served as a technical playground for implementing the core pillars of the RPG genre—including complex state management, A* pathfinding, and integrated merchant economies.
  </div>
  <div align="center" style="margin: 25px 0;">
    <a href="https://youtu.be/8z6vDdhrYUA" target="_blank" class="video-thumb">
      <img src="https://img.youtube.com/vi/8z6vDdhrYUA/maxresdefault.jpg" alt="YourDarkSide Gameplay" style="width: 100%; max-width: 850px; aspect-ratio: 16 / 9; object-fit: cover; border-radius: 12px; border: 2px solid #a5472d; box-shadow: 0px 0px 20px rgba(165, 71, 45, 0.2);">
    </a>
  </div>

  <h3 style="margin-bottom: 5px; color: #ffffff;">Core Contributions</h3>
  <div style="height: 2px; background: #a5472d; margin-bottom: 20px; border-radius: 2px;"></div>

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
</div>


<div id="dungeon" class="portfolio-tab" style="display: none;">
  <div style="display: flex; justify-content: space-between; align-items: center;">
    <img src="https://img.shields.io/badge/Dungeon%20Crawler-a5472d?style=for-the-badge&logo=python&logoColor=white" height="35"/>
    <img src="https://img.shields.io/badge/2017-333333?style=for-the-badge" height="35"/>
  </div>
  <div style="display: flex; justify-content: space-between; margin-top: 8px;">
    <b style="color: #f0f6fc;">2D Dungeon Crawler RPG</b>
    <b style="color: #f0f6fc;">Solo Developer</b>
  </div>
  <div style="background: #161b22; padding: 12px; border-radius: 8px; border-left: 5px solid #a5472d; margin-bottom: 15px; margin-top: 15px; color: #f0f6fc;">
    This project represents my first deep dive into the RPG genre and complex system architecture. Developed entirely on an iPad, this was an ambitious leap from previous work, driven by a passion for dungeon crawlers. It stands as a milestone where I successfully implemented interlocking systems like inventory management, class-based stats, and enemy AI.
  </div>
  <div align="center" style="margin: 25px 0;">
    <a href="https://youtu.be/HNQjJI9nPDQ" target="_blank" class="video-thumb">
      <img src="https://img.youtube.com/vi/HNQjJI9nPDQ/maxresdefault.jpg" alt="Dungeon Crawler Gameplay" style="width: 100%; max-width: 850px; aspect-ratio: 16 / 9; object-fit: cover; border-radius: 12px; border: 2px solid #a5472d; box-shadow: 0px 0px 20px rgba(165, 71, 45, 0.2);">
    </a>
  </div>

  <h3 style="margin-bottom: 5px; color: #ffffff;">Core Contributions</h3>
  <div style="height: 2px; background: #a5472d; margin-bottom: 20px; border-radius: 2px;"></div>

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
</div>


<div id="hit-run" class="portfolio-tab" style="display: none;">
  <div style="display: flex; justify-content: space-between; align-items: center;">
    <img src="https://img.shields.io/badge/Hit%20%26%20Run-a5472d?style=for-the-badge&logo=python&logoColor=white" height="35"/>
    <img src="https://img.shields.io/badge/2016-333333?style=for-the-badge" height="35"/>
  </div>
  <div style="display: flex; justify-content: space-between; margin-top: 8px;">
    <b style="color: #f0f6fc;">2D Survival Endless Scroller</b>
    <b style="color: #f0f6fc;">Solo Developer</b>
  </div>
  <div style="background: #161b22; padding: 12px; border-radius: 8px; border-left: 5px solid #a5472d; margin-bottom: 15px; margin-top: 15px; color: #f0f6fc;">
    As my first step into game development, Hit & Run was built in Python on the iPad to explore the core architecture of a functional game loop. This project served as my primary classroom for learning scaling difficulty and persistent progression systems—foundational concepts that have informed every project since.
  </div>
  <div align="center" style="margin: 25px 0;">
    <a href="https://youtu.be/FSjgXKFcKIo" target="_blank" class="video-thumb">
      <img src="https://img.youtube.com/vi/FSjgXKFcKIo/maxresdefault.jpg" alt="Hit & Run Gameplay" style="width: 100%; max-width: 850px; aspect-ratio: 16 / 9; object-fit: cover; border-radius: 12px; border: 2px solid #a5472d; box-shadow: 0px 0px 20px rgba(165, 71, 45, 0.2);">
    </a>
  </div>

  <h3 style="margin-bottom: 5px; color: #ffffff;">Core Contributions</h3>
  <div style="height: 2px; background: #a5472d; margin-bottom: 20px; border-radius: 2px;"></div>

  <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #a5472d; margin-bottom: 12px; color: #f0f6fc;">
    <b style="color: #ffffff;">Survival Loop Architecture</b>
    <ul style="margin-top: 5px; margin-bottom: 0; padding-left: 20px;">
      <li><b>Engineered</b> a stationary combat loop managing high-volume enemy convergence on a fixed player position.</li>
      <li><b>Developed</b> a scaling difficulty system to handle persistent intensity across long-term play sessions.</li>
    </ul>
  </div>

  <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #a5472d; margin-bottom: 12px; color: #f0f6fc;">
    <b style="color: #ffffff;">Combat Mechanics</b>
    <ul style="margin-top: 5px; margin-bottom: 0; padding-left: 20px;">
      <li><b>Implemented</b> a non-targeting swing mechanic that calculates damage for all enemies within a frontal arc.</li>
      <li><b>Integrated</b> a real-time cooldown system dynamically tied to a character "Haste" stat.</li>
    </ul>
  </div>

  <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #a5472d; margin-bottom: 12px; color: #f0f6fc;">
    <b style="color: #ffffff;">Persistent Progression</b>
    <ul style="margin-top: 5px; margin-bottom: 0; padding-left: 20px;">
      <li><b>Engineered</b> a multi-tiered reward system and a comprehensive shop framework for permanent stat upgrades.</li>
      <li><b>Managed</b> rare currency logic to handle ability unlocks and persistent player progression.</li>
    </ul>
  </div>
</div>

<script>
function switchTab(event, tabId) {
  // Hide all tabs using direct style object manipulation
  const tabs = document.getElementsByClassName("portfolio-tab");
  for (let i = 0; i < tabs.length; i++) {
    tabs[i].style.setProperty('display', 'none', 'important');
    tabs[i].classList.remove("active-content");
  }

  // Deactivate all button highlights
  const buttons = document.getElementsByClassName("tab-btn");
  for (let i = 0; i < buttons.length; i++) {
    buttons[i].classList.remove("active-tab");
  }

  // Actively display chosen tab
  const activeTab = document.getElementById(tabId);
  activeTab.style.setProperty('display', 'block', 'important');
  activeTab.classList.add("active-content");
  
  // Highlight clicked button
  event.currentTarget.classList.add("active-tab");
  
  // Smooth scroll back up to the tab window bar
  document.querySelector('.tab-container').scrollIntoView({ behavior: 'smooth' });
}
</script>
