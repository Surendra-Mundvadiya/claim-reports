# Claim Mapping: US 9,354,742 B2 → Potentially Infringing Products

**Patent:** US 9,354,742 B2
**Title:** Foldable Electronic Device and Method of Managing Visible Regions Thereof
**Inventor:** Samudrala Nagaraju
**Assignee:** Samsung Electronics Co., Ltd.
**Filed:** April 10, 2014 | **Issued:** May 31, 2016

---

## Patent Claims Reference

**Independent Claim 1 (Method):**
- 1(a) Detecting if the foldable electronic device is bent
- 1(b) Determining a flat view area and a bent view area in response to detection of bending
- 1(c) Providing at least one user interface in a bent view area of the rear display unit
- 1(d) The UI is associated with applications **different from** the application in the flat view area

**Independent Claim 10 (Device):** Hardware version — touch-sensitive display body with front + rear display unit + microprocessor configured as in Claim 1

**Key Dependent Claims:** 2 (touch), 3 (angle threshold), 5 (re-layout), 6 (UI on both), 7 (squeeze), 8-9 (roll)

---

## TIER 1: HIGH SEVERITY (Literal Infringement Likely)

### 1. Huawei Mate X / Mate Xs / Mate Xs 2

| Claim Element | Product Feature | Evidence |
|---|---|---|
| 1(a) Bend detection | Falcon-wing hinge with sensors detects fold state | Huawei spec sheet; iFixit teardown |
| 1(b) Flat + bent view area | 6.6" front "flat" panel + 6.38" rear panel from single 8" OLED | Wikipedia: "8-inch OLED that can fold outwards resulting in a 6.6-inch main display and a 6.38-inch rear display" |
| 1(c) UI on rear display unit | Rear portion of wraparound display runs independent UI | PCWorld hands-on, Huawei marketing |
| 1(d) Different applications | Rear can show selfie viewfinder while front shows camera controls | Huawei camera app demos |
| Claim 10 (device) | Touch-sensitive flexible OLED body + Kirin processor | Official specs |
| Claim 2 (touch) | Touch active on both halves | Reviews confirm |
| Claim 5 (re-layout) | UI re-flows when unfolded to 8" tablet mode | EMUI documentation |
| Claim 6 (UI on both) | Both halves display content simultaneously | Standard operation |
| Claims 7-9 | ❌ No squeeze/roll events | N/A |

**Verdict: LITERAL INFRINGEMENT — Claims 1, 2, 5, 6, 10**

---

### 2. Royole FlexPai 1 / FlexPai 2

| Claim Element | Product Feature | Evidence |
|---|---|---|
| 1(a) Bend detection | Hinge sensors detect fold | Royole specs |
| 1(b) Flat + bent view area | Single 7.8" OLED → two outward-facing halves when folded | Android Authority, Engadget |
| 1(c) UI on rear display unit | Each half acts as independent homescreen | XDA Developers |
| 1(d) Different applications | **Confirmed**: "Instagram on front screen, WhatsApp on back screen" | XDA Developers FlexPai 2 hands-on |
| Claim 10 (device) | Flexible OLED + Snapdragon + waterOS | Official specs |
| Claim 2 (touch) | Touch on both halves | XDA review |
| Claim 5 (re-layout) | Re-layout on unfold to 7.8" tablet | waterOS behavior |
| Claim 6 (UI on both) | Yes, simultaneous | XDA review |
| Claims 7-9 | ❌ Not implemented | N/A |

**Verdict: LITERAL INFRINGEMENT — Claims 1, 2, 5, 6, 10 (strongest match of any product)**

---

### 3. Huawei Mate XT Ultimate (Tri-fold)

| Claim Element | Product Feature | Evidence |
|---|---|---|
| 1(a) Bend detection | Dual-hinge sensors (inward + outward folds) | TechInsights teardown |
| 1(b) Flat + bent view area | Z-fold creates flat + outward-bent sections | Designboom |
| 1(c) UI on rear display unit | Outward-folded section faces rear, runs UI | Huawei demos |
| 1(d) Different applications | "Dual mode... different apps displayed on each" | Designboom |
| Claim 10 (device) | 10.2" flexible OLED, tri-fold | Huawei specs |
| Claim 2 (touch) | Touch on all sections | Reviews |
| Claim 5 (re-layout) | Re-layout across 6.4"/7.9"/10.2" modes | Android Authority |
| Claim 6 (UI on both) | Yes | Demos |

**Verdict: LITERAL INFRINGEMENT — Claims 1, 2, 5, 6, 10**

---

## TIER 2: MEDIUM SEVERITY (Doctrine of Equivalents)

### 4. Google Pixel Fold / Pixel 9 Pro Fold / Pixel 10 Pro Fold

