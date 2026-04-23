# BASSCOM AI Conference 2026

Presentation assets and working notes for the BASSCOM AI Conference 2026 session.

## Layout

| Path | Contents |
|---|---|
| `docs/` | Written reference — branding colors, design notes, plans |
| `images/` | Slide screenshots, terminal captures, and device mockups |
| `.claude/` | Claude Code project settings |

## Image mockup tooling

Screenshots in `images/` are polished with a reusable Claude Code skill installed
at `~/.claude/skills/image-mockup/`. It wraps any screenshot in a MacBook-style
frame (notch, bezels, hinge, base) or applies just a soft drop shadow, then
writes a new PNG alongside the source.

### Quick use

```bash
# MacBook mockup with right+bottom shadow (default)
~/.claude/skills/image-mockup/scripts/image-mockup.sh images/shot.png
# → images/shot-laptop.png

# Drop shadow only
~/.claude/skills/image-mockup/scripts/image-mockup.sh --style shadow images/shot.png
# → images/shot-shadow.png

# Full help (every tunable flag)
~/.claude/skills/image-mockup/scripts/image-mockup.sh --help
```

Inside Claude Code, the skill auto-triggers on prompts such as:

- "put this on a laptop" / "mock it up on a MacBook"
- "add a drop shadow to X.png"
- "make the image look nicer for a slide"

### Defaults

Shadow is biased to the right and bottom so the image reads as "lifted" on a
light slide background:

| Setting | Default | Flag |
|---|---|---|
| Shadow opacity | 60 | `--shadow-opacity` |
| Shadow blur (sigma) | 25 | `--shadow-blur` |
| Shadow offset X / Y | 35 / 40 | `--shadow-x` / `--shadow-y` |
| Screen bezel | 18px | `--bezel` |
| Notch width × height | 180 × 14 | `--notch-w` / `--notch-h` |
| Base extension per side | 90px | `--base-extra` |
| Canvas padding | 80px | `--pad` |

See `~/.claude/skills/image-mockup/SKILL.md` for the full reference.

### Requirements

- ImageMagick (`magick` or `convert` in `$PATH`).
  On Debian/Ubuntu: `sudo apt install imagemagick`.

## Conventions

- Raw screenshots keep their plain name: `claude-code-review-plan.png`.
- Polished variants use suffixes: `-laptop.png`, `-shadow.png`.
- Originals are never overwritten — the script always writes a new file.
