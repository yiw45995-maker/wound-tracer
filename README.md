Wound Tracer

A lightweight, browser-based tool for measuring wound / skin-lesion areas from
photographs and expressing them as a percentage of a baseline time point
(wound area ratio, % of baseline). It runs entirely in the browser — no
installation, no server, and (for image input) no internet connection required.
It is intended for wound-healing and skin-lesion studies in which a size
reference of known dimensions (a fixed-diameter coloured marker, or a ruler /
scale bar) is included in every photograph, so that measurements are calibrated
per image and are independent of camera-to-subject distance.

Features
Load a composite figure (a grid of group × time-point photos) or a single
photograph. Accepts PNG / JPG / WEBP directly; PDF via a built-in reader.
Define a group × time-point grid over a composite figure, then click a
cell to zoom in and measure one photo at a time.
Per-image spatial calibration from a known reference:
auto-detect a coloured circular marker of known diameter (one click detects
every marker of that colour and size across the figure), or
drag along a ruler / scale bar of known length ("Set scale").
Manual wound delineation by fitting an ellipse to the wound margin.
Automatic normalization of every time point to a chosen baseline
(baseline = 100%).
Export results as CSV, or copy a group's table for pasting into
GraphPad Prism.
Save / load the whole session (grid, calibration, all measurements) as a
JSON project file.

Requirements
Any modern web browser (Chrome, Edge, Firefox, or Safari). No installation.
Image input (PNG / JPG / WEBP) works fully offline.
PDF input loads a PDF reader from a CDN and therefore needs an internet
connection; if offline, export the figure as PNG and load that instead.

Usage
Open wound_tracer_app_v2(1).html in your browser (double-click the file).
Open image / PDF (or drag a file onto the window).
Layout — enter the column labels (groups) and row labels (every time
point present in the figure), the baseline row, and the marker diameter in
mm. Click Apply layout, then drag the grid frame to line it up with the
photos.
Scale — if the figure uses coloured markers, click "Click a coloured
dot → auto-scale all" and click one marker. If you use a ruler/scale bar,
set the scale inside each cell (step 6).
Click a cell to zoom into it.
Trace — drag over a wound to fit an ellipse; click to select; drag a
corner to resize or the middle to move; press 1–X to set the mouse
number; Del to remove. For a ruler, enter the real length of the span you
will drag in the "ruler/dot length" box and click Set scale (drag), then
drag along that span.
Read off the wound area ratio (% of baseline) table on the right;
Download CSV or Copy this group for Prism.
Save project periodically to keep your work.

Method summary (for reproducibility)
For each photograph, the spatial scale (mm per pixel) is derived from a
reference of known size present in that image (a marker of known diameter, or a
ruler graduation) and applied to that image only. The wound margin is delineated
manually by fitting an ellipse, and the enclosed area is converted to mm². For
each wound, the area at each time point is normalized to its own baseline value
and expressed as a percentage. A single, consistent wound-boundary criterion
should be applied across all images; measuring in duplicate and/or blinded to
group allocation is recommended.

Limitations
Measurements are operator-defined (manual tracing); reproducibility
depends on applying one consistent boundary rule and, ideally, blinding.
Wound area is approximated by an ellipse fit; for highly irregular wounds
this is an approximation.
For publication, measure the original-resolution photographs, not a
downsampled composite figure.
Automated colour detection of markers may miss markers whose colour overlaps
the wound or that are washed out; those cells can be calibrated manually.

Development note
This tool was developed with the assistance of an AI coding assistant
(Claude, Anthropic); the method, requirements, and testing were specified and
carried out by the author(s). Please check your target journal's policy on
disclosing AI assistance and adjust wording accordingly.