| Claim Element | Product Feature | Evidence | Match? |
|---|---|---|---|
| 1(a) Bend detection | Hall-effect hinge sensor | Teardowns | ✅ |
| 1(b) Flat + bent view area | Inner main display + separate cover display | Google specs | ⚠️ DOE only — separate panels, not one bent display |
| 1(c) UI on rear display unit | Cover screen displays UI when folded | Google support | ⚠️ DOE — cover ≠ "rear of foldable body" literally |
| 1(d) Different applications | "Continue using apps on fold" in Android 14 QPR1+ | 9to5Google (Sept 2023) | ✅ |
| Claim 10 (device) | Two displays + Tensor processor | Specs | ⚠️ DOE |

**Verdict: DOE INFRINGEMENT plausible — Claims 1, 10 (literal weak due to separate cover screen)**

---

### 5. OnePlus Open / Oppo Find N / N2 / N3 / N5

| Claim Element | Product Feature | Evidence | Match? |
|---|---|---|---|
| 1(a) Bend detection | Hinge sensor | Oppo specs | ✅ |
| 1(b) Flat + bent view area | Cover + inner foldable | Oppo specs | ⚠️ DOE |
| 1(c) UI on rear | Cover screen runs UI when folded | OnePlus documentation | ⚠️ DOE |
| 1(d) Different applications | Swipe-up-to-continue gesture pioneered here | Android Authority | ✅ |
| Claim 10 | Snapdragon + dual displays | Specs | ⚠️ DOE |

**Verdict: DOE INFRINGEMENT plausible — Claims 1, 10**

---

### 6. Honor Magic V / V2 / V3 / V5 / Vs Ultimate / V Flip

| Claim Element | Product Feature | Evidence | Match? |
|---|---|---|---|
| 1(a) Bend detection | Hinge sensor | Honor specs | ✅ |
| 1(b) Flat + bent view area | Cover + inner foldable | Honor specs | ⚠️ DOE |
| 1(c) UI on rear | Cover screen UI when folded | MagicOS docs | ⚠️ DOE |
| 1(d) Different applications | **Face-to-Face Translation**: source language on inner, translated on cover — clearly different apps simultaneously | Honor marketing, Amateur Photographer review | ✅ Strong |
| Claim 10 | Dual display + Snapdragon | Specs | ⚠️ DOE |

**Verdict: STRONG DOE INFRINGEMENT — Claims 1, 10 (best DOE case among book-style)**

---

### 7. Xiaomi Mix Fold 1 / 2 / 3 / 4 / Mix Flip

| Claim Element | Product Feature | Evidence | Match? |
|---|---|---|---|
| 1(a) Bend detection | Hinge sensor | Xiaomi specs | ✅ |
| 1(b) Flat + bent view area | Cover + inner foldable | Xiaomi specs | ⚠️ DOE |
| 1(c) UI on rear | Cover screen UI | MIUI Fold docs | ⚠️ DOE |
| 1(d) Different applications | "After folding" options: continue app on cover, or different app | GSMArena Mix Fold 3 review | ✅ |
| Claim 10 | Dual display + Snapdragon | Specs | ⚠️ DOE |

**Verdict: DOE INFRINGEMENT plausible — Claims 1, 10**

---

### 8. Motorola Razr / Razr Plus / 40 Ultra / 50 Ultra / Razr Fold

| Claim Element | Product Feature | Evidence | Match? |
|---|---|---|---|
| 1(a) Bend detection | Hinge sensor (clamshell) | Motorola specs | ✅ |
| 1(b) Flat + bent view area | Large cover (3.6"-6.6") + inner foldable | Motorola.com | ⚠️ DOE — but cover IS on rear face when folded |
| 1(c) UI on rear display unit | Full Android apps run on cover/rear face | Android Central, MakeUseOf | ⚠️ DOE-leaning-literal |
| 1(d) Different applications | "Continue apps on cover screen" — independent app launch on cover | Motorola support docs | ✅ |
| Claim 10 | Dual display + Snapdragon | Specs | ⚠️ DOE |

