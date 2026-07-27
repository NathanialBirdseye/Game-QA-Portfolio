# QF-002 - Gameplay State Fails to Restore After EQO Intro Cutscene

---

## Project Information

| Property | Value |
|----------|-------|
| **Project** | Quantum Flip |
| **Report ID** | QF-002 |
| **Status** | Closed |
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

**High**

The player is unable to properly continue gameplay after the cutscene due to multiple gameplay systems failing to restore.

---

## Priority

**High**

---

## Frequency

**100%**

Issue is consistently reproducible when the Player reference is not assigned within the EQO Intro Cutscene Manager.

---

## Preconditions

- Player prefab is **not** assigned to the Player field within the EQO Intro Cutscene Manager.
- Begin a new game and trigger the EQO intro cutscene.

---

## Reproduction Steps

1. Remove the Player reference from the EQO Intro Cutscene Manager.
2. Launch the game.
3. Progress until the EQO intro cutscene begins.
4. Allow the cutscene to complete.
5. Observe gameplay after control is returned.

---

## Expected Result

Once the cutscene finishes:

- Camera returns to the player.
- Camera follow resumes.
- EQO returns to the player's shoulder.
- Player regains normal gameplay control.

---

## Actual Result

After the cutscene completes:

- Camera remains zoomed out.
- Camera follow does not resume.
- EQO does not return to the player's shoulder.
- Player can move around the cutscene room while the camera remains locked.

---

## Workaround

No gameplay workaround has been identified.

---

## Possible Related Systems

The issue appears related to the missing Player reference within the EQO Intro Cutscene Manager.

Several restoration events appear dependent upon this reference during cutscene completion.

---

## Attachments(Inside Media Folder)

- QF-002-Problem.mp4 — Demonstrates gameplay state failing to restore.
- QF-002-Fix.mp4 — Demonstrates normal behavior after assigning the Player reference.

---

## Notes

This issue is fully resolved by assigning the Player prefab reference within the EQO Intro Cutscene Manager Inspector.

---

## Video Evidence

If GitHub does not preview the video in your browser, click the file and select **Download raw file** to view the recording locally.

- `QF-002-Problem.mp4`
- `QF-002-Fix.mp4`

---

## Resolution

**Status:** Closed
