---
name: wireframe-to-figma
description: Converts text descriptions, page briefs, tables, or images into a mid-fidelity wireframe written directly into a Figma file as editable frames — matching the HD Schools design language (dark canvas, white content column, orange section badges, right-side specifications panel). Use this skill whenever the user wants to turn a page brief, site structure, content outline, spreadsheet, or screenshot into a Figma wireframe — even if they say "make a wireframe", "sketch this in Figma", "lay out these sections in Figma", "turn this into a wireframe", or "can you wireframe this for me". Also triggers when the user pastes a list of page sections and asks to visualize them. Always use this skill when Figma MCP is connected and the user wants a wireframe output.
---

# Wireframe to Figma

Converts any user input (text, tables, images, screenshots) into a **mid-fidelity wireframe** written directly into a Figma file. All output must match the HD Schools reference design system exactly.

---

## Reference design system

Extracted from node `6202:45`, file `1YHshjU6JasefK78i3H479`. Every wireframe produced by this skill must use these exact values.

### Canvas structure
| Element | Value |
|---|---|
| Canvas bg | `#323131` |
| "WIREFRAME" label | 11px Inter Regular, white, uppercase, letter-spacing 1.68px, x=35 y=33 |
| Page title | 72px Inter Regular, white, tracking -3%, x=32 y=46 |
| Content column | 1060px wide, x=176, y=354, white bg |
| Spec panel bg | `#f4f4f4`, x=1485, w=430px |
| Section badges (orange) | 24px circle, fill `#ff6f00`, x=1246 |
| Spec badges (orange) | 22px circle, fill `#ff6f00`, x=1510 |
| Spec title | "Specifications", 16px Regular, `#030303`, x=1510 y=56, tracking -3% |
| Spec text | 13px Regular, `#030303`, x=1542, w=336px, line-height 1.55 |
| Spec divider | 0.5px `#d1d1d1`, w=370px, x=1510 |

### Typography — Inter only (cloud font, always available)
| Use | Size | Weight | Color | Tracking |
|---|---|---|---|---|
| Page title (canvas) | 72px | Regular | `#ffffff` | -3% |
| Section heading | 30px | Regular | `#030303` | -3% |
| Mission body | 35px | Medium | `#030303` | -3% |
| Why HD number | 30px | Medium | `#030303` / `#8b8b8b` | -3% |
| Why HD title | 25px | Medium | `#030303` | -3% |
| Stat number | 34px | Regular | `#030303` | -3% |
| Letter headline | 26px | Regular | `#030303` | -3% |
| News date | 12px | Medium | `#000000` | 0% |
| Nav link | 10px | Regular | `#8b8b8b` | 0% |
| Button / pill | 10–11px | Regular | varies | 0% |
| Caption / muted | 9–10px | Regular | `#8b8b8b` | 0% |
| Spec text | 13px | Regular | `#030303` | 0% |

### Color tokens
```
#030303  — primary text, filled pills, tag badges, CTA bg
#8b8b8b  — muted text, outlined pill stroke/text
#d9d9d9  — image placeholders, text bar stacks
#f3f3f3  — nav background
#2a2a2a  — footer background
#666666  — footer logo / link column label
#4d4d4d  — footer link bar fills
#b8b8b8  — stat grid hairline borders, why-HD row hairlines
#d1d1d1  — spec panel dividers
#ff6f00  — section badges (orange) — canvas left AND spec panel right
```

### Component library

#### Nav (h=56px, bg=#f3f3f3)
- Logo: 80×37px rect, fill `#666`, radius 2
- Links: 10px `#8b8b8b`, px=10 py=4, gap=4px between items
- CTA: bg `#030303`, white text 10px, px=14 py=6, radius=100px

#### Hero (h=560px, bg=#d9d9d9)
- Play circle: 74px ellipse, no fill, stroke `#8b8b8b` 1.5px, centered
- Label text: 11px muted, centered, opacity 0.7

#### Mission (white, px=32 py=40 gap=20)
- Body text: 35px Medium, width=W-64, line-height 140%
- Filled pills: bg `#030303`, white text 10px, px=12 py=5, radius=100
- Outlined pills: border 0.75px `#8b8b8b`, `#8b8b8b` text 10px, px=12 py=5, radius=100

