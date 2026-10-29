# Brief and storyboard

Use this reference to turn a product idea into scene decisions before implementing the composition. Adapt the three-scene planning pattern below to the actual product.

## Minimum useful brief

Record the product, audience, intended action, factual claim, supporting asset or interface state, call to action, requested languages, formats, duration, and deliverable. Missing noncritical details can remain explicitly marked assumptions. Ask for a missing fact when inventing it would change the story.

The example JSON is planning data. It is not a Remotion configuration file or ready-made input props. Map the fields deliberately into the composition you build.

## A story that shows something

Start with the audience's situation, show one product action, then give a clear next step. The example uses three scenes at 30 FPS:

| Scene | Start frame | End frame, exclusive | Visible purpose |
| --- | ---: | ---: | --- |
| Idea | 0 | 90 | Show the idea the viewer wants to keep |
| Action | 90 | 240 | Show a note being added and found |
| Next step | 240 | 360 | Hold a readable call to action |

These are editable example timings. For other durations, choose the reading and demonstration time first, then convert seconds to integer frames. Use half-open intervals `[start, end)` so adjacent scenes share a boundary without adding an extra frame.

A scene record should answer: what changes on screen, which words explain it, what proof is visible, and where the next scene begins. A transition may overlap scenes; it must not silently shorten the intended reading hold.

## Language decisions

Keep language variants separate from visual structure. Use locale identifiers `ru`, `en`, and `kk`; preserve names and approved product terminology. Check translated calls to action as carefully as headlines.

Longer text needs space or time. Prefer a shorter, accurate sentence or a different line break before reducing the font. Verify the actual rendered font, particularly Kazakh-specific letters and mixed Latin/Cyrillic product names.

If narration exists, align captions to that narration. If a promo is silent, use concise on-screen copy and describe it as such. Avoid fabricating quotes, reviews, usage statistics, or product outcomes to fill a scene.

## Format decisions

Example presets are 1080 x 1920, 1920 x 1080, and 1080 x 1080. They are design targets rather than platform guarantees.

For each ratio, decide the subject's position, text column width, UI crop, caption position, and call-to-action area. A portrait composition may stack the headline above the product view while a landscape version places them side by side. Recheck the action after reframing: the button, result, and text must remain visible.

Preview at a realistic display size, including roughly phone-width playback. Check actual platform overlays when the destination is known. A fixed generic safe margin does not establish that text is clear of every platform's controls.
