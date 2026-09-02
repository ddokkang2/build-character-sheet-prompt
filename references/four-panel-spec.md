# Four-Panel Character Sheet Specification

Apply this specification to the concrete details observed in the user's character image. Write a finished image-generation prompt, not a meta-template.

## Contents

- Output contract
- Required four-panel composition
- Character analysis content
- Background, lighting, and presentation
- Bottom-heavy preservation block
- Negative constraints

## Output Contract

Return only:

1. One production-ready English prompt in a clean copyable code block.
2. A two- or three-sentence Korean summary covering the character's key identity and outfit details, the left-panel face-exclusion rule, and the exact 90-degree side-view rule.

The English prompt must be 5,000 characters or fewer, counting letters, spaces, punctuation, and line breaks inside the prompt but excluding code-fence markers and the Korean summary. Target approximately 4,500–4,800 characters. If the draft is too long, compress repeated details and generic adjectives while preserving every mandatory composition rule, exact required sentence, core identity and outfit evidence, preservation block, and essential negative constraint.

Do not add headings, analysis notes, caveats, alternatives, placeholders, or setup instructions outside those two items.

## Required Composition

Specify one clean professional character reference sheet divided into four tall vertical panels arranged left-to-right in a single row. Use this exact order:

1. Leftmost: front outfit and body view, face excluded.
2. Center-left: exact 90-degree full-body side view.
3. Center-right: complete full-body back view.
4. Rightmost: close-up face portrait.

### Panel 1: Front Outfit and Body View, Face Excluded

Include this meaning explicitly and unambiguously:

> Front-facing character view framed intentionally from the base of the neck to the soles of the shoes. Show the character completely from neck to toe, with the full shoulders, torso, arms, hands, waist, legs, and shoes fully visible inside the frame without any cropping below the neck.

Require a straight neutral pose. Place the upper frame boundary at the base of the neck, immediately above the collar and shoulder line. Exclude the face, chin, mouth, nose, eyes, eyebrows, ears, hair, hairline, scalp, skull, and every other part of the head.

State that the missing head must not be replaced with a blank or featureless head, mannequin, silhouette, mask, blur, shadow, black void, or floating facial features. Describe the composition as an intentional neck-to-toe costume and body reference, not an accidental crop or decapitation effect. Keep the neckline, collar, complete shoulder construction, arms, hands, legs, and both shoes readable and uncropped.

### Panel 2: Exact 90-Degree Full-Body Side View

Include this exact sentence:

> Full-body exact 90-degree side-profile shot showing the character completely from head to toe, with the top of the head and shoes fully visible inside the frame without any cropping.

Show the character facing the right edge of the sheet in a strict orthographic-style profile. Keep the head, neck, shoulders, ribcage, pelvis, knees, and feet aligned in a true 90-degree side orientation. Do not turn the face, shoulders, torso, hips, or feet toward the camera. Do not use a front three-quarter, rear three-quarter, or near-profile angle.

Use a straight neutral standing pose with the head level. Keep the arms relaxed and preserve a narrow but readable separation between near and far limbs without rotating the torso. Keep both legs and both shoes legible with minimal, non-dynamic fore-aft separation if needed.

Clearly show the forehead-to-nose-to-lips-to-chin facial silhouette, front and rear hair contour, chest and back depth, abdomen, pelvis, garment thickness, sleeve profile, belt and strap depth, pocket projection, side-mounted accessories, knee shape, calf shape, heel, toe, sole thickness, and side construction of the footwear.

Maintain the character's exact scale, height, body proportions, identity, hairstyle, outfit, materials, colors, props, weapons, and accessory placement. Preserve asymmetric left/right details correctly for the chosen side and do not mirror or relocate them.

### Panel 3: Complete Back View

Include this exact sentence:

> Full-body shot showing the character completely from head to toe, with the top of the head and shoes fully visible inside the frame without any cropping.

Require a straight neutral back-facing pose. Show the rear hairstyle, head shape, collar, shoulder construction, garment layers, seams, closures, rear pockets, straps, belts, holsters, bags, accessories, legs, heels, and soles. Match the first and second panels' character, scale, body proportions, clothing, materials, colors, and equipment.

### Panel 4: Close-Up Face Portrait

Show the complete head, hairstyle, face, neck, and upper shoulders of the same character. Require the exact facial identity visible in the source: face shape, proportions, hairline, eyebrows, eye shape and color when visible, nose, lips, jaw, chin, ears when visible, skin tone and texture, makeup, freckles, moles, scars, tattoos, facial paint, piercings, glasses, headwear, and other distinctive details. Use a neutral expression unless the source has a defining expression.

