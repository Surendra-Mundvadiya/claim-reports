# Patent Infringement Claim Chart

## US 9,253,270 B2 — Method and System to Share, Synchronize Contents in Cross Platform Environments

**Assignee:** Samsung Electronics Co., Ltd. (Suwon-si, KR)
**Filed:** Apr. 11, 2013 | **Granted:** Feb. 2, 2016 | **Priority:** Apr. 11, 2012 (IN 1456/CHE/2012)
**Inventors:** Bharshankar, Jain, Nawle, Thattai, Kulkarni, Sathyanarayanan, Saiffuddin (Bangalore, IN)

---

### Purpose & format

This claim chart maps each limitation of US 9,253,270 B2 (all 20 claims) against 14 product families that potentially read on the claims. The deliverable consists of (i) a master matrix giving claim-by-claim, product-by-product hit/partial/miss status, and (ii) detailed per-product Claim 1 charts for the highest-severity targets.

**Legend for the master matrix:**

| Symbol | Meaning |
|---|---|
| ✓ Yes | element literally present in the accused product as documented in public sources |
| ~ Partial | element arguably present but requires a non-literal / doctrine-of-equivalents reading, or evidence is incomplete |
| ✗ No | element absent or contradicted by available evidence |

### Critical caveats up front

1. **Claim 1's literal scope is extraordinarily broad**: display item → user selects → action → upload. Practically every cross-platform "Share to…" workflow shipped since iOS 6 (2012) and Android 1.0 (2008) reads on it. Mapping is mechanical; the harder question is validity, not infringement.
2. **The patent has NEVER been asserted, licensed, or challenged in IPR in ~10 years of life.** Samsung's silence is the strongest market signal of low enforcement value.
3. **Strong invalidity exposure** under §101/Alice (abstract idea) and §102/§103 (Facebook US 2009/0144392 published Jun 4, 2009 anticipates substantial parts of Claims 1, 3, 8; Android ACTION_SEND prior art since 2008). A defendant's correct move is to invalidate, not design around.
4. **This is a technical mapping for diligence/strategy.** It is not a legal infringement opinion and does not constitute legal advice. A qualified patent attorney must review the file wrapper, claim construction, and accused product source code for any litigation purpose.

### Document organization

- **Section 1**: Master matrix — 22 claim limitations × 14 product families
- **Section 2**: Product-family directory — full product names by short code
- **Section 3**: Detailed Claim 1 element-by-element charts for the six highest-severity products: Apple iOS, Google Android, Meta Business Suite, Hootsuite, IFTTT, Pushbullet
- **Section 4**: Severity & confidence summary by product
- **Section 5**: Validity flags affecting the chart's enforceability

---

## 1. Master matrix — claims vs. products

Rows: each limitation of each claim of US 9,253,270 B2 (paraphrased for table fit; refer to the issued patent for verbatim text). Columns: the 14 product families analyzed. Cell values use the legend above.

