# CSI: Naches — The Science of Evidence

A standalone, dependency-free, GitHub Pages–ready educational forensic science investigation game for **grades 5–12**, built for the Naches Learning Hub.

**Recommended repository:** `csi-naches`  
**Expected GitHub Pages address:** `https://jkramer-cloud.github.io/csi-naches/`

## GitHub description

Solve five fictional forensic-science mysteries inspired by Naches and the Yakima Valley. Investigate clues, interview witnesses, test scientific models, analyze data, and defend evidence-based conclusions. Grades 5–12.

## Features

- Five complete fictional investigations, geographically inspired by the Naches River corridor, Cowiche Canyon, Tieton/Yakima Valley orchards, Yakima Greenway, and Selah foothills.
- Seven evidence exhibits, four interviews, three simulated lab tests, one calculation, four-event timeline, and Claim–Evidence–Reasoning report **per case**.
- Real-world scientific practices represented as simplified educational models. No experiments use actual chemicals, hazardous materials, or live electrical wiring.
- Grade selection 5–12; four writing expectation bands: 5–6, 7–8, 9–10, 11–12.
- Case progress and student writing saved separately for each grade in the current browser via `localStorage`. No cloud accounts, names, tracking pixels, or external libraries.
- Case report exported as readable `.txt` for teacher review. Students should avoid personal identifiers in their writing.
- Responsive layout with a focus/fullscreen option.

## Install on GitHub Pages

1. Create a public GitHub repository named `csi-naches`.
2. Upload **`index.html`, `styles.css`, `app.js`, and the complete `cases/` folder**, all at the repository root. Preserve the `cases/` subfolder. Do not create an extra `CSI_NACHES_V1/` folder at the repository root.
3. Also upload `README.md`, `TEACHER_GUIDE.md`, and `CASE_AUTHORING_GUIDE.md` if you want documentation in the repository.
4. Open **Settings → Pages → Build and deployment → Deploy from a branch → main / (root)**. Save.
5. Visit `https://jkramer-cloud.github.io/csi-naches/` and try a case. If it doesn't show the cases, check that `cases/catalog.json` and all five case files were uploaded.
6. Once the site works, upload the **separate Hub update** to the Naches Learning Hub repository.

Do **not** upload the ZIP itself as the GitHub Pages website. Unzip it and upload its contents.

### Important scope

All people, incident accounts, schools, laboratories, and facilities in this game are fabricated. Geographic references use public place names solely as inspiration. No actual allegation of wrongdoing is made. Characters are fictional, and real forensic identification cannot be performed using these simplified models.

The estimated time of **20–30 minutes** is a design target, not a timed or classroom-validated completion guarantee. Students can revisit cases, and there is no penalty for revising an incorrect response.

The app does not synchronize student progress between devices or users. Shared school Chromebooks need separate browser profiles if students want private, independent progress. Clearing browser data may erase progress. Exported case reports are the most reliable portable record.
