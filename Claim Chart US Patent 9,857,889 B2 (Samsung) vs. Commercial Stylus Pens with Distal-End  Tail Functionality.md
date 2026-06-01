# Claim Chart: US Patent 9,857,889 B2 (Samsung) vs. Commercial Stylus Pens with Distal-End / Tail Functionality

## TL;DR
- **Across all 20+ products mapped, ZERO literally infringe claim 1 of US 9,857,889** because element E4 — "displaying a request screen for assigning the predefined action" when none is assigned — is not implemented by any commercial stylus stack surveyed. Every product uses pre-shipped defaults, a passive "off/nothing" state, or requires the user to navigate to Settings; none surfaces a runtime "assign now" dialog triggered by an unassigned distal-end event.
- **The only product family with a credible (though contested) Doctrine of Equivalents read is Wacom Pro Pen 2 / Pro Pen 3E** — true EMR rubber eraser on the rear (E1, Claim 2/8 literal), per-application settings table in Wacom Tablet Properties driver (E2, E3, Claim 6/12 strong), and full retrieve+perform path (E5/E6). DOE rises or falls on whether the silent "All other" fallback is an insubstantial substitute for a request screen.
- **Apple Pencil 2/Pro, Huawei M-Pencil 2/3, Honor Magic-Pencil 3, and Xiaomi Smart Pen all use barrel or side-button gestures (not distal-end events) and fail E1 on its face.** Microsoft Surface Pen Models 1710/1776 and Surface Slim Pen 2 have true tail buttons (literal E1) but the action is a global OS shortcut, not an app-routed lookup — failing E2/E3/E4. Recommended priority: deep-dive Wacom only; monitor Microsoft for future per-app routing; deprioritize all others.

---

## Key Findings

### 1. The patent's threshold limitation is the "distal end"
Claim 1 begins: "identifying an event invocation using the **distal end** of the stylus pen at a touchscreen of the device" (US 9,857,889 B2, claim 1). The specification distinguishes the "front end" (writing tip) from the "distal end" (opposite end). **Any product whose user-actuated event originates on the barrel, side button, or grip — not the rear end touching the screen — fails E1 facially.** This eliminates Apple Pencil 2/Pro (barrel tap/squeeze), Huawei M-Pencil 2/3 (lower-barrel double-tap), Honor Magic-Pencil 3 (barrel touch zone near front end), Xiaomi Smart Pen 2 (side buttons), Lenovo Precision Pen 2 (side buttons), and Samsung's own S Pen (side button + Air Actions).

### 2. The "request screen" limitation (E4) is dispositive
Claim 1 requires that the device, upon detecting a distal-end event for which **no predefined action is assigned for the currently running app**, display a request screen prompting the user to assign one. **No product surveyed implements this runtime prompt.** Microsoft, Wacom, Apple, Huawei, Amazon, reMarkable, and Boox all use pre-shipped defaults (e.g., Surface Pen single-click = Whiteboard / OneNote) or silent no-op states; configuration is proactive in Settings, never reactive to an unassigned event.

### 3. Microsoft tail buttons are system-level, not app-routed (E2/E3 fail)
Per Microsoft Support, the Surface Pen top-button shortcuts are configured globally at **Start > Settings > Bluetooth & devices > Pen & Windows Ink**, with three system-level dropdowns (single-click, double-click, press-and-hold). Apps may intercept only if the user explicitly enables "**Allow apps to override the shortcut button behavior**" (Windows 10/11 Pen & Windows Ink setting). By default the top button launches the same OS action regardless of foreground app, so E2 (determine currently running app) and E3 (per-app predefined-action lookup) are not met for the Surface family.

### 4. Wacom Pro Pen 2 is the closest analog
The Pro Pen 2 has a true rubber eraser end. EMR signaling distinguishes tip from eraser (Wacom Support: "Some of our pens even have side switches and an eraser that can be activated anytime the pen is near the sensor"). Wacom Tablet Properties supports per-application settings: "Application-specific settings can be used with all Wacom devices… The Application list in Wacom Tablet Properties enables you to add individual applications, and then tailor your customizable component settings for that application." This satisfies E1, E2, E3 (partially), and E5/E6 — but the driver supplies a default "All other" fallback rather than a request screen, so **E4 fails**.

