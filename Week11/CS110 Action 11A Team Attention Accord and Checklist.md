# CS110 Action 11A: Team Attention Accord and Checklist

Team: Lexxie, Nico, Paulina, Rudy, Sam

## Critical Rule (Read First)

Every learner submits **their own personal GitHub repository link** to Canvas Action 11A by **3:05 PM Pacific**. A team folder alone does not replace a personal upload. The team repository is the shared hub that links to each member's personal repository.

| Requirement | Points | What each person submits |
| --- | --- | --- |
| R1 | 3 | Attention Accord notes, whiteboard photos, C# to engine translation, one discovery brought back |
| R2 | 6 | Working base: Translate, Rotate and Color on one cube, with predictions and evidence |
| R3 | 3 | One extension experiment (prediction, one change, result or exact error) |
| R4 | 3 | Prefab or saved scene, two instances, per-instance state, and the memory/pooling explanation |

Everyone builds the whole base. Focus questions organize deeper investigation; they do not split the work.

## Proposed Focus for Sam

**Reuse and Physics Tester** (Developer / Architect way of thinking)

- **Investigates:** prefab or saved scene vs. live instances vs. object pooling, and why live instances use runtime memory.
- **Helps teammates:** tell Transform movement apart from Rigidbody physics so extensions do not fight each other. Keep physics tests small, on a copy.
- **Keeps a trap sheet:** Unity `Update` vs. Godot `_Process`, serialized fields vs. exported properties, Inspector edits vs. setters.
- **Alternatives if Sam prefers:** run the debrief timekeeping and gap check, or own the C#-to-engine comparison table.

These are ways of directing attention, not ranks or permanent roles. Rotate them in later work.

## Team Matrix

| Member | Way of thinking | Focus question | Promised return | Extension (R3) |
| --- | --- | --- | --- | --- |
| **Lexxie** | Orchestrator (lead, Git) | Who calls `Update`, and how does `Time.deltaTime` turn a rate into this frame's motion? | Annotated TranslateObject, Speed 0/1/2 prediction vs. result, repo structure, access check | Keyboard input control |
| **Nico** | Architect (whiteboard, prototype) | How does a class become engine behavior, and how do values reach the visible object? | Whiteboard photos before and after revision: class, object, data, method, visible result | Boundary reversal (fly out and return) |
| **Paulina** | Collaborator (evidence, review) | Why does changing Tint after `Start` not reapply it, and why does the Inspector not call the setter? | Test notes with screenshots, evidence checklist, team index | Timed color oscillation |
| **Rudy** | Learner (bounded AI check, QA) | What does an AI answer about one engine API get right or wrong against official docs and my test? | Question, checked source, keep/change/reject decision, and correction of the false prefab-memory claim | Rigidbody jump impulse (on a copy) |
| **Sam** | Developer (reuse, physics) | How do prefabs, live instances and pooling differ, and what does each cost? | Prefab vs. instance vs. pooling guide, two-instance comparison, Transform vs. physics trap note | Lifetime-limited spawning or 3 instances at different speeds |

Notes:

- Everyone does their own extension; the assignment does not require them to differ, but different ones give the team more to compare.
- Sam's extension should go beyond the two-instance test that R4 already requires.
- Rudy's AI use is one small question checked against an official reference. It does not write anyone's notes or evidence.

## Folder Structure

Each person, in their **own personal repository**:

```text
MyPersonalCS110Repo/
└── 11A/
    ├── README.md                    personal URL, team URL, reflections
    ├── preparation-receipt.json
    ├── EngineProject/
    │   ├── Assets/Scripts/EngineTransfer11A/
    │   │   ├── TranslateObject.cs
    │   │   ├── RotateObject.cs
    │   │   └── ChangeObjectColor.cs
    │   └── Assets/Prefabs/
    └── Evidence/
        ├── Whiteboard/              shared board copy (attributed) + own sketches
        ├── BaseTests/               running cube, Inspector values, predictions
        └── Extension/               screenshots, logs, errors
```

Shared team repository:

```text
TeamRepo/
└── 11A/
    ├── README.md                    member names, focus, links to 5 personal repos
    └── SharedBoard/                 board photos and Attention Accord summary
```

