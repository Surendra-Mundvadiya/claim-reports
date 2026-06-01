# Claim-by-Claim Infringement Mapping Chart — US 10,484,528 B2

## 1. Introduction & Methodology

This chart maps the asserted claims of U.S. Patent No. **10,484,528 B2** ("Apparatus and Method for Managing Operations for Providing Services Automatically," Samsung Electronics, filed Jan. 30, 2018, issued Nov. 19, 2019, priority Jan. 30, 2017) onto ten accused product features. Methodology: (i) parse each independent claim into limitations as supplied in the task brief; (ii) characterize each accused product based on first-party documentation (Apple Support, Huawei Consumer, Xiaomi HyperOS, OPPO, Microsoft Learn) and corroborating tech-press (MacRumors, 9to5Mac, AppleInsider, Android Authority, 9to5Google, TechCrunch, Windows Latest); (iii) score each element **YES / PARTIAL / NO** against the claim language; (iv) where a literal element fails, structure a Function–Way–Result doctrine-of-equivalents (DoE) analysis.

The single most decisive limitation across all ten products is **[1d]** — the function on the first device must be tied to an activity executing on the second device **while the gesture is performed**. This ties infringement to *gesture-triggered* (not merely *proximity-triggered* or *cloud-pushed*) handoffs. This is a technical mapping, **not a legal opinion**.

**Caveat on patent text**: A subagent was unable to retrieve the verbatim claim text of US 10,484,528 B2 from patents.google.com, USPTO PatFT, or Espacenet within this session (the fetch layer blocked external patent URLs that did not surface through web_search results). All claim language used below is paraphrased from the structured claim summary supplied in the task brief. Before any pre-suit demand letter or contention chart is finalized, the verbatim text from the issued grant must be re-pulled from USPTO Patent Center and the mapping re-validated against the actual words. The precise meaning of "gesture performed with a second electronic device" and the phrase "while the gesture is performed" will drive every borderline call.

## 2. Patent Claim Summary

- **Claim 1 (method)** — (1a) detect a gesture performed with a second device and receive content-related information from it; (1b) execute an application based on that information; (1c) perform a function associated with the content in that application; (1d) the function is tied to the activity executing on the second device **while the gesture is performed**.
- **Claim 6 (apparatus)** — Parallel to Claim 1 as a first electronic device with a communication circuit and processor.
- **Claim 11 (CRM)** — Non-transitory computer-readable medium storing the Claim 1 instructions.
- **Claim 2** — Establish a communication link with the second device in response to detecting the gesture, then receive information via that link.
- **Claim 3** — Content = notification of message arrival; application = messaging app; function = displaying a software keyboard; activity = inputting a response on the second device.
- **Claim 4** — Information includes (i) identifier of a "related application" on the second device and (ii) identifier of the activity in that related application; first-device application corresponds to the second-device related application.
- **Claim 5** — Transmit control information to a third electronic device connected with the first device.
- **Claim 13** — Identify the function corresponding to the activity, where the function is also capable of being performed by the second device.
- **Claim 14** — First gesture triggers first function; second (different) gesture triggers second (different) function.
- **Claim 15** — Function performed automatically in response to detecting the gesture.

---

## 3. Product-by-Product Mapping

### Product 1 — Apple HomePod / HomePod mini Handoff (U1)

- **Company**: Apple Inc.
- **Version/Release**: HomePod Software 14.4 / iOS 14.4, released **January 26, 2021** (U1-enhanced UWB Handoff); shipping through HomePod 17.x / iOS 18.x and HomePod mini (2nd-gen, midnight) as of 2026.
- **Technology overview**: While media plays on iPhone (or HomePod mini), the user moves the iPhone toward the top of the HomePod mini; the U1 ultra-wideband chip ranges the two devices, escalating haptic feedback as proximity decreases until a Handoff card appears and audio transfers. Apple Support: "hold your iPhone near the top of HomePod until the transfer is complete."

**Claim 1 mapping**

- **[1a]**: HomePod mini detects the iPhone via U1 ranging; the iPhone is the "first device" receiving information about audio playing on the HomePod ("second device"). 9to5Mac describes the increasing haptic rhythm and Handoff card as the iPhone approaches the speaker. **Match: YES** — the deliberate movement toward the speaker is an affirmative gesture, not ambient proximity.
- **[1b]**: Receipt of info launches the source app (Music, Podcasts, third-party Lock-screen-media app such as YouTube). 9to5Mac (Dec. 16, 2020): "tapping the album artwork opens the source audio application on your iPhone." **Match: YES**.
- **[1c]**: Function = audio playback control / continuation (Now Playing, transport, AirPlay re-route) within Music/Podcasts. **Match: YES**.
- **[1d]**: Audio currently playing on HomePod (activity) is the same audio whose playback continues on iPhone (function); true at the moment of the gesture. **Match: YES**.

**Overall Claim 1 literal: YES (HIGH CONFIDENCE)**

**Dependent claims**

- **Claim 2**: BLE pairing pre-exists between iCloud-paired devices, but the AirPlay session is *actively* brought up in response to the gesture. **YES/PARTIAL**.
- **Claim 3**: Handoff extends to phone calls but not to a messaging-keyboard reply. **NO**.
- **Claim 4**: The audio app on HomePod (Music) corresponds to the same app on iPhone (Music). **YES**.
- **Claim 5**: The AirPlay button in the Handoff card lets the user reroute to another speaker — control to a third device. **YES**.
- **Claim 13**: Audio playback is performable on both. **YES**.
- **Claim 14**: Transfer-to vs. transfer-from HomePod uses the same physical proximity gesture; differentiation is by source-of-playback. **PARTIAL**.
- **Claim 15**: Transfer-to is automatic on proximity; transfer-from requires confirmation. **PARTIAL/YES**.

