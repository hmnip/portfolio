# Media and content checklist

Every placeholder on the site, generated from the pages. Search the repo for `TODO` to find each one in context.

## How to prepare files

| Type | Format | Size | Where it goes |
|---|---|---|---|
| Card hero (home page) | WebP | 1200x750 (16:10), under 150 KB | `assets/img/<project>/hero.webp` |
| Gallery photo | WebP | 1600 px long edge, under 200 KB | `assets/img/<project>/<name>.webp` |
| CAD render | WebP (or PNG for line art) | 1600 px long edge | `assets/cad/<project>/<name>.webp` |
| Looping clip | MP4 (H.264), no audio track | 4 to 8 s, 1280x720, under 2 MB, plus a WebP poster frame | `assets/video/<project>/<name>.mp4` |

Convert a photo to WebP with ImageMagick (PowerShell):

```powershell
magick input.jpg -resize "1600x1600>" -strip -quality 80 assets\img\bear-den\workcell.webp
```

Crop a home-page card hero to exactly 1200x750:

```powershell
magick input.jpg -resize "1200x750^" -gravity center -extent 1200x750 -strip -quality 80 assets\img\arctos\hero.webp
```

Then replace the placeholder `<div class="media-placeholder" ...>` with the `<img>` or `<video>` markup in the HTML comment above it. Always fill in `alt` (images) and keep `loading="lazy"` / `preload="none"`.

## 1. Media (34 items)

### Home page

| Done | Kind | Ideal shot | Folder |
|---|---|---|---|
| [ ] | Photo | BEAR-DEN hero photo, arm on rail at the workcell, 16:10 | `assets/img/bear-den/hero.webp` |
| [ ] | Photo | ARCTOS hero photo, arm and rail over the bins, 16:10 | `assets/img/arctos/hero.webp` |
| [ ] | Photo | Oystare hero photo, vessel on the water, 16:10 | `assets/img/oystare/hero.webp` |
| [ ] | Photo | mobile manipulator photo, 16:10 | `assets/img/mobile-manipulator/hero.webp` |
| [ ] | Graphic | pallet station flow diagram, no site photos, 16:10 | `assets/img/amazon-pallet-flow/hero.webp` |
| [ ] | Photo | oscillator test rig photo, 16:10 | `assets/img/nonlinear-oscillator/hero.webp` |
| [ ] | Photo | drone racing photo, 16:10 | `assets/img/bwsi-drone-racing/hero.webp` |

### BEAR-DEN

| Done | Kind | Ideal shot | Folder |
|---|---|---|---|
| [ ] | Photo | workcell overview, arm on rail with instruments, 16:9 | `assets/img/bear-den/` |
| [ ] | Photo | ACUCS gantry close-up, 16:9 | `assets/img/bear-den/` |
| [ ] | Video | 6 s loop, arm and rail moving a 96-well plate, 16:9 MP4 | `assets/video/bear-den/` |
| [ ] | CAD | end effector CAD render, 1:1 | `assets/cad/bear-den/` |
| [ ] | CAD | SolidWorks mount render or photo of the printed part, 1:1 | `assets/cad/bear-den/` |
| [ ] | Photo | end-of-arm camera frame of a plate check, 16:9 | `assets/img/bear-den/` |
| [ ] | Graphic | MuJoCo or Isaac Sim screenshot of the arm and rail twin, 16:9 | `assets/img/bear-den/` |

### ARCTOS

| Done | Kind | Ideal shot | Folder |
|---|---|---|---|
| [ ] | Video | 6 s loop, arm picking and sorting, top-down, 16:9 MP4 | `assets/video/arctos/` |
| [ ] | CAD | Onshape render of the linear rail, 16:9 | `assets/cad/arctos/` |
| [ ] | Photo | overhead camera frame with detected objects, 16:9 | `assets/img/arctos/` |
| [ ] | Graphic | Isaac Sim screenshot of the arm twin, 16:9 | `assets/img/arctos/` |
| [ ] | Photo | team with the arm, 16:9 | `assets/img/arctos/` |

### Oystare

| Done | Kind | Ideal shot | Folder |
|---|---|---|---|
| [ ] | Photo | vessel on the water, 16:9 | `assets/img/oystare/` |
| [ ] | Photo | Wellfleet site visit, drag or depth test, 16:9 | `assets/img/oystare/` |
| [ ] | CAD | probe housing CAD render, 1:1 | `assets/cad/oystare/` |
| [ ] | Video | 6 s loop, vessel following waypoints, 16:9 MP4 | `assets/video/oystare/` |
| [ ] | Photo | sample reef map or camera frame of a reef, 16:9 | `assets/img/oystare/` |

