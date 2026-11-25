# sci-fig-editor

**Independent free alternative to cell_su7. Convert scientific figures to editable PPT/Illustrator without paid credits. Free, local-first image-to-editable-vector reconstruction**. Exports editable PowerPoint / SVG, with optional local OCR and opt-in third-party AI. This is an independent MIT-licensed project inspired by [`yrui-cmd/cell_su7`](https://github.com/yrui-cmd/cell_su7), and is not affiliated with the original author or paid image-recognition provider.

**Current release:** 4.2.1. Local precision tracing, perceptual color reconstruction, basic geometry/object detection, visual editing and optional OCR. This version does **not** promise pixel-perfect or semantically complete restoration; automatically recognized text requires proofreading.

### Quick start (Windows)

```powershell
py -3 -m pip install -r requirements.txt
py -3 app.py
```

```powershell
py -3 -m pip install -r requirements-optional.txt
py -3 app.py examples/demo_scientific.png -o output.pptx --ocr --ocr-lang eng --ocr-layout line --backend precision --colors 32 --color-mode perceptual --structure-mode objects
```

Offline OCR requires an installed Tesseract executable and language data. `requirements-ai.txt` is optional and needed only for explicitly chosen cloud integrations. **No API key or paid call is needed for core vector reconstruction.**

### Examples and data policy

The bundled `examples/diagram_raster.png` and `examples/demo_scientific.png` are demonstration fixtures created for the project. Previously used third-party/user-supplied biomedical illustrations and generated results have been omitted from this public release because redistribution rights have not been established. Historical benchmark scores cited in the archived documentation are not reproducible from the new bundled fixture. Benchmark against your own input files.

### Features

- Free offline precision vector tracing with color-aware segmentation and editable SVG/PPTX geometry.
- Optional geometric object/scene metadata and visual canvas editing.
- Local OCR (Tesseract), editable text frames and inpainting. OCR results may be inaccurate.
- Optional configured AI providers (including DeepSeek OCR adapter); API usage may be billed by your provider.
- Quality reports and regression tests.

### Security and provenance

API keys are not included. Keep `.env`, tokens, exported user images and generated reports outside version control. Please review the privacy policy of a third-party AI provider before uploading images. The independent code is MIT-licensed; see [THIRD_PARTY.md](THIRD_PARTY.md).

### More documentation

See [`docs/`](docs/) for editor, OCR, structure-aware tracing and debugging details. The historical changelog is in [CHANGELOG.md](CHANGELOG.md). For a guided publish workflow, see [PUBLISHING.md](PUBLISHING.md).
