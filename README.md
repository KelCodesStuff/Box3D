# Box3D
Box3D is an open-source 3D physics engine, built upon the well-known Box2D physics engine, offering a robust and community-driven solution for 3D game and simulation development.

[![CircleCI](https://dl.circleci.com/status-badge/img/gh/KelCodesStuff/Box3D/tree/main.svg?style=shield)](https://dl.circleci.com/status-badge/redirect/gh/KelCodesStuff/Box3D/tree/main)

## Roadmap

This section outlines the planned features for Box3D.

*   **Rigid Body Simulation:**
    *   Sphere
    *   Box
    *   Capsule
    *   Cylinder
    *   Convex hull
    *   Plane
    *   Compound
    *   Mesh (triangle)
    *   Terrain (height field)

*   **Constraint Simulation:**
    *   Fixed
    *   Point
    *   Distance (including springs)
    *   Hinge
    *   Slider (also called prismatic)
    *   Cone
    *   Rack and pinion
    *   Gear
    *   Pulley

*   **Collision Detection:**
    *   Casting rays
    *   Testing shapes vs shapes
    *   Casting a shape vs another shape.

*   **Advanced Features:**
    *   Animated Ragdolls
        *   Hard keying (kinematic only rigid bodies)
        *   Soft keying (setting velocities on dynamic rigid bodies)
        *   Driving constraint motors to an animated pose
        *   Mapping a high detail (animation) skeleton onto a low detail (ragdoll) skeleton and vice versa
    *   Soft Body Simulation
        *   Edge constraints
        *   Dihedral bend constraints
        *   Tetrahedron volume constraints
        *   Long range attachment constraints (also called tethers)
        *   Limiting the simulation to stay within a certain range of a skinned vertex
        *   Internal pressure
        *   Collision with simulated rigid bodies
        *   Collision tests against soft bodies
    *   Water buoyancy calculations

## Current Status

Box3D is in early development.

## Compatibility

Currently supports macOS. Builds with CMake and Clang. Cross-platform support (Windows, Linux) is planned for the future.

## Building for Xcode
- Install [CMake](https://cmake.org)
- Add Cmake to the path in .zsh `export PATH="/Applications/CMake.app/Contents/bin:$PATH"`
- cd to the cloned project
- mkdir build
- cd build
- cmake -G Xcode ..
- open Box3D.xcodeproj
- Select the samples scheme
- Run the samples

## Documentation

*   [Manual](https://box3D.org/documentation/)

## Community

*   [Discord](YOUR_DISCORD_LINK_HERE)

## License

Box3D is actively developed by Kel Reid and uses the [MIT license](https://en.wikipedia.org/wiki/MIT_License).

## Sponsorship

Support the development of Box3D through [GitHub Sponsors](https://github.com/sponsors/kelcodesstuff).

Please consider starring this repository and subscribing to my [YouTube channel](https://www.youtube.com/@kelcodes).
