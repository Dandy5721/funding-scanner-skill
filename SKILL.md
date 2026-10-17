---
name: funding-scanner
description: Scan federal and private research funding sources (NIH, NSF, DoD/CDMRP, ARPA-H, private foundations, industry/company research awards) for grant opportunities relevant to a researcher, built from the user's own materials and answers, and produce a ranked digest with a deadline tracker. Use whenever the user asks to find, summarize, scan, monitor, or digest funding opportunities, grant announcements, FOAs, NOFOs, RFAs, NIH guide notices, foundation grants, or company research awards (Amazon, Google, Microsoft, Meta, Anthropic, NVIDIA, pharma), even without naming an agency; for a weekly funding update; to surface limited-submission awards; or to compare a researcher profile against open calls. Trigger on phrases like "find grants", "what funding is open for", "scan for FOAs", "build a funding digest", "what should [PI] apply to".
---

# Funding Opportunity Scanner

Help researchers find relevant open funding calls without manually browsing each agency. The skill takes a researcher profile **built from the user's own materials** (research themes, career stage, mechanism preferences, eligibility constraints) and produces:

1. A **ranked markdown digest** of opportunities with deadlines, amounts, and fit notes
2. An **Excel tracker** with one row per opportunity for deadline management

The skill is designed to be re-run on a weekly or monthly cadence. Each run is a snapshot of currently open calls relevant to that profile.

## Environment

- **Skill folder**: the folder that holds this SKILL.md (called `<skill_dir>` below); the tracker script is `<skill_dir>/scripts/build_tracker.py`. Never write results into it.
- **Output folder**: **the user chooses it** (see "Ask the user first"). Never create a default folder.
- **Internet**: web search and fetch are used interactively in the session. Do not submit funding scans as batch jobs.
- **Python / openpyxl**: `build_tracker.py` needs `openpyxl`. Check `python3 -c "import openpyxl"`; if it is missing, tell the user and ask where it may be installed (for example `pip3 install openpyxl --target <folder the user names>`); do not install into a personal home environment on your own.

## Ask the user first (before any search)

This skill is run on the **user's own materials**. Nothing about the person, the lab or the institution may be assumed, taken from a bundled file, or guessed from a name, e-mail, path or the machine you are on. Ask with `AskUserQuestion` (or plain questions, a few at a time); skip only what the request already states:

