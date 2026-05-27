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
    display: inline-flex !important;
    flex-direction: column !important;
    align-items: center !important;
    justify-content: center !important;
    line-height: 1.2 !important;
    padding: 8px 16px !important;
    min-height: 54px !important;
    background-color: #161b22 !important;
    color: #c9d1d9 !important;
    border: 1px solid #30363d !important;
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

<div class="tab-container">
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

<div style="width: 100%; height: 2px; background: linear-gradient(90deg, transparent 5%, #bd4c2a 50%, transparent 95%); margin: 25px 0; opacity: 0.7;"></div>

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
  function switchTab(evt, tabId) {
    const tabs = document.getElementsByClassName("portfolio-tab");
    for (let i = 0; i < tabs.length; i++) {
      tabs[i].style.display = "none";
    }
    const buttons = document.getElementsByClassName("tab-btn");
    for (let i = 0; i < buttons.length; i++) {
      buttons[i].classList.remove("active-tab");
    }
    document.getElementById(tabId).style.display = "block";
    evt.currentTarget.classList.add("active-tab");
    window.scrollTo({top: 0, behavior: 'smooth'});
  }
</script>

<div id="about-tab" class="portfolio-tab" style="display: block;">
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
          A 2026 Honors Graduate in Game Development, I have maintained a 3.86 GPA while dedicating myself to building a portfolio of modular core systems and dynamic user interfaces.
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
          <img src="assets/Icons/JiraIcon.png" height="40" style="vertical-align: middle; border-radius: 5px;" onerror="this.src='https://skillicons.dev/icons?i=aws&theme=dark'"/>
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
          <img src="assets/Icons/3dsmaxIcon.png" height="40" style="vertical-align: middle; border-radius: 5px;" onerror="this.src='https://skillicons.dev/icons?i=svg&theme=dark'"/>
          <img src="https://skillicons.dev/icons?i=blender&theme=dark" height="40" style="vertical-align: middle;" />
          <img src="https://skillicons.dev/icons?i=photoshop&theme=dark" height="40" style="vertical-align: middle;" />
          <img src="https://skillicons.dev/icons?i=illustrator&theme=dark" height="40" style="vertical-align: middle;" />
          <img src="https://skillicons.dev/icons?i=pr&theme=dark" height="40" style="vertical-align: middle;" />
          <img src="https://skillicons.dev/icons?i=au&theme=dark" height="40" style="vertical-align: middle;" />
        </div>
      </td>
    </tr>
  </table>

  <div style="width: 100%; height: 2px; background: linear-gradient(90deg, transparent 5%, #bd4c2a 50%, transparent 95%); margin: 25px 0; opacity: 0.7;"></div>

  <div align="center" style="width: 100%; padding-bottom: 30px; padding-top: 5px;">
    <img src="myselfLevelup.jpg" alt="Tristan Anglin - Level Up Showcase" style="width: 100%; height: auto; border-radius: 12px; border: 2px solid #a5472d; box-shadow: 0px 0px 15px rgba(165, 71, 45, 0.15);" />
  </div>
</div>