**Claims 6 / 11**: Same mapping. iPhone (U1 + BLE + Wi-Fi + processor) satisfies the apparatus structure; iOS contains the CRM. **YES**.

**DoE**: Not required (literal). For Claim 14 PARTIAL, same function/way/result favors equivalence.

**Overall assessment**: Literal **YES**; **Severity: HIGH**; **Confidence: Very High**.

**Design-arounds for Apple**: (1) Require explicit confirmation tap on both sides (kills Claim 15 auto-execution); (2) replace U1 gesture with passive BLE detection (breaks gesture element); (3) refactor receiving iPhone to display only static controls without launching the music app (avoids [1b]).

**Sources**:
1. MacRumors, "Testing the HomePod Mini's New U1 Handoff Functionality" (Jan. 26, 2021): "As the iPhone gets closer to the HomePod mini's location, it begins a soft haptic touch rhythm that gets faster and faster… Eventually, the song transfer interface opens up." — https://www.macrumors.com/2021/01/26/homepod-mini-14-4-u1-handoff/
2. 9to5Mac, "Hands-on with new iOS 14.4 beta changes and features" (Dec. 16, 2020): "Tapping the album artwork opens the source audio application on your iPhone." — https://9to5mac.com/2020/12/16/ios-14-4-beta-changes-features-homepod-mini-u1-handoff-video/
3. Apple Support, "Play audio on HomePod using iPhone or iPad": "To transfer audio, hold your iPhone near the top of HomePod until the transfer is complete." — https://support.apple.com/guide/homepod/play-audio-using-your-iphone-or-ipad-apdfb81a72e4/homepod

---

### Product 2 — Apple iOS 17+ AirDrop "Bringing Devices Together" / NameDrop / Proximity SharePlay

- **Company**: Apple Inc.
- **Version/Release**: iOS 17.1 (Oct. 25, 2023) and later; through iOS 26 (2025) and iOS 27 betas (2026).
- **Technology overview**: With two unlocked iPhones, the user brings the top edges into near-contact. A NameDrop / Proximity Sharing / SharePlay-by-proximity sheet automatically appears on both screens. The setting is **Settings → General → AirDrop → "Bringing Devices Together."**

**Claim 1 mapping**

- **[1a]**: Per TechCrunch (June 5, 2023) WWDC keynote coverage, Craig Federighi, Apple's senior vice president of Software Engineering, said during the event: "We're also using this same gesture to make it easier than ever to AirDrop content and even kick off shared experiences." Apple itself calls the bring-together motion a "gesture." **Match: YES**.
- **[1b]**: Contacts surfaces NameDrop UI; Photos/Files surfaces Proximity Sharing; Messages/Music/TV surface SharePlay. **YES**.
- **[1c]**: Function (display contact, send file, join SharePlay) operates on the content. **YES**.
- **[1d]**: Function on the receiving iPhone (e.g., joining a SharePlay session) is tied to the activity on the sending iPhone (playing that content) at the moment of the gesture. **YES**.

**Overall Claim 1 literal: YES (HIGH CONFIDENCE)**

**Dependent claims**

- **Claim 2**: Peer-to-peer Wi-Fi/Bluetooth link is brought up in response to the proximity gesture. **YES**.
- **Claim 3**: SharePlay-by-proximity routes through the Messages app but does not show a software keyboard to reply to a notification. **NO/PARTIAL**.
- **Claim 4**: The receiving iPhone opens Contacts (or Music for SharePlay) — corresponding to the sender's app. **YES**.
- **Claim 5**: SharePlay can extend to AirPods, Apple TV, or HomePod via AirPlay. **PARTIAL/YES**.
- **Claim 13**: Performable on both devices. **YES**.
- **Claim 14**: Same physical bring-together gesture triggers different functions depending on foreground app context (NameDrop, AirDrop, SharePlay). **PARTIAL** — same gesture, different functions; the claim language likely contemplates physically distinct gestures.
- **Claim 15**: Share sheet appears automatically; final transfer requires user tap. **PARTIAL/YES** — the *function of displaying the share UI* is automatic.

**Claims 6 / 11**: Same mapping. iPhone hardware + iOS firmware. **YES**.

**DoE**: For Claim 14 PARTIAL, the different foreground contexts plus the slightly varying top-edge/side-edge trajectories documented in Apple's NameDrop guidance achieve substantially the same function-way-result as the "different gestures" embodiment.

**Overall assessment**: Literal **YES**; DoE **YES** (reinforcing); **Severity: HIGH**; **Confidence: Very High**.

**Design-arounds**: Require explicit share-sheet selection before the bring-together gesture is honored (kills [1a]); restrict feature to FaceTime-initiated SharePlay only (kills proximity element).