1. **Whose scan is it, and which materials?** - the user themselves or someone else, and what you may read: CV / biosketch, specific aims or a funded proposal, a list of abstracts or papers, a lab web page, or a short description pasted in chat. Ask for the paths or the pasted text; do not search the disk for them. If the user has a saved profile from an earlier run, ask for its path.
2. **Research focus** - confirm the keywords and themes you drew from the materials (show them back; the user corrects them), plus topics to exclude.
3. **Career stage and eligibility** - career stage (e.g. early-stage investigator, mid-career, senior), whether they or the project are limited to US citizens / permanent residents, institution type, and any exclusions ("no SBIR/STTR", "no clinical trials", "no DoD"). These decide what is dropped; never infer them.
4. **Preferences** - award size and duration range, mechanisms they favour, agencies to include or exclude (default offer: NIH, NSF, DoD/CDMRP, ARPA-H, private foundations, industry awards - the user may switch any off), and whether to list trainee mechanisms (F/K99/T) for them to forward.
5. **Institution** - ask which institution(s) the PI is at; institutional pilot programmes (Step 2) are searched **only** for the institution the user names. Do not assume any institution.
6. **Output folder** - always ask, even when you could suggest one (you may offer a folder in the user's own workspace as one option). Digest, JSON and tracker go there, and so does a new profile unless the user names another place. Never write into the skill folder.
7. **First run or update** - if there is an earlier digest, ask for its folder (for the "What's changed" diff).

Privacy: the profile holds personal details (career stage, citizenship, publications). Keep it and the outputs on the server; do not upload them or paste them into web pages. **Web search queries contain topic keywords only** - never the person's name, citizenship, institution-internal details or the text of their materials.

## Workflow

Run the four steps below in order.

### Step 1: Build the profile from the user's materials

- **Use only what the user gave you in the questions above.** Read the materials they pointed to (and nothing else), draft the profile with `assets/profile_template.md`, and **show it to the user for confirmation or correction before searching**. Minimum needed: research keywords, career stage, citizenship/PR eligibility, preferred award size range, agencies to exclude.
- **Saved profiles from earlier runs** may exist; read one only when the user names it and confirm it is still current. Do not read, list or reuse other people's profiles, even if the files are on disk.
- Save the confirmed profile to the folder the user chose (Step "Output folder"), as `profile_<lastname>.md`, so it can be reused next time.

A profile is the most important input - relevance ranking is only as good as the profile.

### Step 2: Search the configured sources

Read `references/sources.md` for the agency / foundation / industry catalog and the query patterns. Search the categories the user switched on, and within them only the programmes that fit the **field the user confirmed** (the catalog's field-specific sections are examples, not a checklist; for a field it does not cover, find the field's main funders by search and say so):

- **Federal** - NIH Guide (R01, R21, R03, K, P, U series, NOSIs), NSF (directorate solicitations, CAREER, cross-cutting programmes), DoD / CDMRP, ARPA-H, other federal agencies that fund the field (DOE, NASA, NEH, USDA, ...) when relevant.
- **Private foundations** - those matching the field, with career-stage window, citizenship rule and limited-submission flag for each.
- **Industry research awards** - cash, credits or in-kind compute from companies, when the profile is a fit (flag cash vs. credits vs. in-kind).
- **Limited-submission / institutional-nomination programmes** - cross-check strong fits against the limited-submission table in the catalog and the user's institution's own calendar; the institution's **internal deadline is usually 6-10 weeks before the sponsor's**, so surface these early.
- **The user's institution** - internal pilot / seed / bridge programmes, only for the institution the user named.

Use `web_search` and `web_fetch` to pull current open calls. Cap at 2–4 searches per source category; a full run is ~20–30 searches + ~10–15 fetches. For each opportunity capture:

- Title, Agency/sponsor, Mechanism/activity code
- LOI deadline and full proposal deadline (note both); for limited-submission programs, the **institution's internal deadline**
- Award amount / duration (for industry: note cash vs. credits vs. in-kind separately)
- Eligibility (career stage window, citizenship, institution type, limited-submission cap)
- IP / agreement type for industry awards (gift vs. sponsored research — flag "route via the institution's sponsored-programs / tech-transfer office")
- One-sentence summary
- Direct URL to the announcement

If a search returns nothing relevant, note it and move on. Do not pad the digest with off-topic opportunities. If a strong-fit program is between cycles, put it on the digest's **watch list** with the expected next window rather than dropping it.

### Step 3: Filter and rank against the profile

Use `references/eligibility_cheatsheet.md` — including its **foundation & industry eligibility quick table** — to filter before ranking.

**Drop** opportunities the faculty cannot apply to:
- Eligibility mismatch (SBIR/STTR unless startup affiliation, MD-only for PhD, ESI-only past window, citizen/PR-only for a non-PR profile)
- Career stage mismatch (K-series or early-career foundation awards — Pew/Searle/Packard/Sloan/BBRF-YI/CAREER — for tenured/established PIs; senior-only awards for a first-year assistant prof)
- Topic far from profile keywords (narrow topical RFAs get dropped; broad mechanisms like R01/R21 are retained)
- Foundation/industry awards below the profile's minimum-useful-award **unless** the value is compute/access or it is a limited-submission prestige award — then keep and note the caveat

**Rank** survivors:
- **High fit (★★★)** — keyword match in title/summary AND eligibility clean AND deadline workable (>2 weeks out)
- **Medium fit (★★)** — keyword match in summary OR favored mechanism, eligibility clean
- **Low fit (★)** — broadly eligible but topical match weak, or compute-credit-only programs; include as "worth a glance"
- **Limited submission (🏛️)** — strong profile fit BUT the institution can only nominate N. List in a dedicated section with the **institution's internal deadline** (put it in the tracker's LOI column) and an instruction to contact their research office (limited-submissions staff) now. Rank by internal deadline.
- **Trainee (👥)** — F31/F32/K99/T32, PhD fellowships (Google/Apple/NSF GRFP) — separate section for the PI to forward

Sort within each tier by deadline ascending (soonest first). Programs that are a strong fit but **between cycles** go on the digest's **watch list** (with expected next window), not in the drop pile.