### Color-Sorting Mobile Manipulator

| Done | Kind | Ideal shot | Folder |
|---|---|---|---|
| [ ] | Graphic | block diagram. Needs the controller, color sensor, arm actuators, and base drive | `assets/img/mobile-manipulator/` |
| [ ] | Photo | robot photo, 16:9 | `assets/img/mobile-manipulator/` |
| [ ] | Video | 6 s loop, picking and sorting one object, 16:9 MP4 | `assets/video/mobile-manipulator/` |
| [ ] | Graphic | MATLAB Robotics Toolbox plot of the DH model, 16:9 | `assets/img/mobile-manipulator/` |

### Amazon pallet tracking

| Done | Kind | Ideal shot | Folder |
|---|---|---|---|
| [ ] | Graphic | your own sketch of the pallet station layout, 16:9 | `assets/img/amazon-pallet-flow/` |
| [ ] | Graphic | dashboard mockup with sample data only, 16:9 | `assets/img/amazon-pallet-flow/` |

### Nonlinear Oscillator (ME 310)

| Done | Kind | Ideal shot | Folder |
|---|---|---|---|
| [ ] | Photo | test rig photo with the accelerometer, 16:9 | `assets/img/nonlinear-oscillator/` |
| [ ] | Graphic | frequency response plot, 16:9 | `assets/img/nonlinear-oscillator/` |

### Autonomous Drone Racing (BWSI)

| Done | Kind | Ideal shot | Folder |
|---|---|---|---|
| [ ] | Photo | drone photo, 16:9 | `assets/img/bwsi-drone-racing/` |
| [ ] | Video | 6 s loop, drone flying the course, 16:9 MP4 | `assets/video/bwsi-drone-racing/` |

## 2. Missing facts and text  "($([int]# Media and content checklist

Every placeholder on the site, generated from the pages. Search the repo for `TODO` to find each one in context.

## How to prepare files

| Type | Format | Size | Where it goes |
|---|---|---|---|
| Card hero (home page) | WebP | 1200x750 (16:10), under 150 KB | `assets/img/<project>/hero.webp` |
| Gallery photo | WebP | 1600 px long edge, under 200 KB | `assets/img/<project>/<name>.webp` |
| CAD render | WebP (or PNG for line art) | 1600 px long edge | `assets/cad/<project>/<name>.webp` |
| Looping clip | MP4 (H.264), no audio track | 4 to 8 s, 1280x720, under 2 MB, plus a WebP poster frame | `assets/video/<project>/<name>.mp4` |

Convert a photo to WebP with ImageMagick (PowerShell):

```powershell
magick input.jpg -resize "1600x1600>" -strip -quality 80 assets\img\bear-den\workcell.webp
```

Crop a home-page card hero to exactly 1200x750:

```powershell
magick input.jpg -resize "1200x750^" -gravity center -extent 1200x750 -strip -quality 80 assets\img\arctos\hero.webp
```

Then replace the placeholder `<div class="media-placeholder" ...>` with the `<img>` or `<video>` markup in the HTML comment above it. Always fill in `alt` (images) and keep `loading="lazy"` / `preload="none"`.

## 1. Media (34 items)

### Home page

| Done | Kind | Ideal shot | Folder |
|---|---|---|---|
| [ ] | Photo | BEAR-DEN hero photo, arm on rail at the workcell, 16:10 | `assets/img/bear-den/hero.webp` |
| [ ] | Photo | ARCTOS hero photo, arm and rail over the bins, 16:10 | `assets/img/arctos/hero.webp` |
| [ ] | Photo | Oystare hero photo, vessel on the water, 16:10 | `assets/img/oystare/hero.webp` |
| [ ] | Photo | mobile manipulator photo, 16:10 | `assets/img/mobile-manipulator/hero.webp` |
| [ ] | Graphic | pallet station flow diagram, no site photos, 16:10 | `assets/img/amazon-pallet-flow/hero.webp` |
| [ ] | Photo | oscillator test rig photo, 16:10 | `assets/img/nonlinear-oscillator/hero.webp` |
| [ ] | Photo | drone racing photo, 16:10 | `assets/img/bwsi-drone-racing/hero.webp` |

### BEAR-DEN