<div id="blood-lineage" class="portfolio-tab" style="display: none; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif; color: #c9d1d9;">
  <div style="display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 10px;">
    <img src="https://img.shields.io/badge/Blood%20%26%20Lineage-a5472d?style=for-the-badge&logo=unrealengine&logoColor=white" height="35"/>
    <img src="https://img.shields.io/badge/2026-333333?style=for-the-badge" height="35"/>
  </div>
  
  <div style="display: flex; justify-content: space-between; margin-top: 12px; padding-bottom: 4px; flex-wrap: wrap; gap: 5px;">
    <b style="color: #f0f6fc; font-size: 1.1em;">3D Co-op Musou RPG (Capstone Project)</b>
    <b style="color: #da765b; font-size: 1.1em;">Lead Systems Architect & UI Programmer</b>
  </div>

  <div style="display: grid; grid-template-columns: 2fr 1fr; gap: 15px; margin: 20px 0; align-items: center;">
    <div style="background: #161b22; padding: 16px; border-radius: 8px; border-left: 5px solid #a5472d; color: #f0f6fc; line-height: 1.5;">
      Led the technical roadmap and framework development for an 11-person team. Personally architected the core gameplay loops, server-authoritative multiplayer infrastructure, and a comprehensive suite of UI/UX systems. Managed cross-department stability and build delivery utilizing <b>Jira</b> and <b>GitHub</b>.
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
      <iframe src="https://www.youtube.com/embed/tgr0kjX5Q0Q?autoplay=1&mute=1&loop=1&playlist=tgr0kjX5Q0Q&controls=1&modestbranding=1" title="Blood & Lineage Gameplay" style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: none;" allow="autoplay; encrypted-media; picture-in-picture" allowfullscreen></iframe>
    </div>
  </div>

  <div style="background: #161b22; padding: 12px 15px; border-radius: 8px; border-left: 5px solid #6e7681; margin-bottom: 35px; font-style: italic; font-size: 0.9em; color: #c9d1d9; line-height: 1.5;">
    "My workflow prioritizes networking and system state first. I engineer structural foundations and client/server validation profiles before implementing vector aesthetics, custom animations, and responsive motion graphics."
  </div>

  <h3 style="margin-bottom: 5px; color: #ffffff; font-size: 1.3em;">Core Contributions Breakdown</h3>
  <div style="width: 100%; height: 2px; background: linear-gradient(90deg, transparent 0%, #bd4c2a 50%, transparent 100%); margin: 10px 0 25px 0; opacity: 0.7;"></div>

  <div style="background: #161b22; padding: 18px; border-radius: 8px; border-left: 5px solid #a5472d; margin-bottom: 25px; color: #f0f6fc;">
    <div style="display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 5px; margin-bottom: 10px;">
      <b style="color: #ffffff; font-size: 1.1em;">Multiplayer Architecture & Systems Framework</b>
      <span style="font-size: 0.75em; background: #21262d; border: 1px solid #30363d; padding: 3px 8px; border-radius: 20px; color: #8b949e; font-weight: bold;">C++ / Blueprints / Replication</span>
    </div>
    <ul style="margin: 0 0 20px 0; padding-left: 20px; line-height: 1.6; color: #c9d1d9;">
      <li><b>Architected Core Separation:</b> Refactored codebase into a clean model splitting logic across <i>Character</i> (combat), <i>Player Controller</i> (Inputs), and <i>Player State</i> (persistent multiplayer variables).</li>
      <li><b>Engineered Seamless Travel Persistence:</b> Designed deep state copying carrying player statistics, equipment matrices, and inventories across server level boundaries securely.</li>
      <li><b>Prevented Design Soft-locks:</b> Built an automated, scaling Class-Locked Signature Weapon framework ensuring players remain viable without risk of destroying primary tools.</li>
    </ul>

    <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(340px, 1fr)); gap: 15px; margin-top: 15px;">
      <div style="background: #0d1117; border: 1px solid #30363d; border-radius: 6px; padding: 12px; display: flex; flex-direction: column; justify-content: space-between;">
        <div>
          <b style="color: #ffffff; font-size: 0.95em; display: block; margin-bottom: 4px;">PlayerState Data Serialization</b>
          <p style="font-size: 0.85em; color: #8b949e; line-height: 1.4; margin-bottom: 12px;">During travel map streams, the engine re-instantiates Actors. `CopyProperties` intercepts tearing to safely migrate data frames into the new world context.</p>
        </div>
        <div style="text-align: center; background: #161b22; padding: 6px; border-radius: 4px; border: 1px solid #21262d;">
          <img src="Copy Properties.PNG" alt="Player State Data Serialization Code" onclick="zoomImage(this)" style="max-width: 100%; max-height: 220px; width: auto; height: auto; object-fit: contain; border-radius: 4px; cursor: zoom-in;" />
          <span style="font-size: 0.75em; color: #da765b; display: block; margin-top: 6px; font-weight: bold;">🔍 Click to expand CopyProperties.cpp</span>
        </div>
      </div>
      <div style="background: #0d1117; border: 1px solid #30363d; border-radius: 6px; padding: 12px; display: flex; flex-direction: column; justify-content: space-between;">
        <div>
          <b style="color: #ffffff; font-size: 0.95em; display: block; margin-bottom: 4px;">Level Transition UI Garbage Culling</b>
          <p style="font-size: 0.85em; color: #8b949e; line-height: 1.4; margin-bottom: 12px;">Proactively unbinds interactive input contexts and cleans active UI viewports to protect references and eliminate severe pointer leakage.</p>
        </div>
        <div style="text-align: center; background: #161b22; padding: 6px; border-radius: 4px; border: 1px solid #21262d;">
          <img src="Clean UI.PNG" alt="UI Garbage Collection Culling Code" onclick="zoomImage(this)" style="max-width: 100%; max-height: 220px; width: auto; height: auto; object-fit: contain; border-radius: 4px; cursor: zoom-in;" />
          <span style="font-size: 0.75em; color: #da765b; display: block; margin-top: 6px; font-weight: bold;">🔍 Click to expand CleanUI.cpp</span>
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
      <li><b>Interface Suite Development:</b> Programmed over 20+ interface screens including a networked 4-Player Match Lobby, interactive Keybind Remappers, Save Profiles, and specialized Armory systems.</li>
      <li><b>Engineered Custom Visual Payloads:</b> Programmed a unified `UDragDropOperation` subclass passing full `FItemData` memory frames to let user drag actions seamlessly bridge across the distinct Inventory, Forge, and Armory UI panels natively.</li>
      <li><b>Graphic Asset Production:</b> Hand-crafted and vectorized a cohesive library of 50+ custom flat-design icons spanning difficulty tiers, classes, stats, and equipment matrices.</li>
    </ul>

    <b style="color: #ffffff; font-size: 0.95em; display: block; margin-bottom: 10px; padding-left: 5px;">Visual Breakdown: System Prototyping to Production Assets</b>
    <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(240px, 1fr)); gap: 12px;">
      <div style="text-align: center; background: #0d1117; padding: 10px; border-radius: 6px; border: 1px solid #30363d;">
        <img src="InventoryWireframe.png" alt="UX Wireframe Layout" onclick="zoomImage(this)" style="width: 100%; height: auto; aspect-ratio: 16/10; object-fit: contain; background: #161b22; border-radius: 4px; cursor: zoom-in;" />
        <p style="font-size: 0.8em; color: #8b949e; margin-top: 8px; margin-bottom: 0;"><b>Phase 1:</b> Screen Wireframe Grid</p>
      </div>
      <div style="text-align: center; background: #0d1117; padding: 10px; border-radius: 6px; border: 1px solid #30363d;">
        <img src="InventoryFinal.PNG" alt="Inventory Layout Art Integration" onclick="zoomImage(this)" style="width: 100%; height: auto; aspect-ratio: 16/10; object-fit: contain; background: #161b22; border-radius: 4px; cursor: zoom-in;" />
        <p style="font-size: 0.8em; color: #8b949e; margin-top: 8px; margin-bottom: 0;"><b>Phase 2:</b> Vector Layout Integration</p>
      </div>
      <div style="text-align: center; background: #0d1117; padding: 10px; border-radius: 6px; border: 1px solid #30363d;">
        <img src="HUDFinal.PNG" alt="Final Tactical HUD Layout" onclick="zoomImage(this)" style="width: 100%; height: auto; aspect-ratio: 16/10; object-fit: contain; background: #161b22; border-radius: 4px; cursor: zoom-in;" />
        <p style="font-size: 0.8em; color: #8b949e; margin-top: 8px; margin-bottom: 0;"><b>Phase 3:</b> Active HUD Drag Contexts</p>
      </div>
    </div>
  </div>

  <div style="background: #161b22; padding: 18px; border-radius: 8px; border-left: 5px solid #a5472d; margin-bottom: 25px; color: #f0f6fc;">
    <div style="display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 5px; margin-bottom: 10px;">
      <b style="color: #ffffff; font-size: 1.1em;">Advanced Economy Mechanics (Forge & Armory)</b>
      <span style="font-size: 0.75em; background: #21262d; border: 1px solid #30363d; padding: 3px 8px; border-radius: 20px; color: #8b949e; font-weight: bold;">Data Structures / Math Logic</span>
    </div>
    <ul style="margin: 0 0 20px 0; padding-left: 20px; line-height: 1.6; color: #c9d1d9;">
      <li><b>Modular Optimization:</b> Decoupled handling into a thin replication struct block (`FItemData`) nestled in a singular `UObject` interface shell to significantly preserve net memory footprints.</li>
      <li><b>Cross-Item Forging Logic:</b> Created algebraic combining algorithms handling dual material sacrifices through server-validated weighted distribution success logic.</li>
    </ul>

    <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(340px, 1fr)); gap: 15px; margin-top: 5px;">
      <div style="background: #0d1117; border: 1px solid #30363d; border-radius: 6px; padding: 12px; display: flex; flex-direction: column; justify-content: space-between;">
        <div>
          <b style="color: #ffffff; font-size: 0.95em; display: block; margin-bottom: 4px;">Optimized Memory Layout</b>
          <p style="font-size: 0.85em; color: #8b949e; line-height: 1.4; margin-bottom: 12px;">Separating the lightweight array primitives matrix from the networking wrapper objects minimizes RPC signature scales during heavy multi-client trades.</p>
        </div>
        <div style="text-align: center; background: #161b22; padding: 6px; border-radius: 4px; border: 1px solid #21262d;">
          <img src="ItemObject.PNG" alt="Replicated Struct and UObject Definition" onclick="zoomImage(this)" style="max-width: 100%; max-height: 220px; width: auto; height: auto; object-fit: contain; border-radius: 4px; cursor: zoom-in;" />
          <span style="font-size: 0.75em; color: #da765b; display: block; margin-top: 6px; font-weight: bold;">🔍 Click to expand ItemObject.h</span>
        </div>
      </div>
      <div style="background: #0d1117; border: 1px solid #30363d; border-radius: 6px; padding: 12px; display: flex; flex-direction: column; justify-content: space-between;">
        <div>
          <b style="color: #ffffff; font-size: 0.95em; display: block; margin-bottom: 4px;">Server-Side Probability Math</b>
          <p style="font-size: 0.85em; color: #8b949e; line-height: 1.4; margin-bottom: 12px;">Fusing inventory arrays scales item attributes based on random curves tightly clamped behind authority validation loops to secure economy stability.</p>
        </div>
        <div style="text-align: center; background: #161b22; padding: 6px; border-radius: 4px; border: 1px solid #21262d;">
          <img src="ForgeCalculation.PNG" alt="Weighted Forging Compression Rules" onclick="zoomImage(this)" style="max-width: 100%; max-height: 220px; width: auto; height: auto; object-fit: contain; border-radius: 4px; cursor: zoom-in;" />
          <span style="font-size: 0.75em; color: #da765b; display: block; margin-top: 6px; font-weight: bold;">🔍 Click to expand Forge Logic</span>
        </div>
      </div>
    </div>
  </div>

  <div style="background: #161b22; padding: 18px; border-radius: 8px; border-left: 5px solid #a5472d; margin-bottom: 25px; color: #f0f6fc;">
    <div style="display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 5px; margin-bottom: 10px;">
      <b style="color: #ffffff; font-size: 1.1em;">Boss AI & Networked Encounter Design (Hades)</b>
      <span style="font-size: 0.75em; background: #21262d; border: 1px solid #30363d; padding: 3px 8px; border-radius: 20px; color: #8b949e; font-weight: bold;">AI Behavior / Gameplay Scripting</span>
    </div>
    <ul style="margin: 0 0 20px 0; padding-left: 20px; line-height: 1.6; color: #c9d1d9;">
      <li><b>Multi-Phase State Machinery:</b> Programmed multi-tiered Hades boss sequences, custom attack animation layers, and transformation properties.</li>
      <li><b>Network Prediction Meshes:</b> Generated synchronized area danger indicators instantly across client simulations locally, offsetting network jitter margins cleanly.</li>
    </ul>

    <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 15px; margin-top: 5px;">
      <div style="background: #0d1117; border: 1px solid #30363d; padding: 10px; text-align: center; border-radius: 6px;">
        <img src="Hades_State_Machine.png" alt="Multi-Phase Encounter State Machine" onclick="zoomImage(this)" style="max-width: 100%; height: auto; border-radius: 4px; cursor: zoom-in;" />
        <span style="font-size: 0.75em; color: #da765b; display: block; margin-top: 6px; font-weight: bold;">View Boss State Machine Graph</span>
      </div>
      <div style="background: #0d1117; border: 1px solid #30363d; padding: 10px; text-align: center; border-radius: 6px;">
        <img src="Telegraph_Prediction_Mesh.png" alt="Network Predictive Telegraph Mesh" onclick="zoomImage(this)" style="max-width: 100%; height: auto; border-radius: 4px; cursor: zoom-in;" />
        <span style="font-size: 0.75em; color: #da765b; display: block; margin-top: 6px; font-weight: bold;">View Predictive Projection Mesh</span>
      </div>
    </div>
  </div>

  <h3 style="margin-top: 30px; margin-bottom: 5px; color: #ffffff; font-size: 1.3em;">Engineering Post-Mortem</h3>
  <div style="width: 100%; height: 2px; background: linear-gradient(90deg, transparent 0%, #bd4c2a 50%, transparent 100%); margin: 10px 0 25px 0; opacity: 0.7;"></div>

  <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 15px; margin-bottom: 15px;">
    <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #bd4c2a;">
      <b style="color: #ffffff;">The Challenge: High-Density Network Sync</b>
      <p style="margin-top: 5px; margin-bottom: 0; font-size: 0.9em; line-height: 1.5; color: #c9d1d9;">Simultaneous 4-player tracking during intense combat sweeps caused severe client simulation variance and packet processing bottleneck drops.</p>
    </div>
    <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #28a745;">
      <b style="color: #ffffff;">The Resolution: Server Authority Loops</b>
      <p style="margin-top: 5px; margin-bottom: 0; font-size: 0.9em; line-height: 1.5; color: #c9d1d9;">Enforced fully strict server validation rules across loot transactions, completely isolating local UI render states from asynchronous logic updates.</p>
    </div>
  </div>