### 5. The Apple Pencil double-tap/squeeze API explicitly does not prompt
Apple's UIPencilInteraction API delivers events to whatever view controller is in the responder chain; if no app has registered, PencilKit handles the global default set in Settings > Apple Pencil with no prompt. WWDC24 session 10214 (verbatim): "There is a device global preference for what apps should do when Apple Pencil Pro is squeezed. This includes the new options of showing a contextual tool palette or running a system shortcut. Note that if the preference is set to run a shortcut, your app will not be sent the squeeze event." This is the opposite of E4: silent global default; never prompts.

---

## Details — Per-Product Claim Charts

### GROUP 1 — APPLE

**PRODUCT: Apple Pencil (2nd generation), released 2018**

| Claim Element | Present? | Evidence / Source |
|---|---|---|
| E1: Distal-end identification | **NO** | Double-tap sensor located on the **flat side of the barrel near the tip** (not the distal/rear end). Apple Support: "On an Apple Pencil (2nd generation), you can double-tap near the tip of your Apple Pencil to quickly switch back to the tool you used last." How-To Geek: "Hold your Apple Pencil so that your index finger rests naturally on the flat side. Now just double-tap the flat side of the Apple Pencil. The entire bottom third of the Apple Pencil serves as an action button." |
| E2: Currently running app determined | PARTIAL | UIPencilInteraction routes to the foreground responder chain (developer.apple.com/documentation/uikit/uipencilinteraction). |
| E3: Predefined action assigned check | PARTIAL | Apps query `UIPencilInteraction.preferredTapAction` (.ignore, .showColorPalette, .switchEraser, .switchPrevious); system falls back to global preference. |
| E4: Request screen if not assigned | **NO** | No runtime prompt. Configuration is proactive in Settings > Apple Pencil. Selecting "Off" produces a silent no-op. |
| E5: Retrieve predefined action | YES | System reads user-set preference and dispatches. |
| E6: Perform predefined action | YES | Action executes (switch tool / show palette). |
| Claim 2/8: Signal analysis | **NO** | Detection via internal capacitive tap sensor in the Pencil — not analysis of a touchscreen signal from the distal end. |
| Claim 4/10: Idle screen system action | **NO** | No defined behavior at iPadOS Home/Lock idle context. |
| Claim 6/12: App-level action | PARTIAL | Per-app override via UIPencilInteraction (Procreate, LiquidText, PDF Expert). |
| **LITERAL INFRINGEMENT** | **NO** | |
| **DOE** | **NO** | Patent specification distinguishes "front end" from "distal end" as separate physical regions; a barrel gesture is not the substantial equivalent of a distal-end touchscreen invocation. |
| **SEVERITY** | **LOW / NONE** | |

**PRODUCT: Apple Pencil Pro (released May 2024; iPadOS 17.5 released May 13, 2024 added UIKit API support)**

| Claim Element | Present? | Evidence / Source |
|---|---|---|
| E1: Distal-end identification | **NO** | Squeeze gesture acts on the **barrel** (force sensor under grip); double-tap retained on barrel; barrel-roll uses internal gyroscope. No distal-end event. Apple Support: "When you squeeze or double-tap Apple Pencil Pro, you reel a light pulse, which is haptic feedback." |
| E2: Currently running app | PARTIAL | UIPencilInteraction delegate delivery to foreground view. |
| E3: Predefined action check | PARTIAL | Apps may override; otherwise system default from Settings > Apple Pencil > Squeeze. |
| E4: Request screen if not assigned | **NO** | WWDC24 session 10214 (verbatim): "There is a device global preference for what apps should do when Apple Pencil Pro is squeezed. This includes the new options of showing a contextual tool palette or running a system shortcut. Note that if the preference is set to run a shortcut, your app will not be sent the squeeze event." Silent fallback. |
| E5: Retrieve predefined action | YES | Reads global preference or app override. |
| E6: Perform predefined action | YES | Tool Picker / Color Palette / Custom / Off. |
| Claim 2/8: Signal analysis | **NO** | Squeeze detected by internal force sensor in barrel — no touchscreen signal. |
| Claim 4/10: Idle screen system action | **NO** | |
| Claim 6/12: App-level action | YES | Documented per-app override (Procreate, Concepts, Adobe Fresco). |
| **LITERAL INFRINGEMENT** | **NO** | E1 fails. |
| **DOE** | **NO** | Squeeze on barrel ≠ event invocation at the touchscreen using the distal end. |
| **SEVERITY** | **LOW / NONE** | |

