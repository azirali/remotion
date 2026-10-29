# Local render and review

Use the project's installed engine and CLI. The commands below illustrate documented Remotion command shapes; replace the entry point, composition ID, paths, and frame number with values verified in the project.

## Before running a command

Inspect package scripts and the lockfile. Confirm that the local CLI exists, identify the installed package version, and read its help. Prefer a project script or the local executable so a convenience command does not silently fetch a different engine version.

For a project with a local executable at `node_modules/.bin/remotion`, these are example command shapes:

```bash
./node_modules/.bin/remotion compositions src/index.ts
./node_modules/.bin/remotion still src/index.ts Promo out/review-060.png --frame=60
./node_modules/.bin/remotion render src/index.ts Promo out/promo.mp4
```

`src/index.ts`, `Promo`, frame `60`, and the output filenames are examples. Confirm the listed composition's FPS, duration, width, and height before rendering. Use a frame in its valid range. Do not overwrite a user's existing output without an appropriate recoverable copy or a different filename.

If the CLI, browser, or media dependency is missing, resolve the concrete setup requirement within the authorized task. Do not replace a local workflow with an unapproved paid renderer.

## Frame review

Choose samples from the actual timeline:

- The first visible frame of each scene and a frame during its readable hold.
- A transition midpoint where crop or transparency can hide an element.
- The longest headline or caption in each language.
- The final call-to-action hold and last intended visible frame.

Inspect the images, not only the render exit code. Check text clipping, replacement glyphs, aspect ratio, UI crop, media completeness, and whether captions cover the demonstrated action.

For video delivery, play the exported file. A set of stills cannot establish pacing, synchronized captions, or clean audio. Confirm that the delivered file has the intended dimensions, FPS, and duration using an available media inspection tool.

Fix a demonstrated issue, then repeat the affected samples or export. Once the relevant checks pass, deliver the files rather than running unrelated renders.

## Record what happened

Keep a compact result: installed engine version, real composition ID, input or props variant, output path, frame samples, format, FPS, duration, and remaining limitations. Distinguish a checked preview from a rendered and played export.

## Official command references

- [Composition listing](https://www.remotion.dev/docs/cli/compositions)
- [Still rendering and frame selection](https://www.remotion.dev/docs/cli/still)
- [Video rendering](https://www.remotion.dev/docs/cli/render)

Check the relevant current reference when a flag or API is not established by the project's installed CLI.
