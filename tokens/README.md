# Kital PRO Tokens

Current Figma snapshot: 258 local variables across six collections.

| Collection | Count | Purpose |
| --- | ---: | --- |
| 01 — Primitives | 36 | Source-derived palette/raw values |
| 02 — Semantic | 111 | Product/UI roles and component-facing semantics |
| 03 — Dimensions | 36 | Spacing, radius, control sizes, layout dimensions |
| 04 — Type Primitives | 24 | Font families, weights, sizes and line-height primitives |
| 05 — Type Semantic | 44 | Display/heading/body/label semantic typography |
| 06 — Motion | 7 | Functional duration/easing values |

Additional Figma styles:

- 11 Text Styles
- 3 Effect Styles
- 3 Grid Styles

## Dependency model

Preferred use:

`Primitive → Semantic → Component`

Examples:

```text
color/neutral/1000
  → action/primary/background
  → Button/Primary

color/feedback/error/*
  → field/border-error
  → Input/Text · Error

space/16
  → component padding / gap

radius/input = 15
  → field controls

radius/full
  → pill actions
```

## Important source-derived decisions

- Kital primary CTA in the actual product is black/pill, despite a historical generic button component using other colors.
- Coral remains a brand/focus/accent role rather than being forced into the primary CTA background.
- The onboarding coral→orange gradient is preserved as a source-derived identity exception.
- `radius/input = 15` preserves the actual Kital field geometry rather than rounding it to a generic 16.
- Success popup source tone and destructive CTA source tone were preserved instead of approximated.

## Typography

Historical Kital contains Avenir references plus Inter, Nunito and other fragmented font usage. Avenir is currently reported as unavailable/missing in Figma.

PRO systemization uses Inter + Nunito for the reusable layer while explicitly documenting the normalization. It does not claim the historical product used only those families.

## Implementation

Semantic token names are intended to map naturally to code-side custom properties/tokens, e.g.:

```text
action/primary/background → --action-primary-background
field/border-error        → --field-border-error
space/16                  → --space-16
radius/input              → --radius-input
radius/full               → --radius-full
size/control/lg           → --control-lg
```

The live Figma file remains the value authority; this repository documents the contract and snapshot.