---

### GROUP 2 — MICROSOFT

**PRODUCT: Surface Pen Model 1710 (Surface Pro 4 era, October 2015) and Model 1776 (May 2017)**

| Claim Element | Present? | Evidence / Source |
|---|---|---|
| E1: Distal-end identification | **YES (literal)** | Model 1776 has a true tail-mounted eraser button. Wikipedia (Microsoft Pen Protocol): "Microsoft introduced an updated Surface Pen with one side button, a tail-mounted eraser-button and 1,024 levels of pressure." Distinct HID signals reported for tip vs. eraser. |
| E2: Currently running app | **NO** | Tail-button shortcuts are global OS-level events configured in Windows Settings > Pen & Windows Ink. Microsoft Support "How to use your Surface Pen": defaults are Whiteboard / Snip & Sketch / Sticky Notes regardless of foreground app. |
| E3: Predefined action check | **NO** | No per-app lookup. A single global "Allow apps to override the shortcut button behavior" checkbox flips a system-wide override, not a per-app table. |
| E4: Request screen if not assigned | **NO** | Defaults pre-shipped. Thurrott.com (Oct. 23, 2015) documents the three non-customizable defaults on Surface Pro 4: single-click = "Open OneNote and start a new note page"; double-click = "Take a full-screen shot"; press-and-hold = launch Cortana. Setting to "Nothing" produces silent no-op — no assignment dialog. |
| E5: Retrieve predefined action | YES | Windows reads the configured shortcut. |
| E6: Perform predefined action | YES | Launches app / screenshot / etc. |
| Claim 2/8: Signal analysis | **YES (literal)** | Digitizer interprets distinct HID eraser-switch signal from tail. Microsoft Support: "To erase, turn your pen over and rub the end of your pen over your writing or drawing." |
| Claim 4/10: Idle screen system action | YES | Tail-button shortcut launches OneNote/Whiteboard from any screen; affects existing device configuration. |
| Claim 6/12: App-level action | **NO** | No per-app routing of the tail-button event. |
| **LITERAL INFRINGEMENT** | **NO** | E2/E3/E4 fail. |
| **DOE** | **NO** | Global OS shortcut is materially different from per-app lookup + request-screen scheme. |
| **SEVERITY** | **LOW** | Strongest E1/E5/E6 literal read of any pen-tip product in this survey, but E2/E3/E4 absence breaks the chain. |

**PRODUCT: Surface Slim Pen 2 (released October 2021)**

| Claim Element | Present? | Evidence / Source |
|---|---|---|
| E1: Distal-end identification | PARTIAL | Slim Pen 2 has a "shortcut button" at the cap end (no longer doubles as a rubber-eraser-on-screen the way Model 1776 did). Press is a Bluetooth HID event, not a touchscreen distal-end touch. |
| E2: Currently running app | **NO** | Same global-Settings model as Surface Pen 1776. |
| E3: Predefined action check | **NO** | Global, not per-app. |
| E4: Request screen | **NO** | None. |
| E5: Retrieve predefined action | YES | |
| E6: Perform predefined action | YES | |
| Claim 2/8: Signal analysis | PARTIAL | Bluetooth button event, not touchscreen-signal interpretation. |
| Claim 4/10: Idle screen system action | YES | Single-click can wake & launch app. |
| Claim 6/12: App-level action | **NO** | |
| **LITERAL INFRINGEMENT** | **NO** | |
| **DOE** | **NO** | Bluetooth button press is further from the claim than the 1776's eraser-on-screen invocation. |
| **SEVERITY** | **LOW** | |

**Other MPP pens (HP Active Pen, HP Tilt Pen, Lenovo Active Pen 2, Lenovo ThinkPad Pen Pro, Dell Active Pen, ASUS Pen, Acer Active Stylus):** All inherit Windows Pen & Windows Ink global shortcut model. Same non-infringement analysis as Surface Pen / Slim Pen 2. **Severity: LOW.**

---

### GROUP 3 — WACOM AND COMPATIBLE EMR PENS

**PRODUCT: Wacom Pro Pen 2 (KP-504E) with Intuos Pro / Cintiq Pro / MobileStudio Pro**