</div>

<div id="tower-defense" class="portfolio-tab" style="display: none; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif; color: #c9d1d9;">
  <div style="display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 10px;">
    <img src="https://img.shields.io/badge/Tower%20Defense-bd4c2a?style=for-the-badge&logo=cplusplus&logoColor=white" height="35"/>
    <img src="https://img.shields.io/badge/2024-333333?style=for-the-badge" height="35"/>
  </div>

  <div style="display: flex; justify-content: space-between; margin-top: 12px; padding-bottom: 4px; flex-wrap: wrap; gap: 5px;">
    <b style="color: #f0f6fc; font-size: 1.1em;">Custom 2D Engine Grid Strategy Game</b>
    <b style="color: #da765b; font-size: 1.1em;">Solo Core Systems Engineer</b>
  </div>

  <div style="display: grid; grid-template-columns: 2fr 1fr; gap: 15px; margin: 20px 0; align-items: center;">
    <div style="background: #161b22; padding: 16px; border-radius: 8px; border-left: 5px solid #bd4c2a; color: #f0f6fc; line-height: 1.5;">
      Developed a high-performance grid defense strategy game built from scratch inside a custom-engineered C++ 2D engine. Programmed custom memory pools, basic lower-level rendering adapters, pixel-grid tracking metrics, and custom game logic independent of commercial engine runtimes.
    </div>
    <div style="background: #0d1117; border: 1px solid #30363d; padding: 12px; border-radius: 8px; text-align: center;">
      <div style="font-size: 1.8em; font-weight: bold; color: #f0f6fc; margin-bottom: 2px;">0</div>
      <div style="font-size: 0.75em; color: #8b949e; text-transform: uppercase; letter-spacing: 0.5px; margin-bottom: 10px;">Third-Party Engines</div>
      <div style="font-size: 1.8em; font-weight: bold; color: #f0f6fc; margin-bottom: 2px;">60 FPS</div>
      <div style="font-size: 0.75em; color: #8b949e; text-transform: uppercase; letter-spacing: 0.5px;">Fixed Lock Rendering</div>
    </div>
  </div>

  <h3 style="margin-bottom: 5px; color: #ffffff; font-size: 1.3em;">Core Contributions Breakdown</h3>
  <div style="width: 100%; height: 2px; background: linear-gradient(90deg, transparent 0%, #bd4c2a 50%, transparent 100%); margin: 10px 0 25px 0; opacity: 0.7;"></div>

  <div style="background: #161b22; padding: 18px; border-radius: 8px; border-left: 5px solid #bd4c2a; margin-bottom: 25px; color: #f0f6fc;">
    <b style="color: #ffffff; font-size: 1.1em; display: block; margin-bottom: 10px;">Low-Level Systems Architecture</b>
    <ul style="margin: 0; padding-left: 20px; line-height: 1.6; color: #c9d1d9;">
      <li><b>Engine Architecture:</b> Implemented a clean update-render decoupling structure using explicit memory allocations and custom entity handle management models.</li>
      <li><b>Grid Parsing & Pathfinding:</b> Configured optimized spatial partitioning logic enabling rapid tile validation, neighborhood routing checks, and projectile intersection processing.</li>
    </ul>
  </div>

  <h3 style="margin-top: 30px; margin-bottom: 5px; color: #ffffff; font-size: 1.3em;">Engineering Post-Mortem</h3>
  <div style="width: 100%; height: 2px; background: linear-gradient(90deg, transparent 0%, #bd4c2a 50%, transparent 100%); margin: 10px 0 25px 0; opacity: 0.7;"></div>

  <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 15px; margin-bottom: 15px;">
    <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #bd4c2a;">
      <b style="color: #ffffff;">The Challenge: Manual Heap Fragmentation</b>
      <p style="margin-top: 5px; margin-bottom: 0; font-size: 0.9em; line-height: 1.5; color: #c9d1d9;">Instantiating high volumes of independent enemy actors and flying projectiles sequentially caused heap micro-fragmentation and dropped tick frames.</p>
    </div>
    <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #28a745;">
      <b style="color: #ffffff;">The Resolution: Contiguous Allocation</b>
      <p style="margin-top: 5px; margin-bottom: 0; font-size: 0.9em; line-height: 1.5; color: #c9d1d9;">Swapped out dynamic allocations for contiguous array blocks, reusing entity arrays via inactive index swapping to guarantee consistent 16.6ms cycle blocks.</p>
    </div>
  </div>