| Done | Kind | Ideal shot | Folder |
|---|---|---|---|
| [ ] | Photo | workcell overview, arm on rail with instruments, 16:9 | `assets/img/bear-den/` |
| [ ] | Photo | ACUCS gantry close-up, 16:9 | `assets/img/bear-den/` |
| [ ] | Video | 6 s loop, arm and rail moving a 96-well plate, 16:9 MP4 | `assets/video/bear-den/` |
| [ ] | CAD | end effector CAD render, 1:1 | `assets/cad/bear-den/` |
| [ ] | CAD | SolidWorks mount render or photo of the printed part, 1:1 | `assets/cad/bear-den/` |
| [ ] | Photo | end-of-arm camera frame of a plate check, 16:9 | `assets/img/bear-den/` |
| [ ] | Graphic | MuJoCo or Isaac Sim screenshot of the arm and rail twin, 16:9 | `assets/img/bear-den/` |

### ARCTOS

| Done | Kind | Ideal shot | Folder |
|---|---|---|---|
| [ ] | Video | 6 s loop, arm picking and sorting, top-down, 16:9 MP4 | `assets/video/arctos/` |
| [ ] | CAD | Onshape render of the linear rail, 16:9 | `assets/cad/arctos/` |
| [ ] | Photo | overhead camera frame with detected objects, 16:9 | `assets/img/arctos/` |
| [ ] | Graphic | Isaac Sim screenshot of the arm twin, 16:9 | `assets/img/arctos/` |
| [ ] | Photo | team with the arm, 16:9 | `assets/img/arctos/` |

### Oystare

| Done | Kind | Ideal shot | Folder |
|---|---|---|---|
| [ ] | Photo | vessel on the water, 16:9 | `assets/img/oystare/` |
| [ ] | Photo | Wellfleet site visit, drag or depth test, 16:9 | `assets/img/oystare/` |
| [ ] | CAD | probe housing CAD render, 1:1 | `assets/cad/oystare/` |
| [ ] | Video | 6 s loop, vessel following waypoints, 16:9 MP4 | `assets/video/oystare/` |
| [ ] | Photo | sample reef map or camera frame of a reef, 16:9 | `assets/img/oystare/` |

### Color-Sorting Mobile Manipulator

| Done | Kind | Ideal shot | Folder |
|---|---|---|---|
| [ ] | Graphic | block diagram. Needs the controller, color sensor, arm actuators, and base drive | `assets/img/mobile-manipulator/` |
| [ ] | Photo | robot photo, 16:9 | `assets/img/mobile-manipulator/` |
| [ ] | Video | 6 s loop, picking and sorting one object, 16:9 MP4 | `assets/video/mobile-manipulator/` |
| [ ] | Graphic | MATLAB Robotics Toolbox plot of the DH model, 16:9 | `assets/img/mobile-manipulator/` |

### Amazon pallet tracking

| Done | Kind | Ideal shot | Folder |
|---|---|---|---|
| [ ] | Graphic | your own sketch of the pallet station layout, 16:9 | `assets/img/amazon-pallet-flow/` |
| [ ] | Graphic | dashboard mockup with sample data only, 16:9 | `assets/img/amazon-pallet-flow/` |

### Nonlinear Oscillator (ME 310)

| Done | Kind | Ideal shot | Folder |
|---|---|---|---|
| [ ] | Photo | test rig photo with the accelerometer, 16:9 | `assets/img/nonlinear-oscillator/` |
| [ ] | Graphic | frequency response plot, 16:9 | `assets/img/nonlinear-oscillator/` |

### Autonomous Drone Racing (BWSI)

| Done | Kind | Ideal shot | Folder |
|---|---|---|---|
| [ ] | Photo | drone photo, 16:9 | `assets/img/bwsi-drone-racing/` |
| [ ] | Video | 6 s loop, drone flying the course, 16:9 MP4 | `assets/video/bwsi-drone-racing/` |

## 2. Missing facts and text (61 items)

Fill these in only with real numbers. If a number does not exist, delete the row or sentence instead of guessing.

### Home page (`index.html`)

- [ ] add assets/resume.pdf

### BEAR-DEN (`projects/bear-den.html`)

