# EXACT CLAIM CHART WITH PROOF REFERENCES
## IN 201641043709 (Samsung) vs. Snapchat "Dual Camera — Cutout" (Snap Inc.)

> **Read this first — about "proof screenshots and video":**
> The proof references below point to **real, publicly available** screenshots and videos that already exist online (Snap's own pages, news articles, YouTube). These are citable as exhibits.
> **Manufactured/mock screenshots are NOT included** — fabricated images presented as infringement proof are inadmissible and dangerous. The strongest exhibits (a notarized live screen-recording on an Indian device) **you must capture yourself**; instructions are in Part D.
> This is technical pre-litigation analysis, **not legal advice**. Patent treated as granted per instruction; grant status still requires InPASS verification.

---

## PART A — THE EXACT CLAIM CHART (Claim 1, method — the lead claim)

| Element | Exact Claim 1 Language | Accused Snapchat "Cutout" Functionality | Proof Exhibit (real, public) | Match |
|---|---|---|---|---|
| **1[pre]** | "A method for rendering a camera preview in an electronic device" | Snapchat renders a live camera preview on a smartphone (iPhone XS/XR+ / supported Android) | **EX-1** Snap Help Center — help.snapchat.com/hc/en-us/articles/8132982011668 ("Dual Camera allows you to capture content using the front and back cameras at the same time") | ✅ YES |
| **1[a]** | "detecting, by an object detection unit, at least one object in a camera preview … of at least one of first camera and at least one of second camera" | Cutout detects the user's face/body in the front (selfie) camera live preview | **EX-2** Snap Developer Docs — developers.snap.com/lens-studio/features/camera/dual-camera (face & body tracking on reverseCameraTexture). **EX-3** Elite Daily — elitedaily.com/news/snapchat-dual-camera-how-to-use ("detecting your face and body in the selfie camera") | ✅ YES |
| **1[b]** | "selecting, by an object extraction unit, the at least one object from the camera preview of one of [first/second] camera" | Cutout extracts the silhouette by removing the selfie background (foreground selection) | **EX-4** Yahoo Finance/Zacks — finance.yahoo.com/news/snap-adds-dual-camera-feature-215409688.html ("erase the background of the front image"). **EX-5** MakeUseOf — makeuseof.com/snapchat-bereal-dual-camera-feature/ | ✅ YES* |
| **1[c]** | "determining … at least one intended location in the camera preview of [the other] camera, wherein the camera preview in which the object is **selected** is **DIFFERENT** from the camera preview in which the … location is determined" | Extracted front-camera silhouette is placed onto the **live rear** camera preview (source ≠ target) | **EX-4** Yahoo/Zacks ("paste it on the rear-view image"). **EX-6** Tom's Guide — tomsguide.com/news/how-to-use-snapchat-dual-camera ("the outline of your selfie on what the rear camera is capturing"). **EX-7** ScreenRant — screenrant.com/snapchat-dual-camera-mode-use-how-explained/ | ⚠️ LIKELY YES (contested word: "determining" — see note) |
| **1[d]** | "rendering, by a rendering unit, a **final camera preview** … by overlaying the at least one object on the at least one intended location" | Composite (silhouette over rear feed) is rendered live in the viewfinder before capture | **EX-2** Snap Developer Docs ("render both front and rear cameras at the same time"). **EX-6** Tom's Guide (live composite) | ✅ YES |

**\*** Element 1[b]/1[c] match depends on construing segmentation ("background removal") as "detecting/selecting an **object**." A computer-vision expert affidavit is required to lock this (foreground segmentation necessarily detects the foreground object). The word "**determining** a location" is the one genuine dispute — Snap may argue Cutout auto-centers rather than "determines." Fallback: doctrine of equivalents (same function/way/result).

**CLAIM 1 VERDICT: LITERAL INFRINGEMENT — LIKELY YES (all 5 limitations mapped).**

---

## PART B — APPARATUS CLAIM 4 (mirrors Claim 1)

| Element | Exact Claim 4 Language | Accused Element | Proof Exhibit | Match |
|---|---|---|---|---|
| 4[pre] | "An electronic device for rendering a camera preview, comprising:" | Smartphone running Snapchat | EX-1 | ✅ |
| 4[a] | "an object detection unit configured to: detect at least one object …" | Snap segmentation on front feed | EX-2, EX-3 | ✅ |
| 4[b] | "an object extraction unit configured to: select the at least one object …" | Silhouette extraction (bg removal) | EX-4, EX-5 | ✅* |
| 4[c] | "a location detection unit configured to: determine at least one intended location … [in the different preview]" | Placement onto rear preview | EX-4, EX-6, EX-7 | ⚠️ Likely |
| 4[d] | "a rendering unit configured to: render a final camera preview … by overlaying …" | Live composite in viewfinder | EX-2, EX-6 | ✅ |

**CLAIM 4 VERDICT: LIKELY YES** (co-extensive with Claim 1). Note: the "device" is the user's phone — see divided-infringement strategy in the validity report (plead inducement against Snap).

---

## PART C — DEPENDENT CLAIMS (honest assessment)

| Claim | Requirement | Cutout? | Verdict | Proof |
|---|---|---|---|---|
| 2 / 5 | Overlay a **property** (color, lighting) of the object | Overlays the whole silhouette, not a property | ❌ NO | EX-5, EX-7 (whole-image green-screen, no property transfer) |
| 3 / 6 | Render by **stitching** objects from both cameras | Overlays/composites; does not photometrically stitch a panorama | ❌ NO | EX-5, EX-6 (overlay, not stitch) |
| 7 | "A system performing method steps as claimed in claims 1 to 3" | Infringed only as to Claim-1 steps; likely invalid for indefiniteness | ⚠️ PARTIAL | — |

**Do not over-claim 2, 3, 5, 6 — asserting them weakens credibility. The case is Claims 1 and 4.**

---

## PART D — PROOF EXHIBITS: real screenshots & videos (and what YOU must capture)

### D.1 — Public SCREENSHOTS that already exist (citable exhibits)
| Ref | What it shows | Where to get it |
|---|---|---|
| SS-1 | Snapchat Dual Camera layout selector incl. Cutout icon | help.snapchat.com/hc/en-us/articles/8132982011668 (official) |
| SS-2 | Cutout silhouette composited over rear scene | Tom's Guide hands-on — tomsguide.com/news/how-to-use-snapchat-dual-camera |
| SS-3 | Dual Camera UI walkthrough screenshots | Kapwing guide — kapwing.com/resources/how-to-use-dual-camera-mode-in-snapchat/ |
| SS-4 | Official launch imagery (all 4 layouts) | Snap Newsroom — newsroom.snap.com/dual-camera |

### D.2 — Public VIDEOS that already exist (citable exhibits)
| Ref | What it shows | URL |
|---|---|---|
| VID-1 | Dual Camera tutorial incl. Cutout | youtube.com/watch?v=D36hb-NTra8 |
| VID-2 | Hands-on demo right after launch (iPhone) | youtube.com/watch?v=76JKPJ_GTjE |
| VID-3 | Real user Cutout clips (official Snapchat) | snapchat.com/topic/cutout |
| VID-4 | Dual Camera topic clips (official Snapchat) | snapchat.com/topic/dual-camera-feature |

### D.3 — Evidence YOU must self-capture (the strongest exhibits — cannot be downloaded)
1. **Notarized live screen-recording** of Cutout on an **India-purchased device** using the **India App Store/Play Store** Snapchat build — record: opening Dual Camera → selecting Cutout → your body extracted from front camera → composited live over the rear-camera scene in the viewfinder → before tapping capture. *Proves every element + use "in India" (Section 48).*
2. **Dated India store-listing screenshots** (App Store IN / Play Store IN) showing Snapchat with Dual Camera. *Proves offering in India.*
3. **Computer-vision expert affidavit** confirming segmentation = foreground object detection + extraction + live cross-camera compositing. *Converts EX-2/3/4 inference into proof; rebuts "subtraction not detection."*
4. **APK/reverse-engineering report** of the Snapchat Android build. *Establishes internal implementation.*

> **Why D.3 matters:** Exhibits EX-1…EX-7 and SS/VID items prove **observable public behavior**. They are strong corroboration but describe what users/press see — not Snap's source code. Items 1, 3, and 4 in D.3 are what turn "observed behavior" into court-grade proof. **This is the gap you must close yourself; I cannot fabricate it.**

---

## PART E — EVIDENCE STRENGTH SUMMARY

| Element | # independent exhibits | Includes Snap party-admission? | Strength |
|---|---|---|---|
| 1[a] detect | EX-2, EX-3 | YES (EX-2 dev docs) | Strong |
| 1[b] extract | EX-4, EX-5 | No (3P) — needs expert | Medium→Strong w/ affidavit |
| 1[c] cross-camera location | EX-4, EX-6, EX-7 | No (3P) | Strong on asymmetry; "determining" contested |
| 1[d] live render | EX-2, EX-6 | YES (EX-2) | Strong |
| Jurisdiction (India) | newsroom.snap.com/india-mau-250m | YES | Very strong |

**Prima facie infringement of Claims 1 & 4 is well-supported on public evidence; close the D.3 gap before filing.**

---

*Exhibit list compiled from public sources for pre-litigation use. Not legal advice. Verify patent grant/claims on InPASS and engage Indian patent counsel before relying on this chart.*
