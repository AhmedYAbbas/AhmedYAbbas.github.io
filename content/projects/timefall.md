---
title: 'Timefall'
date: "2023-07-06"
cover: 
    image: Images/timefall.png
    alt: 'Timefall - Game Engine'
    caption: 'Timefall - Game Engine'
tags: ["C++", "OpenGL", "Vulkan", "C#", "Premake"]
categories: [Programming, Game Engines]
---

# Timefall (flagship)

Timefall is a game engine built from scratch in C++, originally inspired by [The Cherno's Game Engine Series](https://www.youtube.com/playlist?list=PLlrATfBNZ98dC-V-N3m0Go4deliWHPFwT) and developed well beyond it since. The goal: a Windows-first engine with AAA-grade rendering quality, an editor workflow comparable to commercial tools, and a C#-scripted gameplay layer.

## Renderer
A forward 3D PBR pipeline: metallic-roughness Cook-Torrance lighting (GGX/Smith/Schlick), energy compensation, geometric specular anti-aliasing, and normal mapping. Image-based lighting from HDR environment maps with prefiltered specular and diffuse irradiance convolution. Shadows for all three light types — cascaded shadow maps (up to 4 cascades) for directional lights, plus spot and point (cubemap) shadows, each with hard and PCSS soft-shadow modes. A full HDR pipeline with multiple tonemap operators (Reinhard, ACES, AgX, and more), alongside a 2D batch renderer running in parallel.

## Scene & Scripting
An entt-based ECS with a full scene graph, and C# gameplay scripting (.NET 9, hosted in-process via hostfxr) with assembly hot-reload, covering transforms, components, input, and 2D physics via Box2D.

## Editor
A full Dear ImGui editor: scene hierarchy, inspector, content browser, a viewport with gizmos and entity picking, Edit/Play/Simulate states, and a real-time profiler (Tracy-based CPU/GPU profiling with VRAM tracking).

To stress-test the engine end-to-end, I built a complete Tetris clone on top of it — every gameplay system implemented in pure C# script against the engine's API, with zero engine changes required.

![Timefall - PBR lighting and shadows](/Images/timefall_pbr_scene.png)

***

[GitHub →](https://github.com/AhmedYAbbas/Timefall)
