# UE5 Scroll Walking Character (C++)

Small Unreal Engine 5 gameplay prototype demonstrating a scroll-based character movement system implemented in C++ using the **Enhanced Input System**.

The feature allows the player to dynamically control the character's walking speed with the mouse wheel, similar to movement systems found in games such as *Star Citizen*.  
Speed adjustments are applied in small configurable steps and clamped between defined minimum and maximum values.

---

## Features

- Mouse wheel controlled walking speed
- Configurable speed range (min / max)
- Adjustable step size for fine speed control
- Integration with Unreal Engine's **CharacterMovementComponent**
- Implemented using **UE5 Enhanced Input**
- Clean separation between input handling and movement logic

---

## Controls

| Input | Action |
|------|------|
| W / A / S / D | Move character |
| Mouse | Camera look |
| Mouse Wheel Up | Increase walking speed |
| Mouse Wheel Down | Decrease walking speed |
| Space | Jump |

---

## Implementation Details

The movement speed system modifies the `MaxWalkSpeed` property of the `CharacterMovementComponent`.

Each scroll input event adjusts the current speed value using a configurable step size:

WalkSpeedCurrent = Clamp(
WalkSpeedCurrent ± WalkSpeedStep,
WalkSpeedMin,
WalkSpeedMax
)


This ensures the movement speed always remains within a defined range while allowing smooth player-controlled adjustments.

The implementation uses Unreal Engine's **Enhanced Input framework**, with input actions bound in `SetupPlayerInputComponent`.

---

## Relevant Source Files

ScrollWalkingCharacter.h
ScrollWalkingCharacter.cpp


These files contain the full implementation of the scroll-based movement system and input handling.

---

## Engine Version

Developed using: Unreal Engine 5.7.3


---

## Purpose

This repository is intended as a small **gameplay programming sample** demonstrating:

- C++ gameplay logic in Unreal Engine
- Enhanced Input integration
- Character movement system customization
