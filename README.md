# Unity 6.7 Beta - Vulkan x Depth Texture x MSAA on Meta Quest Bug
In Unity Versions 2022.3.4f (pre security patch) and before, the Meta Quest ran Vulkan with Depth Texture and MSAA *much* more efficiently than in following versions.

The goal of this project is to demonstrate the discrepancy in performance between these two versions of Unity with identical setups, hopefully spurring the Unity team to make Vulkan perform better with MSAA x Depth Texture.

Why is this important? Because many Meta Quest games use MSAA (it's very important) and the depth texture. It's a big hit to have to decide one or the other, or use OpenGL. Meta considers OpenGL to be legacy.

This project has two branches:
- `2022.3.4f` which has the project in Unity version 2022.3.4f, pre security patch.
- `main`, which has the project in Unity version 6.7 Beta.

## How to reproduce bug?
1. Download repository
2. Open the project in Unity 6.7
3. Build to the Meta Quest (ensure that you have the Android platform target)
4. Record the FPS using OVR Metrics or another tool.
5. Switch branch to `2022.3.4f`
6. Build to the Meta Quest.
7. Record the FPS using OVR Metrics or another tool.
8. Compare the FPS.
Unity 6.7 performs much worse than Unity 2022.3.4f. This should not be. It should be the other way around.

#BetaSweepstakes_6_7
