# Litigation-Grade Claim Chart & Patent Validity Analysis
## Indian Patent Application No. 201641043709 (Samsung Electronics Co., Ltd.) v. Snapchat "Dual Camera — Cutout" (Snap Inc.)

> **Nature of this document.** This is technical/strategic pre-litigation analysis, **not legal advice**. Infringement and validity are ultimately legal determinations for a court. Per instruction, the patent is treated as **granted**; however, grant status, claim text as-granted, and family membership could **not** be independently confirmed because the Indian Patent Office InPASS portal is CAPTCHA-gated and the specific Google Patents/Espacenet records were not retrievable in this session. This must be verified manually before filing (see Recommendations). Where a conclusion depends on contested claim construction or on inference from observed public behavior rather than Snap's source code, that is flagged expressly.

---

## TL;DR
- **Snapchat's "Cutout" layout most likely literally infringes independent method Claim 1 and apparatus Claim 4**, and infringes dependent Claims 2/5 only weakly (doctrine of equivalents at best); **Claims 3 and 6 (image "stitching") are NOT infringed**; Claim 7 (system) is infringed to the extent Claim 1 is, but is the single most invalidity-prone claim. The decisive battleground is **claim construction of "object" and "intended location,"** not whether Snap performs the basic cross-camera overlay — it plainly does.
- **The patent is seriously vulnerable.** The most damaging reference, **US 9,307,153 B2, is owned by Samsung itself** (Korean priority **July 5, 2013** — 3.5 years before this patent) and discloses the patent's signature element: detecting a subject in the **front** image and overlaying that partial front image onto the **rear** image. Combined with **Samsung's own Galaxy S4 "Dual Shot" (March 2013)** live cross-camera overlay, this creates an acute **self-collision / obviousness** problem — layered on top of India's **Section 3(k)** computer-programme-per-se eligibility bar, which is the patent's biggest India-specific weakness.
- **Enforcement is viable but not straightforward.** The accused product post-dates the priority date by ~5.7 years (so it is not the patentee's own prior art), and India is Snap's largest market (250M+ MAU). But the method is performed by the **end user** operating the app, not by Snap directly — so the case must be built on an **indirect/inducement** theory, and the patentee enjoys **no statutory presumption of validity** (Section 13(4)), making the interim-injunction prima-facie hurdle harder than in many jurisdictions.

---

## Key Findings

1. **US 9,307,153 B2 ("Method and apparatus for previewing a dual-shot image") is assigned to Samsung Electronics Co., Ltd.** (inventors Seung-pok Lee, Chang-won Son, Dae-young Noh), claiming priority under 35 U.S.C. §119(a) to **Korean application 10-2013-0079005, filed July 5, 2013** (USPTO published specification, image-ppubs.uspto.gov/.../9307153; assignee confirmed at patents.justia.com/assignee/samsung-electronics). Its independent claim recites setting a subject part within the front image, "set an area of pixels of interest … enclosing the subject part, output from the first image sensor a partial image … and create … a combined image by **overlaying the partial image on the rear image**" — i.e., the exact cross-camera asymmetry that is the patent-in-suit's "signature element." This is the patentee's **own** prior art and is potentially dispositive on validity.

2. **Snapchat "Cutout"** uses Snap's Lens/segmentation technology to detect the user's face and body in the **front (selfie)** camera live preview, remove the background, extract the silhouette, and composite it live over the **rear** camera preview in the viewfinder before capture (Snap developer docs; Elite Daily: "Cutout works by detecting your face and body in the selfie camera and removing your background," elitedaily.com, Sep 1, 2022; Tom's Guide: Cutout places "the outline of your selfie on what the rear camera is capturing," tomsguide.com).

3. **Dates are clean and favorable.** Patent filed **Dec 21, 2016**; claims amended **Aug 4, 2020**; Snapchat first teased Dual Camera within "Director Mode" on **April 28, 2022** (TechCrunch); Dual Camera launched on iOS **Aug 29, 2022** (Snap Newsroom; MacRumors), with Android "in the coming months."

4. **India is Snap Inc.'s single largest market globally, with "over 250 million monthly active users (MAU)"** (Snap Newsroom, newsroom.snap.com/india-mau-250m), up from 200M+ in May 2023, with ~90% of daily users aged 13–34 — making India a high-value, properly-grounded enforcement jurisdiction.

5. **No presumption of validity in India.** Section 13(4) of the Patents Act, 1970 provides that examination "shall not be deemed in any way to warrant the validity of any patent," and the Supreme Court in *Bishwanath Prasad Radhey Shyam v. Hindustan Metal Industries*, (1979) 2 SCC 511, held that the grant and sealing of a patent "does not guarantee the validity of the patent." This makes Snap's invalidity defenses unusually potent at the interim stage.

---

## Details

### DELIVERABLE 2 — DATE VERIFICATION TABLE

| Event | Date | Source (name, URL, verbatim where useful) |
|---|---|---|
| Patent filing / priority date | **Dec 21, 2016** | Per task. **Not** independently confirmed (InPASS CAPTCHA-gated). Critical date for prior art. |
| Patent amended claims | **Aug 4, 2020** | Per task. |
| **US 9,307,153 Korean priority** | **July 5, 2013** | USPTO spec: "claims the benefit … of a Korean patent application filed on Jul. 5, 2013 … Serial No. 10-2013-0079005" (image-ppubs.uspto.gov/.../9307153). |
| US 9,307,153 assignee | Samsung Electronics Co., Ltd. | patents.justia.com (Samsung assignee index). |
| Samsung Galaxy S4 "Dual Shot" | **Announced March 14, 2013** (Samsung Unpacked, NYC) | Stuff.tv (Mar 2013); allaboutgalaxys4.com; dpreview.com. |
| US 9,204,026 B2 (LG) priority | Korean priority **Nov 2010** | USPTO/Google Patents (US20120105579A1 family; EP2448278A2). |
| US 10,334,153 B2 issue | **June 25, 2019** | patents.justia.com/patent/10334153 (post-dates patent — context only). |
| Director Mode / Dual Camera teaser | **April 28, 2022** | TechCrunch ("9:51 AM PDT · April 28, 2022"), techcrunch.com. |
| Dual Camera iOS launch | **Aug 29, 2022** | Snap Newsroom (newsroom.snap.com/dual-camera): "available globally on iOS today"; MacRumors 2022/08/29. |
| Dual Camera Android availability | After iOS, "in the coming months" / "soon" | Snap Newsroom; help.snapchat.com/.../8866040216084 ("Dual Camera will be available on Android soon"). Exact Android general-availability date not findable; Director Mode (containing Dual Camera) reached "all Snapchat users on Android and iOS" by late Oct 2022 with two-camera recording rolling to Android "in the weeks ahead" (Engadget/Yahoo). |

**Conclusion:** The accused product post-dates the patent priority date by ~5.7 years. It therefore **cannot** be cited as the patentee's own prior art, and any "we did it first" argument by Snap must rest on third-party or Samsung's own earlier disclosures (which, ironically, also threaten the patent's validity).

---

### DELIVERABLE 1 — ELEMENT-BY-ELEMENT CLAIM CHART

> Evidence is tagged **[Snap admission]** (strongest — party statements) or **[3P]** (third-party). Quotes are <20 words and attributed. Determinations: **YES / NO / PARTIAL**.

#### CLAIM 1 (Method) — independent

| # | Claim language (limitation) | Accused Cutout functionality | Supporting evidence (≥2 independent) | Determination |
|---|---|---|---|---|
| 1a | "detecting, by an object detection unit (202), at least one object in a camera preview … preview of at least one of first camera and at least one of second camera" | Cutout's Lens segmentation detects the user's **face and body** in the front-camera live preview while both cameras run | **[Snap admission]** developers.snap.com/lens-studio/features/camera/dual-camera — extends "face and body tracking to custom textures, including the reverseCameraTexture." **[3P]** Elite Daily (Sep 1, 2022): "Cutout works by detecting your face and body in the selfie camera." | **YES** |
| 1b | "selecting, by an object extraction unit (204), the at least one object from the camera preview of one of [first/second] camera" | Cutout extracts the user's silhouette by removing background (segmentation = selection of foreground object) | **[3P]** Zacks/Yahoo Finance: "cutout layout allows users to erase the background of the front image and paste it." **[3P]** MakeUseOf: "superimposing the image from your selfie camera." | **YES** (subject to "object" construction — see Validity §(b)) |
| 1c | "determining, by a location detection unit (206), at least one intended location in the camera preview of [the other] camera, wherein the camera preview in which the object is **selected** is **DIFFERENT** from the camera preview in which the … location is determined" (cross-camera asymmetry) | The extracted front-camera silhouette is placed onto the **live rear** camera preview — object source (front) ≠ overlay target (rear) | **[3P]** Zacks/Yahoo: "paste it on the rear-view image." **[3P]** ScreenRant: green-screen effect placing the selfie over the rear feed. **[3P]** Tom's Guide: "on what the rear camera is capturing." | **PARTIAL → likely YES.** The asymmetry is met; the contested word is "**determining** … location" (Snap may argue Cutout uses a fixed default placement, not active determination — see DoE below). |
| 1d | "rendering, by a rendering unit (208), a **final camera preview** … by overlaying the at least one object on the at least one intended location" (rendered **live**, pre-capture) | Composite (silhouette over rear feed) is rendered in the viewfinder before the snap is taken | **[Snap admission]** developers.snap.com: Dual Camera "render[s] both front and rear cameras at the same time." **[3P]** Tom's Guide: Cutout "place[s] the outline of your selfie on what the rear camera is capturing." | **YES** |

**Claim 1 overall verdict: LITERAL INFRINGEMENT — LIKELY YES.** Every limitation maps to observed Cutout behavior; the only genuine dispute is element 1c's "determining … intended location."
**Doctrine of equivalents (function-way-result) for 1c, if literal "determining" fails:** Even a fixed/centered placement performs substantially the **same function** (positioning the extracted object within the other camera's preview), in substantially the **same way** (compositing the segmented foreground at a screen coordinate), to reach substantially the **same result** (a live combined preview with the object over the second-camera scene). India recognizes the doctrine of equivalents (*Raj Prakash v. Mangat Ram Chowdhry*, ILR (1978) 2 Del 412). Equivalence is well-supported.

#### CLAIM 2 (Method) — overlay at least one **property** (e.g., color, lighting) of the object
| Limitation | Cutout behavior | Evidence | Determination |
|---|---|---|---|
| Render by overlaying a **property** of the object (spec examples: lipstick color, lighting) onto the location | Cutout overlays the **entire silhouette image**, not an extracted property such as a color or lighting value | **[3P]** MakeUseOf, ScreenRant (describe whole-image green-screen compositing, no property transfer). | **NO** literally; **DoE weak** — transferring a whole object is a different way/result than transferring an abstracted property. |

**Claim 2 verdict: NO.**

#### CLAIM 3 (Method) — render final preview by **STITCHING** at least one object from first and second camera (panorama-type)
| Limitation | Cutout behavior | Evidence | Determination |
|---|---|---|---|
| "stitching" objects from both cameras' previews | Cutout **overlays/composites** (layers) the silhouette over the rear feed; it does not photometrically **stitch** images into a single seamless panorama | **[3P]** All press describes overlay/green-screen, not stitching; spec's stitching example is a selfie merged into a rear-camera panorama. | **NO** |

**Claim 3 verdict: NO.**

#### CLAIM 4 (Apparatus) — electronic device with units 202/204/206/208/210 performing Claim 1 steps
| Limitation | Accused element | Evidence | Determination |
|---|---|---|---|
| Electronic device comprising the four functional units performing Claim 1 | The iPhone (XS/XR or newer) or supported Android device **running Snapchat** embodies the units in software/hardware | **[Snap admission]** help.snapchat.com/.../8132982011668 ("Dual Camera allows you to capture content using the front and back cameras at the same time"). Mirrors Claim 1 mapping above. | **YES** (co-extensive with Claim 1) |

**Claim 4 verdict: LITERAL INFRINGEMENT — LIKELY YES.** Note: the accused "device" is the user's phone, which Snap neither makes nor sells — central to the divided-infringement analysis (§(d)).

#### CLAIM 5 (Device) — rendering unit overlays a **property** of the object → same as Claim 2 → **NO**.
#### CLAIM 6 (Device) — rendering unit **stitches** objects → same as Claim 3 → **NO**.

#### CLAIM 7 — "A system performing method steps as claimed in claims 1 to 3"
| Limitation | Accused element | Determination |
|---|---|---|
| A "system" performing the steps of Claims 1–3 | To the extent Claim 1 is infringed, the Snapchat-on-device "system" reads on it; but the claim incorporates Claim 3 (stitching), which is not infringed; and the claim is likely **indefinite/invalid** (see §(c)). | **PARTIAL** (infringed only as to the Claim-1 steps; vulnerable to invalidity). |

**Summary infringement verdict:** Strong on Claims 1 and 4; weak/absent on 2, 3, 5, 6; conditional on 7. The case rises and falls on Claim 1 (and its mirror, Claim 4).

---

### DELIVERABLE 3 — PROOF / EVIDENCE INVENTORY (ranked by strength)

**Tier 1 — Snap Inc. party-admissions (strongest):**
- newsroom.snap.com/dual-camera — official launch; four layouts incl. Cutout; iOS Aug 29, 2022. *Supports: existence/launch date, cross-camera capture (all elements).*
- creators.snapchat.com/blog-dual-camera — "Introducing Dual Camera"; global iOS availability. *Supports: product identity, dates.*
- help.snapchat.com/hc/en-us/articles/8132982011668 and /8866040216084 — official how-to and availability. *Supports: dual front+back simultaneous operation (1a, 1d, 4).*
- developers.snap.com/lens-studio/features/camera/dual-camera — `reverseCameraTexture`; "face and body tracking to custom textures"; "render both front and rear cameras at the same time." *Supports: detection (1a), live cross-camera rendering (1c, 1d) — the strongest technical admission.*
- newsroom.snap.com/india-mau-250m — India 250M+ MAU. *Supports: jurisdiction, damages/market.*
- Snap Inc. SEC filings (10-K/10-Q, EDGAR) — to be pulled for India revenue/users. *Supports: damages, jurisdiction.*

**Tier 2 — Independent tech-press descriptions (corroboration):**
- TechCrunch (Apr 28, 2022) — Director Mode/Dual Camera teaser. *Supports: timeline.*
- Tom's Guide — "place the outline of your selfie on what the rear camera is capturing." *Supports: 1c, 1d.*
- Elite Daily (Sep 1, 2022) — "Cutout works by detecting your face and body in the selfie camera and removing your background." *Supports: 1a, 1b.*
- MakeUseOf — "superimposing the image from your selfie camera." *Supports: 1b, 1c.*
- ScreenRant — green-screen effect over rear feed. *Supports: 1c, 1d.*
- Zacks/Yahoo Finance & Nasdaq — "erase the background of the front image and paste it on the rear-view image." *Supports: 1b, 1c.*
- MacRumors (Aug 29, 2022), Android Central, XDA, PhoneArena, Kapwing — launch and layout corroboration.

**Tier 3 — Video evidence (to be preserved with URLs/timestamps):**
- Tom's Guide article links to "Snapchat Dual Camera in action"; Snap's own SPS 2022 demo (newsroom.snap.com/sps2022creators). *Action: download and notarize; capture a Cutout demo specifically showing the body silhouette composited over the rear feed.*

**Tier 4 — Evidence the user must still self-collect (essential for a plaint):**
- **Notarized screen recording** of Cutout used on an **Indian-purchased device** with India App Store/Play Store Snapchat build (establishes use "in India" under Section 48). *Supports: all elements + territoriality.*
- **India App Store / Play Store listings** (screenshots with dates). *Supports: offering/availability in India.*
- **Computer-vision expert affidavit** explaining that Cutout performs segmentation-based foreground detection, extraction, and live compositing onto the second camera feed. *Supports: 1a–1d technical mapping; rebuts "subtraction not detection" defense.*
- **Reverse-engineering / APK analysis report** of the Snapchat Android package. *Supports: internal implementation (currently only inferred from behavior).*
- **Snap Inc. financial filings** (India MAU/revenue). *Supports: damages, balance of convenience.*

---

### DELIVERABLE 4 — PATENT VULNERABILITY / VALIDITY ANALYSIS

#### (a) Prior art (published/filed BEFORE Dec 21, 2016)

| Reference | Date / assignee | What it discloses | Threat level |
|---|---|---|---|
| **US 9,307,153 B2** "Method and apparatus for previewing a dual-shot image" | KR priority **Jul 5, 2013**; **Samsung Electronics Co., Ltd.** (Lee, Son, Noh) | Detects/sets subject part in **front** image, sets area of pixels of interest, outputs **partial** front image, "create … a combined image by **overlaying the partial image on the rear image**," displays it. This is the cross-camera asymmetric live overlay — the patent's core. | **CRITICAL — potentially dispositive on novelty/obviousness.** Patentee's own. If the patent-in-suit is anticipated or rendered obvious by Samsung's earlier filing, the whole case collapses. Strategy implication: Samsung cannot disclaim its own prior art, and a §64 revocation/counterclaim would feature this front-and-center. |
| **Samsung Galaxy S4 "Dual Shot"** | **Announced Mar 14, 2013** (Samsung Unpacked, NYC) | Per allaboutgalaxys4.com: "The photo taken from the front camera (2MP) is overlayed on the photo taken from the rear camera (13MP)" — movable/resizable inset; per Stuff.tv (Mar 2013): "Dual Shot allows you to take photos using the 2MP front and 13MP rear cameras at the same time… the same dual trick with **video**" (i.e., live cross-camera overlay). | **HIGH — Samsung's own public, commercial prior disclosure.** Supports an obviousness attack: the only arguable delta is automated **segmentation/cutout** vs. a rectangular inset — and segmentation was itself well known (see matting literature). Self-collision risk. |
| **US 9,204,026 B2** "Mobile terminal and method of controlling an image photographing therein" | KR priority **Nov 2010**; **LG** | Controller "generat[es] a third image by synthesizing the photographed first and second [camera] images," displayed as the photographed image; preview-image embodiments. | **MEDIUM-HIGH** — third-party prior art for combining first+second camera images into a composite, with preview. |
| **US 10,334,153 B2** "Image preview method, apparatus and terminal" | Issued Jun 25, 2019 (CN priority CN105100615A, 2015) | Dual-camera **real-time preview** with depth-based background segmentation/blur. The **Chinese family CN105100615A pre-dates Dec 2016** and discloses real-time dual-camera preview segmentation. | **MEDIUM** — relevant to "live preview segmentation," though directed to bokeh, not cross-camera overlay. Cite the pre-2016 CN member, not the 2019 US grant. |
| **Frontback (2013), MixCam, "Camera FrontBack," "DuoCam," "2sidez," "Dblcam"** | 2013–2014 apps | Simultaneous/sequential front+back composition; PiP; split-screen. DPReview (2013) notes pre-S4 apps "don't take pictures simultaneously… live preview or picture-in-picture video is not possible." | **LOW-MEDIUM** — establishes the dual-capture concept was commonplace; weak on **live cross-camera overlay** specifically. |
| **BeReal** | Launched 2020 | Simultaneous front+back capture. | **NOT prior art** (post-dates patent). Context only — explains why Snap built Dual Camera. |
| **Nokia "Bothie" / Dual-Sight (Nokia 8)** | 2017 | Live front+back composite. | **NOT prior art** (post-dates priority). Context only. |
| **Academic real-time matting / background segmentation / mobile compositing** (pre-Dec 2016) | 2015–2016 | Real-time video matting and mobile background segmentation were active research areas before the priority date. | **MEDIUM (obviousness building block)** — supplies the "automated segmentation" element to combine with S4 Dual Shot / '153 to render the patent obvious. *Note: specific citations not pulled in this session — to be sourced for a formal invalidity contention.* |
| **Green-screen / chroma-key live compositing** | Long-established | Live keying/compositing of a foreground over a background. | **MEDIUM** — the press itself repeatedly calls Cutout a "green-screen effect," underscoring that live foreground-over-background compositing is old art. |

**Bottom line on prior art:** The patent's distinguishing feature over the broad prior art is the **specific combination** of (i) automated object **segmentation** of a subject in one camera with (ii) **live overlay** onto a **different** camera's preview. US 9,307,153 (Samsung's own) discloses essentially that combination as of 2013. This is the strongest invalidity vector and is **self-inflicted**.

#### (b) Claim-construction weaknesses (and rebuttals)
- **"object."** The specification's examples are small accessory objects (spectacles, lipstick). Snap will argue a **whole person/body** is not the "object" contemplated, narrowing the claim to accessories — which Cutout does not transfer. **Rebuttal:** Claim 1 is unrestricted ("at least one object"); the spec examples are non-limiting; a body is an "object" detected/extracted from a preview. But this is a genuine dispute and the patentee should brief it early.
- **"determining … at least one intended location."** Snap may argue Cutout always **centers/auto-places** the silhouette and never "determines" a location, so element 1c is absent. **Rebuttal:** placement at a default coordinate is still a determination of location; alternatively, DoE (above). Flag: contested.
- **"preview" / "live."** Snap may argue near-real-time buffered rendering is not "preview." **Rebuttal:** the composite is shown in the viewfinder pre-capture — the ordinary meaning of preview. Low risk.
- **"detecting/selecting an object" vs. background subtraction.** Snap may frame Cutout as **removing a background** (subtraction), not "detecting/selecting an object." **Rebuttal:** segmentation necessarily detects the foreground object to remove the background; the expert affidavit should establish that foreground detection is a precondition. This is why the **CV expert affidavit is essential**.

#### (c) Validity / enablement / prosecution-history risks (India-specific)
- **Section 3(k) — computer programme per se (MAJOR).** A pure software image-processing method running on a general-purpose smartphone is squarely within the §3(k) exclusion unless it demonstrates a **"technical effect"/technical contribution** beyond the program itself (per *Ferid Allani v. Union of India*, Delhi HC 2019, and subsequent jurisprudence; Khurana & Khurana; IIPRD; Lexology). The patent claims functional "units" (202/204/206/208) that are software modules on standard hardware — exactly the profile examiners and courts scrutinize. **This is the most likely ground on which Snap defeats the patent in India**, independent of prior art. Mitigation for the patentee: argue an enhanced-functionality technical effect (real-time cross-camera compositing improving the camera system); but the absence of novel hardware is a serious handicap.
- **Claim 7 indefiniteness (Section 10 / Section 59).** "A system performing method steps as claimed in claims 1 to 3" is a vague, omnibus-style claim lacking structural definition — vulnerable as indefinite/insufficiently particular under Section 10(4)/(5), and any attempt to cure it by amendment is constrained by Section 59 (amendments must be by disclaimer/correction/explanation and within the scope of the granted claims).
- **Prosecution-history estoppel from the Aug 4, 2020 amendments.** Adding reference numerals (202/204/206/208) and a new system claim 7 can narrow scope and create estoppel; if limitations were added to overcome prior art or §3(k) objections, Snap will argue the patentee surrendered equivalents — directly weakening the DoE argument for element 1c. Pull the full file wrapper before relying on DoE.
- **No presumption of validity.** Section 13(4), Patents Act 1970 ("shall not be deemed in any way to warrant the validity of any patent") and *Bishwanath Prasad Radhey Shyam v. Hindustan Metal Industries*, (1979) 2 SCC 511 ("the grant and sealing of the patent … does not guarantee the validity") mean the patentee carries the full burden at the interim stage.

#### (d) Enforceability risks
- **Single-jurisdiction exposure.** Family membership could not be confirmed; the number format (201641043709, filed 21 Dec 2016, no "CHENP/DELNP" national-phase suffix) is consistent with an **ordinary Indian filing** rather than a PCT national-phase entry — implying enforcement may be **India-only** unless a US/PCT/EP/KR/CN sibling exists. (Samsung does hold related US assets — e.g., US 10,616,502 "Camera preview" — but these were not confirmed to be family members.) **Verify the INPADOC family before sizing the campaign.**
- **Divided / indirect infringement (CRITICAL practical hurdle).** The method (Claims 1–3) and the apparatus (Claim 4 — the user's phone) are **performed/embodied by the end user**, not by Snap, which supplies only the app. India's Patents Act does not codify contributory/induced infringement; these are argued via **common-law principles** (S.S. Rana; Mondaq; Legal500 India guide). The patentee must therefore: (1) plead **inducement** — Snap actively instructs and encourages users via help.snapchat.com tutorials and in-app UI; and (2) consider whether Claim 4's "electronic device … comprising [the units]" reads on Snap's **own servers/Lens infrastructure** or only on the handset. Knowledge/notice (a cease-and-desist) strengthens an inducement/willfulness theory.
- **Section 3(k) as a live invalidity defense** (above) will be raised as a counterclaim for revocation, which under the proviso to Section 104 **transfers the suit to the High Court**.

---

## Recommendations (staged, with decision thresholds)

**Stage 0 — Verify before doing anything else (days):**
1. **Confirm patent status and claims as-granted** on InPASS (search.ipindia.gov.in → Application Status → 201641043709 + CAPTCHA) and pull the **E-register and full file wrapper**. *Threshold: if the patent is not granted/in force, or if Claim 1 was amended away from cross-camera overlay, stop and reassess.*
2. **Map the INPADOC family** (Espacenet/Google Patents) to learn whether US/PCT/EP/KR/CN siblings exist. *Threshold: a US sibling materially expands leverage; its absence confines the campaign to India.*

**Stage 1 — Build the technical record (weeks):**
3. Commission a **computer-vision expert affidavit** (foreground detection → extraction → live cross-camera compositing) and an **APK/reverse-engineering report**. *This converts inferred behavior into proof and pre-empts the "subtraction not detection" and "no live preview" defenses.*
4. Capture a **notarized screen recording** of Cutout on an India-purchased device with the India store build, plus dated India store-listing screenshots.

**Stage 2 — Clearance and claim-construction positioning (parallel):**
5. Run a **full prior-art clearance** centered on **US 9,307,153 (Samsung's own)** and **Galaxy S4 Dual Shot**, plus CN105100615A and pre-2016 matting literature. *Threshold: if US 9,307,153 anticipates Claim 1, do not litigate — the §64 counterclaim will likely win and Samsung would be invalidating its own asset.*
6. Lock down claim-construction briefs on **"object"** (body = object) and **"intended location"** (default placement = determination, or DoE), checking the file wrapper for **estoppel**.

**Stage 3 — Enforcement (if Stages 0–2 clear):**
7. Serve a **cease-and-desist** on Snap Inc. (establishes knowledge for inducement/willfulness and triggers the limitation clock; Limitation Act 1963 — 3 years from infringement).
8. File suit in the **Delhi High Court Intellectual Property Division** (preferred — most developed IP bench; Madras HC IPD is the alternative), pleading **direct infringement by users + inducement/contributory infringement by Snap**, and seek an **interim injunction**.

**Interim-injunction benchmarks (India three-factor test; American Cyanamid-derived, applied per WIPO Patent Judicial Guide and IAM India guide):**
- **Prima facie case** — hardest factor given **no presumption of validity (s.13(4))**; the §3(k) and US 9,307,153 defenses may defeat it. *If prima facie validity looks weak, pivot from injunction to a damages/account-of-profits strategy at trial.*
- **Balance of convenience** — Snap's 250M Indian users and entrenched market position cut both ways (large infringing footprint vs. disruption to a major platform).
- **Irreparable injury** — quantifiable royalties weigh against irreparability; emphasize market-share/erosion if pursued.

**Decision rule:** Proceed to an injunction motion **only if** (a) the patent is confirmed granted with Claim 1 intact, (b) prior-art clearance shows US 9,307,153 does not anticipate Claim 1, and (c) the §3(k) "technical effect" argument is credible. If any fails, restructure as a licensing demand or a damages-only suit rather than risk an early invalidity ruling.

---

## Caveats
- **Patent status/claims/family unconfirmed.** Grant status, as-granted claim text, legal status, and family membership of IN 201641043709 could not be independently verified (InPASS is CAPTCHA-gated; specific Google Patents/Espacenet records were not retrievable here). All infringement conclusions assume the amended claims quoted in the instructions are the granted claims.
- **Cutout's internal implementation is inferred** from Snap's public developer documentation and third-party descriptions of observed behavior, **not from source code**. The CV expert affidavit and APK analysis are required to convert observation into proof — flagged at each affected element.
- **US 9,307,153 details** (Samsung assignee, July 5, 2013 KR priority, "overlaying the partial image on the rear image" claim language) were taken directly from the USPTO published specification and the Justia/Samsung assignee index retrieved in research; the enrichment pass could not separately re-confirm them, so verify against the official USPTO PDF before citing in a pleading.
- **Section 3(k) eligibility and infringement (incl. indirect/divided liability) are legal determinations** that turn on judicial construction; this analysis identifies the strongest positions and the genuine disputes but does not predict outcomes with certainty.
- Several prior-art "obviousness building blocks" (academic matting literature; specific pre-2016 dates for some app releases) were identified by category but not individually sourced in this session and should be pinned down for a formal invalidity contention.