## Character Analysis Content

Convert image evidence into exact visual language. Include all applicable details:

- **Identity and build:** apparent ethnicity, gender presentation, age impression, height impression, build, posture, shoulder width, torso, waist, hips, limb proportions, skin tone, undertone, and silhouette.
- **Hair:** style, length, color, roots, highlights, part, bangs, volume, texture, waves, curls, braids, tied or shaved sections, hairline, loose strands, and flyaways. Apply hair to the side, back, and portrait panels only.
- **Face:** structure, forehead, eyebrows, eyes, eyelids, lashes, nose, cheekbones, jaw, chin, lips, ears, skin texture, makeup, marks, scars, tattoos, paint, and piercings. Preserve the side silhouette in Panel 2 and full identity details in Panel 4.
- **Outfit:** describe visible layers from inner to outer. Identify garment type, exact color placement, material, texture, finish, fit, length, construction, seams, stitching, panels, collars, cuffs, hems, pockets, buttons, zippers, buckles, laces, closures, patterns, visible symbols, wear, dirt, and damage.
- **Footwear:** type, height, toe and heel design, sole thickness and color, fastening, panels, stitching, material, finish, wear, and exact color placement. Keep the shoes complete and readable in the front, side, and back body-reference panels.
- **Props and accessories:** weapons, holsters, sheaths, belts, pouches, bags, backpacks, harnesses, tags, badges, jewelry, watches, glasses, goggles, gloves, mechanical parts, technology, and tools. State each item's location, side, orientation, size, shape, material, color, and attachment.

Use precise visible colors rather than broad labels. Match the source's realistic, illustrated, stylized, 2D, 3D, or hybrid rendering register. For unseen areas, specify only a conservative continuation of visible construction.

## Background, Lighting, and Presentation

Include these requirements verbatim:

> Neutral light grey studio background in all four panels.

> Soft studio product photography lighting, subtle grounded contact shadows under feet.

Keep light direction, softness, exposure, white balance, color temperature, material response, and shadow density consistent. Add subtle grounded contact shadows under the feet in the front, side, and back body-reference panels. Use a seamless uncluttered studio background, accurate anatomy, clear silhouettes, neutral reference poses, crisp garment construction, balanced spacing, consistent body-view scale, and production-quality detail.

Exclude scenery, furniture, architecture, narrative action, decorative graphics, captions, arrows, logos not present on the character, watermarks, measurement lines, and UI elements.

## Bottom-Heavy Preservation Block

Near the bottom of the English prompt, explicitly state:

> Strictly maintain identical proportions, identity, and clothing across all panels.

Then reinforce that all four panels show the exact same character at the same age with identical apparent identity, build, proportions, skin tone, hairstyle, hair color, face, outfit layers, garment construction, materials, textures, colors, footwear, props, weapons, accessories, lighting, and render style.

Clarify that Panel 1 represents the same character even though the head is outside the frame. The exclusion is a framing choice only and must not change the neck, shoulders, body proportions, clothing, or identity.

Clarify that Panel 2 is a geometric side reference, not an expressive three-quarter view. Keep it at exactly 90 degrees with no torso twist, perspective drift, or turn toward the camera.

Preserve the correct left/right placement of asymmetric details when rotating the character. Do not mirror them incorrectly. Keep every visible layer, collar, sleeve, seam, closure, pocket, strap, belt, buckle, holster, weapon, and accessory in its consistent applicable position.

Forbid redesigning, simplifying, recoloring, removing, replacing, or adding character elements. Forbid alternate costumes, age changes, body changes, style variants, and inconsistent panel scales.

## Negative Constraints

End with a compact but explicit negative block prohibiting:

- any face, head, chin, ear, or hair entering Panel 1;
- blank or featureless heads, mannequins, masks, blurs, shadows, blacked-out faces, floating features, or a decapitation effect;
- a three-quarter angle, near-profile angle, torso twist, camera-facing shoulders, or perspective distortion in Panel 2;
- cropped shoulders, hands, fingers, legs, shoes, feet, the side-panel head, the side-panel shoes, the back-panel head, or the back-panel shoes;
- missing, extra, fused, duplicated, or distorted anatomy;
- different identities, ages, proportions, hairstyles, outfits, colors, accessories, lighting, or render styles between panels;
- incorrectly mirrored asymmetric details;
- added or missing props, weapons, logos, or accessories;
- dynamic poses, wide-angle distortion, duplicate characters within a panel, dramatic backgrounds, text, labels, captions, decorative borders, and watermarks.

