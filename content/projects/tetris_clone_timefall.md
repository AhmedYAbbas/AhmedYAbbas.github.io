---
title: 'TetrisClone-Timefall'
date: "2026-08-04"
weight: 2
cover: 
    image: Images/tetris_clone_timefall.png
    alt: 'TetrisClone-Timefall'
    caption: 'TetrisClone-Timefall'
tags: ["C#", "Timefall"]
categories: [Programming, Game Engines]
---

# TetrisClone-Timefall

A guideline-inspired Tetris implementation built in C# on top of [Timefall](/projects/timefall/) — created as a full, non-trivial game to stress-test the scripting layer end-to-end. Every gameplay system (piece spawning, movement, rotation, line clears, scoring) is pure C# scripting against the engine's entity API. The rule during development: if a feature needed a new engine capability, that capability got added as a generic, reusable engine system — never a Tetris-specific workaround.

Implements the real ruleset: 7-bag randomizer, SRS rotation with wall/floor kicks, DAS/ARR movement tuning, lock delay, hold piece, a 5-piece next queue, ghost piece, and level-scaling gravity.

![TetrisClone-Timefall gameplay](/Images/tetris_clone_timefall.png)

***

[GitHub →](https://github.com/AhmedYAbbas/TetrisClone-Timefall)
