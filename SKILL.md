---
name: build-character-sheet-prompt
description: "Analyze an attached full-body person or character reference image and write a production-ready English prompt for Nano Banana Pro, FLUX, or Midjourney that creates a consistent four-panel character sheet: a face-excluded front view framed from the base of the neck to the shoes, an exact 90-degree head-to-toe side view, a complete head-to-toe back view, and a close-up face portrait. Use for requests such as 캐릭터 시트 프롬프트, 인물 설정 시트, 4면 캐릭터 레퍼런스, 측면 전신, 의상 정면과 후면, 얼굴 클로즈업, or converting a character image into a reusable image-generation prompt."
---

# Build Character Sheet Prompt

Create a prompt from the supplied visual reference; do not generate an image unless the user separately asks for image generation.

## Workflow

1. Confirm that at least one usable character image is available in the conversation or workspace. If it is missing, ask the user to attach it and stop.
2. Inspect the image closely with the available vision capability. Base all concrete details on the image. Describe apparent ethnicity, gender presentation, and age only as visual impressions, not verified facts.
3. Read [references/four-panel-spec.md](references/four-panel-spec.md) completely and apply every mandatory layout, analysis, preservation, and output rule.
4. Translate the visual evidence into precise production language. Cover identity, proportions, hair, face, skin, every garment layer, footwear, materials, colors, props, weapons, and accessories.
5. For details hidden in the reference, use the simplest visually consistent continuation. Do not invent prominent new design elements, logos, weapons, or accessories.
6. Check the final prompt against the checklist below before answering.

## Framing Priority

- Treat the left panel as an intentional **front outfit/body reference**, not a conventional full-body portrait. Start the frame at the base of the neck and exclude the complete head, face, hair, ears, and chin.
- Preserve the collar, shoulder line, both hands, both legs, and both shoes in the left panel. Never hide a generated face with a mask, blur, shadow, blank head, or mannequin head.
- Show the second panel as an exact 90-degree full-body side profile from the top of the head to the soles. Forbid a three-quarter angle, torso twist, or turn toward the camera.
- Show the third panel from the top of the head to the soles, viewed directly from the back, without cropping.
- Use the fourth panel for the same character's complete facial identity and hair details.
- If instructions conflict, these panel-specific framing rules override generic phrases such as "full-body front view" or "head to toe."

## Final Check

Verify that the output:

- contains a single English image-generation prompt in one clean code block;
- contains no placeholders or unfilled brackets;
- explicitly states the mandatory front, exact 90-degree side, back, and portrait panel framing;
- makes identity, proportions, clothing construction, colors, accessories, lighting, and rendering identical across all panels;
- places the strongest preservation and negative constraints near the bottom of the English prompt;
- uses a neutral light grey studio background and soft studio product lighting with subtle foot contact shadows;
- ends with only a concise two- or three-sentence Korean summary after the code block.

