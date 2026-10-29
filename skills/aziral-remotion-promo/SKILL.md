---
name: aziral-remotion-promo
description: Create localized product promos in Remotion with RU/EN/KK copy, aspect-ratio adaptation, frame-based storyboards, and local frame review. Use for app demos and motion graphics with a separate Remotion project.
---

# AZIRAL Remotion Promo

Turn a product brief into an editable composition and the preview or video the user requested. This is an independent AZIRAL workflow for the Remotion engine.

## Establish the working project

- Inspect the existing project, its package scripts, lockfile, and installed Remotion packages before choosing commands or APIs. Resolve the project-local CLI and check its help and installed version. Use the existing package manager and version set.
- If no project exists, explain the required setup and use the current [official setup documentation](https://www.remotion.dev/docs/) within the user's authorized scope. This skill installs instructions, not the engine.
- Check the engine's [current license](https://www.remotion.dev/docs/license/pricing) for the intended use. A paid subscription, license purchase, or cloud-rendering service needs the user's approval. Prefer the existing local environment.

## Shape the promo

Read [Brief and storyboard](references/brief-and-storyboard.md) when preparing the story, translations, or multiple formats.

1. Extract the audience, product action, evidence, call to action, languages, duration, formats, and requested deliverable. Reuse supplied facts and assets. Label a fictional example or an unconfirmed claim rather than presenting it as a real product capability.
2. Build the story around one observable product action. Show the interface change that supports the claim. Give each scene a purpose, copy, visual subject, and frame interval.
3. Keep separate copy for Russian, English, and Kazakh. Translate meaning, then adjust line breaks and reading time for each language. Do not hard-code all languages into one crowded frame.
4. Adapt the composition for each requested ratio. Reposition the subject, reflow text, and adjust caption placement; scaling or cropping a finished landscape layout is not sufficient when it hides the action.

## Implement predictable timing

- Derive visual state from the render frame and composition FPS. Keep scene ranges explicit and use integer frames. Ensure the final scene ends at the composition duration.
- Use the installed Remotion version's supported timing and animation APIs. Avoid wall-clock timers, uncontrolled randomness, and animations that depend on when a browser happened to load.
- Wait for required fonts and media using the project's supported loading approach. Check Kazakh glyphs in the actual font: `Ә Ғ Қ Ң Ө Ұ Ү Һ І ә ғ қ ң ө ұ ү һ і`.
- Treat captions as part of the layout. Use timed speech captions for actual speech; use screen copy for a silent promo. Keep important UI, faces, and the call to action visible at the intended viewing size.
- Preserve an existing project's structure and design choices unless the brief calls for changes. Keep brand colors, copy, timing, and layout presets easy to edit.

## Preview, export, and inspect

Read [Local render and review](references/render-review.md) when running the composition or delivering an export.

- Open a working local preview as soon as a composition is available. Inspect the real composition, including its longest text variant and smallest requested format.
- Use the verified local CLI to list compositions, render review frames, and export when the requested deliverable includes a video. Check project-specific type or build diagnostics where applicable.
- Review frames at scene starts, readable holds, transition midpoints, and the final call to action. Check missing media, fallback glyphs, text overflow, crop, black frames, and caption overlap. Watch the exported file to check pacing and audio.
- If a tool or dependency blocks execution, report the exact blocker and the work completed. Do not describe a brief, composition source, preview, or still image as a rendered video.

Deliver the requested files with the engine version used, language and format variants, output dimensions, FPS, duration, and a short account of what was actually inspected.
