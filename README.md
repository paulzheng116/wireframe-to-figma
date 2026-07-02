# Wireframe to Figma

`wireframe-to-figma` is a Codex/Claude skill that turns text briefs, page outlines, tables, or screenshots into editable mid-fidelity wireframes in Figma.

The skill is opinionated: it produces wireframes in a fixed HD Schools-inspired design language with a dark canvas, white content column, orange section badges, and a right-side specifications panel.

## What it does

- Parses page briefs, bullet lists, tables, spreadsheets, and screenshots.
- Converts content into a structured section plan before generating Figma nodes.
- Writes editable frames directly into a Figma file when the Figma MCP/integration is connected.
- Uses a consistent wireframe system: navigation, hero, mission, founder letter, stats grid, feature rows, news cards, and footer.
- Adds product-design specifications beside the wireframe so reviewers can understand section intent.

## Best for

- Landing page wireframes
- Site structure visualization
- Content outline exploration
- Mid-fidelity UX direction
- Client-facing page sketches
- Turning raw page notes into a clear Figma frame

## Repository structure

```text
wireframe-to-figma/
├── SKILL.md       # The installable skill definition and implementation guidance
├── README.md      # Project overview and installation instructions
├── .gitignore
└── .gitattributes
```

## Installation

### Option 1: Install from this repository

Use Codex's skill installer with this GitHub repository:

```text
paulzheng116/wireframe-to-figma
```

After installing, restart Codex so the new skill is picked up.

### Option 2: Manual local install

Copy this repository into your Codex skills directory:

```bash
mkdir -p ~/.codex/skills
cp -R wireframe-to-figma ~/.codex/skills/wireframe-to-figma
```

Then restart Codex.

## Usage

Ask for a wireframe and provide either a brief, page structure, table, or screenshot.

Example prompts:

```text
Turn this landing page outline into a Figma wireframe.
```

```text
Create a mid-fidelity wireframe in Figma from these sections:
1. Hero
2. Mission
3. Stats
4. Feature rows
5. News
6. Footer
```

```text
Use this screenshot as a reference and recreate it as an editable wireframe in Figma.
```

When Figma is connected, the skill asks for a Figma file URL, extracts the file key, and writes the wireframe into the current Figma page.

## Output style

The generated wireframe follows the design system defined in `SKILL.md`:

- Dark canvas background: `#323131`
- White content column
- Orange numbered section badges: `#ff6f00`
- Right-side specifications panel
- Inter typography
- Gray placeholder bars for unresolved body copy
- Editable Figma frames, text, rectangles, ellipses, and layout groups

## Notes

- The skill is intentionally mid-fidelity, not final visual design.
- Body copy that is not supplied by the user should remain as placeholder bars.
- The skill should not invent missing sections or rewrite user-provided headings.
- Figma output requires the Figma MCP/integration to be connected.

## Main skill file

See [`SKILL.md`](./SKILL.md) for the full trigger description, design system, and Figma generation workflow.