### Step 4: Generate outputs

**Output directory**: the folder the user gave (`<output_dir>` below). Create it only if the user said to; otherwise report that it does not exist and ask.

Produce the three files A-C below, then hand them over (D):

**A. Opportunities JSON** at `<output_dir>/opportunities_<YYYY-MM-DD>.json`
Build this first — it feeds the Excel tracker. Schema is in `scripts/build_tracker.py`'s docstring.

**B. Markdown digest** at `<output_dir>/funding_digest_<YYYY-MM-DD>.md`
Use the template at `assets/digest_template.md`. Lead with a short executive summary (N opportunities found, top 3 by fit, urgent deadlines <2 weeks). Group by fit tier.

**C. Excel tracker** at `<output_dir>/funding_tracker_<YYYY-MM-DD>.xlsx`
```bash
python3 "<skill_dir>/scripts/build_tracker.py" \
  --opportunities <output_dir>/opportunities_<YYYY-MM-DD>.json \
  --output <output_dir>/funding_tracker_<YYYY-MM-DD>.xlsx \
  --pi-name "<PI Full Name>"       # add PYTHONPATH=<folder> if openpyxl was installed to a folder the user named
```

**D. Hand the results to the user**
List the files with their absolute paths (`ls -l`), give the executive summary (counts per tier, urgent deadlines), and name anything you could not verify. The digest is plain Markdown and the tracker an `.xlsx`; do not upload them anywhere.

## Re-running on a cadence

When the user asks for a "weekly update" or "what's new since last time":

- Look in the earlier-digest folder the user gave for the most recent prior digest
- Run the full search again
- Diff: flag new opportunities, deadlines now <2 weeks (urgent), and opportunities that have closed (drop)
- Lead the new digest with a "What's changed" section before the full ranked list

## Important behaviors

- **Don't fabricate opportunities.** If a search returns nothing, say so. Never invent a grant title, deadline, or URL.
- **Verify deadlines on the source page.** Search snippets are often stale. When an opportunity makes the digest, `web_fetch` the announcement page and confirm the deadline before writing it.
- **Note when info is uncertain.** If award amount or eligibility is missing after fetching, write "not specified" rather than guessing.
- **Respect the profile's exclusions.** Honor "no SBIR," "no clinical trials," etc. even if the opportunity otherwise looks strong.
- **Career-stage awareness.** A K99 for a tenured PI is noise; an R01 for a postdoc is noise. Early-career foundation awards (Pew, Searle, Packard, Sloan, BBRF YI) are noise for an established PI; senior-only awards are noise for a first-year assistant prof. Read career stage carefully.
- **Institutional sources only for the user's institution.** Search the institution's internal pilot/seed programmes only for the institution the user named; do not apply one institution's list to another.
- **Foundations and industry awards are not optional** when they fit the profile the user confirmed: scan the foundation lists and the tech AI-award list that match the research themes on every run, not just when the user names a foundation. Foundation cash is often modest; weight the compute/access/collaborator value and the career-stage fit, not just the dollar figure.
- **Limited submission = act now.** When a strong-fit program caps institutional nominees, the binding deadline is the institution's *internal* one (typically 6-10 weeks early). Put it in the limited-submission section and the tracker's LOI column, and tell the PI to contact their research office now.
- **Industry awards: flag the agreement type.** Most are gifts or sponsored-research agreements with distinct IP terms; always add "route via your sponsored-programs / technology-transfer office for review". Do not present a company "research award" as equivalent to a federal grant.
- **Don't cite retired programs.** Verify the program still exists (e.g. Google replaced the Research Scholar Program with GARA; Microsoft AFMR is folding into AARI). If a program is between cycles, use the digest watch list.

## Reference files

- `references/sources.md` — Full agency/program list and search query patterns
- `references/eligibility_cheatsheet.md` — Eligibility codes (ESI, NI, K-eligibility, citizenship rules)
- `assets/profile_template.md` — Blank researcher profile template
- Saved profiles live in the folder the user chose for outputs (`profile_<lastname>.md`), never in this skill folder; read one only when the user names it
- `assets/digest_template.md` — Markdown digest structure
- `scripts/build_tracker.py` — Excel tracker builder (requires openpyxl)