- [ ] Title block / Team size: team size
- [ ] video link
- [ ] any cost, space, or schedule constraints, e.g. the budget behind "low-cost" in ACUCS
- [ ] what the 3 integrated systems were, and the before/after throughput in plates or samples per hour
- [ ] Measured results / ACUCS throughput: before/after rate
- [ ] Measured results / Plate validation: if measured
- [ ] Measured results / Plate transfer cycle time: s
- [ ] Measured results / Runs logged by the orchestrator: count
- [ ] 2 to 4 sentences in your own words. For example, what debugging live runs across mechanical, electrical, and software taught you, or why you chose a task queue with append-only logs.

### ARCTOS (`projects/arctos.html`)

- [ ] Title block / Team size: team size
- [ ] GitHub link, confirm BURC-ARCTOS-ARM is public
- [ ] video link
- [ ] current status or first result, e.g. first successful sort
- [ ] object types, number of bins, and any cycle time or accuracy target
- [ ] confirm the control board is the Arduino, and that the rail runs on the same CAN bus
- [ ] Specs and results / Rail travel: mm
- [ ] Specs and results / Sort success rate: %
- [ ] Specs and results / Sort success rate: number of trials
- [ ] Specs and results / Time per pick: s
- [ ] 2 to 4 sentences in your own words. For example, what you learned from assigning one owner per software system.
- [ ] the team's next milestones

### Oystare (`projects/oystare.html`)

- [ ] Title block / Team size: team size
- [ ] video or report link after water testing
- [ ] Mechanical requirements / Portability: test
- [ ] Mechanical requirements / Freeboard: test
- [ ] Mechanical requirements / Reserve buoyancy: test
- [ ] Mechanical requirements / Sealing and corrosion: test
- [ ] Mechanical requirements / Thruster guards: test
- [ ] where the Kalman filter runs, and how camera data reaches the Pi or storage
- [ ] trade study criteria and scores, and the drag and depth numbers from Wellfleet
- [ ] Results (pending water testing) / Waypoint tracking error: m
- [ ] Results (pending water testing) / Waypoint tracking error: waypoint accuracy in m
- [ ] Results (pending water testing) / Total mass: kg
- [ ] Results (pending water testing) / Freeboard: cm
- [ ] Results (pending water testing) / Reserve buoyancy: %
- [ ] Results (pending water testing) / Camera depth: m
- [ ] Results (pending water testing) / Camera depth: m
- [ ] 2 to 4 sentences in your own words. For example, how the stakeholder interviews changed the project.

### Color-Sorting Mobile Manipulator (`projects/mobile-manipulator.html`)

- [ ] video or report link
- [ ] final demo result, e.g. objects sorted correctly out of total
- [ ] course task spec, e.g. number and type of objects, arena size, time limit, allowed hardware
- [ ] what you built or tested
- [ ] sensors and boards used, and your part
- [ ] details
- [ ] Results / Set-distance accuracy: mm
- [ ] Results / Sort success: x of y
- [ ] 2 to 4 sentences in your own words

### Amazon pallet tracking (`projects/amazon-pallet-flow.html`)

- [ ] any public-safe constraint, e.g. the fix had to fit the existing intake layout
- [ ] Results (public-safe only) / Impact: only if public-safe
- [ ] 2 to 4 sentences in your own words. For example, what leading associates on the floor taught you about designing systems people actually use.

### Nonlinear Oscillator (ME 310) (`projects/nonlinear-oscillator.html`)

- [ ] Title block / My role: your part
- [ ] Title block / Team size: team size
- [ ] report link, if you want to share it
- [ ] the main finding, e.g. how the response differed from a linear system
- [ ] your part of the setup, data collection, or analysis, and the tools you used

### Autonomous Drone Racing (BWSI) (`projects/bwsi-drone-racing.html`)

- [ ] Title block / Team size: team size
- [ ] video link, if you have one
- [ ] the outcome, e.g. course completed or race result
- [ ] the drone platform, what the vision system detected, and the control approach

## 3. Site-wide files

- [ ] `assets/resume.pdf`: your current resume. Every Resume link points here.
- [ ] `assets/img/share.png`: placeholder share image (1200x630). Replace it with a real one if you like, same size.
- [x] Absolute `og:image`, `twitter:image`, and `og:url` set for https://hmnip.github.io/portfolio/ (update if you add a custom domain).
- [x] JSON-LD `url` and GitHub profile added in `index.html`.
.Groups[1].Value - 1) items)`r`n`r`nFill these"  in only with real numbers. If a number does not exist, delete the row or sentence instead of guessing.

### Home page (`index.html`)

- [ ] add assets/resume.pdf

### BEAR-DEN (`projects/bear-den.html`)