| Claim | Limitation (paraphrased) | iOS | Android | Meta | MSFT | Samsung | OEMs | Hootsuite | Buffer | IFTTT | Zapier | Pushbullet | AirDroid | Snapdrop | MgmtTools |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| **1[a]** | displaying ≥1 item associated with ≥1 entity of the plurality of entities | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| **1[b]** | receiving a selection of ≥1 item corresponding to a first entity | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| **1[c]** | in response to ≥1 action to share the selected item with a second entity | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| **1[d]** | uploading the selected item to a server corresponding to the second entity | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ~ | ~ | ~ | ✓ |
| **2** | item comprises at least one of content and contacts | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| **3** | entity = SNS, relational view, content hosting server, or device | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| **4** | action = gesture/voice/gaze; gesture includes tap, scroll, drag, drop, pinch, swipe, hover, emotion | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| **5** | sharing ≥1 content with ≥1 contact associated with ≥1 relational view (e.g., contact group) | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ~ | ~ | ~ | ~ | ✓ | ✓ | ✓ | ~ |
| **6** | storing a preference of ≥1 contact to share content + sharing based on the stored preference | ~ | ~ | ~ | ✗ | ~ | ✗ | ✓ | ~ | ✓ | ✓ | ✗ | ✗ | ✗ | ~ |
| **7** | creating ≥1 album using content associated with ≥1 entity + editing (add/remove content) | ✓ | ✓ | ~ | ~ | ✓ | ~ | ~ | ~ | ✗ | ✗ | ✗ | ✗ | ✗ | ~ |
| **8** | reformatting ≥1 shared content based on a format supported by the destination entity | ~ | ~ | ✓ | ~ | ~ | ~ | ✓ | ✓ | ✓ | ✓ | ~ | ~ | ~ | ✓ |
| **9** | acquiring information associated with ≥1 shared content before sharing (path, data, tags) | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| **10** | system comprising a device configured to perform Claim 1 | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| **11** | electronic device with integrated circuit + processor + memory performing Claim 1 | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| **12** | (device) item = content and/or contacts | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| **13** | (device) entity = SNS, relational view, content hosting server, or device | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| **14** | (device) action = gesture/voice/gaze; gesture includes tap, scroll, drag, drop, pinch, swipe, hover, emotion | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| **15** | (device) share content with contact via relational view | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ~ | ~ | ~ | ~ | ✓ | ✓ | ✓ | ~ |
| **16** | (device) store + apply per-contact sharing preference | ~ | ~ | ~ | ✗ | ~ | ✗ | ✓ | ~ | ✓ | ✓ | ✗ | ✗ | ✗ | ~ |
| **17** | (device) create + edit album from multi-entity content | ✓ | ✓ | ~ | ~ | ✓ | ~ | ~ | ~ | ✗ | ✗ | ✗ | ✗ | ✗ | ~ |
| **18** | (device) reformat shared content per destination format | ~ | ~ | ✓ | ~ | ~ | ~ | ✓ | ✓ | ✓ | ✓ | ~ | ~ | ~ | ✓ |
| **19** | (device) acquire content info before sharing | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| **20** | non-transitory computer-readable storage medium storing instructions for Claim 1 | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |

### Reading the matrix

- All 14 products read on **Claim 1** (the only independent method claim) literally or near-literally.
- All 14 products read on **Claims 10, 11, 20** (system, electronic-device, and CRM independent claims) by direct corollary.
- **Claim 6** (per-contact stored sharing preference + routing) is the strongest narrowing claim. Cross-posting tools (Hootsuite, IFTTT, Zapier) read on it literally; consumer OSes only read on it in part.
- **Claim 8** (reformat per destination) is most clearly practiced by social-media management platforms (Hootsuite, Buffer, IFTTT, Zapier) and Meta Business Suite; OSes practice it only via third-party share extensions.
- **Claim 7** (album from multiple entities + edit) is best practiced by consumer photo platforms (Apple Photos, Google Photos, Samsung Gallery); SaaS scheduling tools largely do NOT read on it.

---

## 2. Product-family directory

Short codes used in the master matrix expand to the following product families. Each family aggregates multiple individual products that share the same core cross-platform sharing architecture.

| Code | Full product family |
|---|---|
| **iOS** | Apple iOS Share Sheet / Photos / Continuity |
| **Android** | Google Android Sharesheet / Photos / Quick Share |
| **Meta** | Meta Business Suite (FB / Instagram / Threads cross-post) |
| **MSFT** | Microsoft Windows Share / Phone Link / OneDrive |
| **Samsung** | Samsung One UI / Quick Share / Galaxy Share |
| **OEMs** | Xiaomi / Huawei / Oppo / Vivo / OnePlus (Android OEMs) |
| **Hootsuite** | Hootsuite |
| **Buffer** | Buffer |
| **IFTTT** | IFTTT (Pro+ multi-action / Ultimate Cross-Posting) |
| **Zapier** | Zapier (social-media automation) |
| **Pushbullet** | Pushbullet |
| **AirDroid** | AirDroid |
| **Snapdrop** | Snapdrop / Xender / ShareIt / SHAREit |
| **MgmtTools** | Sprout Social / Later / SocialPilot / Loomly / Sendible / MeetEdgar |

---

## 3. Detailed Claim 1 element-by-element charts

The following charts use the standard three-column patent claim-chart format: **claim element | accused functionality in the product | evidence source**. Six product families are charted at this level of detail because they collectively cover the dominant cross-platform sharing patterns in the market: consumer mobile OSes (iOS, Android), Meta's own cross-posting tooling, two leading SaaS social-management tools (Hootsuite, IFTTT), and a device-to-device cross-platform tool (Pushbullet).

For products not charted at this depth (Buffer, Zapier, AirDroid, Microsoft, Samsung, Snapdrop family, OEM family, MgmtTools cluster), the Claim 1 mapping follows the same logic as the closest analog in the detail set: Buffer ≈ Hootsuite; Zapier ≈ IFTTT; AirDroid ≈ Pushbullet; Samsung/MSFT/OEMs ≈ Android (which their share systems are built on); Snapdrop family ≈ Pushbullet (device-to-device peer transfer); MgmtTools ≈ Hootsuite/Buffer.