(This tree assumes Unity. For Godot, keep `project.godot`, scripts, scenes and C# project files instead.)

## Master Checklist

### Phase 1: 10-Minute Huddle (before the seminar)

- ☐ **Everyone:** open the local CS110 repo, make a small checkpoint, commit, push, and confirm the commit and an old image or link on GitHub.
- ☐ **Lexxie:** confirm the team repo is accessible to all five members and the instructor.
- ☐ **Nico:** lead the whiteboard. Draw the accord and later the class, object, data, method, visible result sketch.
- ☐ **Paulina:** record huddle start and end times and save the completed accord.
- ☐ **Everyone:** say your focus, capture method, promised return and return time out loud (read-back). Check gaps and overlap.
- ☐ **Everyone:** photograph the board and save it to `11A/Evidence/Whiteboard/` in your own repo, with attribution.

### Phase 2: Seminar and Host Translation (R1)

- ☐ Write class and object in your own words.
- ☐ Note one field or property and one method.
- ☐ Map one familiar C# idea to its engine equivalent (data, action, trigger, visible result).
- ☐ Note who calls initialization and repeated updates.
- ☐ Record one discovery to share with the team.
- ☐ **Rudy leads, everyone records:** one AI or documentation check, verified against an official reference.

### Phase 3: Individual Base Build (R2)

Every member, in their own project copy.

- ☐ Scene `EngineTransfer11A` with Main Camera and Directional Light.
- ☐ Cube `MyMarker` at scale (1, 1.5, 1), camera at (0, 2, -10), rotation (10, 0, 0).
- ☐ Three separate scripts attached: Translate, Rotate, ChangeObjectColor.
- ☐ White material assigned. Start with Speed 1, Degrees Per Second 90, Tint cyan.
- ☐ Run about 3 seconds. Predict, then test Speed 0 and Speed 2.
- ☐ Change Tint while stopped, run again, and note what happens.
- ☐ Save screenshots to `11A/Evidence/BaseTests/`.

### Phase 4: Individual Extension (R3)

- ☐ Make a copy or Git checkpoint first.
- ☐ Record your prediction, the one change you made, and the result or exact error.
- ☐ Write what you learned. A failed experiment with a clear record counts.
- ☐ Confirm the base still works.

### Phase 5: Reuse and Memory (R4)

- ☐ Save a prefab (Unity) or packed scene (Godot) while stopped.
- ☐ Place a second instance, offset it, and change only its Speed.
- ☐ Explain per-instance state in your README.
- ☐ Explain why templates do not automatically prevent memory growth (template vs. live instance vs. pooling), and why "a prefab means bullets use no extra memory" is incorrect.
- ☐ **Sam and Paulina:** share a starter explanation teammates adapt in their own words.

### Phase 6: Debrief and Handoff (by 3:05 PM Pacific)

- ☐ Debrief: each person shares one discovery and one difficulty, and what they learned from a teammate.
- ☐ Each person compares their promised contribution with what they actually returned.
- ☐ **Paulina:** update `TeamRepo/11A/README.md` with all five personal repo links and contributions.
- ☐ **Everyone:** personal README has your repo URL, the team repo URL, and your reflection.
- ☐ **Everyone:** keep editable source; omit `Library`, `Temp`, `Logs` and builds (Unity) or `.godot` and caches (Godot).
- ☐ **Everyone:** commit and push, then open your repo in a private window to check files, images, links and instructor access. No passwords or tokens.
- ☐ **Everyone:** submit your personal GitHub URL in Canvas Action 11A and verify the confirmation.

## Attention Accord Fields (to fill in at the huddle)

- Huddle start / end (at least 10 minutes): \_\_\_\_\_\_
- Team / lead / production purpose: Lexxie leads. We need to understand how a class becomes engine behavior before we build our game.
- Plan file, board photo or shared-document link: \_\_\_\_\_\_
- Return-to-team time: \_\_\_\_\_\_
- How we will use the findings: movement behavior from Lexxie's and Paulina's findings, setup approach from Sam's and Rudy's, extension ideas from Nico's boundary and Rudy's jump tests.