**Sources**:
1. MacRumors, "iOS 17 AirDrop Features: NameDrop, SharePlay, and Proximity Sharing": "Bringing two devices together will automatically pop up a contact sharing interface… Starting SharePlay content and then bringing your iPhone next to another iPhone will initiate a SharePlay session through the Messages app." — https://www.macrumors.com/guide/ios-17-airdrop/
2. TechCrunch, "AirDrop in iOS 17 will let you share contact info by bringing two iPhones close together" (June 5, 2023), quoting Apple SVP Craig Federighi — https://techcrunch.com/2023/06/05/airdrop-in-ios-17-will-let-you-share-contact-info-by-bringing-two-iphones-close-together/
3. AppleInsider, "How to use NameDrop to exchange iPhone contacts in seconds" (May 22, 2026): "Hold the top edges of both iPhones close together for a second or two." — https://appleinsider.com/articles/26/05/22/how-to-use-namedrop-to-exchange-iphone-contacts-in-seconds

---

### Product 3 — Huawei Share OneHop / Multi-Screen Collaboration

- **Company**: Huawei Technologies Co., Ltd.
- **Version/Release**: Huawei Share OneHop since EMUI 9.1 (2019); continuing through **HarmonyOS 6.1 (stable launch April 20, 2026)**; PC Manager 9.0+; OneHop Kit SDK published on Huawei Developer.
- **Technology overview**: Per Huawei's official support page, the user opens a file (photo, video, document, or recording target) on the phone, then **taps the phone's NFC area against the Huawei Share sensor** on a Huawei laptop, tablet, Vision TV, Sound X speaker, or AX3 router. NFC handshakes; phone and PC bring up a Wi-Fi P2P connection; the file (or screen mirror / call relay / clipboard) is transferred and opened in the corresponding app on the PC (Image Viewer for photos, WPS for documents, etc.).

**Claim 1 mapping**

- **[1a]**: NFC tap is the canonical affirmative gesture; the phone (first device) receives information from the laptop/tablet (second device) via NFC tag exchange. **YES** — Huawei's OneHop Engine developer page explicitly states: "Triggers features with NFC while using Bluetooth and Wi-Fi to connect device, transfer data and launch features."
- **[1b]**: PC Manager / Image Viewer / WPS Office is automatically executed based on the file-type/activity info conveyed via the NFC payload. **YES**.
- **[1c]**: The opened app displays/operates on the content. **YES**.
- **[1d]**: For OneHop screen recording, the phone records the activity visible on the laptop at the moment of the tap; for OneHop file transfer, the function (open in Image Viewer / WPS) is tied to the file selected in the source app at the moment of the tap. **YES**.

**Overall Claim 1 literal: YES (HIGHEST CONFIDENCE — most textbook reading across the entire chart)**

**Dependent claims**

- **Claim 2**: NFC tap triggers Wi-Fi P2P link establishment. Huawei Support: "You will hear your phone vibrate or play a notification sound to indicate a successful connection." **YES**.
- **Claim 3**: Multi-Screen Collaboration projects the phone screen to the laptop and lets the user reply to SMS via the computer keyboard. Huawei Support: "Open Messaging to view and reply to SMS messages." **YES** — the most exact Claim 3 hit across the entire chart.
- **Claim 4**: The "related application" identifier (Gallery → Image Viewer; WPS-phone → WPS-PC) is conveyed via NFC payload through the OneHop Kit. **YES**.
- **Claim 5**: Multi-Screen Collaboration can route phone calls through laptop mic/speaker. **YES**.
- **Claim 13**: Function (open file / record / make call) is performable on both devices. **YES**.
- **Claim 14**: Huawei distinguishes two distinct gestures with two distinct functions: NFC tap = file transfer / screen project; **shake-then-tap within 5 sec** = screen recording. Huawei Support: "Shake your phone (when the screen is unlocked), and then within five seconds, tap the NFC area." **YES** — textbook two-gesture / two-function mapping.
- **Claim 15**: Automatic after the NFC tap (with one consent on first pairing only). **YES**.

**Claims 6 / 11**: Same mapping. Huawei phone hardware (NFC, BT, Wi-Fi, processor) + EMUI/HarmonyOS firmware. **YES**.

**DoE**: Not needed.

**Overall assessment**: Literal **YES**; **Severity: HIGH** (most textbook reading); **Confidence: Very High**.

**Design-arounds**: Move NFC tag to a stationary base and require in-app initiation tap before NFC handshake is honored (preserves utility but weakens gesture-trigger); abandon shake-and-tap (kills Claim 14 only); none eliminate Claim 1.

**Sources**:
1. Huawei Support Global, "Huawei Share" — https://consumer.huawei.com/en/support/huaweishare/
2. Huawei Developer, "OneHop Engine" — https://developer.huawei.com/consumer/en/onehop-kit/
3. Huawei Support, "Multi-screen Collaboration Between Your Phone and Tablet" — https://consumer.huawei.com/en/support/content/en-us15957398/

---

### Product 4 — Xiaomi HyperConnect Touch-to-Share (贴贴分享) + App Relay

- **Company**: Xiaomi Corporation
- **Version/Release**: **Xiaomi HyperOS 3, global launch September 24, 2025**, alongside the Xiaomi 15T series launch event, per Gizmochina (Sept. 25, 2025); rollout completing by **March 2026** for all eligible Xiaomi, Redmi, and Poco devices.
- **Technology overview**: Xiaomi's official HyperConnect page (hyperos.mi.com) describes "贴贴分享" literally as: "与另一个小米手机或 iPhone 的 NFC 区域靠近，即可快速分享" ("bring NFC area close to another Xiaomi or iPhone NFC area to quickly share"). Implementation: NFC tap establishes a handshake; Wi-Fi Direct moves data; supports photos, videos, files, vCard contacts, Wi-Fi credentials, and Mi-Browser/Safari URLs.

**Claim 1 mapping**

