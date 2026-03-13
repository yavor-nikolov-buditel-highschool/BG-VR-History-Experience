\# Virtual Museum of Bulgarian History

\### Interactive VR Educational Platform



\*\*Project ID:\*\* 299  



An interactive \*\*Virtual Reality (VR) educational platform\*\* that allows users to explore Bulgarian history inside an immersive 3D museum environment.



The project recreates a \*\*virtual museum space\*\* where visitors can freely move, interact with historical exhibits, and listen to audio information about them.



The goal of the project is to create a \*\*new type of educational experience\*\* that combines historical knowledge, interactivity, and modern visualization technologies.



---



\# Overview



The Virtual Museum includes several thematic exhibitions:



\### Shipka Epic

Historical paintings such as:

\- \*The Volunteers at Shipka\*

\- \*The Battle of Shipka\*



\### Panagyurishte Treasure

\- Interactive artifacts

\- 3D model of the main ceremonial vessel



\### Bulgaria During World War II



Inside each exhibition room, users can activate \*\*audio recordings\*\* that provide historical context and explanations.



---



\# Technologies Used



\- \*\*Unity 6000.2.14f1\*\*

\- \*\*C#\*\*

\- \*\*XR Interaction Toolkit\*\*

\- \*\*Action-based Input System\*\*

\- \*\*XR Origin\*\*

\- \*\*Unity Profiler\*\*

\- \*\*Light Baking\*\*

\- \*\*GitHub Version Control\*\*



\### Hardware

\- \*\*Oculus Quest 2\*\*



---



\# Project Architecture



The system is built using a \*\*modular architecture\*\*, which allows easy expansion and maintainability.



Main modules:



\### Navigation Module

Handles movement inside the VR environment.



Supported movement methods:

\- Teleport navigation

\- Smooth locomotion



\### Interaction Module

Allows interaction with 3D objects using VR controllers.



Users can:

\- Pick up objects

\- Examine artifacts

\- Trigger interactions



Example:  

Users can grab and inspect the \*\*Panagyurishte treasure vessel\*\* in 3D.



\### Audio Module

Plays historical narration when the user approaches an exhibit.



Implementation:

\- Trigger zones using \*\*Box Colliders\*\*

\- `OnTriggerEnter()` activates the \*\*Audio Source\*\*



\### Scene Management Module

Handles loading of scenes using asynchronous loading.



```



SceneManager.LoadSceneAsync()



```



\### UI Module

Responsible for:



\- Main menu

\- Settings

\- System interface



\### Data Module

Stores information about:



\- Exhibits

\- Audio files

\- Configuration settings



---



\# Development Process



\## 1. Research and Concept

Initial analysis of existing \*\*VR museum experiences worldwide\*\*.



The project was inspired by virtual exhibitions used in major international museums.



The idea was adapted to present \*\*Bulgarian history and cultural heritage\*\*.



---



\## 2. Architecture Design



The system was designed using a \*\*modular architecture\*\* to allow:



\- Easy maintenance

\- Expansion with new exhibitions

\- Rapid feature implementation



---



\## 3. Development



Main development tasks included:



\- Creating virtual museum spaces

\- Integrating 3D models

\- Developing object interaction systems

\- Implementing audio information triggers

\- Implementing VR navigation

\- Performance optimization



---



\## 4. Testing



Usability testing was performed with users \*\*without prior VR experience\*\*.



Testing helped improve:



\- Navigation

\- Interface

\- Interaction mechanics



Special attention was given to \*\*VR motion sickness\*\*, which led to the implementation of two movement systems:



\- Standard movement

\- Teleport navigation



---



\# Performance Optimization



VR applications require \*\*high and stable FPS\*\* to prevent user discomfort.



Optimization techniques used:



\- Fully baked lighting

\- Lightmaps

\- Optimized meshes

\- Unity Profiler performance analysis



\### Performance Metrics



| Metric | Value |

|------|------|

| PC FPS | 60–90 FPS |

| Target FPS | 72 FPS |

| Build Size | ~1.6 GB |



---



\# Application Features



\### Main Menu

Users can:



\- Start the virtual museum

\- Adjust audio settings

\- Exit the application



\### Inside the Museum

Users can:



\- Explore multiple exhibition halls

\- Activate audio guides

\- Interact with artifacts

\- Navigate using teleport or locomotion



---



\# 3D Assets



Two types of assets are used:



\### Custom Models

\- UI panels

\- Parts of the museum architecture



\### External Resources

\- Sketchfab models

\- Unity Asset Store assets



All assets are used according to their respective licenses.



---



\# Target Users



The system can be used by:



\- Students

\- Teachers

\- Museums

\- History enthusiasts

\- Cultural institutions



---



\# Marketing Strategy



The project is promoted through social media platforms:



\- TikTok

\- Instagram

\- YouTube



The content strategy uses \*\*short-form video hooks\*\* to capture audience attention in the first seconds of the video.



Platform-specific hashtags are also used to improve reach.



---



\# Future Development



Potential future features include:



\- AI-powered virtual museum guide

\- Multilingual audio support (Bulgarian / English)

\- WebVR version

\- Additional historical exhibitions

\- Interactive historical simulations where users can "enter" historical paintings



---



\# Conclusion



The project demonstrates the potential of \*\*Virtual Reality as a tool for education and cultural presentation\*\*.



The platform combines:



\- Interactive 3D environments

\- Educational audio content

\- VR interaction systems

\- Modular software architecture



The flexible architecture allows the project to be expanded with new exhibitions, artifacts, and features.



The long-term goal is to \*\*modernize the way Bulgarian history is presented and learned\*\*, making it accessible to both local and international audiences.



---



\# Authors



\*\*Yavor Nikolov\*\*  

Private High School of Digital Sciences "SoftUni Buditel"  



\*\*Viktor Devanathan\*\*  

Private High School of Digital Sciences "SoftUni Buditel"



---



\# Supervisor



\*\*Nikolay Palashev\*\*  

Teacher  