- [ ] Title block / Team size: team size
- [ ] video link
- [ ] any cost, space, or schedule constraints, e.g. the budget behind "low-cost" in ACUCS
- [ ] what the 3 integrated systems were, and the before/after throughput in plates or samples per hour
- [ ] Measured results / ACUCS throughput: before/after rate
- [ ] Measured results / Plate validation: if measured
- [ ] Measured results / Plate transfer cycle time: s
- [ ] Measured results / Runs logged by the orchestrator: count
- [ ] 2 to 4 sentences in your own words. For example, what debugging live runs across mechanical, electrical, and software taught you, or why you chose a task queue with append-only logs.

### ARCTOS (`projects/arctos.html`)

- [ ] Title block / Team size: team size
- [ ] GitHub link, confirm BURC-ARCTOS-ARM is public
- [ ] video link
- [ ] current status or first result, e.g. first successful sort
- [ ] object types, number of bins, and any cycle time or accuracy target
- [ ] confirm the control board is the Arduino, and that the rail runs on the same CAN bus
- [ ] Specs and results / Rail travel: mm
- [ ] Specs and results / Sort success rate: %
- [ ] Specs and results / Sort success rate: number of trials
- [ ] Specs and results / Time per pick: s
- [ ] 2 to 4 sentences in your own words. For example, what you learned from assigning one owner per software system.
- [ ] the team's next milestones

### Oystare (`projects/oystare.html`)

- [ ] Title block / Team size: team size
- [ ] video or report link after water testing
- [ ] Mechanical requirements / Portability: test
- [ ] Mechanical requirements / Freeboard: test
- [ ] Mechanical requirements / Reserve buoyancy: test
- [ ] Mechanical requirements / Sealing and corrosion: test
- [ ] Mechanical requirements / Thruster guards: test
- [ ] where the Kalman filter runs, and how camera data reaches the Pi or storage
- [ ] trade study criteria and scores, and the drag and depth numbers from Wellfleet
- [ ] Results (pending water testing) / Waypoint tracking error: m
- [ ] Results (pending water testing) / Waypoint tracking error: waypoint accuracy in m
- [ ] Results (pending water testing) / Total mass: kg
- [ ] Results (pending water testing) / Freeboard: cm
- [ ] Results (pending water testing) / Reserve buoyancy: %
- [ ] Results (pending water testing) / Camera depth: m
- [ ] Results (pending water testing) / Camera depth: m
- [ ] 2 to 4 sentences in your own words. For example, how the stakeholder interviews changed the project.

### Color-Sorting Mobile Manipulator (`projects/mobile-manipulator.html`)

- [ ] video or report link
- [ ] final demo result, e.g. objects sorted correctly out of total
- [ ] course task spec, e.g. number and type of objects, arena size, time limit, allowed hardware
- [ ] what you built or tested
- [ ] sensors and boards used, and your part
- [ ] details
- [ ] Results / Set-distance accuracy: mm
- [ ] Results / Sort success: x of y
- [ ] 2 to 4 sentences in your own words

### Amazon pallet tracking (`projects/amazon-pallet-flow.html`)

- [ ] any public-safe constraint, e.g. the fix had to fit the existing intake layout
- [ ] Results (public-safe only) / Impact: only if public-safe
- [ ] 2 to 4 sentences in your own words. For example, what leading associates on the floor taught you about designing systems people actually use.

### Nonlinear Oscillator (ME 310) (`projects/nonlinear-oscillator.html`)

- [ ] Title block / My role: your part
- [ ] Title block / Team size: team size
- [ ] report link, if you want to share it
- [ ] the main finding, e.g. how the response differed from a linear system
- [ ] your part of the setup, data collection, or analysis, and the tools you used

### Autonomous Drone Racing (BWSI) (`projects/bwsi-drone-racing.html`)

- [ ] Title block / Team size: team size
- [ ] video link, if you have one
- [ ] the outcome, e.g. course completed or race result
- [ ] the drone platform, what the vision system detected, and the control approach

## 3. Site-wide files

- [ ] `assets/resume.pdf`: your current resume. Every Resume link points here.
- [ ] `assets/img/share.png`: placeholder share image (1200x630). Replace it with a real one if you like, same size.
- [x] Absolute `og:image`, `twitter:image`, and `og:url` set for https://hmnip.github.io/portfolio/ (update if you add a custom domain).
- [x] JSON-LD `url` and GitHub profile added in `index.html`.
