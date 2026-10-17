# funding-scanner

A [Claude Code](https://claude.com/claude-code) skill that scans research funding sources for opportunities relevant to a specific researcher and turns the results into a ranked digest and a deadline tracker.

The skill works from the **user's own materials and answers**. It does not ship with, assume or reuse anyone's profile, institution or output location: before it searches, it asks who the scan is for, what it may read, the research focus, career stage and eligibility, preferences, institution and where to write the results.

## What it produces

For each run, in a folder the user chooses:

| File | Content |
|---|---|
| `opportunities_<date>.json` | Structured list of opportunities (schema in `scripts/build_tracker.py`) |
| `funding_digest_<date>.md` | Ranked Markdown digest: executive summary, fit tiers, limited-submission section, trainee section, watch list, and a "what changed" section on re-runs |
| `funding_tracker_<date>.xlsx` | Excel tracker, one row per opportunity, for deadline management |
| `profile_<lastname>.md` | The confirmed researcher profile, so the next run can reuse it |

Opportunities are ranked into tiers: high fit, medium fit, low fit, limited submission (institution can nominate only N applicants), and trainee mechanisms for the PI to forward. Strong fits that are between cycles go on a watch list instead of being dropped.

## Sources searched

The catalog is in [`references/sources.md`](references/sources.md). The skill searches only the categories the user switches on and, within them, the programmes that fit the confirmed research field.

- **Federal:** NIH Guide, NSF, DoD / CDMRP, ARPA-H, other federal funders when relevant
- **Private foundations:** field-specific and early-career programmes, with career-stage window, citizenship rule and limited-submission flag
- **Industry research awards:** company cash, credit and in-kind compute programmes, flagged by agreement type
- **Limited-submission programmes:** with the institution's internal deadline surfaced early
- **The user's own institution:** internal pilot, seed and bridge programmes (only for the institution the user names)

The field-specific sections in the catalog are examples rather than a checklist. For a field the catalog does not cover, the skill finds the field's main funders by search and says so.

## How it works

1. **Ask first.** Whose scan it is and which materials it may read (CV, biosketch, aims, abstracts or pasted text), research keywords, career stage, citizenship or residency limits, exclusions, award size, agencies to include, institution, output folder, and whether this is a first run or an update.
2. **Build the profile** from only those materials, show it to the user, and search after the user confirms.
3. **Search** the selected sources. Every deadline is checked on the announcement page, not taken from a search snippet.
4. **Filter and rank** against the profile, dropping what the researcher cannot apply to.
5. **Write** the JSON, digest and tracker, and hand them to the user with absolute paths.

Re-running on a cadence (for example weekly) compares against the previous digest and leads with what is new, urgent or closed.

## Install

Copy the skill folder (without the `.git` directory) into a Claude Code skills directory:

```bash
git clone https://github.com/Dandy5721/funding-scanner-skill.git
mkdir -p ~/.claude/skills/funding-scanner
cp -r funding-scanner-skill/{SKILL.md,assets,references,scripts} ~/.claude/skills/funding-scanner/
```

A project-level `.claude/skills/` directory works the same way. The skill name is `funding-scanner`.

### Requirements

- Claude Code with web search and web fetch available in the session
- Python 3 with [`openpyxl`](https://pypi.org/project/openpyxl/) for the Excel tracker (`pip install openpyxl`)

## Usage

Ask Claude Code in natural language, for example:

- "Find funding opportunities for me."
- "Scan for FOAs that fit my research and build a funding digest."
- "What should [PI] apply to this year?"
- "Weekly funding update."

The skill then starts with its questions.

## Repository layout

```
SKILL.md                          skill definition and workflow
assets/profile_template.md        blank researcher profile
assets/digest_template.md         digest structure
references/sources.md             funder catalog and query patterns
references/eligibility_cheatsheet.md  eligibility codes and quick tables
scripts/build_tracker.py          Excel tracker builder
```

To build a tracker by hand from an opportunities file:

```bash
python3 scripts/build_tracker.py \
  --opportunities opportunities.json \
  --output funding_tracker.xlsx \
  --pi-name "PI Full Name"
```

## Privacy

A profile contains personal details such as career stage, citizenship or residency, and publications. The skill keeps profiles and outputs in the folder the user chose and does not upload them. Web searches use topic keywords only: never the person's name, citizenship, internal institutional details or the text of their materials.

## Limitations

- Programme details, deadlines and eligibility change often. Treat the catalog as a starting point; the skill verifies each listed opportunity on its source page, and you should confirm before applying.
- Relevance ranking depends on the profile. The more specific the materials, the better the result.
- Results are a snapshot of what is currently open, not a guarantee of completeness.

## License

No license has been chosen yet. Until one is added, all rights are reserved by the author.