</div>

<div id="darkside" class="portfolio-tab" style="display: none; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif; color: #c9d1d9;">
  <div style="display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 10px;">
    <img src="https://img.shields.io/badge/Your%20Dark%20Side-007396?style=for-the-badge&logo=java&logoColor=white" height="35"/>
    <img src="https://img.shields.io/badge/2023-333333?style=for-the-badge" height="35"/>
  </div>

  <div style="display: flex; justify-content: space-between; margin-top: 12px; padding-bottom: 4px; flex-wrap: wrap; gap: 5px;">
    <b style="color: #f0f6fc; font-size: 1.1em;">2D Top-Down Psychological Action Game</b>
    <b style="color: #da765b; font-size: 1.1em;">Self-Taught Systems Programmer</b>
  </div>

  <div style="display: grid; grid-template-columns: 2fr 1fr; gap: 15px; margin: 20px 0; align-items: center;">
    <div style="background: #161b22; padding: 16px; border-radius: 8px; border-left: 5px solid #007396; color: #f0f6fc; line-height: 1.5;">
      Constructed as an ambitious self-taught initiative to break past academic curricula. Developed custom multi-threaded game state clocks, interactive tile mapping matrix structures, sprite sheet frame-strippers, and a responsive input router utilizing <b>Java AWT/Swing</b> libraries natively.
    </div>
    <div style="background: #0d1117; border: 1px solid #30363d; padding: 12px; border-radius: 8px; text-align: center;">
      <div style="font-size: 1.8em; font-weight: bold; color: #f0f6fc; margin-bottom: 2px;">100%</div>
      <div style="font-size: 0.75em; color: #8b949e; text-transform: uppercase; letter-spacing: 0.5px; margin-bottom: 10px;">Self-Taught Logic</div>
      <div style="font-size: 1.8em; font-weight: bold; color: #f0f6fc; margin-bottom: 2px;">Multi-Threaded</div>
      <div style="font-size: 0.75em; color: #8b949e; text-transform: uppercase; letter-spacing: 0.5px;">State Processing</div>
    </div>
  </div>

  <h3 style="margin-bottom: 5px; color: #ffffff; font-size: 1.3em;">Core Contributions Breakdown</h3>
  <div style="width: 100%; height: 2px; background: linear-gradient(90deg, transparent 0%, #bd4c2a 50%, transparent 100%); margin: 10px 0 25px 0; opacity: 0.7;"></div>

  <div style="background: #161b22; padding: 18px; border-radius: 8px; border-left: 5px solid #007396; margin-bottom: 25px; color: #f0f6fc;">
    <b style="color: #ffffff; font-size: 1.1em; display: block; margin-bottom: 10px;">State Separation Mechanics</b>
    <ul style="margin: 0; padding-left: 20px; line-height: 1.6; color: #c9d1d9;">
      <li><b>Loop Isolation Architecture:</b> Engineered separate execution loops allocating background threads to track logic metrics, keeping rendering loops completely unblocked.</li>
      <li><b>Procedural Texture Stripping:</b> Programmed runtime asset readers to break combined image matrices smoothly down into clean layout animation grids based on custom dimensions.</li>
    </ul>
  </div>

  <h3 style="margin-top: 30px; margin-bottom: 5px; color: #ffffff; font-size: 1.3em;">Engineering Post-Mortem</h3>
  <div style="width: 100%; height: 2px; background: linear-gradient(90deg, transparent 0%, #bd4c2a 50%, transparent 100%); margin: 10px 0 25px 0; opacity: 0.7;"></div>

  <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 15px; margin-bottom: 15px;">
    <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #bd4c2a;">
      <b style="color: #ffffff;">The Challenge: Concurrency Collisions</b>
      <p style="margin-top: 5px; margin-bottom: 0; font-size: 0.9em; line-height: 1.5; color: #c9d1d9;">Asynchronous loops editing state matrices concurrently triggered severe structural race conditions and application thread lockouts.</p>
    </div>
    <div style="background: #161b22; padding: 15px; border-radius: 8px; border-left: 5px solid #28a745;">
      <b style="color: #ffffff;">The Resolution: Synchronized Locks</b>
      <p style="margin-top: 5px; margin-bottom: 0; font-size: 0.9em; line-height: 1.5; color: #c9d1d9;">Implemented strict synchronized checkpoint access points, isolating data mutations into distinct step buffers before passing them to visual contexts.</p>
    </div>
  </div>
