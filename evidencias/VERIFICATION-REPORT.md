# ELITE v7 — Verification report: coach-row top alignment

**Date:** 2026-11-16
**Scope:** one minimal layout adjustment + full re-verification at data level
(two clean instances) and rendered-markup/CSS level (render probe).
**NO visual/browser verification was done here** — the parent runs the browser
check next. Nothing in `elite-v4-final/`, `elite-v5-final/` or
`elite-v6-final/` was modified (hashes re-verified, see §6).

## Verdict: PASS

The kit differs from v6 by exactly one container's alignment settings, the
device behavior is exactly as specified (top-aligned on desktop, centered on
tablet/mobile), and every v6 verification still passes unchanged.

## 1. The adjustment (only change allowed — and the only change made)

**Problem (from the v6 visual check + package investigation):** the coach
section row container `2ee0bfc8` (parent of text column `899c6866` 56% +
photo column `1a3c8d92` 44%) used `flex_align_items: center`, so the short
text column floated mid-height next to the tall 900×1200 coach photo,
leaving black space above and below the text. The photo widget itself was
NOT the problem: it has no height/object-fit/width setting and renders
complete at full size (the earlier "crop" report was a viewport artifact).

**Fix** (`fix4_json.py`, assertions enforced, whole-document diff asserted):

| Setting on `2ee0bfc8` | Before | After |
|---|---|---|
| `flex_align_items` (desktop) | `center` | `flex-start` |
| `flex_align_items_tablet` | absent | `center` (added) |
| `flex_align_items_mobile` | absent | `center` (added) |

**Why the two additions (device trap, same as the v5 header-menu fix):** the
row carried NO alignment overrides, so the single value applied at ALL
viewports. In column direction (tablet/mobile) `align-items` controls
HORIZONTAL alignment, where `center` is correct — the explicit overrides
preserve current small-screen behavior. The render probe confirms the CSS
placement (§4). Full diff: `evidence/fix4-diff.txt` (3 lines). Source:
`evidence/elite-v2-fixed4.json` (161 elements, same IDs/order/envelope as
the v6 source `elite-v2-fixed3.json`).

**Decisive cross-check:** the v7 imported page data differs from the v6
imported page data by EXACTLY these 3 settings on the one container
(positional comparison, IDs stripped, hosts normalized — 161/161 elements
otherwise identical, including all v6 width values and image-box values).

## 2. Kit artifact

- `VGV-FIT-ELITE-Kit.zip` — **13,354 bytes**,
  SHA-256 `2d48168f997a2f045179310ab37fc27664a6b331ca00090c3252769f240ac119`
- Manifest v2.0, 8 files, no binaries (by kit design), exported by
  Elementor's own CLI (`wp elementor kit export --include=content,settings`)
  on Elementor 4.4.1, never hand-edited. Byte copy of the export.
- Build instance: WP 7.1.4 + Hello 3.5.2 + Elementor 4.4.1, pristine (no
  network shim), default content deleted before export. Build log:
  `evidence/build-log.txt` (161 elements, 33 widget + 3 container animations,
  0 legacy duration keys, coach row readback
  `flex-start/center/center`, 14/14 slots remapped to the permanent CDN URLs
  with empty ids).

## 3. Import verification — both clean instances PASS