---

### 3.1 Apple iOS Share Sheet / Photos / Continuity

> **Severity:** HIGH | **Confidence:** Very High
> Apple's UIActivityViewController and Photos app are the textbook implementation of Claim 1: a grid of items, user selection, share action, upload to destination service. Caveat: Apple does not itself reformat content (Claim 8) — third-party share extensions do.

| Claim Element | Accused Functionality in iOS | Evidence / Source |
|---|---|---|
| **Preamble**: A method for managing ≥1 item associated with a plurality of entities | iOS provides Share Sheet / UIActivityViewController, Photos app, and Continuity to manage photos, files, and contacts across multiple entities (Photos library, iCloud, Messages, Mail, third-party SNS apps like Instagram/Facebook/X). | Apple Support: `support.apple.com/guide/iphone/intro-to-continuity-iphf5fa30b66/ios` |
| **1[a]**: displaying the ≥1 item associated with ≥1 entity | Photos app displays a grid of photos/videos associated with Camera Roll, Albums, Shared Albums, and library sources. Share Sheet displays icons for each registered share-target entity (SNS, AirDrop devices, Messages contacts). | 9to5Mac (2016-06-06): `9to5mac.com/2016/06/06/instagram-share-extension/`; iOS Human Interface Guidelines |
| **1[b]**: receiving a selection of ≥1 item | User taps a photo (or multi-selects) in Photos = selection of item; the photo is associated with Photos/iCloud = first entity. | allthings.how guide on iOS drag-and-drop sharing |
| **1[c]**: in response to ≥1 action to share with a second entity | User taps Share button → taps Instagram/Facebook/Mail/AirDrop icon (tap gesture = action per Claim 4) → invokes share extension for second entity. iOS 15+ also supports literal drag-and-drop of photos between apps. | loopinsight.com (2018-01-02) on drag-and-drop in Share Sheet |
| **1[d]**: uploading to a server corresponding to the second entity | Selected photo is uploaded via the third-party share extension to the respective server (Instagram's CDN, Facebook's Graph API endpoint, iCloud sync, etc.). | Instagram Share Extension docs; 9to5Mac coverage of Instagram share extension launch (2016) |

---

### 3.2 Google Android Sharesheet / Photos / Quick Share

> **Severity:** HIGH | **Confidence:** Very High
> Android's `Intent.ACTION_SEND` has been the platform's universal share mechanism since Android 1.0 (2008) — predating the patent's 2012 priority date by ~4 years and providing a strong anticipation defense in any enforcement action.

| Claim Element | Accused Functionality in Android | Evidence / Source |
|---|---|---|
| **Preamble** | Android provides `Intent.ACTION_SEND` (since Android 1.0, 2008) and Sharesheet for managing items across Photos, Drive, Messages, Gmail, and third-party SNS apps registered as share targets. | `developer.android.com/training/sharing/send` |
| **1[a]**: displaying the item | Google Photos displays a grid of photos by date and source (device, Drive, partner sharing, content from other apps such as Instagram, Slack, Messenger). | 9to5Google (2025-02-04): `9to5google.com/2025/02/04/google-photos-grid-customizations/`; `support.google.com/photos` |
| **1[b]**: receiving selection | Long-press or tap selects a photo in Google Photos. The selected photo is associated with the Photos/Drive entity. | Google Photos Help Center; Android Sharesheet documentation |
| **1[c]**: action to share with second entity | Tap Share → Sharesheet appears with list of target apps → tap Instagram/Twitter/Gmail (tap = gesture per Claim 4) sends `Intent.ACTION_SEND` with `EXTRA_STREAM`. | Android Developers Blog "Share With Intents" (Feb 2012); Sharesheet docs |
| **1[d]**: upload to second-entity server | Selected item is passed to target app, which uploads to its respective server (Instagram CDN, Twitter media endpoint, Gmail SMTP). | `developer.android.com/training/sharing/send` (EXTRA_STREAM section) |

---

### 3.3 Meta Business Suite (Facebook + Instagram + Threads cross-posting)

> **Severity:** HIGH | **Confidence:** Very High
> Cleanest literal read of Claim 8 (reformat per destination): aspect-ratio adjustment from Facebook 16:9 to Instagram 1:1/4:5 is automatic. Notable: Facebook's own US 2009/0144392 (published 2009) discloses cross-platform sharing with formatting parameters — Meta has its own pre-2012 prior-art shield.

