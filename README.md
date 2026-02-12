# Claude Code Skills

Personal skills for Claude Code. These live at `~/.claude/skills/` and are available globally across all projects.

## Skills

| Skill | Type | Description |
|-------|------|-------------|
| **lila-voice** | Voice / Persona | Write as Lila Monroe — romance author persona. Covers casual (social/blog), marketing (blurbs/ads), and email (newsletters) contexts. |
| **humanizer** | Editing | Remove AI writing patterns from text. Based on Wikipedia's "Signs of AI writing" guide. 24 pattern categories. |
| **design-system** | Reference | Design system conventions. |
| **screenshot** | Tool | Screenshot capture and analysis (`/ss`). |
| **md-to-dictate** | Tool | Convert markdown to dictation-friendly format. |

## Usage

```bash
# In any Claude Code session:
/lila-voice            # Write in Lila's voice (auto-detects context)
/lila-voice casual     # Social media, about page, blog
/lila-voice marketing  # Blurbs, ads, Amazon copy
/lila-voice email      # Newsletters, Kit sequences

/humanizer             # Strip AI patterns from any text
```

## Installation

Clone to `~/.claude/skills/`:

```bash
git clone https://github.com/vicky3074/claude-skills.git ~/.claude/skills/
```

## Credits

- **humanizer** — adapted from [blader/humanizer](https://github.com/blader/humanizer) (Apache 2.0)
- **lila-voice** — original, built from Lila Monroe persona documents