- **[1a]**: NFC tap between two phones is a deliberate gesture; first phone receives info about the content (file metadata, vCard pointer). **YES**.
- **[1b]**: Receiving phone executes Photos/Files/Contacts/Browser context based on payload. **YES**.
- **[1c]**: Function (open photo / save file / save contact / connect Wi-Fi) operates on received content. **YES**.
- **[1d]**: Activity on sender at gesture time (Gallery photo selected, Wi-Fi connected, contact card open) maps to function on receiver. **YES**.

**Overall Claim 1 literal: YES (HIGH CONFIDENCE)**

**Dependent claims**

- **Claim 2**: NFC tap → Wi-Fi Direct link. **YES**.
- **Claim 3**: HyperConnect's 应用接力 (App Relay): "iPhone 与小米手机间可双向同步通知提醒…iPhone 点击通知，打开小米手机的应用回复消息" — user can tap synced notification on the iPhone and open the Xiaomi-phone messaging app to reply with a software keyboard. **YES** for App Relay path; **PARTIAL** for pure NFC tap variant.
- **Claim 4**: Source app identifier conveyed via Touch-to-Share payload. **YES**.
- **Claim 5**: HyperConnect supports routing to a third HyperOS device (tablet, laptop, TV, Mac/iPad via Mi Interconnectivity). **YES**.
- **Claim 13**: Performable on both. **YES**.
- **Claim 14**: Same NFC tap, different functions by open-app state (photo / Wi-Fi password / URL). **PARTIAL**.
- **Claim 15**: Automatic upon tap with one consent. **YES**.

**Claims 6 / 11**: Same mapping. **YES**.

**DoE**: For Claim 14 PARTIAL, function/way/result analysis favors equivalence.

**Overall assessment**: Literal **YES**; **Severity: HIGH**; **Confidence: High**.

**Design-arounds**: Remove cross-app context awareness so Touch-to-Share only sends the foreground item explicitly selected via long-press (preserves utility, weakens [1d]).

**Sources**:
1. Xiaomi HyperConnect official, "贴贴分享" page — https://hyperos.mi.com/continuity/abilities
2. Xiaomi HyperConnect official, Xiaomi-Apple interop detail page — https://os1.hyperos.mi.com/continuity/abilities/ab0016
3. Apple App Store, "Xiaomi Interconnectivity" (developer Xiaomi, HyperOS 2 requirement) — https://apps.apple.com/us/app/xiaomi-interconnectivity/id6673908449

---

### Product 5 — Google / Samsung Android 17 / One UI 9 "Tap to Share" (Quick Share NFC)

- **Company**: Samsung Electronics; Google LLC
- **Version/Release**: Surfaced in leaked One UI 9 builds (Android Authority, **March 30, 2026**; SammyGuru, April 2026; 9to5Google, April 17, 2026). Galaxy S26 firmware contains production-ready feature. Stable launch **expected July 2026 alongside Galaxy Z Fold 8 and Galaxy Z Flip 8**, per SammyFans (April 17, 2026). Google I/O 2026 (May 19–20) is the expected announcement window per 9to5Google.
- **Technology overview**: Tap two unlocked Android phones top-edge-to-top-edge; NFC executes the handshake (Galaxy S26 series has NFC antennas on both back and top); Quick Share over Wi-Fi Direct moves files. From Home Screen the gesture exchanges contact business cards; from Gallery / Quick Share / share sheet it transfers selected files. Samsung's One UI 9 settings string reads: "Just hold the top of your phone close to the device, and the files will be sent." Android 17 beta and Canary builds reference a system-level service called "TapToShare" — operating at the OS level, likely powered by Google Play Services, suggesting cross-OEM support beyond Galaxy.

**Claim 1 mapping**

- **[1a]**: NFC tap gesture; first phone receives metadata payload from second phone. **YES** — Android Authority (March 30, 2026) confirms: "NFC may simply act as the trigger, while Quick Share handles the actual transfer."
- **[1b]**: Quick Share / Contacts / Gallery executes based on payload. **YES**.
- **[1c]**: Function (display contact card, receive file) on content. **YES**.
- **[1d]**: Tied to what user has open on source phone. **YES**.

**Overall Claim 1 literal: YES (when stable-released)**

**Caution**: As of May 27, 2026, the feature is in late-stage beta and pre-stable. Damages would not accrue until release. Android Authority and 9to5Google flag the standard "predicted features that may not make it to public release" — though Galaxy S26 firmware containing the feature suggests imminent launch.

**Dependent claims**

- **Claim 2**: NFC tap → Wi-Fi P2P link. **YES**.
- **Claim 3**: No native messaging-keyboard flow in current Tap to Share leaks. **NO**.
- **Claim 4**: Source app identifier conveyed via NFC tag / Play Services. **YES**.
- **Claim 5**: Quick Share supports multi-recipient broadcast but not specifically "control to third device" in the Claim 5 sense. **PARTIAL**.
- **Claim 13**: Performable on both. **YES**.
- **Claim 14**: Per 9to5Google (April 17, 2026): "Tapping your device to another supported phone while Gallery, Quick Share, or the share panel are open on your phone allows you to send selected images, videos, and other files. Tapping from the home screen, however, just shares your contact profile." Same NFC tap, different functions per context. **PARTIAL**.
- **Claim 15**: Automatic upon tap. **YES**.

**Claims 6 / 11**: Same mapping. Samsung phone hardware + Android 17 / One UI 9 firmware. **YES**.

