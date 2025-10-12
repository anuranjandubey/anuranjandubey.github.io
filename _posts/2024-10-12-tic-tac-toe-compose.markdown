---
title: "Tic-Tac-Toe (Jetpack Compose)"
layout: post
date: 2024-10-12 12:00:00 -0700
projects: true
category: project
externalLink: https://github.com/almique/project_app
description: "Compose-first Tic-Tac-Toe with AI, local, and Bluetooth multiplayer plus persistent match history."
tag:
  - Android
  - Jetpack Compose
  - Bluetooth
  - Game Dev
---

## Overview

A modern Jetpack Compose spin on Tic-Tac-Toe featuring adaptive AI opponents, local two-player mode, and Bluetooth peer-to-peer sessions. Match outcomes persist with Room so players can review their history and adjust settings to tailor the experience.

## Features

- **Single-player AI** with EASY, MEDIUM, and HARD difficulties powered by a minimax algorithm enhanced with alpha-beta pruning.
- **Local multiplayer** pass-and-play flow with turn indicators and distinct board coloring.
- **Bluetooth multiplayer** that discovers paired devices, hosts or joins sessions, and syncs game state via RFCOMM sockets.
- **Persistent history** using Room entities, `GameResultDao`, and `PastGamesScreen()` for browsing prior matches.
- **Customizable settings** to pick opponent type, tweak difficulty, and reset boards instantly.

## Tech Stack

- UI built with Jetpack Compose, Material3, and Navigation Compose orchestrated by `MainActivity`.
- State handled through `ViewModel`, `StateFlow`, and Kotlin coroutines across `GameViewModel`, `SettingsViewModel`, `BluetoothViewModel`, and `PastGamesViewModel`.
- Persistence managed by a Room database (`AppDatabase`, `GameResultDao`) storing match summaries.
- Bluetooth multiplayer implemented with classic Bluetooth APIs, RFCOMM sockets, and JSON payloads.

## Structure

- Core Kotlin sources under `app/src/main/java/` encompassing composables, view models, Room entities, and Bluetooth logic.
- Resources in `app/src/main/res/` for theming, icons, and localized strings.
- Module configuration in `app/build.gradle.kts` enabling Compose and declaring dependencies.

## Prerequisites

- Android Studio Iguana (2023.2.1) or newer with the matching AGP and Gradle wrapper.
- JDK 17 (bundled with recent Android Studio versions).
- Device or emulator running Android 10 (API 29) or above.
- Bluetooth-capable hardware and permissions for remote matches.

## Getting Started

1. Clone the repository and open it in Android Studio.
2. Sync Gradle to resolve Compose, Room, and Navigation dependencies.
3. Run on a device or emulator via the Run configuration.

### Command line build

- `./gradlew assembleDebug`
- `./gradlew installDebug`
- `./gradlew connectedAndroidTest`

## Usage Tips

- Switch modes with the settings screen to select AI, local, or Bluetooth play and adjust difficulty.
- Pair devices in system settings before attempting Bluetooth connections.
- Review completed matches in the Past Games tab with timestamps and difficulty context.

## Testing & Contribution

- Add unit tests under `app/src/test/` and instrumented Compose/database tests under `app/src/androidTest/`.
- Follow Kotlin style guidelines and keep UI logic inside composables backed by ViewModel state.
- Run `./gradlew lintDebug testDebugUnitTest` before submitting changes.