| Claim Element | Present? | Evidence / Source |
|---|---|---|
| E1: Distal-end identification | **YES (literal)** | True rubber eraser end. Wacom Support: "Some of our pens even have side switches and an eraser that can be activated anytime the pen is near the sensor." EMR digitizer distinguishes tip and eraser via separate HID switch states. |
| E2: Currently running app | **YES (partial)** | Wacom driver maintains the Application list in Wacom Tablet Properties; driver detects foreground application to select settings profile. Wacom 101 Help: "Application-specific settings… The Application list in Wacom Tablet Properties enables you to add individual applications, and then tailor your customizable component settings for that application." |
| E3: Predefined action check | **PARTIAL** | If an application-specific entry exists, driver uses it; otherwise the "All other" fallback applies. This is the closest literal read to E3 in any product surveyed. |
| E4: Request screen if not assigned | **NO** | Fallback to "All other" is silent. User must proactively open Wacom Tablet Properties and click "+" to add an application. |
| E5: Retrieve predefined action | **YES** | Driver retrieves the assigned mapping (default: Erase). |
| E6: Perform predefined action | **YES** | Action executes (Click, Erase, Keystroke, Right Click, etc.). |
| Claim 2/8: Signal analysis | **YES (literal)** | EMR signal includes distinct eraser-switch state; digitizer interprets that signal as originating from the distal end. |
| Claim 4/10: Idle screen system action | PARTIAL | At desktop/idle the eraser end uses the "All other" profile — system-level default applies. |
| Claim 6/12: App-level action | **YES** | Per-app eraser remapping is the canonical Wacom feature. |
| **LITERAL INFRINGEMENT** | **NO** | E4 absent. |
| **DOE** | **PARTIAL** | Strongest equivalents argument in the survey. Wacom driver does perform per-app lookup → fallback; a trier of fact could find silent fallback an insubstantial substitute for a request screen. Patent specification appears to make the request screen a deliberate UX choice, so caution is warranted. |
| **SEVERITY** | **MEDIUM** | |

**PRODUCT: Wacom Pro Pen 3 (ACP-500)** — Base Pro Pen 3 has **no eraser end**: "The pen DOES NOT include an eraser at the other end. Instead, use one of the 3 buttons as the eraser" (sevenpens.com reference). E1 fails. **LITERAL/DOE: NO; SEVERITY: NONE.**

**PRODUCT: Wacom Pro Pen 3E** — Wacom: "features an eraser switch at the rear and a hole for attaching a pen tether." Per-app driver behavior identical to Pro Pen 2. **NO literal (E4 absent); DOE PARTIAL; SEVERITY MEDIUM-LOW.**

**XP-Pen ACK05 / Artist Pro stylus with eraser end:** XP-Pen driver has analogous per-app architecture to Wacom Tablet Properties. **NO literal (E4); DOE PARTIAL; SEVERITY MEDIUM-LOW.**

**Huion PenTech 3.0/4.0 pens (PW517, PW550, PW550S, PW600):** Per huion.com and sevenpens.com, current flagship pens have **two side buttons but no distal-end eraser**. E1 fails. **NO; NONE.** (Some legacy Huion pens have eraser ends; for those, follow the Pro Pen 2 pattern.)

---

### GROUP 4 — CHINESE OEMs

**PRODUCT: Huawei M-Pencil (2nd generation, CD54) and (3rd generation, CE81)**

| Claim Element | Present? | Evidence / Source |
|---|---|---|
| E1: Distal-end identification | **NO** | Double-tap is on the **lower barrel**, not the distal end. Huawei Support (consumer.huawei.com en-us15823256): "double-tap the lower half of the stylus body… within 40 mm." Detection via internal capacitive sensor in pen. |
| E2: Currently running app | **YES** | Huawei is explicitly app-aware: "You can go to Settings > Accessibility features > Stylus > Double-tap to set the double-tap feature for pre-installed apps, such as Notepad and Notes. You can also configure the double-tap switching feature on third-party apps such as TouchNotes." |
| E3: Predefined action check | **YES** | Per-app config; four options: Switch between current tool and eraser / Switch to previous tool / Open color palette / Open shortcut menu. |
| E4: Request screen if not assigned | **NO** | No runtime prompt. App-list configured proactively in Settings. |
| E5: Retrieve predefined action | YES | |
| E6: Perform predefined action | YES | |
| Claim 2/8: Signal analysis | **NO** | Capacitive tap sensor in pen, not touchscreen signal. |
| Claim 4/10: Idle screen system action | PARTIAL | "Open shortcut menu" operates system-wide. |
| Claim 6/12: App-level action | **YES** | Explicit per-app config. |
| **LITERAL INFRINGEMENT** | **NO** | E1 fails (barrel ≠ distal end); E4 fails. |
| **DOE** | **NO** | Barrel double-tap is not equivalent to distal-end on-screen invocation. |
| **SEVERITY** | **LOW** | Strongest read on E2/E3/E6/Claim 12 among Chinese OEMs. |

