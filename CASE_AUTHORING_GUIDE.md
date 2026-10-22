# CSI: Naches — Adding investigations

The app loads `cases/catalog.json`, which lists the playable cases. Each case's content is in its own `.json` file. Ordinary new cases do **not** require editing `app.js`.

## How to add another case

1. Copy `cases/river-logger.json` to `cases/new-case-id.json`.
2. Replace all fictional characters, settings, evidence, and text with new original material. Never imply that a real person or business committed a real offense.
3. Preserve these top-level fields: `id`, `num`, `title`, `place`, `short`, `field`, `accent`, `icon`, `time`, `brief`, `caseQuestion`, `sites`, `clues`, `witnesses`, `labs`, `math`, `events`, `evidence`, `culprit`, `explanation`, and `note`.
4. In Version 1, use four `sites`, seven `clues`, four `witnesses`, three `labs`, and four chronological `events`. Every evidence item's `site` must match a `sites[].id`. Every quiz has three options and a zero-based `correct` answer index (0, 1, or 2).
5. Each lab defines an input `variable` and an `output`. For `model: "linear"`, the app calculates `output.base + output.factor × input`. For `model: "inverse"`, it calculates `output.base / input` (choose a strictly positive input range). Describe each model's simplifying assumptions.
6. Set `culprit` to one of the fictional witness IDs, and set `evidence` to IDs of at least two relevant clues. The term `culprit` is an internal field for the key actor; the story need not allege criminal wrongdoing.
7. Add a corresponding entry to `cases/catalog.json` with `id`, `num`, `title`, `place`, `short`, `field`, `accent`, `icon`, `time`, `file: "cases/new-case-id.json"`, and `status: "ready"`.
8. Supported scene icons are `river`, `canyon`, `orchard`, `greenway`, and `station`; unknown icons show the river design. You can introduce new designs by extending `caseScene()` in `app.js`.
9. Validate the JSON, all referenced IDs, units, answer indices, model mathematics, and evidence-based resolution. Play the entire case at more than one grade band before publishing.
10. To add a regular new case to GitHub, upload **only the new `cases/*.json` file and the modified `cases/catalog.json`** within your repository's existing `cases/` directory. Preserve all older cases and the game engine.

## Educational safeguards

Clues, samples, and suspects are fictional. Teach that a similar tread, fiber, or color does not individually identify a person. Alternate explanations and the limitations of each scientific model matter. Write stories to be safe for middle-school students, and review any high-school extensions before classroom use.

## Future expansion

The same architecture can support interactive microscopes, sample comparisons, evidence chains, multiple witness responses, additional location maps, student notebooks, and a teacher dashboard. Those features require their own design and validation rather than assuming the present simulation is a real forensic instrument.