</div>

<div id="dungeon" class="portfolio-tab" style="display: none; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif; color: #c9d1d9;">
  <div style="display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 10px;">
    <img src="https://img.shields.io/badge/Dungeon%20Crawler-3776AB?style=for-the-badge&logo=python&logoColor=white" height="35"/>
    <img src="https://img.shields.io/badge/2017-333333?style=for-the-badge" height="35"/>
  </div>

  <div style="display: flex; justify-content: space-between; margin-top: 12px; padding-bottom: 4px; flex-wrap: wrap; gap: 5px;">
    <b style="color: #f0f6fc; font-size: 1.1em;">ASCII Procedural Roguelike Systems Engine</b>
    <b style="color: #da765b; font-size: 1.1em;">Systems Designer & Logic Programmer</b>
  </div>

  <div style="display: grid; grid-template-columns: 2fr 1fr; gap: 15px; margin: 20px 0; align-items: center;">
    <div style="background: #161b22; padding: 16px; border-radius: 8px; border-left: 5px solid #3776AB; color: #f0f6fc; line-height: 1.5;">
      An early foundation exploring modular parsing. Built a grid-based turn strategy framework tracking coordinate arrays inside multidimensional list maps. Implemented inventory structures, encounter calculations, and automated text output parsing layers.
    </div>
    <div style="background: #0d1117; border: 1px solid #30363d; padding: 12px; border-radius: 8px; text-align: center;">
      <div style="font-size: 1.8em; font-weight: bold; color: #f0f6fc; margin-bottom: 2px;">2D Matrix</div>
      <div style="font-size: 0.75em; color: #8b949e; text-transform: uppercase; letter-spacing: 0.5px; margin-bottom: 10px;">World Grid Mapping</div>
      <div style="font-size: 1.8em; font-weight: bold; color: #f0f6fc; margin-bottom: 2px;">Turn-Based</div>
      <div style="font-size: 0.75em; color: #8b949e; text-transform: uppercase; letter-spacing: 0.5px;">Step Track Engine</div>
    </div>
  </div>

  <h3 style="margin-bottom: 5px; color: #ffffff; font-size: 1.3em;">Core Contributions Breakdown</h3>
  <div style="width: 100%; height: 2px; background: linear-gradient(90deg, transparent 0%, #bd4c2a 50%, transparent 100%); margin: 10px 0 25px 0; opacity: 0.7;"></div>

  <div style="background: #161b22; padding: 18px; border-radius: 8px; border-left: 5px solid #3776AB; margin-bottom: 25px; color: #f0f6fc;">
    <b style="color: #ffffff; font-size: 1.1em; display: block; margin-bottom: 10px;">Procedural Text Processing Logic</b>
    <ul style="margin: 0; padding-left: 20px; line-height: 1.6; color: #c9d1d9;">
      <li><b>Coordinate Step Maps:</b> Programmed clean tracking grids mapping characters and environmental structures into distinct numerical coordinates for conflict checks.</li>
      <li><b>Dynamic Stat Generation:</b> Developed item tables calculating random attribute modifiers and equipment requirements based on character progression scales.</li>
    </ul>
  </div>