**PRODUCT: Xiaomi Smart Pen 2nd generation** — Pen has **side buttons only**, no distal-end feature. mi.com FAQ: "When the tablet screen is on, long press the up key (screenshot key) to take a screenshot, long press the shorthand key (shorthand key) to quickly enter the note APP." Button mapping is not user-customizable in HyperOS (confirmed by XDA Forums). **LITERAL/DOE: NO; SEVERITY: NONE.**

**PRODUCT: Lenovo Precision Pen 2 (Android)** — Tail of pen is the USB-C charging port under a removable cap; only two side buttons. Per parkablogs.com: "The side buttons can't be customised within Android, and not all apps allow you to customise the shortcut buttons." MyNextTablet: "If you press the upper button, you get to the start screen. And if you press the lower button, a smart bar opens. That's it." **LITERAL/DOE: NO; SEVERITY: NONE.**

**PRODUCT: Honor Magic-Pencil 3** — No distal-end button. Honor product page: "The pen's body is equipped with an invisible touch control, allowing you to switch between pen and eraser by double-clicking the front end of the pen." Touch area is near front end, configurable only as global on/off, not per-app routing. **LITERAL/DOE: NO; SEVERITY: NONE.**

---

### GROUP 5 — E-INK TABLETS

**PRODUCT: reMarkable Marker Plus (RM212)**

| Claim Element | Present? | Evidence / Source |
|---|---|---|
| E1: Distal-end identification | **YES (literal)** | Physical eraser button at top end with audible click. reMarkable Support: "To erase with Marker Plus: Simply flip the Marker Plus upside down and start erasing like you would with a traditional pencil eraser." Good e-Reader: "it actually has a button, which presses down and you hear an audible click… you have to click down on the part you want to delete." |
| E2: Currently running app | **NO** | Single-purpose device; reMarkable OS does not host third-party apps in a multitasking sense. |
| E3: Predefined action check | **NO** | Eraser action is hard-wired. |
| E4: Request screen if not assigned | **NO** | |
| E5: Retrieve predefined action | PARTIAL | Fixed (erase), not retrieved from a map. |
| E6: Perform predefined action | YES | Erases strokes. |
| Claim 2/8: Signal analysis | **YES** | EMR digitizer distinguishes tip vs. eraser. |
| Claim 4/10: Idle screen system action | **NO** | |
| Claim 6/12: App-level action | **NO** | |
| **LITERAL INFRINGEMENT** | **NO** | |
| **DOE** | **NO** | Single fixed function is not an equivalent of per-app configurable action with request-screen assignment. |
| **SEVERITY** | **NONE** | |

**PRODUCT: Amazon Kindle Scribe Premium Pen**

| Claim Element | Present? | Evidence / Source |
|---|---|---|
| E1: Distal-end identification | **PARTIAL** | Distal end is a passive Wacom-EMR eraser; the configurable button is on the side. Amazon Customer Service: "Flip your stylus pen so the eraser at the top is facing the screen. To activate the eraser, press the pen firmly down." |
| E2: Currently running app | **NO** | No app-context routing. |
| E3: Predefined action check | PARTIAL | Side-button (not distal) is configurable from 8 options. Distal eraser is fixed. |
| E4: Request screen if not assigned | **NO** | Amazon Customer Service: configuration via Settings > Pen settings > Shortcut button. No runtime prompt. |
| E5: Retrieve predefined action | PARTIAL | For side button only. |
| E6: Perform predefined action | YES | Selected tool engages on side-button press. |
| Claim 2/8: Signal analysis | YES | EMR signal differentiates eraser tip. |
| Claim 4/10: Idle screen system action | NO | |
| Claim 6/12: App-level action | NO | |
| **LITERAL INFRINGEMENT** | **NO** | Distal end is passive; configurable button is on side. |
| **DOE** | **NO** | |
| **SEVERITY** | **NONE** | |

