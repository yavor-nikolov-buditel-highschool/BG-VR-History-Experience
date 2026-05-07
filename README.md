# 🏛️ Virtual Museum of Bulgaria
### An Interactive Multimedia VR Platform for Bulgarian History

[![Unity](https://img.shields.io/badge/Engine-Unity%206000.2.14f1-blue)](https://unity.com/)
[![Platform](https://img.shields.io/badge/Platform-Meta%20Quest%202%20%7C%203S-blueviolet)](https://www.meta.com/quest/)
[![Language](https://img.shields.io/badge/Language-C%23-green)](https://learn.microsoft.com/en-us/dotnet/csharp/)
[![License](https://img.shields.io/badge/License-Open-brightgreen)](LICENSE)

---

## 📖 Overview

**Virtual Museum of Bulgaria** is a fully interactive educational VR platform that presents key moments of Bulgarian history in an engaging, modern, and accessible way. Designed for students, tourists, museum visitors, and history enthusiasts, the platform offers an immersive alternative to traditional textbooks and static exhibitions.

While leading world institutions such as the Louvre, Rijksmuseum, and the National Museum of Ukraine have already adopted VR experiences, no widely accessible interactive VR solution dedicated to Bulgarian national history existed before this project. We identified this gap and built it.

---

## ✨ Features

- 🗺️ **Three themed exhibition halls** — The Battle of Shipka, The Panagyurishte Treasure, and Bulgaria in World War II
- 🎧 **Audio narration** in both **Bulgarian and English**
- 🖐️ **Interactive 3D objects** — pick up, rotate, and inspect artefacts with VR controllers
- 🔫 **Particle-based effects** — fire a historical Mannlicher M95 rifle in the WWII hall
- 🚶 **Dual navigation system** — teleportation (motion-sickness friendly) and joystick movement
- 🔊 **Proximity-triggered audio** — narration plays automatically as you approach exhibits
- ⚙️ **In-game settings** — adjustable sound, music, and language switching at any time
- 📦 **Modular prefab architecture** — new halls can be added almost entirely via drag-and-drop

---

## 🎮 Demo & Social Media

| Platform | Link |
|---|---|
| 🎥 YouTube | [@virtualhistorybg](https://www.youtube.com/@virtualhistorybg) |
| 📸 Instagram | [@vrhistorybg](https://www.instagram.com/vrhistorybg) |
| 🎵 TikTok | [@vr.history.bg](https://www.tiktok.com/@vr.history.bg) |

---

## 🚀 Getting Started

### Prerequisites

- A Meta Quest 2 or Meta Quest 3S headset
- A PC with a USB Link Cable **or** [Virtual Desktop](https://www.vrdesktop.net/) for wireless streaming

### Installation

1. Clone or download this repository:
   ```bash
   git clone https://github.com/yavor-nikolov-buditel-highschool/BG-VR-History-Experience.git
   ```
2. Navigate to the `build` folder.
3. Connect your VR headset to your PC via Link Cable or Virtual Desktop.
4. Launch `the bulgaria museum the virtual experience.exe`.
5. The application will automatically appear in your connected VR headset.

---

## 🏗️ Architecture

The project is built on a fully **modular prefab system** — every feature is a standalone, reusable component that can be dropped into any scene with minimal configuration.

### Core Modules

| Module | Description |
|---|---|
| **Start Screen** | Launch screen with Start, Exit (with confirmation dialog), and Settings buttons |
| **Main Hub** | Central room with a console for selecting a themed hall; plays a one-time welcome audio guide |
| **Navigation Module** | Dual system: teleportation (motion-sickness safe) + joystick movement |
| **Area Detection Module** | `BoxCollider` trigger that auto-plays intro audio when the player enters an exhibit zone |
| **Button Interaction Module** | Physical 3D buttons next to each exhibit that trigger detailed audio narration |
| **XR Object Interaction** | Allows picking up, rotating, and inspecting 3D artefacts via `XR Grab Interactable` |
| **Language Manager** | Singleton component persisting across scenes; manages all audio clips per active language |
| **Scene Manager & Loader** | Asynchronous scene transitions with animated loading screens |
| **Pause Module** | Accessible from any scene; pauses movement, shows settings and exit options |
| **NPC System** | Foundational architecture ready for future expansion into simulated historical scenes |

---

## 🛠️ Technology Stack

| Category | Technology |
|---|---|
| Engine | Unity 6000.2.14f1 |
| Language | C# |
| VR Framework | Unity XR Interaction Toolkit |
| Input | Action-based Input System |
| Performance | Baked lighting with lightmaps, LOD optimization, Unity Profiler |
| VFX | Unity Particle System (weapon fire effects) |
| Target Hardware | Meta Quest 2, Meta Quest 3S |

### Why Unity?

We evaluated both Unity and Unreal Engine. Unity was chosen for its native Meta Quest support via XR Plugin Management, its well-documented XR Interaction Toolkit, strong mobile VR optimization capabilities, and its large, active community. Unreal Engine was ruled out due to more complex standalone VR configuration and higher hardware requirements incompatible with our target platform.

---

## 📐 Development Stages

| Stage | Period | Description |
|---|---|---|
| 1 — Research & Concept | Month 1 | Analysed existing VR museum solutions (Louvre, Rijksmuseum, emuseum.ua); defined historical themes and team roles |
| 2 — Architecture Design | Month 2 | Designed the modular prefab system and defined all core module interfaces |
| 3 — Core Development | Months 3–5 | Built the main menu, hub, three exhibition halls, audio systems, and integrated all 3D assets |
| 4 — Testing & Iteration | Months 5–6 | User testing with VR newcomers and motion-sickness-prone users; performance optimization (3 iterations) |
| 5 — Marketing & Launch | Month 6 | Published to social media channels; released promotional videos and demos |

---

## 🧪 Testing & Performance

Testing was conducted across four dimensions:

- **VR newcomers** (including first-time headset users): revealed UX issues in menus → led to simplified controls and first-launch audio instructions
- **Motion sickness testing**: joystick-only navigation caused discomfort → teleportation system was added as an equal alternative
- **Performance benchmarking** on Meta Quest 2 and Meta Quest 3S: initial dynamic lighting caused FPS drops to 45–50 → resolved with baked lighting and polygon optimisation across 3 iterations
- **Historical accuracy review**: audio narration validated by a history teacher

**Result: stable ~70 FPS on both target platforms.**

---

## ⚙️ Key Technical Challenges & Solutions

### 1. FPS Stability
Dynamic lighting caused drops to 45–50 FPS (threshold for VR comfort is 72 FPS). Solved by switching to fully baked lighting with lightmaps, reducing polygon counts, and using Unity Profiler to eliminate draw call bottlenecks. **Final result: stable ~70 FPS.**

### 2. Motion Sickness & Accessibility
Joystick-only navigation caused discomfort for inexperienced users. Solved by implementing a **teleportation system** as a parallel alternative — both modes coexist and can be switched at any time.

### 3. Modular Scalability
Adding a new hall should not require rewriting code. Solved by building all functionality as **independent prefabs** (Area Detector, Button Module, XR Interactable, Audio Player) that are self-contained and reusable via drag-and-drop.

### 4. Multilingual Support
Synchronising language state across scene transitions was non-trivial. Solved with a **singleton Language Manager** that persists between scenes and automatically applies the selected language to all audio and UI elements.

### 5. 3D Asset Integration
Assets from Sketchfab arrived in various polygon densities and texture formats. Each model required manual **polygon reduction, texture format conversion**, and LOD configuration for mobile VR performance.

---

## 🎨 3D Assets & Credits

| Asset | Source |
|---|---|
| Mannlicher M95 rifle | [Sketchfab](https://sketchfab.com/3d-models/mannlicher-m95-infanterie-repetier-gewehr-m95-a5387036a8e84edf88fdcc96c7c88f61) — free licence |
| Vase (base model) | [Sketchfab](https://sketchfab.com/3d-models/f4d651a377fd424b882c0d38aebf1a89) — free licence |
| Museum gallery environment | [Sketchfab](https://sketchfab.com/3d-models/vr-moody-lighting-art-gallery-scene-06-00096961521145f9a8c964fd98c3dca0) — free licence |
| Vase body & weapon variants | Provided by **Alexander Zahariev** — portfolio contribution |

---

## 🔭 Roadmap

- [ ] Additional themed halls covering broader periods of Bulgarian history
- [ ] Fully simulated historical battles with NPC allies and enemies
- [ ] Expanded 3D artefacts and interactive maps (in collaboration with graphic designers and historians)
- [ ] Publication on the **Meta Quest Store** for worldwide access

---

## 👥 Authors

**Yavor Yavorov Nikolov** — Technical development, programming, system architecture  
School: ЧПГДН "СофтУни Будител", Class VIII  
📧 iavor.nikolov.highschool@buditel.bg

**Viktor Ramakrishna Devanathan** — Historical research, audio script, visual organisation  
School: ЧПГДН "СофтУни Будител", Class VIII  
📧 viktor.devanathan.highschool@buditel.bg

**Supervisor:** Nikolay Nikolov Palashev — Lecturer  
📧 nikolai.palashev@buditel.bg

---

## 📄 Licence

This project is open source. 3D assets from Sketchfab are used under their respective free licences. Please refer to individual asset pages for specific terms.

---

> *"Virtual Museum of Bulgaria is not just a technical project — it is a contribution to promoting Bulgarian history and heritage among present and future generations, realised through the tools of modern technology."*
