# QF-003 - Lever Base Rotates Instead of Handle, Blocking Progression

---

## Project Information

| Property | Value |
|----------|-------|
| **Project** | Quantum Flip |
| **Report ID** | QF-003 |
| **Status** | Open |
| **Reported By** | Nathanial Birdseye |
| **Date** | July 30, 2026 |
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

**Critical**

The lever cannot be operated correctly, preventing progression through the Rootward area.

---

## Priority

**Critical**

---

## Frequency

**100%**

Issue is consistently reproducible whenever the player attempts to operate the lever.

---

## Preconditions

- Progress to the Rootward lever interaction.
- Player is within interaction range.
- Lever interaction is available.

---

## Reproduction Steps

1. Approach the Rootward lever.
2. Hold **Shift** to begin interacting with the lever.
3. Press **A** or **D** to move the lever.
4. Observe the lever animation.

---

## Expected Result

When interacting with the lever:

- The lower base remains stationary within the housing.
- The upper lever handle rotates smoothly left and right around its pivot.
- Once fully activated, the lever remains locked in its activated position.
- The connected vine door retracts upward, allowing progression to the Mawvine room.

---

## Actual Result

When interacting with the lever:

- The lower lever base rotates outward instead of remaining stationary.
- The lever rotates around an incorrect pivot point.
- The intended lever animation cannot complete correctly.
- The connected vine door cannot be activated, preventing progression.

---

## Workaround

No gameplay workaround has been identified.

---

## Possible Related Systems

The issue appears related to the lever's transform hierarchy, pivot placement, or rotation reference.

The incorrect object appears to be receiving the rotation rather than the lever handle itself.

---

## Attachments

- QF-003-Problem.mp4 — Demonstrates incorrect lever rotation and blocked progression.
- QF-003-Fix.mp4 — Demonstrates correct lever behavior and successful door activation.

---

## Notes

This issue prevents players from accessing the Mawvine room, blocking progression toward the Kharos chase sequence.

---

## Resolution

**Status:** Open
