# CLAIM-TO-DESCRIPTION MAPPING

## IN 201641043709 — “Methods and systems for rendering a camera preview in an electronic device”

This document maps every element of Claims 1–7 (as amended 4 Aug 2020) to the paragraphs of the Complete Specification where that element is described, explained, or exemplified. Paragraph numbers ([001]–[0040]) and Figures (FIGS. 1–7b) refer to the filed specification.

-----

## QUICK REFERENCE — Where Each Claim Lives in the Description

|Claim                      |Primary support paragraphs       |Figures                  |
|---------------------------|---------------------------------|-------------------------|
|Claim 1 (method)           |[004], [0018], [0030]–[0033]     |FIG. 3 (flow diagram 300)|
|Claim 2 (property overlay) |[005], [0026]–[0027], [0036]     |FIGS. 5a–5c              |
|Claim 3 (stitching)        |[006], [0027], [0038]            |FIGS. 7a–7b              |
|Claim 4 (apparatus)        |[007], [0019], [0025]–[0027]     |FIG. 2                   |
|Claim 5 (device, property) |[0026]–[0027], [0036]            |FIGS. 5a–5c              |
|Claim 6 (device, stitching)|[0027], [0038]                   |FIGS. 7a–7b              |
|Claim 7 (system)           |⚠️ No dedicated support — see note|—                        |

-----

## CLAIM 1 (METHOD) — ELEMENT-BY-ELEMENT

### Element 1[a] — “detecting, by an object detection unit (202), at least one object in a camera preview, wherein the camera preview includes preview of at least one of first camera and at least one of second camera”

|Description support          |What it says                                                                                                                                                                                                                               |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|**[004]** (Summary)          |“The method includes detecting at least one object in a camera preview, wherein the camera preview includes preview of at least one of first and at least one of second camera of the electronic device.” — verbatim basis for the element.|
|**[0030]** (FIG. 3, step 302)|“At step 302, the method includes detecting one or more object(s) in a camera preview. The method allows the object detection unit 202 to detect the one or more object(s)…”                                                               |
|**[0025]**                   |Defines the object detection unit 202 as configured to “detect one or more object(s) in a camera preview, wherein the camera preview includes preview of one or more of first and one or more of second camera(s).”                        |
|**[0023]** (FIG. 1 example)  |Concrete example: rear camera previews a mannequin wearing spectacles; the device “detect[s] and extract[s]/select[s] an interested object (for example, the spectacle).”                                                                  |
|**[0035]** (FIG. 4)          |Repeats the spectacles/mannequin walk-through: “the object detection unit 202 can be configured to detect an object of interest (here the object of interest refers to the spectacle).”                                                    |

### Element 1[b] — “selecting, by an object extraction unit (204), the at least one object from the camera preview of one of the at least one of first camera (102) and at least one of second camera (104)”

|Description support               |What it says                                                                                                                                                                                 |
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|**[004]**                         |“Further, the method includes selecting the at least one object from the camera preview of one of the at least one of first and at least one of second camera.”                              |
|**[0031]** (FIG. 3, step 304)     |“the method includes selecting the one or more object(s)… The method allows the object extraction unit 204 to select the one or more object(s)…”                                             |
|**[0025]**                        |Object extraction unit 204 “configured to select the one or more object(s) from the camera preview of one of the one or more of first camera(s) 102 and one or more of second camera(s) 104.”|
|**🔑 [0026] — CRITICAL DEFINITION**|“In an example herein, **the object can be a hat, earring, necklace, hair wigs, spectacle, an image itself or a part of the image, or the like.**”                                           |


> **⚖️ LITIGATION SIGNIFICANCE OF [0026]:** This sentence is your single most valuable claim-construction asset. Snap’s predicted defense is that a *whole person/body* is not an “object” because the spec only contemplates small accessories. But [0026] expressly says the object can be “**an image itself or a part of the image**” — i.e., ANY image region, which plainly covers a segmented human silhouette. This paragraph substantially defuses the “object = accessory only” narrowing argument.

### Element 1[c] — “determining, by a location detection unit (206), at least one intended location in the camera preview of one of [first/second] camera, wherein the camera preview in which the at least one object is selected is DIFFERENT from the camera preview in which the at least one intended location is determined”