#### Letter from founders (white, px=32 py=40 gap=32, horizontal)
- Left image: 420×300px, fill `#d9d9d9`, radius 4
- Right column (gap=16): eyebrow 10px muted → headline 26px → 4 bars [340,340,340,220]×9px → sig row (30px circle + 10px name) → outlined CTA pill

#### Stats grid (2 rows × 3 cols, width=996px)
- Each cell: 332×160px, px=20 pt=24 pb=20, gap=10 (vertical)
- Stat number: 34px Regular, tracking -3%
- 3 placeholder bars: [272, 195, 239]px × 9px, fill `#d9d9d9`, radius 2
- Borders: 0.5px `#b8b8b8` — top for row 2, left for cols 2 & 3

#### Why HD feature rows (3 items, px=32 py=40)
- Each row: horizontal, gap=32, py=28, width=W-64
- Image: 280×190px, fill `#d9d9d9`, radius 4
- Body: number 30px Medium → title 25px Medium → 3 bars [360,360,250]×9px
- Number color: `#030303` for first item, `#8b8b8b` for subsequent
- Hairline top border 0.5px `#b8b8b8` between rows (not on first)

#### News cards (3 columns, px=32 py=40 gap=24)
- Section header: 30px heading + "View all" outlined pill (right-aligned)
- Each card: vertical, width≈332px
  - Thumbnail: h=180px, fill `#d9d9d9`, radius=10
  - Tag badge: bg `#030303`, white 9px text, px=8 py=3, radius=4, x=7 y=155
  - Body: py=16 gap=8 — date 12px Medium + 3 bars [328,328,199]×9px

#### Footer (bg=#2a2a2a, px=32 py=40 gap=24)
- Grid row (gap=60): brand col (w=180) + 3 link cols (w=140 each)
- Brand: 72×14px rect fill `#666` + 2 tagline bars [140,95]px fill `#4d4d4d`
- Link col: 9px uppercase label `#666` + 3 bars [100,70,50]px fill `#4d4d4d`
- Divider: 0.5px `#4d4d4d`, w=996px
- Bottom: 9px copyright `#666` + 3×18px circles fill `#333`

---

## Step 1 — Parse user input

Accept any of these inputs:

**Text / bullet list** → identify section names and content → map to section types above.

**Spreadsheet / table** → each row = one data item → identify which section template it fits (stat grid, card grid, feature list).

**Image / screenshot** → use vision to identify layout, section types, text content, and hierarchy.

Build a section plan before writing any code:
```
Page: [page name]
Sections:
  1. nav — links: [...], cta: '...'
  2. hero — label: '...'
  3. mission — text: '...', filledPills: [...], outlinedPills: [...]
  4. letter — eyebrow: '...', headline: '...', sigName: '...'
  5. stats — title: '...', items: [{num:'...', label:'...'}, ...]
  6. feature — title: '...', items: [{n:'01', title:'...', body:'...'}, ...]
  7. news — title: '...', items: [{tag:'...', date:'...'}, ...]
  8. footer — cols: [{title:'...'}, ...], copyright: '...'
```

If a section type is unclear, choose the closest match. Never invent content — use gray bars for body text not provided by the user. Keep all heading/label text exactly as the user provided.

---

## Step 2 — Write spec descriptions

For each section, write a 1–2 sentence design spec in the voice of a senior product designer. These appear in the right-side Specifications panel.

**Good spec language:**
- "Navigation. Logo left, nav links centre, primary CTA right. Keep interactions minimal at this fidelity."
- "Hero / Opening animation. Full-screen placeholder communicates a video or animated intro. Sets the brand atmosphere before content begins."
- "Mission statement. 35px editorial text sets the brand voice. Filled pills highlight core pillars; outlined pills show supporting values."
- "Stats grid. 2×3 layout shows 6 key metrics without crowding. Hairline borders separate cells with minimal visual weight."
- "Feature rows. Numbered image-left / text-right rows communicate differentiators. Image placeholders to be replaced with photography."
- "News cards. 3-column grid with thumbnail, tag, date, and text lines. "View all" links to the full news index."
- "Footer. Dark background anchors the page. Logo + 3 link columns + divider + copyright."

