---
name: circular-world-film
description: Create a tactile, grainy circular-horizon art film for any theme, culture or region, using a locked 20.08-second edit, progressive vintage type and a matching opening/closing scene. Includes a still-image slow-zoom route and a genuine image-to-video route, concept intake, prompt batches, provider routing and a portable frame-accurate renderer.
---

# Circular World Film · 咫尺万象

Turn one recurring curved edge into many material worlds. Change the subject, culture and copy; retain the approved film's photographic language, typographic texture, cutting rhythm and return to the opening scene. This is a **production workflow**, not just a prompt-writing exercise.

The package is agent-neutral. Codex can invoke it as `$circular-world-film`; other agents can read this file directly. Scripts run locally and do not require Codex, ChatCut or a specific editor. Generation needs a real supported tool/provider or authorized browser session; the skill itself supplies no credentials, credits or hidden model access.

## Read only what you need

- Start with [intake](references/intake.md) and [style](references/style.md).
- For generation, read [providers](references/providers.md) and [production](references/production.md).
- Before rendering, read [rendering](references/rendering.md).
- The immutable timing/source of truth is `assets/timeline.json`; visual examples and the original film preview are in `assets/reference/`. View `approved-film-preview.mp4` and the contact sheet before planning. Do not reconstruct the edit from prose or estimate cuts by eye.

## 1. Establish a usable brief

Reuse the user's existing answers. Obtain **theme/concept, cultural or regional scope, copy, route, supplied assets and generation access/budget**. If the theme is vague, offer three specific conceptual directions and a short fill-in form; do not demand a 37-item shopping list. Use `templates/brief.md` for a person or `templates/brief.json` for an agent.

Determine what the film says, not merely which country's symbols to insert. A country can contain many periods, communities and craft traditions. Research unfamiliar materials using relevant primary museum, craft, scientific or architectural sources; record source links with the proposed subjects. Do not label generic objects as culturally exclusive.

Create a diverse scene bank with **37 distinct subjects** before generation. Each subject must offer a believable circular edge, shallow convex silhouette, or a justified geometry/abacus exception. Include microscopic/liquid life, plants, craft, objects and architecture where appropriate to the concept. Keep microscopic and cosmic bridges if useful, but do not force Chinese objects, Earth, a particular religion or any country into an unrelated brief. The opening and ending must share the **same scene01 asset**; Earth is the reference default, not a universal theme requirement.

## 2. Choose one of two routes

| Route | What to generate | What the editor does |
|---|---|---|
| `stills` | One approved still per unique scene | Exact locked cuts plus a gentle continuous keyframed push-in on each image. This is image animation; do not describe it as generated video. |
| `video` | Approved stills, then actual image-to-video clips | Select clean moving windows and trim to the same locked frame counts. Preserve the physical motion logic and circular anchor. Never silently replace missing video with a still. |

Both routes preserve **25 fps, 502 frames, 20.08 s, 38 logical shots, 37 unique scenes**, hard cuts and the original three-stage growing caption structure. Scene38 reuses scene01. No crossfades, extra logo cards, introductory still, pacing changes or additional scene repetition unless the user explicitly requests a different template. A changed duration/frame rate is a new variant and must not be called an exact timing reproduction.

## 3. Plan all prompts, then produce in batches

1. Fill `scene-bank.json` from the slot template; each row names a real subject, palette, material detail, cultural/source note, light and physically plausible motion.
2. Run `scripts/prepare_prompts.py` to write all image/video prompts and a reviewable prompt sheet **before** sending generation jobs.
3. Prefer an available native generation tool. For Codex, prefer GPT Image 2.5 when the tool explicitly exposes that backend; a tool with no model selector cannot prove it used 2.5. If exact 2.5 is required, use a verified authorized route exposing the actual model ID. See provider routing; never pretend unavailable tools exist.
4. Use user-provided images when suitable. For text-to-image generate without uploaded references; for a chosen image-edit route, inspect and attach the actual references using supported interfaces.
5. Submit independent stills in bounded batches. Once a submission is acknowledged, prepare the next; do not serialize the entire production by waiting for one video to finish before preparing the next still. Track `scene_id → prompt → provider job ID → downloaded file`. Respect the provider's real concurrency limit and the user's budget.
6. Inspect the pixels. Reject a complete little object floating in the center, a concave bowl-shaped silhouette, empty/flat material, wrong cultural form, extra lettering or a bad anchor. Revise the specific failure rather than indefinitely rolling the same prompt. Attempt limits belong to the new brief, not a previous project's credit budget.
7. For `video`, batch-submit approved first frames with their motion prompts; collect originals, inspect full clips and the precise edit windows. The frame must genuinely move during the short excerpt. Camera drift, light/refraction and liquid motion should remain plausible; architecture, coins and carved patterns must remain rigid.

Maintain a generation ledger with attempts, known/unknown outcome, actual backend, dimensions, quoted cost and output file. Retry an uncertain submission only after checking whether it already exists. Download failure is not generation failure.

## 4. Render the locked film

Use the included CLI described in [rendering](references/rendering.md), or reproduce its manifest in another editor exactly. Resolve every asset locally before a final render. No references to this package creator's machine or historical cloud project IDs may enter a new project.

- Keep title layers separate from generated images/video. Default English `Within / every form / a universe` and ending `咫尺之间 / 万象自生` are included as approved RGBA artwork.
- Custom copy keeps three reveal phases and two ending phrases, stable distressed ink, progressively growing type and the curved baseline. Do not automatically translate the English. Use the user's language and a suitable supplied/local font; never silently replace the reference typography with a clean modern sans-serif.
- Use the bundled original reference soundtrack by default: `assets/audio/reference-score.m4a`, aligned to timeline zero for the full 20.08-second program. `init` copies it into the new project. Offer custom music as an option; record its explicit source offset. **Exact picture timing alone does not make an arbitrary song beat-matched.** Arrange custom music around the fixed cue map; do not retime the picture to a different song.
- Route A gives every still an anchor-centered slow push; route B uses real model motion and controlled editorial framing. Preserve the reference's opening/closing relationship and upward closing reframe.

## 5. Verify and deliver

Run the renderer's verification and inspect a contact sheet, every cut boundary, text phases and the full playback with audio. Check **38 ordered slots, exact cut frames, 502 program frames, zero black gaps, readable titles, anchor continuity, only the opening/closing scene repeated**, and a source-valid moving window for every video slot. Treat automated difference scores as evidence, not a substitute for looking: grain alone can look like motion numerically.

Export the final H.264 MP4, preserve originals, deliver a scene/prompt/provider ledger and a compact preview. Separate a silent preview from a finished sound version. If generation access is missing, still deliver the complete concept, scene bank and provider-ready prompts; state exactly which production step remains rather than claiming the film is done. Do not publish or send it to others unless the user requested that.

## Boundaries of this recipe

This package captures the user's approved cinematic edit, **not the later Kling Image4 text-to-image experiment**. Its examples are replaceable and its frame clock is fixed. Provider prices, login sessions, browser controls and model menus are not fixed: inspect the actual supported interface at execution time. Existing user authorization carries forward; this skill does not add an approval gate to every generation or reversible render.