**Critical caveat — Samsung self-licensing**: Samsung is the assignee of US 10,484,528 B2 — Samsung's own Galaxy Tap to Share is self-licensed by definition and cannot infringe its own patent. The real target is **Google's** platform-level "TapToShare" service in Play Services and Android 17, insofar as Pixel and other non-Samsung OEMs adopt the Google implementation.

**Overall assessment**: Literal **YES against non-Samsung licensees** (notably Google's Pixel implementation if/when adopted); **Severity: HIGH** for Google's platform-level service; **Confidence: High (pending stable release)**.

**Design-arounds**: Limit Tap to Share to Galaxy-only (Samsung self-licensed); refactor Google's Play Services "TapToShare" to require explicit share-sheet selection before tap is honored (kills [1a]).

**Sources**:
1. Android Authority, "Exclusive: Android could soon get its own AirDrop-style 'tap to share' feature" (March 30, 2026) — https://www.androidauthority.com/android-tap-to-share-quick-share-3652981/
2. 9to5Google, "Latest One UI 9 leak shows off 'Tap to Share,' adds Bixby widgets to home screen" (April 17, 2026) — https://9to5google.com/2026/04/17/samsung-one-ui-9-leak-tap-to-share-bixby-widgets/

---

### Product 6 — OPPO / OnePlus / realme O+ Connect / ColorOS Touch-to-Share

- **Company**: OPPO (Guangdong OPPO Mobile Telecommunications Corp.); OnePlus (subsidiary); realme
- **Version/Release**: ColorOS 15 (Touch-to-share between OPPO and iPhone/iPad via O+ Connect, requiring ColorOS 15.0+ and iOS/iPadOS 15.0+); ColorOS 16 (extends to Mac).
- **Technology overview**: OPPO's official ColorOS 15 page is explicit: "Touch. Share. Celebrate. Seamlessly connect Android and iOS, exchanging photos and videos with friends." Footnote 7 ties to the O+ Connect app and ColorOS 15.0+ / iOS 15.0+. NFC is the trigger; the O+ Connect app handles the cross-platform handshake.

**Claim 1 mapping**

- **[1a]**: NFC-tap gesture. **YES**.
- **[1b]**: O+ Connect / Photos / Files launches on receiving device. **YES**.
- **[1c]**: Function (receive photo/video/file) on content. **YES**.
- **[1d]**: Tied to what the sender has open in the foreground. **YES**.

**Overall Claim 1 literal: YES**

**Dependent claims**

- **Claim 2**: NFC → P2P link. **YES**.
- **Claim 3**: ColorOS 16 supports answering iPhone calls and receiving its messages on an OPPO via pre-installed Odialer (OPPO ColorOS 16 page, footnote 6). Closer to call-forwarding than software-keyboard reply, but iPhone-message reply on OPPO arguably reads. **PARTIAL/YES**.
- **Claim 4**: Source-app identifier conveyed. **YES**.
- **Claim 5**: O+ Connect bridges to a Windows PC as a third device. **YES**.
- **Claim 13**: Performable on both. **YES**.
- **Claim 14**: Same NFC tap, different functions by context. **PARTIAL**.
- **Claim 15**: Automatic upon tap. **YES**.

**Claims 6 / 11**: **YES**.

**DoE**: For Claim 14 PARTIAL, equivalence holds.

**Overall assessment**: Literal **YES**; **Severity: MEDIUM** (narrower U.S. footprint than Apple/Huawei/Xiaomi); **Confidence: Medium-High** (deep technical confirmation of gesture-as-trigger versus app-button-as-trigger requires teardown testing).

**Design-arounds**: Replace NFC-tap trigger with QR code scan or in-app picker (kills [1a]).

**Sources**:
1. OPPO Global, "ColorOS 15" — https://www.oppo.com/en/coloros15/
2. OPPO Global, "ColorOS 16" — https://www.oppo.com/en/coloros16/

---

### Product 7 — Apple "Classic" Handoff (iPhone ↔ Mac ↔ iPad, non-HomePod)

- **Company**: Apple Inc.
- **Version/Release**: First introduced with iOS 8 / OS X Yosemite (2014); current through iOS 26 / macOS Sequoia (2025).
- **Technology overview**: Per Apple Platform Security ("Handoff security"), classic Handoff broadcasts the current activity via BLE; other iCloud-paired devices in range surface a Handoff icon on the Dock / Lock screen / app switcher. The user **taps the icon** on the receiving device to continue the activity. There is no proximity gesture beyond ambient BLE detection.

**Claim 1 mapping**

- **[1a]**: The user does not perform an affirmative proximity gesture — BLE detection is passive and ambient. The user's tap on the Handoff icon is *on the first device itself*, not a gesture *with* the second device. **NO** — this is the patentee's likely litmus test for non-infringement, as flagged in the task brief.
- **[1b]**: After the user taps the Handoff icon, the corresponding app launches. Satisfied as code but not in the gesture-conditioned claim combination.
- **[1c]**: App opens to the same content. YES in isolation.
- **[1d]**: Activity association exists continuously, not "while the gesture is performed" (no gesture). **NO**.

**Overall Claim 1 literal: NO** — fails on **[1a]** and **[1d]**.

**DoE analysis**:
- **Function**: Same — continue an activity across devices.
- **Way**: Different — passive BLE advertising + UI tap on receiving device, vs. active proximity gesture between devices.
- **Result**: Same — receiver runs the same app with the same activity context.

The **way** is meaningfully different. The patent was filed Jan. 2018, when Apple's 2014 Handoff was clear prior art; the patentee very likely narrowed the claims to gesture-triggered operations during prosecution specifically to avoid reading on classic Handoff. **DoE is likely barred** by prosecution-history estoppel or simply fails because gesture-vs.-ambient is a meaningful technological distinction.

**Overall assessment**: Literal **NO**; DoE **NO** (likely barred); **Severity: LOW/NONE**; **Confidence: High**.

**Design-arounds**: N/A — already does not infringe.

**Sources**:
1. Apple Support, "Handoff security": "the two devices establish a Bluetooth Low Energy (BLE) 4.2 pairing out-of-band using APNs… This key can encrypt and authenticate the BLE advertisements that communicate the device's current activity to other iCloud paired devices using AES-256 in GCM mode." — https://support.apple.com/guide/security/handoff-security-secf78dbe639/web
2. iMore, "How to set up and use Handoff on your iPhone and iPad": "Handoff broadcasts activities using Bluetooth Low Energy (BT LE) and transfers them using Wi-Fi, either directly or through iCloud." — https://www.imore.com/how-use-handoff-iphone-and-ipad

---

### Product 8 — vivo Office Kit / EasyShare One-Tap Transfer

- **Company**: vivo Communication Technology Co., Ltd.
- **Version/Release**: vivo X300 series + OriginOS 6 launched globally in late 2025; vivo Office Kit iOS app on App Store; EasyShare v54+.
- **Technology overview**: Manila Standard (Oct./Nov. 2025) describes the X300 One-Tap Transfer: "long press to select photos or files on your X300 Series smartphone, tap the NFC area of the iPhone, and accept the transfer instantly." Requires EasyShare app on iPhone (v54+), Bluetooth, Wi-Fi, NFC, and unlocked state. Office Kit (separate app) provides screen mirroring iPhone↔iPad, multi-device note sync, File EasyShare.

**Claim 1 mapping**

- **[1a]**: NFC tap is a gesture; phone receives file metadata. **YES**.
- **[1b]**: EasyShare / Photos app on iPhone executes. **YES**.
- **[1c]**: Receive-file function. **YES**.
- **[1d]**: Tied to the selected files. **YES**.

**Overall Claim 1 literal: YES**

**Dependent claims**

- **Claim 2**: NFC → Wi-Fi link. **YES**.
- **Claim 3**: No messaging-keyboard flow. **NO**.
- **Claim 4**: App identifier conveyed (EasyShare → Photos). **PARTIAL/YES**.
- **Claim 5**: Office Kit can bridge to Windows or Mac PC. **PARTIAL/YES**.
- **Claim 13**: Performable on both. **YES**.
- **Claim 14**: One physical gesture, one function (file transfer). **NO**.
- **Claim 15**: Automatic after tap. **YES**.

**Claims 6 / 11**: **YES**.

**Overall assessment**: Literal **YES**; **Severity: LOW** (low U.S. market presence — concentrated in China, SEA, India); **Confidence: Medium**.

**Design-arounds**: Replace NFC tap with QR code pairing or in-app picker.

**Sources**:
1. Manila Standard, "vivo X300 Series One-Tap Transfer: Breaking barriers between Android and iOS" — https://manilastandard.net/tech/314684213/vivo-x300-series-one-tap-transfer-breaking-barriers-between-android-and-ios.html
2. Apple App Store, "vivo Office Kit" — https://apps.apple.com/us/app/vivo-office-kit/id6748333034

---

### Product 9 — Apple Watch Handoff / Auto-Unlock Mac

- **Company**: Apple Inc.
- **Version/Release**: Auto-Unlock Mac introduced with macOS Sierra / watchOS 3 (2016); current through macOS Sequoia / watchOS 11 (2025).
- **Technology overview**: Apple Support: "While you're wearing Apple Watch, your Mac can sense when you're nearby and automatically log you in… Auto Unlock works when you're wearing your unlocked watch and are very close to your Mac." Apple's Platform Security guide adds: "Distance measured between the Mac and Apple Watch needs to be 2–3 meters or less."

**Claim 1 mapping**

- **[1a]**: No user gesture — the watch passively broadcasts via BLE/802.11ac time-of-flight; the Mac performs ambient ranging. The watch side-button double-press is required only for *approving administrator-password prompts*, not the basic unlock. **NO** for basic unlock; **PARTIAL** for password-approval prompts.
- **[1b]**: Mac auto-unlocks; no application execution per se. The claim contemplates app launch; unlocking the system is not an "application." **NO**.
- **[1c]**: N/A. **NO**.
- **[1d]**: No "activity" being continued. **NO**.

**Overall Claim 1 literal: NO**

**DoE**: Function (cross-device authentication) is different in kind from the patent's "continue an activity." **NO**.

**Overall assessment**: Literal **NO**; DoE **NO**; **Severity: NONE**; **Confidence: Very High**.

**Sources**:
1. Apple Support, "Unlock your Mac with your Apple Watch" — https://support.apple.com/en-us/102442
2. Apple Support, "Automatically unlock Apple devices" (Platform Security guide) — https://support.apple.com/guide/security/automatically-unlock-apple-devices-sec6ab47ebfc/web

---

### Product 10 — Microsoft Phone Link / Cross-Device Resume (XDR) / Edge Continue on PC

- **Company**: Microsoft Corporation
- **Version/Release**: Phone Link (renamed from "Your Phone"); Cross Device Resume initially shipped for OneDrive cloud files in May 2025; expanded to Spotify in August 2025; to M365 Copilot (Word/Excel/PowerPoint online) on Samsung/Honor/Huawei/Oppo/vivo phones in **November 2025** (Windows 11 Insider Build 26220.7271 / KB5070307). Continuity SDK published on Microsoft Learn.
- **Technology overview**: Microsoft Learn ("Cross Device Resume"): "Resume is a Limited Access Feature… apps can use activities to enable users to get back to what they were doing in their app, across multiple devices. Activities created by any mobile app appear on users' Windows device(s) so long as those devices have been Cross Device Experience Host (CDEH) provisioned." Trigger is *not* a gesture — it is a background AppContext push from the phone via Link to Windows to the PC, surfaced as a small phone-badge icon overlaid on the matching app icon in the Windows 11 Taskbar. The user clicks the taskbar icon to resume.

**Claim 1 mapping**

- **[1a]**: No gesture. AppContext push is over Microsoft's cloud / Link-to-Windows pipe regardless of physical proximity. **NO**.
- **[1b]**: PC app launches when the user clicks the taskbar resume badge, not in response to a gesture-conveyed info packet. **NO** as to gesture nexus.
- **[1c]**: App opens the same content. YES in isolation but not in claim combination.
- **[1d]**: No "while the gesture is performed" element. **NO**.

**Overall Claim 1 literal: NO**

**DoE**: Way is meaningfully different (network sync + Taskbar UI vs. proximity gesture). **NO**.

**Overall assessment**: Literal **NO**; DoE **NO**; **Severity: NONE/LOW**; **Confidence: Very High**.

**Sources**:
1. Microsoft Learn, "Use the Continuity SDK to implement Cross Device Resume (XDR) for Android and Windows Applications" — https://learn.microsoft.com/en-us/windows/apps/develop/windows-integration/cross-device-resume
2. Windows Latest, "Microsoft is using Windows 11 taskbar to resume your Android activities" (Nov. 25, 2025): "Your phone creates a small 'context packet' that contains the app, the content you are using, and instructions on how your PC should continue it. Windows receives that packet through the Cross Device Experience Host and launches the correct app or browser tab." — https://www.windowslatest.com/2025/11/25/microsoft-is-using-windows-11-taskbar-to-resume-your-android-activities/

---

## 4. Summary Comparison Table

| # | Product | [1a] | [1b] | [1c] | [1d] | Cl. 2 | Cl. 4 | Cl. 13 | Cl. 14 | Cl. 15 | Cl. 1 Literal | DoE | **Severity** |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 1 | Apple HomePod (mini) U1 Handoff | YES | YES | YES | YES | YES | YES | YES | PARTIAL | YES | **YES** | n/a | **HIGH** |
| 2 | iOS 17+ NameDrop / Proximity AirDrop / SharePlay | YES | YES | YES | YES | YES | YES | YES | PARTIAL | YES/PART | **YES** | YES | **HIGH** |
| 3 | Huawei Share OneHop / Multi-Screen Collab | YES | YES | YES | YES | YES | YES | YES | YES | YES | **YES** | n/a | **HIGH** |
| 4 | Xiaomi HyperConnect Touch-to-Share + App Relay | YES | YES | YES | YES | YES | YES | YES | PARTIAL | YES | **YES** | YES | **HIGH** |
| 5 | Google/Samsung Android 17/One UI 9 Tap to Share | YES | YES | YES | YES | YES | YES | YES | PARTIAL | YES | **YES**\* | YES | **HIGH** |
| 6 | OPPO/OnePlus/realme O+ Connect Touch | YES | YES | YES | YES | YES | YES | YES | PARTIAL | YES | **YES** | YES | **MEDIUM** |
| 7 | Apple Classic Handoff | NO | YES† | YES† | NO | NO | n/a | n/a | n/a | NO | **NO** | NO | **LOW/NONE** |
| 8 | vivo Office Kit / EasyShare One-Tap | YES | YES | YES | YES | YES | PARTIAL | YES | NO | YES | **YES** | n/a | **LOW** |
| 9 | Apple Watch Auto-Unlock Mac | NO | NO | NO | NO | NO | n/a | n/a | n/a | NO | **NO** | NO | **NONE** |
| 10 | Microsoft Phone Link / XDR / Edge Continue | NO | NO | YES† | NO | NO | n/a | n/a | n/a | NO | **NO** | NO | **NONE/LOW** |

\* Pending stable release (expected July 2026 alongside Galaxy Z Fold 8 / Flip 8). † Element satisfied in isolation but not in the gesture-conditioned combination required by Claim 1.

(Note: **Claim 3**, "messaging-keyboard for replying to a notification," is materially hit only by Huawei Multi-Screen Collaboration and partially by Xiaomi HyperConnect App Relay. **Claim 5**, "control info to third device," is satisfied by Apple HomePod (AirPlay), Huawei Multi-Screen (call routing), Xiaomi HyperConnect (cross-device casting), Google/Samsung Quick Share (multi-recipient), OPPO O+ Connect (PC bridging), and partly vivo Office Kit.)

## 5. Conclusions — Which Products Are Most Exposed

**Top tier (HIGH severity; strong literal Claim 1 + most dependent claims)**:

1. **Huawei Share OneHop / Multi-Screen Collaboration** — the cleanest, most textbook read across the entire chart. NFC-tap gesture, automatic app launch, content-bound function, *plus* a Claim-3-grade messaging-keyboard reply ("Open Messaging to view and reply to SMS messages"), *plus* a Claim-14-grade two-gesture mapping (tap vs. shake-then-tap). The strongest first defendant.
2. **Apple iOS 17+ AirDrop "Bringing Devices Together" / NameDrop / SharePlay-by-proximity** — Apple's own SVP Craig Federighi publicly called this a "gesture" during the WWDC 2023 keynote. Three distinct contextual functions (NameDrop, file share, SharePlay) all triggered by the same proximity move, mapping squarely onto Claim 1.
3. **Apple HomePod / HomePod mini U1 Handoff** — Apple Support explicitly directs users to "hold your iPhone near the top of HomePod until the transfer is complete," and the U1 chip's deterministic ranging gives the patentee a defensible *gesture* (not merely ambient proximity).
4. **Xiaomi HyperConnect Touch-to-Share (贴贴分享) + App Relay** — Xiaomi's own marketing copy describes the NFC tap in near-patent terms; App Relay adds a Claim 3 hit via cross-device notification reply.
5. **Google / Samsung Android 17 / One UI 9 Tap to Share (Quick Share)** — Once stable, structurally identical to Huawei OneHop and Xiaomi Touch-to-Share. **Caveat**: Samsung is the patent's assignee (self-licensed); the real target is **Google's** platform-level "TapToShare" service on non-Galaxy hardware (notably Pixel). As of May 27, 2026, the feature is in late-stage beta, not stable; the SammyFans timeline projects stable launch in **July 2026 alongside the Galaxy Z Fold 8 / Flip 8**.

**Middle tier (MEDIUM)**:
6. **OPPO / OnePlus / realme O+ Connect Touch-to-Share** — likely literal infringement but materially smaller U.S. footprint; depends on user installing the O+ Connect iOS app.

**Bottom tier (LOW)**:
7. **vivo Office Kit / EasyShare** — likely infringes Claim 1 mechanically; very limited U.S. presence.

**Likely non-infringing**:
8. **Apple "Classic" Handoff** — fails [1a] (ambient BLE, no affirmative gesture).
9. **Apple Watch Auto-Unlock Mac** — fails all four limitations; different problem domain (authentication, not activity continuation).
10. **Microsoft Phone Link / Cross-Device Resume / Edge Continue on PC** — fails [1a] (cloud/Link-to-Windows AppContext push, no proximity gesture).

**Strategic implication**: The patent has its strongest read against **NFC-tap-to-share** implementations (Huawei, Xiaomi, OPPO, vivo, Google/Samsung Tap to Share) and against **UWB-proximity-gesture** implementations on Apple (HomePod mini U1 Handoff, iOS 17 AirDrop proximity). Conversely, the patent does **not** read on pure BLE-broadcast continuity (classic Handoff, Phone Link XDR) or on authentication-only proximity (Auto-Unlock Mac). For a patent owner enforcement strategy, the highest-leverage first defendants are Huawei (most textbook read; multiple dependent-claim hits) and Apple (largest U.S. damages base; gesture explicitly admitted by Federighi).

## 6. Caveats & Limitations

1. **Patent text not independently verified.** The mapping uses the claim-element summary supplied in the task brief; the subagent dispatched to pull the verbatim text of US 10,484,528 B2 from patents.google.com, USPTO PatFT, and Espacenet returned "unable to retrieve" due to a fetch-tool permissions restriction on patent domains. Before any pre-suit demand letter or contention chart is finalized, the verbatim issued claims must be pulled from USPTO Patent Center and this chart re-validated word-for-word. The precise meaning of "gesture performed with a second electronic device" and "while the gesture is performed" will drive borderline calls on iOS 17 proximity and U1 HomePod.
2. **Claim construction assumptions.** "Gesture" is treated as requiring an affirmative user-initiated motion (tap, bring-together, shake) and not satisfied by ambient BLE detection. The patentee may attempt a broader construction sweeping in classic Handoff and Auto-Unlock; the prosecution history (which we did not access) may resolve this either way.
3. **Pre-release products.** Google/Samsung Tap to Share is observed only in late-beta One UI 9 leaks (Android Authority, March 30, 2026; 9to5Google, April 17, 2026; SammyGuru, April 2026). Stable launch is projected for July 2026 alongside the Galaxy Z Fold 8 / Flip 8. Damages do not accrue until release. Sources explicitly flag the standard caveat that "predicted features may not make it to a public release."
4. **No teardown evidence.** Mapping for OPPO O+ Connect, Xiaomi Touch-to-Share, and vivo One-Tap Transfer relies on first-party marketing pages and tech-press coverage. Validation against actual firmware behavior (logcat / Wireshark capture of the NFC payload) is recommended before litigation.
5. **Samsung self-licensing.** Samsung is the patent assignee; its own Galaxy Tap to Share / One UI 9 implementation cannot infringe its own patent. The chart's Product 5 entry is primarily about *Google's* platform-level "TapToShare" service in Play Services and Android 17, which will run on non-Samsung handsets (Pixel and other OEMs).
6. **U.S. nexus.** Several of the accused products (Huawei OneHop, Xiaomi HyperConnect, vivo Office Kit) have substantially reduced U.S. footprints due to U.S. export restrictions, BIS Entity List actions, and the absence of those brands from U.S. carrier shelves. This materially reduces realistic U.S. damages exposure even where infringement is technically clean.
7. **No legal opinion.** This is a technical claim-by-claim mapping, not infringement counsel. Final infringement determination requires claim construction under *Phillips v. AWH Corp.* and consideration of prosecution history, prior art, and ensnarement under DoE — none of which were performed here.