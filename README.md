## ⛏️ Mini Craft: 3D Third-Person Character Replicate

A lightweight, high-performance, and "free-to-use" 3D Minecraft-style character controller built using Three.js. This project features a modular humanoid model constructed entirely from geometric primitives, complete with a third-person camera system, smooth movement physics, and procedural limb animations.

---

## 🚀 Live Features

Modular Character Model: A detailed "Blocky" humanoid including a torso, head (with hair, eyes, and pupils), limbs, and a belt with a buckle.

Third-Person Orbit Controls: Intelligent camera that follows the player with smooth damping and zoom constraints.

Procedural Animation:

Dynamic walking cycle (opposite arm/leg swinging).

Natural "body bob" effect while moving.

Smooth rotation lerping (character faces the direction of travel).

Interactive HUD: Real-time keyboard visualizer (WASD) and control hints.

Environment: A stylized grass field with a grid helper, fog effects, and randomly generated block towers.

Responsive Design: Auto-adjusts to any screen size or orientation.

---

## 🕹️ Controls

Action

Control

Move

W A S D or Arrow Keys

Orbit Camera

Left Click + Drag

Zoom

Scroll Wheel

Pan Camera

Right Click + Drag

---

## 🛠️ Technical Implementation

Character Architecture

The character is a THREE.Group containing several sub-groups. This allows for hierarchical animation (e.g., rotating an arm group around a shoulder pivot point).

// Example of the limb pivot logic used in the project
const leftArm = new THREE.Group();
leftArm.position.set(-0.56, 2.25, 0); // Shoulder Pivot
leftArm.add(mkBox(0.31, 0.45, 0.31, MAT.shirt, 0, -0.22, 0)); // Offset part
player.add(leftArm);


Dependencies

Three.js (r128): Core 3D engine.

OrbitControls.js: For the orbital camera system.

Lighting & Atmosphere

Directional Light: Acts as a "Sun" with high-resolution shadow mapping (PCFSoft).

Ambient Light: Provides soft fill light to prevent pitch-black shadows.

Fog: Exponential fog used to create depth and hide the edges of the 70x70 grid.


---

## 📂 Installation & Usage

Since this is a single-file implementation, you can run it directly:

Copy the code into an index.html file.

Open the file in any modern web browser.

No build tools or local servers are required as dependencies are pulled via CDN.

---

## 📜 License & Usage

Free Public Use: This character model and controller logic are free to use for personal and commercial projects.

You may modify the MAT (Material Palette) object to change skin tones, clothing colors, or hair styles.

You can extend the animate() loop to add jumping, crouching, or tool-swinging animations.

---

## 📜AUTHOR

®TSCreates

Github: https://github.com/digitalguidance0-star
Built with ❤️ for the 3D Web Community.