|Description support          |What it says                                                                                                                                                                                                                                                                        |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|**[004]**                    |“…determining at least one intended location in the camera preview… wherein the camera preview in which the at least one object is selected is different from the camera preview in which the at least one intended location is determined.” — the cross-camera asymmetry, verbatim.|
|**[0032]** (FIG. 3, step 306)|“the method includes determining one or more intended location(s)… The camera preview in which the one or more object(s) is selected is different from the camera preview in which the one or more intended location(s) is determined.”                                             |
|**[0026]**                   |Location detection unit 206 definition + **example of intended location: “the intended location(s) can be a part of face, upper torso or the like.”**                                                                                                                               |
|**[0023]** (FIG. 1)          |Example: “determine an intended location in the preview of the second image (i.e., user image) and render the preview of the second image by overlaying the spectacles on the intended location.”                                                                                   |
|**[0035]** (FIG. 4)          |“The location detection unit 206 can be configured to determine the intended location on the preview of the user selfie to place the spectacle.”                                                                                                                                    |


> **⚖️ LITIGATION NOTE on “determining”:** The spec gives examples (“part of face, upper torso”) but never requires *user-driven* or *dynamic* location selection — determination by automated logic suffices. This supports rebutting Snap’s anticipated “Cutout just auto-centers, it doesn’t *determine*” defense: the spec’s location detection unit is itself an automated determiner. Note also FIG. 7b’s repositioning concept ([0038]: “reposition the objects… in the rendered final camera preview image for a better view”) shows placement logic is contemplated as adjustable — and Snapchat Cutout reportedly allows the cutout position to be adjusted, which would map onto this.

### Element 1[d] — “rendering, by a rendering unit (208), a final camera preview of one of [first/second] camera, wherein the final camera preview is rendered by overlaying the at least one object on the at least one intended location”

|Description support          |What it says                                                                                                                                                                                                                        |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|**[004]**                    |“…rendering a final camera preview of one of the at least one of first and at least one of second camera, wherein the final camera preview is rendered by overlaying the at least one object on the at least one intended location.”|
|**[0033]** (FIG. 3, step 308)|“the method includes rendering a final camera preview… The final camera preview is rendered by overlaying the one or more object(s) on the one or more intended location(s).”                                                       |
|**[0026]**                   |Rendering unit 208 definition (same overlay language).                                                                                                                                                                              |
|**[0024]**                   |Purpose/effect: “allow the user to preview, how the object looks on self by means of superimposition or overlaying the objects… a unique way of trying out cosmetic ornaments products without using them physically.”              |
|**[0023] + FIG. 1**          |The rendered result: spectacles overlaid on the user’s selfie preview “as shown in FIG. 1.”                                                                                                                                         |


> **⚖️ “PREVIEW” = LIVE:** [002] (background) frames the problem in terms of live camera use; [0022] describes “dynamically rendering a final camera preview”; FIG. 3’s flow operates on previews, not stored files. This supports construing “preview” as the live viewfinder — exactly where Snapchat Cutout renders its composite.

-----

## CLAIM 2 (METHOD — PROPERTY OVERLAY)

**Claim language:** “rendering the final camera preview by overlaying at least one property of the at least one object on the at least one intended location.”

|Description support            |What it says                                                                                                                                                                                                                                                                                                                               |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|**[005]** (Summary)            |“the method includes rendering the final camera preview by overlaying at least one property of the at least one object on the at least one intended location.”                                                                                                                                                                             |
|**🔑 [0027] — PROPERTY DEFINED**|“In an example, **the property can be a color, lighting or the like.**”                                                                                                                                                                                                                                                                    |
|**[0036] + FIGS. 5a–5c**       |Full worked example: lipstick previewed in first camera (FIG. 5a); lips previewed in second camera (FIG. 5b); “the object of interest can be identified as the lipstick and the property identified can be the color of the lipstick”; the lips preview is rendered “by overlaying the color of the selected lipstick as shown in FIG. 5c.”|
|**[0036]**                     |Also shows detection of “properties such as color and lighting” by the object detection unit.                                                                                                                                                                                                                                              |