**PRODUCT: Onyx Boox Pen2 Pro** — shop.boox.com: "The Pen2 Pro is a passive stylus that requires no extra power or Bluetooth pairing… With the eraser on the bottom, you can remove notes quickly." Fixed-function eraser; no app-context routing; no configurable actions beyond erase. **LITERAL/DOE: NO; SEVERITY: NONE.**

**Viwoods Stylus Pro:** Similar passive-eraser-only behavior. **NO; NONE.**

---

### GROUP 6 — SAMSUNG (Assignee, documented for completeness)

**PRODUCT: Galaxy S Pen (through Galaxy S25 Ultra)** — S Pen has a side button and Air Actions (BLE gestures via accelerometer/gyro in S Pen Pro and recent Note S Pens); no distal-end feature. Air Actions are app-context-aware with per-app configuration (Samsung Support: "Open Settings, and then search for and select Air actions. Tap your desired app under App actions. … Tap your desired gesture (e.g. Left), and select a new command"). However, Samsung is the assignee — **no infringement risk to Samsung itself**.

---

## Master Summary Table

| Product | E1 | E2 | E3 | E4 | E5 | E6 | Literal? | DOE? | Severity |
|---|---|---|---|---|---|---|---|---|---|
| Apple Pencil 2 (2018) | NO | PARTIAL | PARTIAL | NO | YES | YES | NO | NO | LOW |
| Apple Pencil Pro (2024) | NO | PARTIAL | PARTIAL | NO | YES | YES | NO | NO | LOW |
| Surface Pen 1710 (2015) | YES | NO | NO | NO | YES | YES | NO | NO | LOW |
| Surface Pen 1776 (2017) | YES | NO | NO | NO | YES | YES | NO | NO | LOW |
| Surface Slim Pen 2 (2021) | PARTIAL | NO | NO | NO | YES | YES | NO | NO | LOW |
| HP/Dell/Lenovo/ASUS/Acer MPP | varies | NO | NO | NO | YES | YES | NO | NO | LOW |
| **Wacom Pro Pen 2** | **YES** | **YES** | **PARTIAL** | **NO** | **YES** | **YES** | **NO** | **PARTIAL** | **MEDIUM** |
| Wacom Pro Pen 3 (base) | NO | — | — | — | — | — | NO | NO | NONE |
| Wacom Pro Pen 3E | YES | YES | PARTIAL | NO | YES | YES | NO | PARTIAL | MEDIUM-LOW |
| XP-Pen w/ eraser end | YES | YES | PARTIAL | NO | YES | YES | NO | PARTIAL | MEDIUM-LOW |
| Huion PW517/550/600 | NO | — | — | — | — | — | NO | NO | NONE |
| Huawei M-Pencil 2/3 | NO | YES | YES | NO | YES | YES | NO | NO | LOW |
| Xiaomi Smart Pen 2 | NO | — | — | — | — | — | NO | NO | NONE |
| Lenovo Precision Pen 2 | NO | — | — | — | — | — | NO | NO | NONE |
| Honor Magic-Pencil 3 | NO | — | — | — | — | — | NO | NO | NONE |
| reMarkable Marker Plus | YES | NO | NO | NO | PARTIAL | YES | NO | NO | NONE |
| Kindle Scribe Premium Pen | PARTIAL | NO | PARTIAL | NO | PARTIAL | YES | NO | NO | NONE |
| Onyx Boox Pen2 Pro | YES | NO | NO | NO | PARTIAL | YES | NO | NO | NONE |
| Viwoods Stylus Pro | YES | NO | NO | NO | PARTIAL | YES | NO | NO | NONE |
| Samsung S Pen | NO (Assignee) | — | — | — | — | — | N/A | N/A | N/A |

---

## Recommendations

**Stage 1 — Highest priority: Wacom Pro Pen 2 / Pro Pen 3E.** Only product family with a credible doctrine-of-equivalents theory: true EMR distal-end signal (E1, Claim 2/8 literal) + documented per-app lookup in Wacom Tablet Properties (E2, E3, Claim 6/12) + retrieve+perform path (E5, E6). Before any enforcement action: (a) confirm whether the Wacom driver, on first encounter of an unrecognized application, displays any UI to the user — even a system-tray balloon would strengthen E4 DOE; (b) obtain Wacom driver binary versions sold during the period of enforceability and review application-lookup logic; (c) commission an independent expert declaration on whether silent "All other" fallback is or is not an insubstantial alternative to a request screen; (d) review prosecution history of US 9,857,889 for any disclaimer of silent-fallback equivalents.

