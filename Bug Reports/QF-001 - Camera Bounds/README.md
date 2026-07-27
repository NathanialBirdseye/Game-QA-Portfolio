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

---

## Priority

**Medium**

---

## Frequency

**100%**

---

## Preconditions

- Player begins in Rootward.
- Player returns directly to Lunareth through a scene transition trigger.

---

## Reproduction Steps

1. Launch the game.
2. Load into Rootward.
3. Exit Rootward through a scene transition trigger.
4. Return to Lunareth.
5. Walk toward the left side of the level.

---

## Expected Result

The camera bounds should fully reset to the Lunareth level boundaries after transitioning back from Rootward.

---

## Actual Result

- The left camera boundary is significantly shorter than intended.
- The player reaches an invisible camera stop before reaching the proper edge of the level.

---

## Workaround

Traveling to Verdant and then returning to Lunareth correctly restores the camera bounds.

---

## Possible Related Systems

- Camera Bounds
- Scene Transition Manager
- Camera Initialization
- Level Boundary Loading

---

## Attachments(Inside Media Folder)

- QF-001-Problem.mp4 — Demonstrates the incorrect camera bounds after transitioning from Rootward to Lunareth.
- QF-001-WorkAround.mp4 — Demonstrates that transitioning through Verdant correctly restores the camera bounds.

---

### Workaround Demonstration

Demonstrates that transitioning through Verdant correctly restores the camera bounds.

---

## Notes

The issue consistently reproduces when returning directly from Rootward to Lunareth.

Traveling through Verdant refreshes the camera boundary values and restores normal behavior, suggesting the camera bounds are not being properly reinitialized during the direct Rootward → Lunareth transition.

---

## Video Evidence

If GitHub does not preview the video in your browser, click the file and select **Download raw file** to view the recording locally.

- `QF-001-Problem.mp4`
- `QF-001-WorkAround.mp4`

---

## Resolution

**Status:** Open
