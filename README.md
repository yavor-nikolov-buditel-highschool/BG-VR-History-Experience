
---

# Virtual Museum of Bulgarian History

### Interactive VR Educational Platform

An immersive **Virtual Reality (VR) application** that enables users to explore Bulgarian history through an interactive 3D museum environment. The platform combines historical content, real-time interaction, and spatial audio to create a modern educational experience.

---

# 🚀 Getting Started

## Running the Application

Follow these steps to launch the project:

### 1. Clone the Repository

```bash
git clone https://github.com/yavor-nikolov-buditel-highschool/BG-VR-History-Experience.git
```

### 2. Navigate to the Build Directory

Locate the compiled build inside the repository.

### 3. Run the Executable

Start the application by launching:

```
bulgaria museum the virtual experience.exe
```

> ⚠️ Ensure all `.dll` files and the `_Data` folder are in the same directory as the executable.

---

## 🖥️ System Requirements

### Hardware

* VR Headset: **Oculus Quest 2 (recommended)**
* PC capable of running VR applications

### Performance Targets

* **Target FPS:** 72 FPS
* **Observed FPS:** 60–90 FPS
* **Build Size:** ~1.6 GB

---

# 🧭 Project Overview

The application recreates a **virtual museum space** where users can:

* Move freely using VR locomotion
* Interact with historical artifacts
* Explore curated exhibitions
* Listen to contextual audio narration

---

# 🏛️ Exhibitions

### Shipka Epic

* *The Volunteers at Shipka*
* *The Battle of Shipka*

### Panagyurishte Treasure

* Interactive artifacts
* Detailed 3D ceremonial vessel

### Bulgaria During World War II

Each exhibition includes **audio guides** triggered by proximity.

---

# 🧩 Architecture

The system follows a **modular architecture**, designed for scalability and maintainability.

### Core Modules

#### Navigation Module

* Teleport movement
* Smooth locomotion

#### Interaction Module

* Object manipulation via VR controllers
* Artifact inspection

#### Audio Module

* Trigger-based narration
* Uses `OnTriggerEnter()` with Audio Sources

#### Scene Management

```csharp
SceneManager.LoadSceneAsync();
```

#### UI Module

* Main menu
* Settings interface

#### Data Module

* Exhibit metadata
* Audio assets
* Configuration

---

# 🛠️ Technologies

* Unity 6000.2.14f1
* C#
* XR Interaction Toolkit
* Action-based Input System
* XR Origin
* Unity Profiler
* Light Baking
* GitHub Version Control

---

# ⚙️ Features

## Main Menu

* Start experience
* Adjust audio settings
* Exit application

## In-Experience

* Explore multiple exhibition halls
* Activate audio guides
* Interact with 3D objects
* Switch movement modes

---

# ⚡ Performance Optimization

To ensure a smooth VR experience:

* Fully baked lighting
* Lightmaps
* Optimized meshes
* Profiling via Unity Profiler

---

# 🎨 Assets

### Custom

* UI panels
* Museum architecture

### External

* Sketchfab models
* Unity Asset Store assets

All assets are used בהתאם their respective licenses.

---

# 👥 Target Users

* Students
* Teachers
* Museums
* History enthusiasts
* Cultural institutions

---

# 🔮 Future Development

* AI-powered virtual guide
* Multilingual support (Bulgarian / English)
* WebVR version
* Additional exhibitions
* Interactive historical simulations

---

# 👨‍💻 Authors

**Yavor Nikolov**
Private High School of Digital Sciences "SoftUni Buditel"

**Viktor Devanathan**
Private High School of Digital Sciences "SoftUni Buditel"

---

# 🎓 Supervisor

**Nikolay Palashev**
Teacher

---

# 📌 Summary

This project demonstrates how **Virtual Reality can transform education** by combining:

* Interactive 3D environments
* Immersive storytelling
* Modular software architecture

The system is designed for **future expansion**, making it a scalable platform for presenting Bulgarian cultural heritage.

---