| Claim Element | Accused Functionality in Meta Business Suite | Evidence / Source |
|---|---|---|
| **Preamble** | Meta Business Suite is a single composer for managing posts across Facebook Pages, Instagram, and Threads — multiple platform entities owned by Meta. | `graphed.com/blog/how-to-crosspost-on-meta-business-suite` (2024); `business.facebook.com` |
| **1[a]**: displaying the item | User selects media from device, Facebook library, or Instagram library — items associated with a first entity (e.g., user device or Facebook library). | Meta Business Suite product documentation; `metricool.com/meta-business-suite` (2026) |
| **1[b]**: receiving selection | User picks media via Composer's "Add photo" dialog; first entity = source library. | contentstudio.io guide to Meta Business Suite |
| **1[c]**: action to share with second entity | User checks "Also post to Instagram" / "Share to Threads" toggles, or clicks "Crosspost" button — click action = gesture per Claim 4 = action to share to second entity. | `guidingtech.com` on Facebook→Instagram automatic sharing (updated Aug 2024) |
| **1[d]**: upload to second-entity server | Cross-post toggle triggers upload to Instagram's CDN / Facebook Graph API / Threads API servers. Format adjustment for aspect ratios is automatic (Claim 8 literal hit). | `graphed.com` (2024); Meta developer docs (`developers.facebook.com`) |

---

### 3.4 Hootsuite

> **Severity:** HIGH | **Confidence:** Very High
> SaaS social-media management tools are the cleanest fit for Claim 8 (per-platform reformatting) and arguably Claim 6 (per-platform sharing preferences stored in the account). Hootsuite, Buffer, Sprout Social all share this architecture.

| Claim Element | Accused Functionality in Hootsuite | Evidence / Source |
|---|---|---|
| **Preamble** | Hootsuite manages posts across Facebook, Instagram, LinkedIn, X (Twitter), TikTok, YouTube, Pinterest, Threads — each a "plurality of entities". | `hootsuite.com/products/social-media-management`; `buffer.com/resources/buffer-vs-hootsuite` |
| **1[a]**: displaying the item | Composer displays draft post + uploaded media. User selects networks via icon toggles. Bulk-uploaded CSV (up to 350 posts) presented as a grid. | Hootsuite Help Center (`help.hootsuite.com`); `zapier.com/blog/hootsuite-vs-buffer` |
| **1[b]**: receiving selection | User picks media from Hootsuite Content Library or device upload; first entity = Hootsuite media library. | Hootsuite user guide |
| **1[c]**: action to share with second entity | Click "Post Now" or "Schedule" button (tap/click = gesture per Claim 4) — action to share with selected second entities. | hashmeta.com Hootsuite vs Buffer review |
| **1[d]**: upload to second-entity server | Upon scheduled time or click, Hootsuite uploads to each selected SNS server via that SNS's API. Per-platform customization (different caption, hashtag set) applied — Claim 8 literal hit. | Hootsuite OwlyGPT documentation; Hootsuite developer docs (`developer.hootsuite.com`) |

---

### 3.5 IFTTT (Pro+ multi-action applets / Ultimate Cross-Posting)

> **Severity:** HIGH | **Confidence:** Very High
> IFTTT's automated trigger→action model arguably reads on Claim 1 even more cleanly than user-driven sharing: the "action" under Claim 4 includes "gesture, voice, gaze" — automated execution is non-gesture, but Claim 1's bare term "action" is broader than the Claim 4 examples.

| Claim Element | Accused Functionality in IFTTT | Evidence / Source |
|---|---|---|
| **Preamble** | IFTTT manages content across hundreds of services: Instagram, Twitter, Facebook, LinkedIn, Pinterest, YouTube, Google Drive, etc. | `ifttt.com/explore/ultimate-cross-posting-applet`; `ifttt.com/solutions/social-media` |
| **1[a]**: displaying the item | Trigger fires when new item appears in source service (e.g., "New photo in Instagram"). Item = the new photo; first entity = Instagram. | `ifttt.com/explore` (trigger documentation) |
| **1[b]**: receiving selection | Applet selects the triggering item automatically (programmatic selection). | IFTTT applet documentation |
| **1[c]**: action to share with second entity | Applet auto-executes action(s) — multi-action applets (Pro+) can fan out to Twitter, LinkedIn, Pinterest. Action is automated rather than user-gesture, but Claim 1's "action" is broadly worded and reads on programmatic actions. | `ifttt.com/explore/guide-to-social-media-automation`; IFTTT pricing page (Pro+ multi-action) |
| **1[d]**: upload to second-entity server | Action uploads/posts to second SNS server. IFTTT AI rewrites caption per platform — Twitter concise, Instagram engaging, LinkedIn professional (literal Claim 8 hit). | `ifttt.com` AI Pro+ documentation; IFTTT API integration docs (`ifttt.com/developers`) |

