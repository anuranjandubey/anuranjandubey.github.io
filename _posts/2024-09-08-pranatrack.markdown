---
title: "PranaTrack"
layout: post
date: 2024-09-08 09:00:00 -0700
projects: true
category: project
externalLink: https://github.com/almique/Project-1-Context-Monitoring-App
description: "Jetpack Compose health monitor capturing heart rate, respiratory rate, and symptom journaling on-device."
tag:
  - Android
  - Jetpack Compose
  - Mobile Health
  - Sensors
---

## Overview

PranaTrack is an Android context-monitoring application that pairs camera-based photoplethysmography (PPG) with on-device sensors and local persistence to help people understand their wellbeing without leaving the handset. The experience is built entirely with Jetpack Compose and modern Android architecture components.

## Key Features

- **Camera-based heart rate** via fingertip videos analyzed inside `HealthViewModel` to estimate beats per minute.
- **Accelerometer-driven respiration** using `respiratoryRateCalculator()` to capture 45-second samples and calculate breaths per minute.
- **Symptom journaling** that records self-reported symptoms and intensity sliders through `SymptomsViewModel`.
- **Local session history** persisted in the `HealthData` SQLite table managed by `AppDatabase` for retrieval or export.
- **Material Design UI** implemented with `HealthTrackerScreen()`, `SymptomsScreen()`, and Navigation Compose.

## App Flow

1. Launch to `HealthTrackerScreen()` for the primary vitals dashboard.
2. Tap **Record Video** to grant camera permission and capture a fingertip clip for heart-rate analysis.
3. Hit **Start Measurement** to begin accelerometer collection and the 45-second respiratory countdown.
4. Choose **Next** to visit the symptoms page, pick relevant symptoms, and rate intensity.
5. Select **Save Symptoms** to persist the full session (heart rate, respiratory rate, symptom scores) locally.

## Architecture Notes

- `MainActivity.kt` wires Compose navigation and view models.
- `HealthViewModel` manages sensor lifecycle, timers, video frame parsing, and data persistence.
- `SymptomsViewModel` steers symptom options, slider state, and form submission.
- `AppDatabase.kt` extends `SQLiteOpenHelper`, creating the `HealthData` table and handling schema upgrades.
- Resources in `app/src/main/res/` provide theming, icons, backup rules, and `file_paths` definitions.

## Tooling & Requirements

- Android Studio Giraffe (2022.3.1) or newer with Kotlin DSL support.
- Android SDK Platform 34, build tools, and a physical Android device with camera and accelerometer.
- Minimum OS level Android 10 (API 29).

## Permissions

`android.permission.CAMERA` for PPG capture, `android.permission.BODY_SENSORS` for accelerometer access, plus optional `RECORD_AUDIO` and `WRITE_EXTERNAL_STORAGE` declarations that can be trimmed if unused.

## Troubleshooting & Testing

- Validate heart-rate capture on real hardware; ensure the fingertip covers the lens and flash.
- Hold the device steady during respiration sampling to avoid zero readings.
- Inspect persisted sessions by pulling `HealthTrackerDatabase.db` from `/data/data/com.example.pranatrack/databases/`.
- Extend instrumentation tests under `app/src/androidTest/` for database and sensor workflows.
