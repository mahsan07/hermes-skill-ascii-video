# How Ascii Video Works

Convert video or audio into colored ASCII MP4 or GIF output.

![Detailed systems blueprint for Ascii Video](../assets/system-blueprint.png)

## Stages

### 1. Inspect duration resolution and audio

**Primary surface:** `Video or audio source`

Record the input, operation, observable output, and any decision that changes scope. Stop here if the output is missing, contradictory, or insufficient for the next stage.
### 2. Choose frame rate width and glyph palette

**Primary surface:** `Frame and beat sampler`

Record the input, operation, observable output, and any decision that changes scope. Stop here if the output is missing, contradictory, or insufficient for the next stage.
### 3. Render each frame as colored characters

**Primary surface:** `Color glyph renderer`

Record the input, operation, observable output, and any decision that changes scope. Stop here if the output is missing, contradictory, or insufficient for the next stage.
### 4. Synchronize frames with source timing

**Primary surface:** `FFmpeg encoder`

Record the input, operation, observable output, and any decision that changes scope. Stop here if the output is missing, contradictory, or insufficient for the next stage.
### 5. Encode MP4 or GIF with FFmpeg

**Primary surface:** `MP4 or GIF`

Record the input, operation, observable output, and any decision that changes scope. Stop here if the output is missing, contradictory, or insufficient for the next stage.
### 6. Inspect motion readability and file size

**Primary surface:** `MP4 or GIF`

Record the input, operation, observable output, and any decision that changes scope. Stop here if the output is missing, contradictory, or insufficient for the next stage.

## Failure handling

- **Authorization failure:** do not probe credentials or broaden access; report the missing authority.
- **Target ambiguity:** stop before mutation and request the minimum identifying information.
- **Tool or service failure:** retain error evidence, retry only safe transient failures, and cap retries.
- **Verification failure:** classify the run as incomplete even when the preceding operation returned success.

## Completion evidence

The handoff should contain the original request, inspection state, preview or plan, exact execution result, direct verification, and a final receipt naming limitations and withheld actions.