---

### 3.6 Pushbullet

> **Severity:** MEDIUM-HIGH | **Confidence:** High
> Device-to-device tools depend on reading "entity" to cover a device (Claim 3 expressly permits this) and "server corresponding to the second entity" to cover the relay infrastructure. The latter is the only soft point in the literal mapping; it would likely succeed under doctrine of equivalents.

| Claim Element | Accused Functionality in Pushbullet | Evidence / Source |
|---|---|---|
| **Preamble** | Pushbullet manages content (photos, files, links, SMS) across multiple devices (Android, iOS, Windows, Mac, Linux, Chrome, Firefox) — devices are valid "entities" per Claim 3. | mundobytes.com Pushbullet guide; `techwiser.com/pushbullet-alternatives` |
| **1[a]**: displaying the item | Pushbullet displays files/notifications/clipboard items associated with each connected device. | Pushbullet user documentation |
| **1[b]**: receiving selection | User selects file/photo on first device (e.g., phone gallery). Item is associated with that device = first entity. | appmus.com Pushbullet vs AirDroid comparison |
| **1[c]**: action to share with second entity | User drags photo onto Pushbullet desktop window OR taps target device in Pushbullet app (drag/drop and tap = gestures per Claim 4). | techwiser.com (2024); mundobytes.com |
| **1[d]**: upload to second-entity server | Pushbullet uploads item to its own backend server, which then pushes to the second device. Whether "server corresponding to the second entity" is met is debatable when both endpoints are user-owned devices and the relay is Pushbullet's intermediate server — reading "server corresponding to the second entity" to cover Pushbullet's relay server requires non-literal interpretation = partial. | Pushbullet architecture docs (`pushbullet.com`) |

---

## 4. Severity & confidence summary

Severity reflects how cleanly the product reads on Claims 1, 10, 11, 20 (the four independent claims) plus the dependent claims that most clearly differentiate the patent (especially Claims 6, 7, 8). Confidence reflects the strength and number of public-source citations underlying the mapping.

| Product family | Severity | Confidence | Claims reading literally / near-literally | Notes |
|---|---|---|---|---|
| Apple iOS Share Sheet / Photos / Continuity | **HIGH** | Very High | 1, 2, 3, 4, 5, 7, 9, 10, 11, 12, 13, 14, 15, 17, 19, 20 | Textbook fit for Claim 1; Claim 6 only partial; Claim 8 via third-party extensions. |
| Google Android Sharesheet / Photos / Quick Share | **HIGH** | Very High | 1, 2, 3, 4, 5, 7, 9, 10, 11, 12, 13, 14, 15, 17, 19, 20 | ACTION_SEND prior art (2008) damages Samsung's own validity case against Google. |
| Meta Business Suite | **HIGH** | Very High | 1, 2, 3, 4, 8, 9, 10, 11, 12, 13, 14, 18, 19, 20 | Cleanest Claim 8 hit; Meta has its own pre-2012 prior art (US 2009/0144392). |
| Microsoft Windows Share / Phone Link | **HIGH** | High | 1, 2, 3, 4, 9, 10, 11, 12, 13, 14, 19, 20 | Standard share dialog + Phone Link cross-device flow. |
| Samsung One UI / Quick Share / Galaxy Share | **HIGH** | Very High | 1, 2, 3, 4, 5, 7, 9, 10, 11, 12, 13, 14, 15, 17, 19, 20 | Samsung itself practices the patent. Not a viable internal target. |
| Xiaomi / Huawei / Oppo / Vivo / OnePlus | **HIGH** | High | 1, 2, 3, 4, 9, 10, 11, 12, 13, 14, 19, 20 | Inherit Android share architecture; Peer-to-Peer Transmission Alliance Quick Share. |
| Hootsuite | **HIGH** | Very High | 1, 2, 3, 4, 6, 8, 9, 10, 11, 12, 13, 14, 16, 18, 19, 20 | Strongest Claim 6 + Claim 8 reads of any analyzed product. |
| Buffer | **HIGH** | Very High | 1, 2, 3, 4, 8, 9, 10, 11, 12, 13, 14, 18, 19, 20 | Mirror of Hootsuite functionality; Claim 6 only partial. |
| IFTTT (Pro+ multi-action) | **HIGH** | Very High | 1, 2, 3, 4, 6, 8, 9, 10, 11, 12, 13, 14, 16, 18, 19, 20 | Automated cross-platform routing reads heavily on Claims 1, 6, 8. |
| Zapier | **HIGH** | Very High | 1, 2, 3, 4, 6, 8, 9, 10, 11, 12, 13, 14, 16, 18, 19, 20 | Same architecture as IFTTT; broader connector library. |
| Pushbullet | **MED-HIGH** | High | 1, 2, 3, 4, 5, 9, 10, 11, 12, 13, 14, 15, 19, 20 | Relies on device-as-entity reading; Claim 1[d] requires non-literal reading. |
| AirDroid | **MED-HIGH** | High | 1, 2, 3, 4, 5, 9, 10, 11, 12, 13, 14, 15, 19, 20 | Mirror of Pushbullet analysis. |
| Snapdrop / Xender / ShareIt | **MEDIUM** | High | 1, 2, 3, 4, 5, 9, 10, 11, 12, 13, 14, 15, 19, 20 | P2P peer-transfer tools; same device-as-entity argument. |
| Sprout / Later / SocialPilot / Loomly / Sendible / MeetEdgar | **HIGH** | Med-High | 1, 2, 3, 4, 8, 9, 10, 11, 12, 13, 14, 18, 19, 20 | Mirror of Hootsuite/Buffer; per-product evidence not gathered individually. |

