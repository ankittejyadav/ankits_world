---
tagline: "A high-performance, interactive 3D portfolio engine leveraging React Three Fiber and WebGL for immersive client-side experiences."
role: "Lead Creative Technologist & Frontend Architect"
status: "production"
stack:
  - React.js
  - Three.js
  - React Three Fiber (R3F)
  - WebGL / GLSL
  - JavaScript (ES6+)
  - HTML5 / CSS3
highlights:
  - "Optimized 3D asset delivery pipeline, reducing initial payload size by 90% through Draco compression and progressive loading."
  - "Engineered a decoupled state synchronization layer between the React DOM UI and the high-frequency Three.js render loop to maintain 60 FPS."
---

## 🌟 Architectural Vision & System Design

The architecture of `ankits_world` is designed to bridge the gap between declarative UI state management (React) and imperative, high-performance 3D graphics rendering (Three.js/WebGL). Rather than treating the 3D scene as a black box, the system is architected as a unified, state-driven interactive application where the DOM and the WebGL context communicate seamlessly without causing performance bottlenecks.

```
┌─────────────────────────────────────────────────────────────────┐
│                        React DOM Layer                          │
│     (UI Overlays, Navigation, Accessibility, State Management)   │
└────────────────────────────────┬────────────────────────────────┘
                                 │
                    State Sync / Event Handlers
                                 │
                                 ▼
┌─────────────────────────────────────────────────────────────────┐
│                   React Three Fiber Bridge                      │
│     (Declarative Scene Graph, Lifecycle & Context Management)   │
└────────────────────────────────┬────────────────────────────────┘
                                 │
                     High-Frequency Render Loop
                                 │
                                 ▼
┌─────────────────────────────────────────────────────────────────┐
│                       Three.js Engine                           │
│     (WebGL Renderer, Shaders, Raycasting, Camera Controllers)   │
└────────────────