# 🔬 SCIENCE LAB: The Lost Energy Core
### 3D Educational Science Adventure Game (Grades 6–10)
*College Major Project*

---

## 🚀 Project Overview
**SCIENCE LAB: The Lost Energy Core** is an interactive 3D science adventure game built with **Three.js (WebGL)**, **Vanilla ES6 Modules**, **HTML5**, and **CSS3**. The player takes the role of a Cadet Scientist in **Nova Science Laboratory** after the central Energy Core suffers a catastrophic power failure. To restore the core and unlock the facility, students must navigate 3D laboratory sectors, complete hands-on scientific experiments, and solve curriculum-aligned science challenges spanning **Chemistry, Biology, Physics, Earth & Environmental Science, and Electricity**.

---

## 📂 Project Architecture & File Structure

```
science lab/
├── index.html                    # Main HTML5 entrypoint with Three.js r160 CDN import map & UI overlay hierarchy
├── css/
│   ├── main.css                  # Core sci-fi design system, color tokens, typography, glassmorphism, animations
│   └── ui.css                    # HUD panels, interaction prompts, reticle crosshairs, modals, mobile joystick, toasts
├── js/
│   ├── main.js                   # Application coordinator & game bootstrap
│   ├── state/
│   │   ├── gameState.js          # Runtime game state manager & event bus
│   │   └── saveSystem.js         # Persistent localStorage manager (Profile, Grade, Stars, XP, Coins, Badges, Cards)
│   ├── core/
│   │   ├── sceneManager.js       # Three.js WebGLRenderer, PerspectiveCamera, dynamic lights, clock loop, disposal
│   │   ├── player.js             # 3D Scientist character avatar, custom physics (gravity/jump), WASD & touch controls
│   │   ├── cameraManager.js      # First-person and Third-person camera view controller with smooth interpolation
│   │   ├── interaction.js        # Raycaster, proximity detection, mesh highlighting, and "Press E" HUD prompts
│   │   └── audio.js              # Web Audio API procedural sound synthesizer (zero external audio file dependencies)
│   ├── data/
│   │   ├── questions.js          # Data-driven question bank organized by Grade (6 to 10) with "Why" explanations
│   │   └── labData.js            # Laboratory configurations, theme colors, story briefings, badges, science cards
│   ├── ui/
│   │   └── uiManager.js          # UI manager for HUD updates, quiz popups, pause menu, toasts, mobile joystick
│   └── levels/
│       ├── baseLevel.js          # Base 3D room generator, wall collisions, workbench builders, GPU memory disposal
│       ├── level0_tutorial.js    # Interactive Level 0 Atrium with 3D instruments, hologram terminal, tutorial mission
│       ├── level1_chem.js        # Chemistry Lab (Matter & Reactions)
│       ├── level2_bio.js         # Biology Lab (Life Systems)
│       ├── level3_phys.js        # Physics Lab (Dynamics & Motion)
│       ├── level4_earth.js       # Earth Lab (Ecological Systems)
│       ├── level5_energy.js      # Energy Lab (Circuits & Ohm's Law)
│       └── level6_core.js        # Final Level (Energy Core Reactor Boss)
└── README.md
```

---

## 🎮 How to Run Locally

Because this project uses modern ES6 modules and Three.js from a CDN with no build step required:
1. Open the project folder in **VS Code**.
2. Right-click `index.html` and click **"Open with Live Server"** (or run any lightweight local HTTP server, e.g., `npx serve .` or `python -m http.server 8000`).
3. Open `http://localhost:5500` (or the server URL) in any modern web browser (Google Chrome, Microsoft Edge, Firefox, or Safari).

---

## 🕹️ Controls Guide
- **W / A / S / D** or **Arrow Keys**: Move Scientist
- **Spacebar**: Jump
- **Mouse Drag / Move**: Look around (Pitch & Yaw)
- **E Key** or **Action Button**: Interact with lab terminals, beakers, instruments, and machines
- **V Key** or **Camera Button**: Toggle between **First-Person** and **Third-Person** perspectives
- **ESC Key** or **Pause Button**: Open Pause Menu & Settings
- **Touch / Mobile**: Use the virtual on-screen joystick on the bottom-left and action buttons on the bottom-right.
