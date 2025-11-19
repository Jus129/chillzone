# Wheels India ACPR Line Dashboard Concepts

This document presents four dark, Grafana-inspired dashboard concepts for the Wheels India ACPR line and AutoSpin machine scope. Each concept maintains the required header controls, a five-card KPI strip with four historical comparison columns (Last shift, -2 shift, -3 shift, 3-shift avg) that use red/yellow/green (or red/green where binary) states, left-panel recommended actions, right-panel alert analytics, and interactive drilldowns.

## Shared KPI Strip Behavior

- **Column order:** `Last shift | Last-2 | Last-3 | 3-shift Avg`.
- **Color semantics:**
  - Green = on target, Yellow = within range but trending away, Red = out of range.
  - Binary KPIs (e.g., Scrap OK/Not OK) use only green/red.
- **Signal clarity:** Each card shows a multi-column grid with mini labels, icons, and textual thresholds, so operators immediately see where attention is needed.
- **Drill-down cues:** Cards glow subtly on hover and display tooltip text (“Click for detailed OEE breakdown”).

## Concept 1 – "Segmented Spine"

### Header
- Full-width bar with left-aligned title lockup and right-aligned segmented filters (date, shift, machine scope) in pill controls inspired by the reference images.

### KPI Strip
- Five spine-aligned cards with bold glyphs and a four-column matrix under the main metric.
- Columns appear as vertically stacked mini tiles to echo the reference layout, each showing value + color-coded background.
- `Target vs actual` indicator shown as a thin bar beneath the grid for OEE, scrap.
- Cards separated by a thin industrial divider to maintain the rigid structure from the screenshots.

### Body Layout
- **Left panel:** Recommended actions list on a carbon fiber background with filter chips and status pills.
- **Right panel:**
  - Category tiles arranged horizontally, each tile uses the same color logic to show severity within that category.
  - Waterfall chart + hourly loss table stacked below.

### Drilldowns
- Slide-over drawers triggered by OEE and UPDT cards; mimic data table modal style from the screenshots.

## Concept 2 – "Split Columns"

### Header
- Header split into two vertical bands: left for identity, right for filters stacked vertically (date picker over shift/machine) to echo the columnar references.

### KPI Strip
- Each card behaves like a mini column chart: column headers (“Last”, “-2”, “-3”, “Avg”) appear at the top, values shown in tall capsules.
- `Scrap` card includes arrow glyph + delta text near the last column to highlight change vs last shift.
- `UPDT` and `PDT` cards show micro tags for top causes/buckets underneath the column grid.

### Body Layout
- **Left panel:** Displays actions as collapsible accordions; each accordion header inherits the category color, and inside are bullet steps with icons.
- **Right panel:** Bars grouped by failure category with on-card micro KPIs. Shift loss chart uses stacked bars that align with the column motif.

### Drilldowns
- Pop-up modals resembling the reference tables, with shift filters pinned inside the modal header.

## Concept 3 – "Dual Track"

### Header
- Dark matte background with two horizontal tracks: top for title, bottom track for filters (date, shift, machine) with neon accent separators.

### KPI Strip
- Cards presented as dual-lane indicators: the top lane holds the main metric + trend sparkline; the bottom lane is a four-cell grid matching the provided color scheme.
- `UPS` card features a tiny stacked bar next to the main number plus major/minor labels under the grid.
- `OEE` card shows Availability/Performance/Quality badges next to the grid.

### Body Layout
- **Left panel:** Looks like a Kanban lane with filters pinned atop, cards with checklists, priority tags on the left edge, and status pills on the right.
- **Right panel:**
  - Category overview uses rectangular chips with embedded mini charts for UPDT and UPS contributions.
  - Loss breakdown uses a waterfall visualization with a metallic gradient background to accentuate drops.

### Drilldowns
- Secondary screens (full-height) slide in from the right, keeping the dual-track aesthetic.

## Concept 4 – "Stacked Modules"

### Header
- Modules stacked: top-level identity, middle-level filter row, bottom-level quick action buttons (e.g., “Open predictive maintenance”).

### KPI Strip
- Each card is a stack of modules: title row, metric row, column grid row, then context row (progress bar, tags, etc.).
- Column grid integrates faint gridlines mimicking the screenshot structure; each cell includes the numerical value plus a micro-indicator (▲/▼) if the trend is worsening.
- Binary measures (e.g., certain scrap thresholds) render only red/green backgrounds.

### Body Layout
- **Left panel:** Three-column action board grouped by category, with filters above; each card includes recommended actions as bullet items with icons.
- **Right panel:**
  - Category overview shown as stacked mini bar charts with clickable headers.
  - Performance & loss section combines a stacked bar with an adjacent table to reduce vertical scrolling.

### Drilldowns
- Modal panels replicate the grid-heavy reference tables, including sortable headers, colored status bars, and machine scope badges.

## Next Steps
Select the concept that best fits Wheels India’s expectations, then we can detail the chosen layout with higher fidelity mockups, component specifications, and data-binding rules for the predictive maintenance entry point.
