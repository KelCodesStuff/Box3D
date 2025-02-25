# Box3D

### A 3D Physics Engine for Game Development

[![Build and Test](https://github.com/KelCodesStuff/Box3D/actions/workflows/build.yml/badge.svg?branch=main)](https://github.com/KelCodesStuff/Box3D/actions/workflows/build.yml)

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

## Introduction

Box3D is a 3D physics engine built as a learning project, forked from the well known 2D physics
engine [Box2D](https://box2d.org/). It's designed to be a hands-on way to understand the fundamentals of rigid body
dynamics, collision detection, constraint solving, and 3D math in the context of game and simulation development.

## Goals

* **Learning:** The primary goal is to deeply understand the core principles of 3D physics engines.
* **Extensibility:** To build a foundation that can be extended with more advanced features.
* **Understandable Code:** To maintain a codebase that is well-commented and relatively easy to follow (compared to
  highly optimized production engines).
* **Visualization:** To provide a basic testbed for visualizing the physics simulation.

## Features (Current and Planned)

* **Rigid Body Dynamics:**
    * 3D vectors, matrices, and quaternions (using GLM) for representing position, orientation, and transformations.
    * Dynamic, static, and kinematic bodies.
    * Linear and angular velocity and acceleration.
    * Application of forces and impulses.


* **Collision Detection:**
    * **Broadphase:** Dynamic AABB tree for efficient collision culling.
    * **Narrowphase:**
        * Sphere-Sphere
        * Sphere-AABB
        * AABB-AABB
        * Box-Box (Oriented Bounding Boxes) using Separating Axis Theorem (SAT).


* **Constraint Solving:**
    * Iterative constraint solver (Sequential Impulses - based on Box2D's approach).
    * **Joints:**
        * Distance Joint (3D) - *In progress*
        * Revolute Joint (3D) - *In progress*
        * Prismatic Joint (3D) - *In progress*


* **Integration:**
    * Euler, Verlet, and Runge-Kutta (RK4) integrators (selectable).


* **Testbed:**
    * Basic 3D visualization using SDL2.
    * Interactive controls for creating and manipulating bodies (planned).
    * Uses a `Box3D::DebugDraw` class for rendering the simulation state.

## Roadmap (Planned Features)

* Convex Hull-Convex Hull collision detection (using GJK and EPA).
* More joint types.
* Continuous Collision Detection (CCD).
* Restitution (Bounciness).
* Friction.
* Sleeping (Deactivating bodies that are at rest).
* Raycasting.
* Interactive controls
---
## Build Instructions

Box3D uses CMake as its build system. This allows for cross-platform builds.

### Prerequisites

Before building, ensure you have the following installed:

* **CMake:** (version 3.17 or higher) - Download from [https://cmake.org/download/](https://cmake.org/download/)
* **C++ Compiler:**  A C++17 compatible compiler (e.g., GCC, Clang, MSVC). This is often already installed on your
  system.
* **SDL2:**  For visualization and input. Installation instructions are platform-specific (see below).
* **GLM:**  For 3D vector, matrix, and quaternion math. GLM is a header-only library, so no separate build is required,
  but you need to make it available to your
  compiler.  [https://glm.g-truc.net/](https://glm.g-truc.net/) ([GitHub](https://github.com/g-truc/glm))

### Xcode

```bash
  git clone https://github.com/KelCodesStuff/Box3D.git
  cd Box3D
  mkdir build
  cd build
  cmake -G Xcode ..
  
  Open `box3d.xcodeproj` in Xcode
  Select the `samples` scheme and run
```

### CLion
1. Open Project in CLion, choose "Open or Import" and select the `Box3D` directory (containing
       `CMakeLists.txt`).
2. Configure Toolchain Go to `File -> Settings` (or `CLion -> Preferences` on macOS), then
   `Build, Execution, Deployment -> Toolchains`. Ensure a C++ compiler is selected.
3. Build: Select `Build -> Build Project`.
4. Run 'samples':
     Go to `Run -> Edit Configurations...`.
    * Add a new "CMake Application" configuration.
    * Set "Target" to `samples`.
    * Set "Executable" to the compiled `samples` executable (in the build directory).
    * Click "OK" and run the configuration.


## License

This project uses the [MIT License](LICENSE).

## Acknowledgements

*   Erin Catto:  The creator of Box2D, whose work inspired this project.
*   The Box2D Community:  For providing a wealth of information and resources.