---

## 5. Validity flags affecting enforceability of this chart

Every infringement reading in this chart must be discounted by the substantial probability that the underlying claim is invalid. The validity issues below are not part of the infringement chart per se, but no diligence consumer of this chart should rely on the infringement findings without simultaneous awareness of the invalidity exposure.

### §101 / Alice (abstract idea)

Claim 1 recites only generic functional steps (display → select → action → upload) with conventional "server," "first entity," "second entity" machinery. Under *Alice Corp. v. CLS Bank* (Sup. Ct. 2014) and its Federal Circuit progeny (e.g., *Electric Power Group v. Alstom*; *Intellectual Ventures v. Capital One*), claims of this generality are routinely held abstract at motion to dismiss. The patent issued Feb 2016, ~20 months post-*Alice* — the prosecution history should be examined to confirm what §101 analysis the examiner performed.

### §102 / §103 (prior art)

Three references were cited by the examiner: **US 8,832,190** (Leske et al.); **US 2011/0252320** (Arrasvuori et al., Nokia); **US 2011/0282942** (Berger et al.). Additional uncited prior art that threatens the claims:

- **Facebook US 2009/0144392** (provisional 61/000,682 filed Oct 26, 2007; non-provisional 12/259,254 filed Oct 27, 2008; published Jun 4, 2009): teaches cross-platform content sharing with formatting parameters and destination parameters. Anticipates Claims 1, 3, 8.
- **Google Android `Intent.ACTION_SEND`** (publicly documented since Android 1.0, 2008): teaches user-action-driven cross-platform upload via share intent.
- **Apple `UIActivityViewController` predecessors** (2010–2011): teach system-provided share menu.
- **US 7,730,216** (Issa, 2010, Facebook predecessor): teaches sharing content across multiple SNS via aggregation node — relevant to Claims 1, 3, 5.

### Litigation history (or lack thereof)

No public record of US 9,253,270 being asserted, licensed, or challenged in IPR/PGR was located. The patent has been alive for ~10 years with zero footprint as a litigation asset. Samsung itself is overwhelmingly a defendant in US patent litigation (404 suits 2019–2023, 208 from NPEs, per KED Global / IFI Claims). Recent adverse verdicts include $279M to Headwater, $192M to Mojo Mobility, $142M to G+ Communications, $112M to Maxell, $78.5M to Anonymous Media Research Holdings. The '270 patent has not appeared as a counter-assertion in any of these.

### Bottom line

This chart establishes that 14 product families practice the literal language of Claim 1. It does **not** establish that any of them face a real enforcement risk. The patent has substantial invalidity exposure and zero assertion history. A defendant receiving an enforcement letter on US 9,253,270 B2 should pursue invalidity, not licensing or design-around. A potential licensor (Samsung) should treat the patent as a portfolio chip rather than a primary monetization asset.

---

*Generated: 2026-06-01 — Technical analysis only — not legal advice.*
