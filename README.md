<div align="center">

# Mr. Vikas AK

**Systems, 3D WebGL & Embedded Smart TV Engineer | Computer Science & Engineering**

Chennai, India · [akvikas.github.io/3d-portfolio](https://akvikas.github.io/3d-portfolio)

[![3D Portfolio](https://img.shields.io/badge/3D%20Portfolio-0A66C2?style=for-the-badge&logo=googlechrome&logoColor=white)](https://akvikas.github.io/3d-portfolio)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ak-vikas-346446291/)
[![E-mail](https://img.shields.io/badge/E--mail-%23EA4335.svg?style=for-the-badge&logo=gmail&logoColor=white)](mailto:akvikas14@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/akvikas)

</div>

---

## What I Do

I engineer hardware-accelerated 3D Web experiences, embedded Smart TV platforms, real-time distributed web systems, and reinforcement learning simulations. My work bridges low-level device constraints—such as ARM Mali GPUs and WebKit runtime focus traps on Samsung Tizen OS—with interactive web graphics (Three.js/WebGL) and strictly-typed server-authoritative backends.

Currently pursuing a **B.E. in Computer Science and Engineering** at **Chennai Institute of Technology and Applied Research** (2023–2027, CGPA: **8.34**), with a deep focus on computer systems architecture, graphics rendering pipelines, and algorithmic simulation.

**Languages:** English (Professional) · Tamil (Native)

---

## Measurable Results & Engineering Impact

| Context / Challenge | Result / Engineering Solution |
|---|---|
| **Samsung Tizen 5.0 Spatial Navigation & Focus Traps** (Model `UA43RU7470UXXL`) | Eliminated WebKit remote control focus traps in Free My TV via capture-phase Down Arrow (`keyCode 40`, `useCapture = true`) listener + programmatic `.focus()` transfer and `tabindex="0"` injection across all DOM elements, achieving **0 ms remote latency** and 100% reliable D-Pad navigation. |
| **Low-Power ARM Mali-TDVX GPU (4K Samsung Smart TV)** | Ported signature Three.js Hero 3D Orbit Sphere from portfolio to Chromium 69 embedded TV runtime with instanced wireframe icosahedrons, sinusoidal core breathing, and dual orbital tori, sustaining **locked 60 FPS** without frame stutter or thermal throttling. |
| **Multi-Tier App Launcher Fallback & Dual-ID Mapping** | Resolved fragmented Tizen OS app identifiers across regions by building a bi-directional resolution table mapping package IDs to Samsung Store numeric IDs (e.g., Netflix `org.tizen.netflix-app` ↔ `3201907018807`, Prime Video `evKhCgZelL.AmazonIgnitionLauncher2`), backed by automatic fallback to `tizen.application.launchAppControl`. |
| **WordTrap Real-Time Multiplayer State Synchronization** | Replaced client-side state propagation with a **100% server-authoritative state machine** over Socket.IO, eliminating desyncs, enforcing atomic round timers, supporting instant disconnect/reconnect restoration, and rendering deterministic SVG avatars. |
| **RL Trading Lab Simulation & Policy Convergence** | Engineered a zero-dependency tabular Q-learning simulation environment with geometric Brownian motion price paths, converging policy returns across 1,000+ synthetic market epochs with **100% reproducible seed-based validation** against buy-and-hold baselines. |
| **Interactive 3D Portfolio WebGL Performance** | Optimized Three.js particle canvas with adaptive device pixel ratio scaling, dynamic camera orbit controls, and tree-shaken Vite bundle, achieving **sub-1.2s initial load** and 60 FPS rendering across mobile, desktop, and Smart TV browsers. |

---

## Featured Projects & Architecture

### 1. [Free My TV — 3D Cyber Edition](https://github.com/akvikas/free-my-tv) · [Live 3D Demo](https://akvikas.github.io/free-my-tv/)
> **Custom 3D Cyber TV Launcher for Samsung Tizen 5.0+, Google TV & LG webOS with Three.js Hero Orbit Sphere, Spatial Navigation & Ad-Free Experience.**

- **Architecture:** WebGL / Three.js embedded rendering engine hosted within a lightweight Samsung Tizen Web Application container (`config.xml`, `tizen/build.py`, `tz pack` signing pipeline).
- **Hero 3D Orbit Sphere:** Custom port of the signature interactive 3D particle sphere from [akvikas.github.io/3d-portfolio](https://akvikas.github.io/3d-portfolio) featuring a cyan wireframe icosahedron (`#4de1ff`), harmonic pulsing core (`#2a7fff`), dual tilted orbital tori, three Keplerian elliptical orbiting satellites, and 45+ floating stardust particles running at locked 60 FPS on ARM Mali GPUs.
- **Tizen Spatial Navigation Engine:** Completely solved remote D-Pad focus traps where cursor was locked in top header actions. Injected `tabindex="0"` on all shelf tiles, picks cards, and drawer keys; registered TV input device keys via `window.tizen.tvinputdevice.registerKey(...)`; implemented a capture-phase keydown escape listener explicitly shifting focus downward to shelf cards.
- **Bi-Directional Samsung App ID Resolution:** Engineered dual-mapping resolution supporting both Tizen application package IDs and Samsung Store numeric IDs with multi-operation fallback to `tizen.application.launchAppControl`.
- **Target Hardware Tested:** Samsung Series 7 43" 4K Smart TV (Model `UA43RU7470UXXL`, Tizen 5.0, Chromium 69 runtime) deployed via SDB CLI (`sdb connect 192.168.1.6:26101`).

`Three.js` · `WebGL` · `Samsung Tizen 5.0` · `Spatial Navigation` · `Chromium 69` · `SDB CLI` · `Tizen Studio`

---

### 2. [WordTrap — Real-Time Multiplayer Word Deduction](https://github.com/akvikas/wordtrap) · [Live Demo](https://wordtrap.vercel.app)
> **Real-time social deduction word game featuring server-authoritative state synchronization, bot simulation tables, and dynamic SVG generation.**

- **Architecture:** Node.js, Express, and Socket.IO backend with a strictly enforced server-side authoritative state machine.
- **Game Engine & Rules Loop:** Everyone except one imposter receives a secret word. Manages timed clue turns, voting phases, tie-reset mechanics with dealt replacement words, and imposter final-guess steal mechanics with complete state tamper resistance.
- **Seamless Disconnect & Reconnect Recovery:** Designed session-bound player tokens allowing instant reconnection and state restoration mid-turn without interrupting game flow.
- **Deterministic Avatars:** Integrated algorithmic SVG avatar generation seeded by player usernames with zero external asset dependencies.
- **Automated Quality Checks:** Comprehensive test suite with `npm test`, TypeScript type checks (`npm run typecheck`), and CI/CD production deployment via Vercel.

`TypeScript` · `Node.js` · `Express` · `Socket.IO` · `Vercel` · `Server-Side State Machine`

---

### 3. [RL Trading Lab — Tabular Q-Learning Sandbox](https://github.com/akvikas/rl-trading-lab) · [Live Demo](https://rl-trading-lab-ptfwpyqvttkq2k2morzc3l.streamlit.app/)
> **An educational, dependency-free Python reinforcement learning sandbox comparing tabular Q-learning policies with buy-and-hold baselines.**

- **Architecture:** Zero external dependencies (pure Python 3.10+ standard library) with modular state-action-reward simulation pipeline.
- **Market Simulator:** Generates reproducible geometric Brownian motion price paths parameterized by configurable drift and volatility with seed-based determinism.
- **Reinforcement Learning Engine:** Implements discrete trend-bucket state representation, temporal-difference Bellman equation updates, and epsilon-greedy exploration over `buy`, `sell`, and `hold` action spaces.
- **Accounting & Cost Modeling:** Realistic one-share portfolio tracking with explicit transaction costs on execution; reward function modeled on differential portfolio value.
- **Validation:** 100% test coverage on environment transitions, terminal states, and Q-table convergence via Python's standard `unittest` framework; interactive analytics frontend built with Streamlit.

`Python 3.10+` · `Reinforcement Learning` · `Tabular Q-Learning` · `Simulation` · `NumPy` · `Streamlit` · `unittest`

---

### 4. [Interactive 3D Developer Portfolio](https://github.com/akvikas/akvikas.github.io) · [Live Demo](https://akvikas.github.io/3d-portfolio)
> **High-performance personal portfolio featuring interactive 3D WebGL scenes, particle physics, and responsive reactive UI.**

- **Architecture:** React, Three.js, Vite, and Tailwind CSS with GitHub Pages CI/CD workflow automation.
- **3D Graphics & Visuals:** Custom WebGL canvas with dynamic orbit controls, mathematical particle trajectory simulations, and interactive cursor-responsive lighting shaders.
- **Performance Optimization:** Sub-1.2s initial load time achieved through dynamic chunk splitting, tree-shaking, and hardware-accelerated CSS transforms.

`React` · `Three.js` · `WebGL` · `Vite` · `Tailwind CSS` · `GitHub Actions`

---

### 5. [EnviConnect — Sustainability Action Platform](https://github.com/akvikas/enviconnect) · [Repository](https://github.com/akvikas/enviconnect)
> **Responsive community platform for discovering, organizing, and launching local ecological and sustainability initiatives.**

- **Architecture:** Modular front-end web application with structured client-side persistence and zero cold-start delay.
- **Real-Time Community Metrics:** Dynamic participant counters, live initiative filtration, and local storage state synchronization.

`JavaScript (ES6+)` · `HTML5` · `CSS3` · `Local Storage API` · `Responsive Design`

---

## Tech Stack

| Category | Technologies & Tools |
|---|---|
| **Languages** | Python · JavaScript (ES6+ & ES5) · TypeScript · HTML5 · CSS3 · SQL · C/C++ |
| **3D & Graphics** | Three.js · WebGL · Shader Programming · HTML5 Canvas API · Lucide Icons |
| **Frontend & UI** | React · Vite · Tailwind CSS · Framer Motion · DOM Spatial Navigation · Web Storage API |
| **Backend & Real-Time** | Node.js · Express · Socket.IO · RESTful APIs · Server-Authoritative State Engines |
| **Embedded & Smart TV** | Samsung Tizen 5.0+ (Web App) · Tizen TV Input API · SDB CLI · Tizen Studio (`tz pack`) · Chromium 69 runtime |
| **AI / ML & Simulation** | Tabular Q-Learning (RL) · NumPy · Streamlit · Stochastic Market Simulation |
| **DevOps, Tools & QA** | Git · GitHub Actions (CI/CD) · Vercel · SDB / ADB · NPM · Unit Testing (`unittest`, Jest) |

---

## Education & Certifications

- **Bachelor of Engineering in Computer Science and Engineering**  
  *Chennai Institute of Technology and Applied Research*, Chennai, India (2023 – 2027)  
  **CGPA:** 8.34 / 10.0  
  *Core Coursework:* Data Structures & Algorithms, Operating Systems, Computer Networks, Database Management Systems, Software Engineering, Object-Oriented Analysis & Design.

- **Technical Certifications & Training:**
  - **Cisco Networking Academy:** Networking Basics, Cybersecurity Essentials
  - **Infosys Springboard:** Python Programming, Web Application Architecture
  - **Industry Hackathons & Workshops:** RMK Engineering College & Regional Technical Symposia

---

<div align="center">

### Connect & Collaborate

[![Portfolio](https://img.shields.io/badge/3D%20Portfolio-akvikas.github.io-0A66C2?style=for-the-badge&logo=googlechrome&logoColor=white)](https://akvikas.github.io/3d-portfolio)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-AK%20Vikas-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ak-vikas-346446291/)
[![GitHub](https://img.shields.io/badge/GitHub-akvikas-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/akvikas)
[![Email](https://img.shields.io/badge/Email-akvikas14%40gmail.com-%23EA4335.svg?style=for-the-badge&logo=gmail&logoColor=white)](mailto:akvikas14@gmail.com)

</div>