> **Why Snapchat does NOT meet Claim 2:** Cutout transfers the entire segmented image region — not an abstracted *property* (color/lighting) of an object. The lipstick example shows Claim 2 means extracting an attribute and applying it to a different surface (lip color onto lips). No Cutout behavior does this.

-----

## CLAIM 3 (METHOD — STITCHING)

**Claim language:** “rendering the final preview by stitching at least one object from the camera preview of the at least one first camera (102) and at least one second camera (104).”

|Description support               |What it says                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|**[006]** (Summary)               |“the method includes rendering the final preview by stitching at least one object from the camera preview of the at least one first and at least one second camera.”                                                                                                                                                                                                                                                                                                 |
|**[0027]**                        |“the rendering unit 208 can be configured to render the final preview by stitching one or more object(s) from preview of the one or more first camera(s) 102 and one or more second camera(s) 104.”                                                                                                                                                                                                                                                                  |
|**[0038] + FIGS. 7a–7b**          |Worked example: device captures images from both cameras and renders the final preview “by stitching one or more object(s)… as shown in FIG. 7a. Thus, the proposed invention provides a **combined view** of the preview images taken from the first camera and the second camera…” and “the electronic device 100 can be configured to **reposition the objects (i.e., people)** in the rendered final camera preview image for a better view as shown in FIG. 7b.”|
|**[0037] + FIGS. 6a–6b** (related)|Selfie-into-panorama example: “The selfie of the user is rendered in to the panoramic image captured by the first camera 102” — note the spec treats this as an **overlay** example (Claim 1 direction front→rear), not stitching.                                                                                                                                                                                                                                   |


> **⚖️ IMPORTANT NUANCE:** [0038] describes stitching as producing a “combined view” with multiple people merged into one scene and repositionable. An aggressive reading could argue Snapchat Cutout (user merged into rear scene, position adjustable) resembles FIG. 7b. The conservative reading (taken in the claim chart) is that Cutout is an *overlay* squarely within Claim 1/[0023]/[0037], not “stitching.” Keep Claim 3 as a fallback theory only — [0037]’s selfie-into-panorama example is described with “rendered in to,” which blurs the overlay/stitch line and could support a secondary Claim 3 argument if claim construction goes sideways on Claim 1.

-----

## CLAIM 4 (APPARATUS) — UNIT-BY-UNIT

**Claim language:** electronic device comprising object detection unit (202), object extraction unit (204), location detection unit (206), rendering unit (208/210).

|Claim 4 unit                        |Description support                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|Preamble — “electronic device (100)”|**[0023]:** “the electronic device 100 can be, for example, a mobile phone, a smart phone, tablet, a phablet, a personal digital assistant (PDA), a wearable computing device or any other electronic device with multiple cameras.” Camera positions: “front, back, side, or at any position” ([0023]).                                                                                                              |
|Object detection unit (202)         |**[007]**, **[0025]** (configured to detect objects in previews of both cameras); FIG. 2 block diagram.                                                                                                                                                                                                                                                                                                               |
|Object extraction unit (204)        |**[007]**, **[0025]** (configured to select the object); object examples **[0026]**.                                                                                                                                                                                                                                                                                                                                  |
|Location detection unit (206)       |**[007]**, **[0026]** (determine intended location in the *different* preview; examples: part of face, upper torso).                                                                                                                                                                                                                                                                                                  |
|Rendering unit (208)                |**[007]**, **[0026]–[0027]** (overlay object / overlay property / stitch).                                                                                                                                                                                                                                                                                                                                            |
|Memory unit (210)                   |**[0027]:** “The memory 210 can be configured to store camera previews… and the rendered final camera preview along with the overlaying one or more object(s).” (Note: memory is described but NOT claimed — claim 4’s rendering unit is numbered 210 in the amended claim text, an apparent typographical inconsistency with the spec where 210 = memory and 208 = rendering unit. Flag for the file-wrapper review.)|
|Units are software-implementable    |**[0028]:** units can be combined; **[0039]:** “embodiments… can be implemented through at least one software program running on at least one hardware device.”                                                                                                                                                                                                                                                       |


