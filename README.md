# Delivery Dash 

A 2D top-down arcade driving and package-delivery game built with **Unity 6** and **C#**. Players navigate city streets, pick up packages, avoid obstacles, and deliver parcels to target drop-off zones.

---

## Gameplay & Core Mechanics

* **2D Vehicle Movement & Steering (`Driver.cs`):** Smooth top-down car physics utilizing Unity's Input System and frame-rate independent movement (`Time.deltaTime`), featuring dynamic speed boosts and collision slowdowns.
* **Package Pickup & Delivery Loop (`Delivery.cs`):** Trigger-based collision detection (`OnTriggerEnter2D` / `OnCollisionEnter2D`) managing package state, preventing multiple pickups at once, and updating vehicle sprite colors for clear visual feedback.
* **Camera Tracking:** Smooth player follow-camera configured with **Cinemachine** and **Universal Render Pipeline (URP) 2D**.

---

## Tech Stack

* **Game Engine:** Unity `6000.4.10f1` (Unity 6)
* **Language:** C# (`.NET Standard 2.1`)
* **Key Unity Systems:** 2D Physics (`Rigidbody2D`, `Collider2D`), Unity Input System, Cinemachine, URP 2D, TextMeshPro

---

## Controls

| Action | Key Binding |
| :--- | :--- |
| **Accelerate / Reverse** | `W` / `S` or `Up` / `Down` Arrow |
| **Steer Left / Right** | `A` / `D` or `Left` / `Right` Arrow |

---

## Project Structure

```text
Assets/
├── Scripts/
│   ├── Driver.cs        # Handles steering, acceleration, boost pads, and bump penalties
│   └── Delivery.cs      # Manages package pickup/drop-off triggers and visual state changes
├── Scenes/              # Main playable game levels
├── Prefabs/             # Reusable car, package, customer, and environment prefabs
└── Settings/            # URP 2D renderer and input action assets