**Stage 2 — Selective monitoring: Microsoft Surface Pen 1776, Slim Pen 2, and broader MPP ecosystem.** E1 reads literally; E5/E6 read literally. Family fails E2/E3/E4 because the tail-button shortcut is OS-global. If Microsoft were to ship a Windows update introducing per-app action routing of the top button **and** a runtime "assign action" prompt (e.g., as part of Click to Do in 24H2+), severity rises to **MEDIUM-HIGH**. Maintain a release-notes watch on the Pen & Windows Ink settings page.

**Stage 3 — Deprioritize: Apple, Huawei, Xiaomi, Lenovo, Honor, reMarkable, Amazon, Boox, Viwoods.** All fail E1 (either no distal-end feature or a fixed-function passive eraser). Patent specification language and the deliberate "distal end" recitation in claim 1 make DOE arguments very weak. No enforcement-justifying read.

**Benchmarks that would change recommendations:**
- New product launching with (i) a distal-end touch/button feature, (ii) per-app configurable actions selected at runtime based on foreground app, AND (iii) a first-use/unassigned-event prompt → severity **HIGH**, escalate.
- If Apple, Microsoft, or Wacom ships a first-time setup UI that triggers when the user double-taps/squeezes/inverts the pen for the first time in an app that has not registered a handler → severity rises to MEDIUM-HIGH for that vendor.
- If Wacom adds a per-application "configure now" prompt when an unrecognized app is detected → Pro Pen 2 severity rises to **HIGH**.

---

## Caveats

- **Negative findings on E4 are based on the absence of documentation** describing any such prompt across Apple Support, Microsoft Support, Wacom Support, Huawei Support, Lenovo Support, Honor Support, Amazon Customer Service, reMarkable Support, and shop.boox.com. A negative cannot be proven absolutely from secondary documentation; firsthand device testing is recommended before any infringement contention, particularly for the Wacom and Huawei cases.
- **The Wacom Pro Pen 2 DOE assessment is the most legally contested call** in this chart. Outcomes could push either way depending on how a court reads "request screen" — narrowly (a modal dialog) vs. broadly (any user-facing indication that no action is assigned). Obtain the full prosecution history of US 9,857,889 before pressing DOE.
- **Patent priority date is June 29, 2012** (Indian Provisional Application No. 2604/CHE/2012); the US continuation (US App. Ser. No. 13/931,159) was filed June 28, 2013. The Surface Pen Model 1616 (Surface Pro 3, May 2014) and Model 1710 (Surface Pro 4, October 2015) **post-date the priority date by approximately 2 and 3 years respectively**, so they do not constitute prior art and the patent owner could in principle reach them. Invalidity-defense research should focus on stylus pen + per-app event-handling art predating June 29, 2012 (e.g., earlier Wacom driver versions on Intuos 4/5; N-Trig Duosense documentation; Microsoft Tablet PC SDK).
- **Apple Pencil Pro squeeze + barrel-roll APIs were introduced in iPadOS 17.5 (released May 13, 2024)** — well after the patent priority. WWDC24 session 10214: "New in iPadOS 17.5, UIKit has support for all the great new features of Apple Pencil Pro." Apple's documented design choice (silent global fallback, never prompts) makes infringement particularly weak for the Pencil Pro.
- **Honor Magic-Pencil 3 was not testable firsthand**; conclusions rely on Honor's official product page and the Honor MagicPad 3 IT Pro review. A hands-on test of supported app list and Settings menu may surface a barrel-end function not visible in marketing copy.
- **Huion's eraser-end SKUs are a moving target.** Older Huion pens shipped with rubber erasers; current flagship PenTech 3.0/4.0 pens (PW517/PW550/PW550S/PW600) lack a distal-end button. Verify product roadmap before publication.
- **Samsung is the assignee.** This chart documents Samsung's own products for completeness only; it does not assess infringement by them.
- **This chart is technical-mapping support only and is not a legal opinion.** Claim construction, prosecution history estoppel, on-sale-bar analysis, and IPR/invalidity defenses (centered on the June 29, 2012 priority date) must be addressed separately before any litigation decision.