> **⚠️ TWO FLAGS FOR THE RECORD:**
> 
> 1. **Reference numeral inconsistency:** Amended Claim 4 recites “a rendering unit (210)” while the spec assigns 210 to the *memory unit* and 208 to the *rendering unit* (and amended Claims 5–6 revert to “(208)”). Minor clerical issue, but opposing counsel may use it; have the explanation ready (obvious typographical error, correctable; numerals are non-limiting).
> 1. **[0039] is a Section 3(k) liability:** “implemented through at least one software program running on at least one hardware device” is the sentence Snap will quote to argue the “units” are pure software on a generic phone (computer programme per se). The counter-narrative must lean on [0024]/[002] (technical effect: solving the underutilized-second-camera problem; real-time dual-camera pipeline).

-----

## CLAIM 5 (DEVICE — PROPERTY) → same support as Claim 2: [005]/[0026]–[0027]/[0036]/FIGS. 5a–5c.

## CLAIM 6 (DEVICE — STITCHING) → same support as Claim 3: [006]/[0027]/[0038]/FIGS. 7a–7b.

-----

## CLAIM 7 — “A system performing method steps as claimed in claims 1 to 3”

|Description support|Assessment                                                                                                                                                                                                                                                                                                                                                  |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|**None dedicated.**|Claim 7 was newly added in the 4 Aug 2020 amendment. The specification never describes a “system” as a distinct entity — only the “electronic device 100” and its units. The only arguably supporting text is the generic [0039] (“software program running on at least one hardware device… network management functions to control the network elements”).|


> **⚠️ This confirms the vulnerability flagged in the validity report:** Claim 7 lacks clear descriptive basis, is omnibus-style, and is exposed under Section 10(4)/(5) (sufficiency/definiteness) and Section 59 (amendment beyond scope). Do not lead with Claim 7.

-----

## SPEC-WIDE DEFINITIONS TABLE (claim-construction arsenal)

|Claim term                |Spec definition/example                                                                                                 |Paragraph    |Use in the Snapchat case                                                                    |
|--------------------------|------------------------------------------------------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------------------------|
|“object”                  |“hat, earring, necklace, hair wigs, spectacle, **an image itself or a part of the image**, or the like”                 |[0026]       |✅ A segmented body IS “a part of the image” — defeats the accessories-only narrowing defense|
|“intended location”       |“a part of face, upper torso or the like”                                                                               |[0026]       |Neutral-to-favorable; automated placement contemplated                                      |
|“property”                |“a color, lighting or the like”                                                                                         |[0027]       |Confirms Claims 2/5 don’t read on Cutout (be honest)                                        |
|“electronic device”       |“mobile phone, a smart phone, tablet… or any other electronic device with multiple cameras”                             |[0023]       |iPhone/Android running Snapchat qualifies                                                   |
|“media”                   |“a video; an image, a screenshot from a video or the like”                                                              |[0023]       |Covers both photo and video Cutout modes                                                    |
|camera positions          |“front, back, side, or at any position”                                                                                 |[0023]       |Front=second/rear=first mapping is flexible — claim doesn’t fix which camera is which       |
|purpose / technical effect|overlay/superimpose to preview objects on self; try products “without using them physically”; solve dual-camera underuse|[002], [0024]|Backbone of the Section 3(k) “technical effect” argument                                    |
|software implementation   |“at least one software program running on at least one hardware device”                                                 |[0039]       |⚠️ Snap’s 3(k) ammunition — prepare counter                                                  |

-----

## BOTTOM LINE

1. **Claims 1 and 4 are fully grounded in the description** — every element traces to [004]/[007] (summary), [0025]–[0027] (units), [0030]–[0033]/FIG. 3 (method flow), with worked examples in [0023]/FIG. 1 and [0035]/FIG. 4.
1. **Paragraph [0026] is your best friend:** “an image itself or a part of the image” makes the segmented-body-as-object construction strongly defensible — the most important spec sentence for the Snapchat case.
1. **Paragraph [0039] is your biggest spec-based liability** (Section 3(k) software-per-se ammunition), and **Claim 7 has no real descriptive home**.
1. The FIG. 6a/6b selfie-into-panorama example ([0037]) is the spec’s closest analogue to what Snapchat Cutout actually does — keep it front and center in the infringement narrative.

-----

*Prepared for claim-construction and pleading support. Paragraph citations refer to the Complete Specification as filed (Form 2). Not legal advice.*