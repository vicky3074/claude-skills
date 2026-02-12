# /dictate - Convert Markdown to Word Dictation Script

Convert any markdown file into a continuous Word Dictate script that can be recorded once and played back hands-free.

## Usage

- `/dictate path/to/file.md` — Convert the file and save as `path/to/file_DICTATE.md`
- `/dictate path/to/file.md --output path/to/output.md` — Custom output path
- `/dictate path/to/file.md --code skip` — Skip all code blocks (default)
- `/dictate path/to/file.md --code dictate` — Attempt to dictate code blocks too (small/simple ones only)
- `/dictate path/to/file.md --tables skip` — Skip tables (default)
- `/dictate path/to/file.md --tables dictate` — Attempt to dictate tables

## Instructions

### Step 1: Read the source markdown file

Read the file provided as the argument.

### Step 2: Analyze the content and categorize

Scan the entire document and categorize each block as one of:
- **Prose** — headings, paragraphs, bullet lists, numbered lists → DICTATE
- **Code blocks** — fenced code (```), JSON, Mermaid, YAML, etc. → SKIP by default (put placeholder)
- **Tables** — pipe-delimited markdown tables → SKIP by default (put placeholder)
- **Inline code** — `backtick` words → spell out naturally (remove backticks)
- **Images/links** — skip images, read link text naturally

### Step 3: Convert to dictation script

Transform each block using these rules:

#### Headings
- `# Heading` → `Heading new paragraph`
- `## Sub heading` → `Sub heading new paragraph`
- `### Sub sub heading` → `Sub sub heading new paragraph`
- Do NOT say "heading 1" etc. — Word Dictate types that literally
- The user will manually format headings afterward by finding the text

#### Paragraphs
- Each paragraph becomes a continuous spoken block
- End each paragraph with `new paragraph` (creates a blank line = easy to find later)

#### Bullet Lists
- Start with `start bullet list`
- Each item: `next bullet` between items
- End with `exit list new paragraph`
- Nested bullets: flatten them (nesting doesn't work in dictation)

#### Numbered Lists
- Start with `start number list`
- Each item: `next bullet` between items (yes, "next bullet" works for numbered lists too)
- End with `exit list new paragraph`

#### Bold Text
- `**word**` → say the word, then `bold that` (bolds the last thing said)
- `**multiple words**` → say the words, then `bold that` — only works reliably for short phrases
- For long bold sections, just say the text normally — user will bold manually

#### Italic Text
- `*word*` → say the word normally (italics rarely matter in technical docs)
- Or say the word, then `italicize that` if emphasis is important

#### Inline Code
- `` `variableName` `` → just say "variableName" naturally, remove backticks
- The user will format these manually later

#### Links
- `[link text](url)` → just say the link text, drop the URL
- If the URL matters, say "link colon" then spell out the URL

#### Code Blocks (when --code skip, the default)
- Replace with: `This section contains a code block that will be inserted separately period new paragraph`
- If the code block has a language tag, say: `This section contains a [language] code block that will be inserted separately period new paragraph`

#### Code Blocks (when --code dictate)
- Only attempt for small blocks (under 10 lines)
- Use these voice commands for symbols:
  - `{` → "open brace"
  - `}` → "close brace"
  - `[` → "open bracket"
  - `]` → "close bracket"
  - `"` → "open quotes" / "close quotes"
  - `:` → "colon"
  - `,` → "comma"
  - `-` → "hyphen" or "dash"
  - `_` → "underscore"
  - `/` → "forward slash"
  - `\` → "backslash"
  - `|` → "pipe character"
  - `@` → "at sign"
  - `&` → "ampersand"
  - `*` → "asterisk"
  - `>` → "greater than sign"
  - `<` → "less than sign"
  - `=` → "equals sign"
  - `.` in code context → "dot" (not "period" which inserts punctuation)
- Warn user that code dictation is error-prone and should be verified
- For blocks over 10 lines, fall back to skip behavior

#### Tables (when --tables skip, the default)
- Replace with: `This section contains a table that will be inserted separately period new paragraph`

#### Tables (when --tables dictate)
- Read as prose: "Row 1 colon [column1] comma [column2] comma [column3] new line"
- User will reformat into a table manually

#### Punctuation (in regular text)
- `.` at end of sentence → already natural, Word Dictate auto-punctuates OR the script says "period"
- Be explicit: always include "period" at end of sentences for reliability
- `?` → "question mark"
- `!` → "exclamation mark"
- `:` → "colon"
- `;` → "semicolon"
- `...` → "ellipsis"
- `—` (em dash) → "m dash"
- `–` (en dash) → "n dash"
- `()` → "open parenthesis" / "close parenthesis"

#### Line Breaks
- Single line break within a section → "new line" (single Enter)
- Between sections/paragraphs → "new paragraph" (double Enter)

#### Abbreviations & Acronyms
- First occurrence: spell out → "A C S comma Access Card System"
- Subsequent occurrences: just say the letters → "ACS"
- Common ones that dictate might mishear: always spell with spaces between letters

### Step 4: Assemble the output file

Create the output file with this structure:

```markdown
# [Original Title] — Dictation Script

## How to Use This File

1. **Record yourself** reading the script below into a voice memo on your phone
2. On the target computer, open **Word** and click **Dictate** on the Home ribbon
   (Use Word's Dictate, NOT Windows Win+H — Word's version supports more commands)
3. **Play the recording** near the laptop mic
4. Walk away. Let it run.
5. Come back and do final cleanup

### Voice Commands Reference
| Say this | It does this |
|----------|-------------|
| "period" | . |
| "comma" | , |
| "colon" | : |
| "question mark" | ? |
| "exclamation mark" | ! |
| "dash" or "hyphen" | - |
| "open/close parenthesis" | ( ) |
| "open/close bracket" | [ ] |
| "open/close brace" | { } |
| "open/close quotes" | " " |
| "underscore" | _ |
| "forward slash" | / |
| "backslash" | \ |
| "new line" | single Enter |
| "new paragraph" | double Enter (blank line) |
| "start bullet list" | begins bullets |
| "start number list" | begins numbered list |
| "next bullet" | next list item |
| "exit list" | ends list |
| "bold that" | bolds last word/phrase |
| "stop dictation" | stops listening |

### Cleanup Guide
[Auto-generated list of what needs manual fixing: headings to format, code blocks to insert, tables to insert, etc.]

---

# READ EVERYTHING BELOW IN ONE GO

[The continuous dictation script here]

End of document period stop dictation
```

### Step 5: Generate a companion skip-list

If any code blocks or tables were skipped, add a section at the bottom:

```markdown
---

# SKIPPED CONTENT — Type or paste these manually

## Skip 1 — [Section name]: [language] code block
[The original code block content, formatted for easy reading/typing]

## Skip 2 — [Section name]: Table
[The original table content]
```

### Step 6: Report summary to user

After creating the file, tell the user:
- Output file path
- Total sections converted
- Number of code blocks skipped (if any)
- Number of tables skipped (if any)
- Estimated reading time (rough: ~150 words per minute)
- Any warnings about content that might not dictate well (unusual symbols, URLs, etc.)
