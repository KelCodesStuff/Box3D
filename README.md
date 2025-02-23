# Box3D 
### A 3D Physics Engine for Game Development

[![Build and Test](https://github.com/KelCodesStuff/Box3D/actions/workflows/build.yml/badge.svg?branch=main)](https://github.com/KelCodesStuff/Box3D/actions/workflows/build.yml)

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE) 
## Introduction

Box3D is a 3D physics engine built as a learning project, forked from the well known 2D physics engine [Box2D](https://box2d.org/).  It's designed to be a hands-on way to understand the fundamentals of rigid body dynamics, collision detection, constraint solving, and 3D math in the context of game and simulation development.

## Goals

*   **Learning:** The primary goal is to deeply understand the core principles of 3D physics engines.
*   **Extensibility:** To build a foundation that can be extended with more advanced features.
*   **Understandable Code:** To maintain a codebase that is well-commented and relatively easy to follow (compared to highly optimized production engines).
*   **Visualization:** To provide a basic testbed for visualizing the physics simulation.

## Features (Current and Planned)

*   **Rigid Body Dynamics:**
    *   3D vectors, matrices, and quaternions for representing position, orientation, and transformations.
    *   Dynamic, static, and kinematic bodies.
    *   Linear and angular velocity and acceleration.
    *   Application of forces and impulses.


* **Collision Detection:**
    *   **Broadphase:** Dynamic AABB tree for efficient collision culling.
    *   **Narrowphase:**
        *   Sphere-Sphere
        *   Sphere-AABB
        *   AABB-AABB
        *   Box-Box (Oriented Bounding Boxes) using Separating Axis Theorem (SAT).
        *   Convex Hull-Convex Hull (using GJK and EPA - **Planned/In Progress**).
    *   Contact manifold generation (contact point, normal, penetration depth).

  
* **Constraint Solving:**
    *   Iterative constraint solver (Sequential Impulses - based on Box2D's approach).
    *   **Joints:**
        *   Distance Joint (3D)
        *   Revolute Joint (3D)
        *   Prismatic Joint (3D)
        *   More joint types (Planned)


*   **Integration:**
    *   Euler, Verlet, and Runge-Kutta (RK4) integrators (selectable).


*   **Testbed:**
    *   Basic 3D visualization using OpenGL (and GLFW or SDL).
    *   Interactive controls for creating and manipulating bodies.


* **Planned:**
    *	Continuous Collision Detection (CCD)
    *	Restitution (Bounciness)
    *	Friction
    *	Sleeping (Deactivating bodies that are at rest)
    *	Raycasting

## Dependencies

*   CMake (3.10 or higher): For generating build files.
*   C++ Compiler (C++11 or higher):  A modern C++ compiler (e.g., GCC, Clang, MSVC).
*   OpenGL: For 3D visualization.

## Building and Running for Xcode

1. Install CMake 
2. Clone the Repository:
    ```bash
    git clone https://github.com/KelCodesStuff/Box3D
    cd Box3D
    ```

3.  Generate Build Files (CMake):
    ```bash
    mkdir build
    cd build
    cmake -G Xcode ..
    ```
    
4. Open the box3d.xcodeproj in Xcode
5. Select and run the samples scheme 

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details. (Box2D itself is under the zlib license, which is very permissive. You should check the Box2D license if you are basing your work on it.)

## Acknowledgements

*   **Erin Catto:**  The creator of Box2D, whose work inspired this project.
*   **The Box2D Community:**  For providing a wealth of information and resources.
