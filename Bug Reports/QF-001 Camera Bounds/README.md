# QF-001 - Camera Bounds Fail to Reset When Transitioning Rootward → Lunareth

---

## Project Information

| Property | Value |
|----------|-------|
| **Project** | Quantum Flip |
| **Report ID** | QF-001 |
| **Status** | Open |
| **Reported By** | Nathanial Birdseye |
| **Date** | July 26, 2026 |
| **Game Build** | Prototype 0.0.1 |
| **Unity Version** | 2022.3.5f1 |

---

## Environment

- Unity Editor
- Windows 11
- Keyboard + Mouse
- Development Build

---

## Severity

**Medium**

Gameplay remains functional, but the incorrect camera boundary negatively impacts player navigation and presentation.

---

## Priority

**Medium**

---

## Frequency

**100%**

Issue is consistently reproducible.

---

## Preconditions

- Player begins in Rootward.
- Player returns directly to Lunareth through the scene transition trigger.

---

## Reproduction Steps

1. Launch the game.
2. Load into Rootward.
3. Exit Rootward through the scene transition.
4. Enter Lunareth.
5. Walk toward the left side of the level.
6. Continue moving until reaching the camera boundary.

---

## Expected Result

The camera should follow the player to the intended left boundary of the Lunareth level.

---

## Actual Result

The left camera boundary terminates prematurely, causing the camera to stop following the player before the intended edge of the level.

---

## Workaround

Travel to Verdant and then return to Lunareth.

This consistently restores the expected camera boundaries.

---

## Possible Related Systems

This issue may be related to camera boundary initialization during the Rootward → Lunareth scene transition.

The Verdant → Lunareth transition appears to correctly refresh the boundary values.

---

## Attachments

- QF-001P.mov — Demonstrates the issue.
- QF-001WA.mov — Demonstrates the workaround.

---

## Notes

Issue has only been reproduced when entering Lunareth directly from Rootward.

The issue has not been reproduced after returning from Verdant.

---

## Resolution

**Status:** Open

Root cause has not yet been identified.