---

## Step 3 — Write to Figma

Use `Figma:use_figma` with the user's `fileKey`. Always wrap in `async function run()` and end with `return run()`. Load both Inter styles first.

### Complete reusable code

```javascript
async function run() {
  await figma.loadFontAsync({ family: 'Inter', style: 'Regular' });
  await figma.loadFontAsync({ family: 'Inter', style: 'Medium' });

  var page = figma.currentPage;
  var NONE = [];
  var fill = function(c, a) { return [{ type: 'SOLID', color: c, opacity: a !== undefined ? a : 1 }]; };

  var C = {
    canvas:    { r:0.196, g:0.192, b:0.192 },
    white:     { r:1,     g:1,     b:1     },
    specBg:    { r:0.957, g:0.957, b:0.957 },
    specLine:  { r:0.820, g:0.820, b:0.820 },
    orange:    { r:1.0,   g:0.435, b:0.0   },
    black:     { r:0.012, g:0.012, b:0.012 },
    muted:     { r:0.545, g:0.545, b:0.545 },
    bars:      { r:0.851, g:0.851, b:0.851 },
    navBg:     { r:0.953, g:0.953, b:0.953 },
    footerBg:  { r:0.165, g:0.165, b:0.165 },
    footerEl:  { r:0.302, g:0.302, b:0.302 },
    footerMid: { r:0.400, g:0.400, b:0.400 },
    hairline:  { r:0.722, g:0.722, b:0.722 },
  };

  var W = 1060, CX = 176, CY = 354, SX = 1510, SW = 336, BADGE_X = 1246;
  var TOTAL_W = SX + SW + 64;

  function T(str, size, wt, color, parent, opts) {
    opts = opts || {};
    var t = figma.createText();
    t.characters = str;
    t.fontName = { family: 'Inter', style: wt >= 500 ? 'Medium' : 'Regular' };
    t.fontSize = size; t.fills = fill(color);
    if (opts.lh) t.lineHeight = opts.lh;
    if (opts.ls !== undefined) t.letterSpacing = { value: opts.ls, unit: 'PERCENT' };
    if (opts.w) { t.textAutoResize = 'HEIGHT'; t.resize(opts.w, t.height); }
    if (opts.align) t.textAlignHorizontal = opts.align;
    if (parent) parent.appendChild(t);
    return t;
  }

  function R(w, h, color, corner, parent) {
    var r = figma.createRectangle();
    r.resize(w, h); r.fills = fill(color);
    if (corner) r.cornerRadius = corner;
    if (parent) parent.appendChild(r);
    return r;
  }

  function BARS(widths, parent) {
    widths.forEach(function(w) {
      var r = figma.createRectangle();
      r.resize(w, 9); r.fills = fill(C.bars); r.cornerRadius = 2;
      parent.appendChild(r);
    });
  }

  function IMG(w, h, corner, parent) {
    var f = figma.createFrame();
    f.resize(w, h); f.fills = fill(C.bars);
    if (corner) f.cornerRadius = corner;
    f.layoutMode = 'NONE';
    if (parent) parent.appendChild(f);
    return f;
  }

  function VF(name, w, gap, pH, pV, bg, parent) {
    var f = figma.createFrame(); f.name = name;
    f.resize(w, 50); f.layoutMode = 'VERTICAL';
    f.primaryAxisSizingMode = 'AUTO'; f.counterAxisSizingMode = 'FIXED';
    f.itemSpacing = gap; f.paddingLeft = f.paddingRight = pH;
    f.paddingTop = f.paddingBottom = pV;
    f.fills = bg ? fill(bg) : NONE;
    if (parent) parent.appendChild(f);
    return f;
  }

  function HF(name, gap, parent) {
    var f = figma.createFrame(); f.name = name;
    f.layoutMode = 'HORIZONTAL'; f.primaryAxisSizingMode = 'AUTO';
    f.counterAxisSizingMode = 'AUTO'; f.itemSpacing = gap; f.fills = NONE;
    if (parent) parent.appendChild(f);
    return f;
  }

  function OUTBTN(label, parent) {
    var f = HF('btn', 0, null);
    f.paddingLeft = f.paddingRight = 16; f.paddingTop = f.paddingBottom = 7;
    f.cornerRadius = 100; f.fills = NONE;
    f.strokes = fill(C.muted); f.strokeWeight = 0.75; f.strokeAlign = 'INSIDE';
    T(label, 11, 400, C.muted, f, { ls: 0 });
    if (parent) parent.appendChild(f);
    return f;
  }

  // Canvas
  var canvas = figma.createFrame();
  canvas.name = PAGE_NAME + ' — Wireframe';
  canvas.resize(TOTAL_W, 6000); canvas.fills = fill(C.canvas);
  canvas.layoutMode = 'NONE'; canvas.clipsContent = false;
  page.appendChild(canvas);

  var specBgRect = R(SW + 64, 6000, C.specBg, 0, null);
  specBgRect.x = SX - 20; specBgRect.y = 0; canvas.appendChild(specBgRect);

  T('WIREFRAME', 11, 400, C.white, canvas, { ls: 1.68 }).x = 35;
  T('WIREFRAME', 11, 400, C.white, canvas, { ls: 1.68 });
  var wfl = T('WIREFRAME', 11, 400, C.white, null, { ls: 1.68 }); wfl.x = 35; wfl.y = 33; canvas.appendChild(wfl);
  var wft = T(PAGE_NAME, 72, 400, C.white, null, { ls: -3 }); wft.x = 32; wft.y = 46; canvas.appendChild(wft);
  var spT = T('Specifications', 16, 400, C.black, null, { ls: -3 }); spT.x = SX; spT.y = 56; canvas.appendChild(spT);

  var cf = VF('content', W, 0, 0, 0, C.white, null);
  cf.x = CX; cf.y = CY; cf.clipsContent = false;
  canvas.appendChild(cf);

  var sY = 0, spY = 96, secN = 0;

  function badge(midY) {
    var g = figma.createFrame(); g.resize(24, 24);
    g.x = BADGE_X; g.y = CY + midY - 12;
    g.cornerRadius = 12; g.fills = fill(C.orange); g.layoutMode = 'NONE';
    var t = T(String(secN), 11, 500, C.white, g, { ls: 0 });
    t.textAlignHorizontal = 'CENTER'; t.textAutoResize = 'HEIGHT';
    t.resize(24, t.height); t.y = Math.max(0, Math.round((24 - t.height) / 2));
    canvas.appendChild(g);
  }

  function spec(text) {
    secN++;
    var sb = figma.createFrame(); sb.resize(22, 22); sb.x = SX; sb.y = spY;
    sb.cornerRadius = 11; sb.fills = fill(C.orange); sb.layoutMode = 'NONE';
    var sbt = T(String(secN), 10, 500, C.white, sb, { ls: 0 });
    sbt.textAlignHorizontal = 'CENTER'; sbt.textAutoResize = 'HEIGHT';
    sbt.resize(22, sbt.height); sbt.y = Math.max(0, Math.round((22 - sbt.height) / 2));
    canvas.appendChild(sb);
    var st = T(text, 13, 400, C.black, null, { w: SW, lh: { value: 155, unit: 'PERCENT' }, ls: 0 });
    st.x = SX + 32; st.y = spY + 2; canvas.appendChild(st);
    spY += st.height + 24;
    var dl = R(SW + 34, 0.5, C.specLine, 0, null); dl.x = SX; dl.y = spY; canvas.appendChild(dl);
    spY += 20;
  }

  // ── NAV ──────────────────────────────────────────────
  function buildNav(links, cta) {
    var nav = figma.createFrame(); nav.name = 'Nav'; nav.resize(W, 56);
    nav.layoutMode = 'HORIZONTAL'; nav.primaryAxisAlignItems = 'SPACE_BETWEEN';
    nav.counterAxisAlignItems = 'CENTER'; nav.paddingLeft = nav.paddingRight = 32;
    nav.fills = fill(C.navBg); nav.primaryAxisSizingMode = 'FIXED'; nav.counterAxisSizingMode = 'FIXED';
    cf.appendChild(nav);
    R(80, 37, C.footerMid, 2, nav);
    var nl = HF('links', 4, nav);
    links.forEach(function(l) {
      var f = HF(l, 0, null); f.paddingLeft = f.paddingRight = 10; f.paddingTop = f.paddingBottom = 4;
      T(l, 10, 400, C.muted, f, { ls: 0 }); nl.appendChild(f);
    });
    var cb = HF('cta', 0, null); cb.paddingLeft = cb.paddingRight = 14; cb.paddingTop = cb.paddingBottom = 6;
    cb.cornerRadius = 100; cb.fills = fill(C.black); T(cta, 10, 400, C.white, cb, { ls: 0 }); nav.appendChild(cb);
    spec('Navigation. Logo left, nav links centre, "' + cta + '" as primary CTA right. Keep navigation minimal and clean.');
    badge(sY + 28); sY += 56;
  }

  // ── HERO ──────────────────────────────────────────────
  function buildHero(label) {
    var hero = figma.createFrame(); hero.name = 'Section — Hero'; hero.resize(W, 560);
    hero.fills = fill(C.bars); hero.layoutMode = 'NONE'; cf.appendChild(hero);
    var pc = figma.createEllipse(); pc.resize(74, 74); pc.x = W/2 - 37; pc.y = 230;
    pc.fills = NONE; pc.strokes = fill(C.muted); pc.strokeWeight = 1.5; hero.appendChild(pc);
    if (label) { var lb = T(label, 11, 400, C.muted, hero, { ls: 0 }); lb.x = W/2 - 100; lb.y = 200; lb.opacity = 0.7; }
    spec('Hero / Opening animation. Full-screen placeholder for a video or animated intro. Sets brand atmosphere before content begins.');
    badge(sY + 280); sY += 560;
  }

  // ── MISSION ──────────────────────────────────────────
  function buildMission(text, filled, outlined) {
    var sec = VF('Section — Mission', W, 20, 32, 40, C.white, null);
    cf.appendChild(sec);
    T(text, 35, 500, C.black, sec, { ls: -3, lh: { value: 140, unit: 'PERCENT' }, w: W - 64 });
    var pr = HF('pills', 8, sec);
    (filled || []).forEach(function(l) {
      var f = HF(l, 0, null); f.paddingLeft = f.paddingRight = 12; f.paddingTop = f.paddingBottom = 5;
      f.cornerRadius = 100; f.fills = fill(C.black); T(l, 10, 400, C.white, f, { ls: 0 }); pr.appendChild(f);
    });
    (outlined || []).forEach(function(l) {
      var f = HF(l, 0, null); f.paddingLeft = f.paddingRight = 12; f.paddingTop = f.paddingBottom = 5;
      f.cornerRadius = 100; f.fills = NONE; f.strokes = fill(C.muted); f.strokeWeight = 0.75;
      T(l, 10, 400, C.muted, f, { ls: 0 }); pr.appendChild(f);
    });
    spec('Mission statement. 35px editorial text sets the brand voice. Filled pills highlight core pillars; outlined pills show supporting values.');
    badge(sY + sec.height / 2); sY += sec.height;
  }

  // ── LETTER ──────────────────────────────────────────
  function buildLetter(eyebrow, headline, sigName) {
    var sec = figma.createFrame(); sec.name = 'Section — Letter from Founders'; sec.resize(W, 50);
    sec.layoutMode = 'HORIZONTAL'; sec.itemSpacing = 32;
    sec.paddingLeft = sec.paddingRight = 32; sec.paddingTop = sec.paddingBottom = 40;
    sec.counterAxisAlignItems = 'CENTER'; sec.fills = fill(C.white);
    sec.primaryAxisSizingMode = 'FIXED'; sec.counterAxisSizingMode = 'AUTO';
    cf.appendChild(sec);
    IMG(420, 300, 4, sec);
    var right = VF('right', 500, 16, 0, 0, null, null); right.fills = NONE; right.counterAxisSizingMode = 'AUTO'; sec.appendChild(right);
    T(eyebrow, 10, 400, C.muted, right, { ls: 0 });
    T(headline, 26, 400, C.black, right, { ls: -3, lh: { value: 115, unit: 'PERCENT' }, w: 444 });
    var ll = VF('lines', 340, 8, 0, 0, null, null); ll.fills = NONE; right.appendChild(ll); BARS([340,340,340,220], ll);
    var sg = HF('sig', 10, right); sg.counterAxisAlignItems = 'CENTER';
    var av = figma.createEllipse(); av.resize(30, 30); av.fills = fill(C.bars); sg.appendChild(av);
    T(sigName, 10, 400, C.muted, sg, { ls: 0 });
    OUTBTN('Read full letter', right);
    spec('Letter from founders. Left image placeholder for founders photo. Right: eyebrow, headline, body text lines, signature, outlined CTA.');
    badge(sY + sec.height / 2); sY += sec.height;
  }

  // ── STATS GRID ──────────────────────────────────────
  function buildStats(title, items) {
    var sec = VF('Section — ' + title, W, 32, 32, 40, C.white, null); cf.appendChild(sec);
    T(title, 30, 400, C.black, sec, { ls: -3 });
    var cols = 3, rowH = 160, colW = Math.floor((W - 64) / cols);
    var rows = Math.ceil(items.length / cols);
    var grid = figma.createFrame(); grid.name = 'stats';
    grid.resize(W - 64, rowH * rows); grid.fills = NONE; grid.layoutMode = 'NONE';
    sec.appendChild(grid);
    items.forEach(function(d, i) {
      var col = i % cols, row = Math.floor(i / cols);
      var cell = figma.createFrame(); cell.name = 'stat-' + i;
      cell.resize(colW, rowH); cell.x = col * colW; cell.y = row * rowH;
      cell.layoutMode = 'VERTICAL'; cell.itemSpacing = 10;
      cell.paddingLeft = cell.paddingRight = 20; cell.paddingTop = 24; cell.paddingBottom = 20;
      cell.primaryAxisSizingMode = 'FIXED'; cell.counterAxisSizingMode = 'FIXED'; cell.fills = NONE;
      if (col > 0 || row > 0) {
        cell.strokes = fill(C.hairline); cell.strokeWeight = 0.5; cell.strokeAlign = 'INSIDE';
        cell.strokeTopWeight = row > 0 ? 0.5 : 0; cell.strokeLeftWeight = col > 0 ? 0.5 : 0;
        cell.strokeRightWeight = 0; cell.strokeBottomWeight = 0;
      }
      T(d.num, 34, 400, C.black, cell, { ls: -3 });
      var lf = VF('lines', colW - 40, 6, 0, 0, null, null); lf.fills = NONE;
      BARS([272, 195, 239], lf); cell.appendChild(lf); grid.appendChild(cell);
    });
    spec(title + '. ' + rows + '×' + cols + ' grid shows ' + items.length + ' key metrics. Hairline borders separate cells. Labels below bars describe each stat.');
    badge(sY + sec.height / 2); sY += sec.height;
  }

  // ── FEATURE LIST ────────────────────────────────────
  function buildFeature(title, items) {
    var sec = VF('Section — ' + title, W, 0, 32, 40, C.white, null); cf.appendChild(sec);
    T(title, 30, 400, C.black, sec, { ls: -3 });
    R(1, 20, C.white, 0, sec);
    items.forEach(function(item, i) {
      var row = figma.createFrame(); row.name = 'item-' + item.n; row.resize(W - 64, 50);
      row.layoutMode = 'HORIZONTAL'; row.itemSpacing = 32; row.paddingTop = row.paddingBottom = 28;
      row.fills = NONE; row.primaryAxisSizingMode = 'FIXED'; row.counterAxisSizingMode = 'AUTO';
      if (i > 0) {
        row.strokes = fill(C.hairline); row.strokeWeight = 0.5; row.strokeAlign = 'INSIDE';
        row.strokeTopWeight = 0.5; row.strokeBottomWeight = 0; row.strokeLeftWeight = 0; row.strokeRightWeight = 0;
      }
      sec.appendChild(row);
      IMG(280, 190, 4, row);
      var body = VF('body', 500, 12, 0, 0, null, null); body.fills = NONE; body.counterAxisSizingMode = 'AUTO'; row.appendChild(body);
      T(item.n, 30, 500, i === 0 ? C.black : C.muted, body, { ls: -3 });
      T(item.title, 25, 500, C.black, body, { ls: -3 });
      var bl = VF('lines', 360, 8, 0, 0, null, null); bl.fills = NONE; body.appendChild(bl);
      BARS([360, 360, 250], bl);
    });
    spec(title + '. Numbered rows: image placeholder left, heading + body text right. Image placeholders to be replaced with photography or illustration.');
    badge(sY + sec.height / 2); sY += sec.height;
  }

  // ── NEWS CARDS ──────────────────────────────────────
  function buildNews(title, items) {
    var sec = VF("Section — What's Happening?", W, 24, 32, 40, C.white, null); cf.appendChild(sec);
    var hdr = figma.createFrame(); hdr.resize(W - 64, 36); hdr.layoutMode = 'HORIZONTAL';
    hdr.primaryAxisAlignItems = 'SPACE_BETWEEN'; hdr.counterAxisAlignItems = 'CENTER';
    hdr.fills = NONE; hdr.primaryAxisSizingMode = 'FIXED'; hdr.counterAxisSizingMode = 'FIXED'; sec.appendChild(hdr);
    T(title, 30, 400, C.black, hdr, { ls: -3 }); OUTBTN('View all', hdr);
    var grid = figma.createFrame(); grid.name = 'grid'; grid.layoutMode = 'HORIZONTAL';
    grid.primaryAxisAlignItems = 'SPACE_BETWEEN'; grid.fills = NONE;
    grid.resize(W - 64, 50); grid.primaryAxisSizingMode = 'FIXED'; grid.counterAxisSizingMode = 'AUTO'; sec.appendChild(grid);
    var cw = Math.floor((W - 64 - (items.length - 1) * 8) / items.length);
    items.forEach(function(c) {
      var card = VF('card', cw, 0, 0, 0, null, null); card.fills = NONE;
      card.primaryAxisSizingMode = 'AUTO'; card.counterAxisSizingMode = 'FIXED'; grid.appendChild(card);
      var th = IMG(cw, 180, 10, card);
      var tg = HF('tag', 0, null); tg.paddingLeft = tg.paddingRight = 8; tg.paddingTop = tg.paddingBottom = 3;
      tg.cornerRadius = 4; tg.fills = fill(C.black); tg.x = 7; tg.y = 155;
      T(c.tag, 9, 400, C.white, tg, { ls: 0 }); th.appendChild(tg);
      var cb = VF('body', cw, 8, 0, 16, null, null); cb.counterAxisSizingMode = 'FIXED'; card.appendChild(cb);
      T(c.date, 12, 500, C.black, cb, { ls: 0 });
      var nl = VF('lines', cw, 6, 0, 0, null, null); nl.fills = NONE; cb.appendChild(nl);
      BARS([cw - 4, cw - 4, Math.floor(cw * 0.6)], nl);
    });
    spec(title + '. ' + items.length + '-column card grid. Each card: thumbnail with tag badge, date, text lines. Replace placeholders with actual news content.');
    badge(sY + sec.height / 2); sY += sec.height;
  }

  // ── FOOTER ──────────────────────────────────────────
  function buildFooter(cols, copyright) {
    var sec = VF('Section — Footer', W, 24, 32, 40, C.footerBg, null); cf.appendChild(sec);
    var fg = HF('grid', 60, sec);
    var bc = VF('brand', 180, 12, 0, 0, null, null); bc.fills = NONE; bc.counterAxisSizingMode = 'AUTO'; fg.appendChild(bc);
    R(72, 14, C.footerMid, 2, bc);
    var ftl = VF('tlines', 140, 6, 0, 0, null, null); ftl.fills = NONE; bc.appendChild(ftl); BARS([140, 95], ftl);
    cols.forEach(function(col) {
      var fc = VF(col.title, 140, 10, 0, 0, null, null); fc.fills = NONE; fc.counterAxisSizingMode = 'AUTO'; fg.appendChild(fc);
      T(col.title.toUpperCase(), 9, 400, C.footerMid, fc, { ls: 0 });
      var fl = VF('links', 140, 6, 0, 0, null, null); fl.fills = NONE; fc.appendChild(fl); BARS([100, 70, 50], fl);
    });
    R(W - 64, 0.5, C.footerEl, 0, sec);
    var btm = figma.createFrame(); btm.resize(W - 64, 20); btm.layoutMode = 'HORIZONTAL';
    btm.primaryAxisAlignItems = 'SPACE_BETWEEN'; btm.counterAxisAlignItems = 'CENTER';
    btm.fills = NONE; btm.primaryAxisSizingMode = 'FIXED'; btm.counterAxisSizingMode = 'FIXED'; sec.appendChild(btm);
    T(copyright || '© All rights reserved.', 9, 400, C.footerMid, btm, { ls: 0 });
    var soc = HF('socials', 8, btm);
    [1,2,3].forEach(function() { var e = figma.createEllipse(); e.resize(18,18); e.fills = fill({ r:0.2,g:0.2,b:0.2 }); soc.appendChild(e); });
    spec('Footer. Dark background. Logo + ' + cols.length + ' link columns + divider + copyright + social circles.');
    badge(sY + sec.height / 2); sY += sec.height;
  }

  // ── CALL SECTIONS (customise per user input) ──────────
  // Replace PAGE_NAME and section content with actual parsed values:

  buildNav(NAV_LINKS, CTA_LABEL);
  buildHero(HERO_LABEL);
  buildMission(MISSION_TEXT, FILLED_PILLS, OUTLINED_PILLS);
  buildLetter(LETTER_EYEBROW, LETTER_HEADLINE, SIG_NAME);
  buildStats(STATS_TITLE, STATS_ITEMS);
  buildFeature(FEATURE_TITLE, FEATURE_ITEMS);
  buildNews(NEWS_TITLE, NEWS_ITEMS);
  buildFooter(FOOTER_COLS, COPYRIGHT);

  // Resize canvas to fit
  var totalH = Math.max(sY + CY + 80, spY + 60);
  canvas.resize(TOTAL_W, totalH);
  specBgRect.resize(SW + 64, totalH);

  figma.viewport.scrollAndZoomIntoView([canvas]);
  return 'Done: ' + canvas.name + ' — ' + secN + ' sections';
}
return run();
```

