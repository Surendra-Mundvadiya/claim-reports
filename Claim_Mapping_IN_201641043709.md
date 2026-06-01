# Claim Mapping — Element-by-Element Charts

**Patent:** Indian Patent Application No. 201641043709
**Title:** "Methods and systems for rendering a camera preview in an electronic device"
**Applicant:** Samsung Electronics Co., Ltd.

Below are detailed claim charts for each product with non-zero infringement potential. Products with NONE severity (ModiFace, Lenskart, YouCam, BeReal, Instagram, TikTok, etc.) are excluded because they fail Claim 1 at the first element (no second camera in use).

---

## Patent Claim 1 — Elements to Map

| # | Element |
|---|---|
| E1 | Detect at least one object in a camera preview |
| E2 | Two cameras (first + second) on same electronic device |
| E3 | Select/extract object from camera 1's preview |
| E4 | Determine intended location in camera 2's preview |
| E5 | Source camera ≠ target camera (cross-camera asymmetry) |
| E6 | Render final preview by overlaying object on intended location (live) |

**All 6 elements must be present for literal infringement of Claim 1.**

---

## Product 1: Snapchat "Dual Camera" — Cutout Layout ⚠️ HIGH

| Element | Snapchat Cutout Implementation | Match? |
|---|---|---|
| E1 — Detect object | Snap's ML segmentation model detects user's face/body in selfie camera feed | ✅ YES |
| E2 — Two cameras | Front + rear cameras of phone run simultaneously | ✅ YES |
| E3 — Extract object | User's body silhouette is segmented (background removed) from front camera | ✅ YES |
| E4 — Intended location | Cutout is positioned within the rear camera's live preview frame | ✅ YES |
| E5 — Cross-camera asymmetry | Object source = front camera; overlay target = rear camera preview | ✅ YES |
| E6 — Live overlay render | Composite shown in real-time viewfinder before capture | ✅ YES |

**Claim 1: LITERAL INFRINGEMENT — all 6 elements satisfied**
**Claim 3 (stitching): YES — cutout stitched into rear scene**
**Claim 4 (apparatus): YES — phone running Snapchat = device with all 4 units**
**Claim 6: YES** | **Claim 7: YES** | **Claim 2/5 (property only): NO**

---

## Product 2: Snap Lens Studio — 3rd-Party Dual Camera Lenses 🟡 MEDIUM

| Element | Implementation | Match? |
|---|---|---|
| E1 — Detect object | Lens creators use face/body/object tracking on either camera feed | ✅ YES |
| E2 — Two cameras | Lens Studio exposes both front + rear via `reverseCameraTexture` | ✅ YES |
| E3 — Extract object | Tracked object isolated from source camera | ✅ YES (per-Lens) |
| E4 — Intended location | Lens logic determines placement in other camera's feed | ✅ YES (per-Lens) |
| E5 — Cross-camera asymmetry | Lens explicitly designed to use opposite camera as background | ✅ YES |
| E6 — Live overlay render | Lens renders in real-time camera preview | ✅ YES |

**Claim 1: Depends on specific Lens — many qualifying Lenses likely exist**
**Severity: MEDIUM (contributory infringement angle — Snap provides the tooling)**

---

## Product 3: Nokia "Bothie" / Dual Sight 🟠 LOW

| Element | Nokia Bothie Implementation | Match? |
|---|---|---|
| E1 — Detect object | ❌ No object detection — just shows both feeds | ❌ NO |
| E2 — Two cameras | Front + rear simultaneous | ✅ YES |
| E3 — Extract object | ❌ No extraction — full feeds shown side-by-side | ❌ NO |
| E4 — Intended location | ❌ No location determination — fixed split-screen | ❌ NO |
| E5 — Cross-camera asymmetry | ❌ Both feeds independently displayed | ❌ NO |
| E6 — Live overlay render | Live, but composition not overlay | ⚠️ PARTIAL |

**Claim 1: NO LITERAL INFRINGEMENT (fails E1, E3, E4, E5)**
**Claim 3 (stitching): Weak DoE argument only — patent's "stitching" means object-level merge, not side-by-side**
**Severity: LOW (very weak case)**

---

## Product 4: Xiaomi / Redmi Dual Video Mode 🟠 LOW

| Element | Xiaomi Dual Video Implementation | Match? |
|---|---|---|
| E1 — Detect object | ❌ No object detection | ❌ NO |
| E2 — Two cameras | Front + rear simultaneous | ✅ YES |
| E3 — Extract object | ❌ No extraction | ❌ NO |
| E4 — Intended location | ❌ Fixed split-screen / PiP | ❌ NO |
| E5 — Cross-camera asymmetry | ❌ Independent feeds | ❌ NO |
| E6 — Live overlay render | Live, but composition only | ⚠️ PARTIAL |

**Claim 1: NO LITERAL INFRINGEMENT**
**Claim 3/6: Weak DoE only**
**Severity: LOW**

---

## Product 5: Apple iOS Multi-Cam / FiLMiC DoubleTake 🟠 LOW

| Element | DoubleTake Implementation | Match? |
|---|---|---|
| E1 — Detect object | ❌ No object detection | ❌ NO |
| E2 — Two cameras | Any two iPhone lenses simultaneous | ✅ YES |
| E3 — Extract object | ❌ No extraction | ❌ NO |
| E4 — Intended location | ❌ Fixed PiP / Split / Discrete modes | ❌ NO |
| E5 — Cross-camera asymmetry | ❌ Independent feeds | ❌ NO |
| E6 — Live overlay render | Live composition only | ⚠️ PARTIAL |

**Claim 1: NO LITERAL INFRINGEMENT**
**Claim 3/6: Weak DoE only**
**Severity: LOW**

---

## Summary — Where Infringement Stands

| Product | Claim 1 | Claim 2 | Claim 3 | Claim 4 | Claim 5 | Claim 6 | Claim 7 | Severity |
|---|---|---|---|---|---|---|---|---|
| **Snapchat Cutout** | ✅ YES | ❌ | ✅ YES | ✅ YES | ❌ | ✅ YES | ✅ YES | **HIGH** |
| Snap Lens Studio (3rd party) | ⚠️ Lens-dependent | ❌ | ⚠️ | ✅ | ❌ | ⚠️ | ✅ | MEDIUM |
| Nokia Bothie | ❌ | ❌ | ⚠️ DoE | ❌ | ❌ | ⚠️ DoE | ❌ | LOW |
| Xiaomi Dual Video | ❌ | ❌ | ⚠️ DoE | ❌ | ❌ | ⚠️ DoE | ❌ | LOW |
| Apple/Filmic DoubleTake | ❌ | ❌ | ⚠️ DoE | ❌ | ❌ | ⚠️ DoE | ❌ | LOW |

---

## Bottom Line

**Only Snapchat Cutout literally maps to Claim 1.** Everything else fails at the "object detection + extraction + cross-camera overlay" steps because they only do simple split-screen or picture-in-picture composition.

**Realistic enforcement target: Snapchat (one product, one feature, one company).**

⚠️ This mapping is only meaningful if IN 201641043709 is **granted** — verify on InPASS first.

---

*Generated for research/pre-screening purposes. Not legal advice.*