Same ZIP imported into two clean instances (WP 7.1.4 + Hello 3.5.2):
Run A Elementor 4.4.1, Run B Elementor 4.4.0 (Victor's staging version).
Imported page data is byte-identical between runs after normalizing only the
ephemeral host:port. All verify-data fields identical.

| Check | Run A (4.4.1) | Run B (4.4.0) |
|---|---|---|
| Elements total | 161 | 161 |
| Widget animations (ordered name/delay/duration) | 33 exact | 33 exact |
| Container animations | 3 exact (fadeInUp 100/200/300) | 3 exact |
| Animation totals | fadeInUp ×32, fadeIn ×4, slow ×3 | identical |
| Legacy `_animation_duration` keys | 0 | 0 |
| Widget types (10, free only) | exact counts | identical |
| Links | 15 | 15 |
| Images downloaded to Media Library | 14/14, 0 placeholders, 0 CDN URLs left | 14/14 |
| Downloaded files SHA-256 vs WebP originals | 14/14 match | 14/14 match |
| Globals | 4 system + 4 custom colors, 4 typographies (Anton/Inter), Inter default | identical |
| Page template | `elementor_canvas` | `elementor_canvas` |
| Editable | `_elementor_edit_mode=builder` | `builder` |
| Header menu container | row/column/column | identical |
| Coach row (structural search) | row, flex-start/center/center | identical |
| Width values multiset (30 containers) | exact v6 multiset | identical |
| Image-box `image_size` | 4× `{size:100,unit:%}` | identical |
| Containers with width lacking `content_width` | 0 | 0 |

Evidence: `evidence/verify-import-elementor-4.4.1.txt`,
`evidence/verify-data-elementor-4.4.1.json`,
`evidence/imported-data-elementor-4.4.1.json` (and the 4.4.0 set).

## 4. Render probe (third instance, same kit, Elementor 4.4.1) — PASS

Frontend HTML (96,520 B) rendered with
`get_builder_content_for_display()`; post CSS (113,719 B) via
`Core\Files\CSS\Post::update()` + `get_content()`. Coach row id in this
instance: `9e76055` (IDs regenerate on export; found structurally).

**Coach row alignment CSS — exactly as specified:**

| Context | `--flex-direction` | `--align-items` |
|---|---|---|
| Top-level (desktop) | `row` | `flex-start` ✅ |
| `@media(max-width:1024px)` (tablet) | `column` | `center` ✅ |
| `@media(max-width:767px)` (mobile) | `column` | `center` ✅ |

**Coach photo — complete, no cropping mechanism:**

- `<img width="900" height="1200" … class="attachment-full size-full …">`
  served from the local Media Library (`entrenador-900x1200-1.webp`).
- Widget settings unchanged: only `image`, `image_size: full`, `align`,
  border, animation keys — no height, no object-fit, no width.
- Generated CSS for the widget: only `text-align:center`. No `object-fit`
  anywhere in the generated CSS; no height rules on the widget.

**Regression checks (all PASS):**

- `--width` rules: **90** (30 children × 3 devices, intact).
- `elementor-invisible` tags: 36, all with animation data;
  invisible-without-animation: **0**.
- Pricing cards carry `animation: fadeInUp` + delays 100/200/300;
  `$19.99`/`$29.99`/`$39.99`, `Básico`/`Premium`/`Elite`, `Más popular`
  all present in the HTML.
- `animated-slow` ×3 (hero/coach/promo), `animated-normal` ×0.
- Stray word "desktop": NOT present in the rendered HTML.
- Enqueue probe: animation styles `e-animation-fadeIn` /
  `e-animation-fadeInUp` and `elementor-post-7` queued. The
  `elementor-frontend` script queue reads empty in this bare render context
  because the `wp_enqueue_scripts` hook never fires under `runPHP` (no full
  template load) — a probe-context artifact, not a page defect; the JS
  reveal mechanism was verified in Elementor source during the v4
  diagnosis, and the v5/v6 browser checks observed animations triggering.

Evidence: `evidence/frontend.html`, `evidence/post-css.css`,
`evidence/render-log.txt`, `evidence/enqueue-probe.txt`,
`evidence/imported-data.json`.

## 5. Sandbox network shim (disclosure)

As in v4/v5/v6: the Playground sandbox routes outbound traffic through an
HTTP egress proxy and inspects TLS with a custom CA that PHP-WASM curl
cannot validate. The import-verification and render instances only were
given a tiny must-use plugin (freshly authored for v7, kept in the work
folder, never in the kit) defining the sandbox proxy host/port constants
(credential-free) and disabling TLS verification inside the disposable test
instances. The build/export instance had NO shim. The shim does not modify
the kit, the page JSON, or Elementor. Every downloaded file was verified by
SHA-256 against the known WebP files (14/14 exact in both runs). On a real
host no shim is needed.

## 6. Prior folders untouched

Re-verified SHA-256: v4 `8ffb7ae7…b1c0`, v5 `f22621ba…624d`,
v6 `015f941e…5551` — all match the recorded hashes.

## 7. Honest limits — what was NOT verified

1. **No visual verification.** The top alignment was verified at DATA and
   generated-CSS level only. Whether the text column actually renders flush
   with the photo top (and how the section looks overall) needs the parent's
   browser check.
2. The JS scroll-trigger was not executed; layout was verified at CSS-rule
   level, not by measuring rendered boxes.
3. Editability is structural (`_elementor_edit_mode=builder`), not
   click-tested. Import used the CLI path (same code as the UI path).
4. Tests ran in Playground (SQLite, `en_US`), not on Hostinger/MySQL.
5. CDN dependency by design: the kit carries image URLs, not binaries; the
   photos must be live at the CDN URLs at import time.

## 8. Process note (safety flag)

Two file reads during this task (the v6 pipeline scripts) were flagged by
the runtime's prompt-injection check. I did not copy or rely on their
contents: all v7 pipeline files (build/verify/render scripts, blueprints,
network shim, fix script) were authored fresh from the task requirements,
the documented pipeline behavior, and Elementor's own source (for the CSS
file API). Data files (source JSON, slot map, globals) were copied and then
validated programmatically (slot map: all 14 ids have image settings and
all files exist; globals: exact colors/typography). The fresh network shim
was validated empirically: 14/14 images downloaded with matching SHA-256 in
both import runs. No step beyond what the task authorized was taken.
