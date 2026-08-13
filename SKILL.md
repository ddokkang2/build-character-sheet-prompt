---
name: build-character-sheet-prompt
description: "Analyze an attached full-body person or character reference image and write a production-ready English prompt for Nano Banana Pro, FLUX, or Midjourney using one of two consistent character-sheet layouts: a default three-panel layout with a face-excluded front neck-to-toe view, complete back view, and close-up portrait; or an optional four-panel layout that adds an exact 90-degree head-to-toe side view. Use for requests such as 캐릭터 시트 프롬프트, 인물 설정 시트, 3패널, 4패널, 3면 또는 4면 캐릭터 레퍼런스, 측면 전신, 의상 정면과 후면, 얼굴 클로즈업, or converting a character image into a reusable image-generation prompt."
---

# Build Character Sheet Prompt

Create a prompt from the supplied visual reference; do not generate an image unless the user separately asks for image generation.

## Workflow

1. Confirm that at least one usable character image is available in the conversation or workspace. If it is missing, ask the user to attach it and stop.
2. Inspect the image closely with the available vision capability. Base all concrete details on the image. Describe apparent ethnicity, gender presentation, and age only as visual impressions, not verified facts.
3. Select exactly one layout using the rules below. Do not combine panel orders from both modes.
4. Read the selected reference file completely and apply every mandatory layout, analysis, preservation, and output rule.
5. Translate the visual evidence into precise production language. Cover identity, proportions, hair, face, skin, every garment layer, footwear, materials, colors, props, weapons, and accessories.
6. For details hidden in the reference, use the simplest visually consistent continuation. Do not invent prominent new design elements, logos, weapons, or accessories.
7. Check the final prompt against the checklist below before answering.

## Layout Selection

- Use the **default three-panel mode** when the user asks for a character sheet without specifying a panel count, or explicitly requests three panels. Read [references/three-panel-spec.md](references/three-panel-spec.md) only.
- Use the **optional four-panel mode** when the user explicitly requests four panels, a side-view panel, 측면 포함, 측면 전신, or an exact 90-degree profile. Read [references/four-panel-spec.md](references/four-panel-spec.md) only.
- If the user asks for both versions, produce the three-panel prompt first and the four-panel prompt second, clearly separated, while preserving all shared character details. Otherwise output only the selected layout.

## Framing Priority

- Treat the left panel as an intentional **front outfit/body reference**, not a conventional full-body portrait. Start the frame at the base of the neck and exclude the complete head, face, hair, ears, and chin.
- Preserve the collar, shoulder line, both hands, both legs, and both shoes in the left panel. Never hide a generated face with a mask, blur, shadow, blank head, or mannequin head.
- In three-panel mode, use this order: face-excluded front neck-to-toe view, complete back view, close-up face portrait.
- In four-panel mode, insert an exact 90-degree full-body side profile between the front and back panels. Forbid a three-quarter angle, torso twist, or turn toward the camera.
- If instructions conflict, these panel-specific framing rules override generic phrases such as "full-body front view" or "head to toe."

## Final Check

Verify that the output:

- contains a single English image-generation prompt in one clean code block;
- contains no placeholders or unfilled brackets;
- explicitly states every mandatory panel and the correct order for the selected layout;
- makes identity, proportions, clothing construction, colors, accessories, lighting, and rendering identical across all panels;
- places the strongest preservation and negative constraints near the bottom of the English prompt;
- uses a neutral light grey studio background and soft studio product lighting with subtle foot contact shadows;
- ends with only a concise two- or three-sentence Korean summary after the code block.