**Before calling `Figma:use_figma`:** replace all CAPS placeholders (`PAGE_NAME`, `NAV_LINKS`, `MISSION_TEXT`, etc.) with actual values from the user's content. Remove any sections that don't appear in the user's brief.

---

## Step 4 — Connect and deliver

### Figma not connected yet

If `Figma:use_figma` is not available, tell the user:

> "To send this wireframe to Figma, you need to connect Claude to Figma first:
> 1. Open **Claude Settings** → **Integrations**
> 2. Find **Figma** → click **Connect**
> 3. Log in with your Figma account
> 4. Come back here and paste your Figma file link"

### Figma is connected

Ask:
> "Which Figma file should I write this to? Please paste the file URL — it looks like `https://www.figma.com/design/XXXXX/...`"

Extract the `fileKey` from the URL (the segment after `/design/`). Call `Figma:use_figma` with it.

After success, tell the user:
- Frame name: **"[PageName] — Wireframe"**
- Which page it was written to (`figma.currentPage.name`)
- Shortcut to jump to it: **Cmd+Shift+H** (Mac) / **Ctrl+Shift+H** (Windows)

---

## Mistakes to avoid

- Never `figma.currentPage = x` — use `await figma.setCurrentPageAsync(x)`
- Never `counterAxisAlignItems = 'START'` — use `'MIN'`
- Always `loadFontAsync` before any text node
- Always end with `return run()` not just `run()`
- Image placeholder frames: set both `primaryAxisSizingMode` and `counterAxisSizingMode` to `'FIXED'`
- Spacer frames: set `fills = NONE` (empty array `[]`), not `fill(white)`, or they show as white boxes
- Stat grid border: use `strokeTopWeight` / `strokeLeftWeight` individually — the general `strokeWeight` sets all sides
- `BARS()` = gray text placeholder stacks — use for ALL body text not provided by user
- Do not add extra sections, rename sections, or change content the user provided