**Verdict: STRONG DOE INFRINGEMENT — Claims 1, 10 (Razr Fold's 6.6" cover is closest to "rear display unit")**

---

### 9. Samsung Galaxy Z Fold 1-7, Z Flip 1-7, Z TriFold

| Claim Element | Product Feature | Match? |
|---|---|---|
| 1(a)-(d) | Cover screen + inner foldable + Flex Mode + App Continuity | ⚠️ DOE — but Samsung CANNOT infringe its own patent |

**Verdict: N/A — Patent owner (used for claim-scope calibration only)**

---

## TIER 3: LOW SEVERITY (Weak / Unlikely Infringement)

### 10. Microsoft Surface Duo 1 / 2

| Claim Element | Product Feature | Match? |
|---|---|---|
| 1(a) Bend detection | 360° hinge angle sensor | ⚠️ Partial |
| 1(b) Flat + bent view area | Two separate panels, not one bent display | ❌ |
| 1(c) UI on rear | Different apps on each panel | ⚠️ DOE only |
| 1(d) Different apps | Yes | ✅ |

**Verdict: WEAK — separate panels, not a foldable display per the patent**

---

### 11. Lenovo ThinkPad X1 Fold / ASUS Zenbook 17 Fold / HP Spectre Foldable

| Claim Element | Product Feature | Match? |
|---|---|---|
| 1(a) Bend detection | Hall-effect sensors trigger orientation change | ✅ |
| 1(b) Flat + bent view area | Single 13.3"-17" foldable OLED creates two regions | ✅ |
| 1(c) UI on rear | When folded, one half faces away in book mode | ⚠️ Partial |
| 1(d) Different apps | Windows allows different apps per half | ✅ |
| Claim 10 | Single foldable OLED | ✅ |

**Verdict: POSSIBLE INFRINGEMENT — Claims 1, 5, 10 (uncommon target — foldable PCs)**

---

### 12. LG Wing

| Claim Element | Match? |
|---|---|
| Foldable display | ❌ Swivel mechanism, not foldable |

**Verdict: NO INFRINGEMENT**

---

### 13. ZTE Axon M

| Claim Element | Match? |
|---|---|
| 1(b) Single foldable display | ❌ Two separate panels with hinge |

**Verdict: NO INFRINGEMENT (same issue as Surface Duo)**

---

### 14. Rollable Concepts (Oppo X 2021, LG Rollable, TCL Rollable, Motorola Rizr)

| Claim Element | Match? |
|---|---|
| 1(a) Roll detection | ✅ Roll sensor |
| 1(b) Flat + bent area | ❌ No rear display — rolled portion is internal |
| Claims 7-9 (squeeze/roll) | ✅ Conceptually fit |

**Verdict: NO INFRINGEMENT of independent claims (never commercially shipped anyway)**

---

## Final Summary Matrix

| Product | Claim 1 | Claim 10 | Dep. 2 | Dep. 5 | Dep. 6 | Dep. 7 | Dep. 8-9 | Severity |
|---|---|---|---|---|---|---|---|---|
| **Huawei Mate X family** | ✅ Literal | ✅ Literal | ✅ | ✅ | ✅ | ❌ | ❌ | **HIGH** |
| **Royole FlexPai 1/2** | ✅ Literal | ✅ Literal | ✅ | ✅ | ✅ | ❌ | ❌ | **HIGH** |
| **Huawei Mate XT** | ✅ Literal | ✅ Literal | ✅ | ✅ | ✅ | ❌ | ❌ | **HIGH** |
| Honor Magic V3/V5 | ⚠️ DOE | ⚠️ DOE | ✅ | ✅ | ✅ | ❌ | ❌ | MED-HIGH |
| Motorola Razr Fold | ⚠️ DOE | ⚠️ DOE | ✅ | ✅ | ✅ | ❌ | ❌ | MED-HIGH |
| OnePlus Open / Oppo Find N | ⚠️ DOE | ⚠️ DOE | ✅ | ✅ | ✅ | ❌ | ❌ | MEDIUM |
| Pixel Fold / 9 Pro Fold | ⚠️ DOE | ⚠️ DOE | ✅ | ✅ | ✅ | ❌ | ❌ | MEDIUM |
| Xiaomi Mix Fold 3/4 | ⚠️ DOE | ⚠️ DOE | ✅ | ✅ | ✅ | ❌ | ❌ | MEDIUM |
| Lenovo X1 Fold / ASUS Fold | ⚠️ DOE | ⚠️ DOE | ✅ | ✅ | ⚠️ | ❌ | ❌ | MEDIUM |
| Samsung Galaxy Z Fold/Flip | N/A | N/A | — | — | — | — | — | OWNER |
| Surface Duo 1/2 | ❌ | ❌ | — | — | — | — | — | LOW |
| LG Wing | ❌ | ❌ | — | — | — | — | — | NONE |
| ZTE Axon M | ❌ | ❌ | — | — | — | — | — | NONE |
| Rollable concepts | ❌ | ❌ | — | — | — | ✅ | ✅ | NONE (no rear display) |

**Legend:** ✅ = element present | ⚠️ DOE = arguable under Doctrine of Equivalents only | ❌ = element absent

---

## Bottom Line

Only **3 product families** (Huawei Mate X, Mate XT, Royole FlexPai) show literal infringement of independent claims. All book-style foldables require Doctrine of Equivalents arguments because they use separate cover screens rather than the patent's described continuous bent display.