</div>

<div id="hit-run" class="portfolio-tab" style="display: none; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif; color: #c9d1d9;">
  <div style="display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 10px;">
    <img src="https://img.shields.io/badge/Hit%20%26%20Run-3776AB?style=for-the-badge&logo=python&logoColor=white" height="35"/>
    <img src="https://img.shields.io/badge/2016-333333?style=for-the-badge" height="35"/>
  </div>

  <div style="display: flex; justify-content: space-between; margin-top: 12px; padding-bottom: 4px; flex-wrap: wrap; gap: 5px;">
    <b style="color: #f0f6fc; font-size: 1.1em;">2D Core Arcade Reflex Game</b>
    <b style="color: #da765b; font-size: 1.1em;">Foundational Software Engineer</b>
  </div>

  <div style="display: grid; grid-template-columns: 2fr 1fr; gap: 15px; margin: 20px 0; align-items: center;">
    <div style="background: #161b22; padding: 16px; border-radius: 8px; border-left: 5px solid #3776AB; color: #f0f6fc; line-height: 1.5;">
      My initial foray into codebase design. Engineered using basic graphic wrappers to master loop handling principles. Programmed real-time tracking checks, automated variable score multipliers, and localized boundary resolution vectors.
    </div>
    <div style="background: #0d1117; border: 1px solid #30363d; padding: 12px; border-radius: 8px; text-align: center;">
      <div style="font-size: 1.8em; font-weight: bold; color: #f0f6fc; margin-bottom: 2px;">2D Screen</div>
      <div style="font-size: 0.75em; color: #8b949e; text-transform: uppercase; letter-spacing: 0.5px; margin-bottom: 10px;">Vector Bounds</div>
      <div style="font-size: 1.8em; font-weight: bold; color: #f0f6fc; margin-bottom: 2px;">Real-Time</div>
      <div style="font-size: 0.75em; color: #8b949e; text-transform: uppercase; letter-spacing: 0.5px;">Coordinate Loops</div>
    </div>
  </div>

  <h3 style="margin-bottom: 5px; color: #ffffff; font-size: 1.3em;">Core Contributions Breakdown</h3>
  <div style="width: 100%; height: 2px; background: linear-gradient(90deg, transparent 0%, #bd4c2a 50%, transparent 100%); margin: 10px 0 25px 0; opacity: 0.7;"></div>

  <div style="background: #161b22; padding: 18px; border-radius: 8px; border-left: 5px solid #3776AB; margin-bottom: 25px; color: #f0f6fc;">
    <b style="color: #ffffff; font-size: 1.1em; display: block; margin-bottom: 10px;">Foundational Architecture Elements</b>
    <ul style="margin: 0; padding-left: 20px; line-height: 1.6; color: #c9d1d9;">
      <li><b>Coordinate Boundaries:</b> Configured boundary checking formulas intercepting player inputs to clamp spatial translation within acceptable window domains.</li>
      <li><b>Incremental Scaling Loops:</b> Managed dynamic difficulty adjustment arrays accelerating object velocities based on elapsed runtime metrics.</li>
    </ul>
  </div>
</div>
