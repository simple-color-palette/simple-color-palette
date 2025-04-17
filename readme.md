# Simple Color Palette

> A minimal JSON-based file format for defining color palettes

It's designed for interoperability, clarity, and ease of use.

**[Feedback wanted on the specification](https://github.com/simple-color-palette/spec)**

> [!CAUTION]
> Work in progress.

## Example

`Favorites.color-palette`:

```json
{
	"name": "Favorites",
	"colors": [
		{
			"name": "Hot Pink",
			"components": [1, 0.1274, 0.418]
		},
		{
			"components": [0.592, 0.278, 0.996, 0.9]
		}
	]
}
```

## Contents

- [Specification](https://github.com/simple-color-palette/spec)
- [FAQ](https://github.com/simple-color-palette/spec#faq)

## Implementations

- [JavaScript](https://github.com/simple-color-palette/javascript-package)
- [Swift](https://github.com/simple-color-palette/SimpleColorPaletteSwift)
- [Rust](https://github.com/simple-color-palette/rust-package)

## Apps

- [Simple Color Palette](https://sindresorhus.com/simple-color-palette) - macOS and iOS app to view, create, and edit palettes in this format.
- [System Color Picker](https://sindresorhus.com/system-color-picker) - macOS app that supports importing palettes in this format.

## Packages

- [ColorPaletteCodable](https://github.com/dagronf/ColorPaletteCodable) - A color palette converter which supports this format.

## Why another format?

Existing color palette formats have limitations:

- Adobe Color (.aco, .ase) - Proprietary binary formats tied to Adobe products
- Sketch (.sketchpalette) - JSON-based but specific to Sketch app
- NSColorList (.clr) - macOS only, binary format
- GIMP/Inkscape (.gpl) - Text-based but limited to 8-bit RGB values

This format addresses these issues by being:

1. Open - JSON-based, human-readable, and freely implementable
1. Modern - Supports HDR colors through extended linear sRGB
1. Simple - Minimal structure with just the essential fields
1. Portable - Not tied to any specific app or platform
1. Precise - Uses raw linear values to avoid gamma ambiguity
