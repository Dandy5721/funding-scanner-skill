# Funding Sources Reference

Standing list of agencies and programs to scan, with search patterns that work well for each. Update this file as new sources are added.

## Federal

### NIH

Primary entry point: https://grants.nih.gov/funding/searchguide/index.html

The NIH Guide is the authoritative listing. Use web_search for the topic + "NIH guide" or "NIH PAR" or "NIH PA" or "NIH RFA" to find current notices. Useful query patterns:

- `site:grants.nih.gov <topic keywords> <current-year>`
- `NIH NOSI <topic>` for Notices of Special Interest
- `NIH <institute> <topic> R01` for institute-specific calls (e.g., NIMH, NIA, NINDS, NIBIB, NHGRI)

Activity codes worth knowing (filter against profile's career stage):
- **R01** — standard independent research, faculty
- **R21** — exploratory/developmental, 2yr, smaller
- **R03** — small grant, 2yr, very small
- **R34** — clinical trial planning
- **K99/R00** — pathway to independence, late postdoc
- **K01/K08/K23/K25** — career development, mentored
- **K18** — career enhancement for established investigators
- **F31/F32** — predoc / postdoc fellowships
- **U01/U54** — cooperative agreements, often consortia
- **DP1/DP2/DP5** — Director's awards (Pioneer, New Innovator, Early Independence)
- **T32** — training grants (institutional)

### NSF

Primary entry point: https://www.nsf.gov/funding/

Search the funding opportunities page directly. Useful directorate filters for biomedical-AI labs:

- **CISE** — Computer & Information Science (IIS, CCF, CNS)
- **BIO** — Biological Sciences (DBI for infrastructure, IOS for organismal)
- **SBE** — Social, Behavioral & Economic
- **MPS** — Math & Physical Sciences
- **CAREER** — early-career faculty, annual cycle
- **Smart Health and Biomedical Research in the Era of AI** (SCH) — recurring solicitation
- **NeuroNex / EFRI / Convergence Accelerator** — interdisciplinary calls

Query patterns:
- `NSF <directorate> solicitation <topic> <current-year>`
- `NSF CAREER deadline <current-year>`

### DoD / CDMRP

Primary entry point: https://cdmrp.health.mil/

Programs rotate annually; check current FY funding opportunities. Programs most relevant to neuro/psych/biomedical-AI:

- **PRMRP** — Peer Reviewed Medical Research Program (broad topic list each year)
- **PHRP** — Psychological Health Research Program
- **PRARP** — Alzheimer's Research Program
- **TBIPHRP** — Traumatic Brain Injury & Psychological Health
- **EMBRP** — Epilepsy
- **PCRP / BCRP / OCRP / LCRP** — cancer programs by site
- **AARP / ALSRP / KCRP / PRCRP** — other peer-reviewed programs

Query: `CDMRP <program-acronym> FY<year> funding`

### ARPA-H

Primary entry point: https://arpa-h.gov/funding

Look for:
- Open BAAs (Broad Agency Announcements)
- Exploratory Topics (ETs)
- Sprints (short-duration focused calls)
- Mission Office solicitations

Query: `ARPA-H open solicitation <current-year>` or `ARPA-H BAA <topic>`

### Other federal

- **AHRQ** — health services research (https://www.ahrq.gov/funding/index.html)
- **PCORI** — patient-centered outcomes (https://www.pcori.org/funding-opportunities)
- **DOE / Office of Science** — computational science, ASCR (https://science.osti.gov/funding-opportunities)
- **NASA** — for biomedical sensing / human factors (https://science.nasa.gov/researchers/solicitations)
- **VA Merit Awards** — for VA-affiliated investigators only

## Private foundations

Profile-dependent — only scan if the foundation matches the research area or the profile flags interest. Scan only the sections that match the research field the user confirmed (the field-specific sections below are examples; add programs for other fields from a web search).

**How to read each entry:** `Program(s) — award size / duration — career-stage window — citizenship — [LIMITED SUBMISSION if institution can only nominate N] — cadence`. Cycles drift year to year; always `web_fetch` the program page to confirm the current deadline and terms before it goes in a digest. "Cit: any" means non-US-citizens on H-1B/O-1/etc. are normally eligible; "Cit: US/PR" means citizen or permanent resident only (auto-drop for non-PR profiles); "Cit: check" means the rule is program-specific or unstated.

### Brain / neuroscience / mental health

- **BBRF (Brain & Behavior Research Foundation / NARSAD)** — Young Investigator ($70K total = $35K/yr × 2; ≤7yr from first faculty appt or still in training; **international eligible**), Independent Investigator ($100K/2yr, mid-career), Distinguished Investigator ($100K/1yr, full prof). Cit: any. Cadence: YI window ~early Feb → early March (e.g. 2027 deadline ~March 5, 2027); DI ~Sept; III ~June. https://bbrfoundation.org/grants-prizes/bbrf-young-investigator-grants
- **McKnight Endowment Fund for Neuroscience** — two current programs: **Scholar Award** ($75K/yr × 3 = $225K; early-career, disorders of learning & memory focus; LOI ~early Jan) and **Neurobiology of Brain Disorders Award** ($100K/yr × 3 = $300K; **must have held a tenured/tenure-track position ≥3yr at time of application**, any career stage otherwise, translating brain-science discoveries toward diagnosis/therapy; **no LOI — direct application, ~Aug open / mid-Oct deadline**; up to 4 awards; cannot double-apply with Scholar same cycle). Cit: US not-for-profit institution required. (The former "Technological Innovations in Neuroscience / Memory & Cognitive Disorders" awards are no longer listed — verify before relying on them.) https://www.mcknight.org/programs/the-mcknight-endowment-fund-for-neuroscience/
- **Klingenstein-Simons Fellowship Awards in Neuroscience** — $150K/yr × 3 ($450K); PhD/MD with all training complete; tenure-track independent investigator with **no more than 4 years between the end of the last postdoc and the deadline**; basic or clinical neuroscience of neurological/psychiatric disease. Cit: any, US institution. LIMITED SUBMISSION at many schools (internal competition at the institution, typically Nov–Dec). Cadence: sponsor deadline ~mid-Feb. https://klingenstein.org/esther-a-joseph-klingenstein-fund/neuroscience/applying/
- **Whitehall Foundation** — Research Grants ($75K/yr up to 3yr) and Grants-in-Aid ($30K/1yr, for assistant profs / those without other funding); basic neurobiology, invertebrate & vertebrate. Cit: any, US institution. Cadence: LOI 3× per year (~Jan/Apr/Oct). Note: leans toward systems/sensorimotor and away from disease models — check fit. https://www.whitehall.org/
- **Dana Foundation** — Neuroscience & Society programs (NextGen, pilot projects); intersection of neuroscience with law, education, ethics, public life. ~$100–200K. Cit: check. Cadence: rolling / periodic RFPs. https://dana.org/
- **Simons Foundation** — SFARI (autism: Research Award, Bridge to Independence $495K/3yr for postdocs→faculty, Pilot); Simons Collaboration on the Global Brain — SCGB (theoretical/computational neuroscience, fellowships + pilot + collaboration); Simons Collaboration on Plasticity and the Aging Brain — SCPAB. Cit: any. Cadence: SFARI RFAs ~1–2×/yr; SCGB pilot/fellowship annual. https://www.simonsfoundation.org/funding-opportunities/
- **Kavli Foundation** — neuroscience institutes + special initiatives (neuro + AI, "NeuroAI", BRAIN-adjacent). Mostly works through Kavli Institutes (check whether the user's institution is one) and partner RFAs; watch for open competitions co-run with SfN / other funders. Cit: varies. https://kavlifoundation.org/
- **One Mind** — Rising Star Awards ($300K = $100K/yr × 3; early-career investigators in neuroscience/psychiatry; up to 5/yr; includes a Science Leaders development program). Cit: check. Cadence: application ~spring (2026 cycle closed Apr 27). https://onemind.org/what-we-do/one-mind-rising-star-academy/one-mind-rising-star-awards/
- **Brain Research Foundation** — Scientific Innovations Award ($150K/2yr, tenured/tenure-track assoc or full prof, novel high-risk) and Fay/Frank Seed Grant ($100K/2yr, assistant prof). LIMITED SUBMISSION (invited nominations from eligible institutions — check whether the user's institution is on the list). Cadence: ~Jan LOI. https://www.thebrainfoundation.org/
- **Klingenstein Third Generation Foundation** — depression & ADHD, child/adolescent focus; Fellowship for clinical researchers. Cit: check. Niche — only if profile hits child psychiatry / ADHD / depression.
- **Grass Foundation** — Grass Fellowships (early-career, MBL summer) and trainee support; mostly bench neurophysiology. Low priority for computational-only labs.
- **American Brain Foundation** (with the American Academy of Neurology) — Next Generation Research Grants, clinician-scientist heavy. Fit only if MD/DO or close neurology collaboration.
- **Foundation of Hope for Research and Treatment of Mental Illness** — NC-based (Raleigh); pilot/seed grants for psychiatry researchers in the Raleigh–Durham–Chapel Hill area (only if the user is there) ($30–50K/1yr). Cit: any. High yield for psychiatry PIs — check annual cycle (~spring). https://walkforhope.com/foundation-of-hope/

### American Heart Association (AHA) — cerebrovascular / brain health / AI (scan when the profile touches cardiovascular, cerebrovascular or brain health)

AHA funds cardiovascular **and** cerebrovascular/brain-health research, including dedicated brain-health and AI-themed programs. Research must be conducted at a US-based nonprofit institution; applicant must be an AHA Professional Member at time of submission (membership processing takes 3-5 days — budget for it). Citizenship: **not** citizen/PR-only — AHA accepts a broad range of visa categories (pending PR, E-3, H-1B, F-1, J-1, O-1, TN; DACA needs extra AHA approval) as long as the applicant holds the degree/career-stage requirement; confirm the specific visa category qualifies before dropping on a citizenship basis.

- **Career Development Award** — early-career faculty within ~6 years of first faculty appointment; ~$231,000 over 3 years (per third-party aggregator — verify against the primary RFP); cardiovascular **or** cerebrovascular research. Cadence: proposal deadline ~Dec 1 (2027 cycle: Dec 1, 2026). Drop for an established/tenured PI (same logic as Pew/Searle/Sloan). https://professional.heart.org/research-programs/aha-funding-opportunities
- **Innovative Project Award** — explicitly **no limit on career stage, academic rank, or discipline** (only requires a PhD/doctoral-level clinical degree and employment beyond the fellowship/training stage) — keeps for both early-career and established PIs. High-risk/unexplored ideas; no preliminary data required or accepted. $100,000/yr x 2 years (incl. 10% indirect). Two-stage: pre-proposal then invited full proposal. Cadence (2027 cycle): RFP posted ~Aug 14; pre-proposal due **Dec 9, 2026**; invitations ~Jan 21, 2027; full proposal ~Mar 4, 2027; award start Jul 1, 2027. https://professional.heart.org/en/research-programs/aha-funding-opportunities/innovative-project-award
- **"Novel AI Approaches to Advance Cardiovascular and Cerebrovascular/Brain Health"** — large special initiative, up to $4,000,000/award (up to 3 awards), 3 years; machine learning / generative AI / robotic process automation for cardiovascular and brain disease. **Currently archived/closed by AHA** (2026 cycle pre-proposal was ~Feb 2026) — direct, strong thematic fit for agentic-AI + brain-health profiles if it reopens. Put on the digest watch list; check for a reissue every run. https://atomgrants.com/grant/novel-ai-approaches-cardiovascular-cerebrovascular-brain-health-american-heart-association
- **Ralph L. Sacco Scholars Program (Brain Health)** — **trainee-facing, not for PI**: postdoctoral fellowship ($150,000/2yr) for MD/PhD/DrPH/DNP postdocs with <5 years research experience and no faculty rank, co-funded with the American Academy of Neurology; project must focus on prevention with a neurological or mental/behavioral-health angle (cardio/cerebrovascular link desirable but not required). Route to the "For Trainees" section. 2026 cycle deadline (Jan 29, 2026) has passed — watch for the 2027 RFP. https://professional.heart.org/en/research-programs/aha-funding-opportunities/ralph-l-sacco-scholars-program
- **Rapid Impact Research Award** — early- and mid-career investigators, stroke and/or vascular dementia among eligible topics; most recent cycle's deadline has passed — watch for reissue. https://www.instrumentl.com/grants/rapid-impact-research-award
- Also scan `professional.heart.org/research-programs/aha-funding-opportunities` each run for other open RFAs (e.g. Women's Health "heart to head to hormones" track) that might newly fit.

Search pattern: `American Heart Association funding opportunities <current-year>` then `web_fetch` the official funding-opportunities page directly (note: professional.heart.org has been unreachable by direct WebFetch in this environment — DNS resolution error consistent with grants.nih.gov/arpa-h.gov/nvidia.com; rely on WebSearch and corroborate across multiple results until direct fetch works).

### AD / ADRD / dementia-specific (scan when the profile touches neurodegeneration / ageing)

- **Alzheimer's Association** — the workhorse. Mechanisms: AARG (Research Grant, $150K/3yr, >10yr but still building program), AARG-D (diversity), AARGA (Research Grant For All, $200K/2–3yr, assistant prof ≤7yr, **international eligible**, 10% indirect cap), AARF / AARFA (fellowships, trainees), ABA (Advancing Research on AD/ADRD), Zenith (senior), Part the Cloud (therapy-focused). Cit: US + international depending on mechanism. LOI required for most. Cadence: main cycle LOI ~Aug, full app ~Oct; some mechanisms have a spring cycle. https://www.alz.org/research/for_researchers/grants/types-of-grants
- **BrightFocus Foundation** — Alzheimer's Disease Research (ADR): Standard Award up to $300K/3yr + Postdoctoral Fellowship $200K/2yr; also National Glaucoma Research and Macular Degeneration Research. Cit: any, any career stage, international eligible. **No LOI (changed) — single full-proposal window, historically ~June 1 → Sept 1** for funding starting the following summer. https://www.brightfocus.org/about/for-scientists/apply-for-a-research-grant/
- **Alzheimer's Drug Discovery Foundation (ADDF)** — Diagnostics Accelerator (DxA): Digital Biomarkers, Neuroimaging & Fluid Biomarkers, Peripheral Biomarkers programs — imaging/AI biomarkers with a "context of use" and commercialization path. Also drug-repurposing / target programs. Awards $100K–$3M, milestone-driven. Cit: any, for-profit and academic. Cadence: DxA runs targeted RFPs (currently *not* taking unsolicited apps — watch the funding-opportunities page); other ADDF programs take rolling LOIs. https://www.alzdiscovery.org/research-and-grants/funding-opportunities
- **Cure Alzheimer's Fund** — invitation / relationship-driven; high-risk biology. Approach via program staff. https://curealz.org/
- **Rainwater Charitable Foundation** — Tau Consortium + Rainwater Prize; tauopathies, FTD. Cit: any. Consortium membership is relationship-based; open RFPs occasionally. https://rainwatercharitablefoundation.org/
- **Association for Frontotemporal Degeneration (AFTD)** — pilot grants, ~$60–150K, FTD-specific. https://www.theaftd.org/
- **Lewy Body Dementia Association (LBDA)** — research grants, DLB-specific.
- **Global Brain Health Institute (GBHI)** — Atlantic Fellows for Equity in Brain Health; also GBHI/Alzheimer's Association "Pilot Awards in Global Brain Health Research" (~$100K/1yr). Cit: any, international. https://www.gbhi.org/
- **American Federation for Aging Research (AFAR)** — Glenn Foundation for Medical Research / AFAR Grants for Junior Faculty ($150K/2yr, MD/PhD within 10yr of training, tenure-track), Sagol Network GerroScience, New Investigator Awards. Cit: US/PR generally. Cadence: ~Dec/Jan LOI. https://www.afar.org/grants
- **Michael J. Fox Foundation** — Parkinson's; large open RFAs (biomarkers, digital, computational) several times a year. Cit: any, international. https://www.michaeljfox.org/grants
- **CHDI Foundation** — Huntington's; contract-style, relationship-driven.

### Biomedical broad / prestige early-career (many are LIMITED SUBMISSION — coordinate with your institution's research office early)

- **Howard Hughes Medical Institute (HHMI)** — Investigator Program (7-yr appointments, rare open competitions), Freeman Hrabowski Scholars, Hanna Gray Fellows (postdoc→faculty). Cit: any. Institutional/eligibility gating. https://www.hhmi.org/programs
- **Burroughs Wellcome Fund (BWF)** — Career Award at the Scientific Interface — CASI ($500K/5yr, postdoc→early faculty, quantitative-science-into-biology — strong fit for computational neuro/imaging), Investigators in the Pathogenesis of Infectious Disease, Collaborative Research Travel. Cit: US/Canada citizen/PR for CASI. LIMITED SUBMISSION for some. Cadence: CASI ~Sept. https://www.bwfund.org/
- **Pew Charitable Trusts** — Pew Scholars in the Biomedical Sciences ($300K/4yr, assistant prof appointed within the last 3yr as of the cycle). Cit: any but must hold a US appointment; **LIMITED SUBMISSION — one nominee per institution**. Cadence: nomination ~Sept. https://www.pewtrusts.org/en/projects/pew-biomedical-scholars
- **Searle Scholars Program** — $300K/3yr; assistant prof, appointment start date within a narrow window (~1st or 2nd year). Cit: any. **LIMITED SUBMISSION — 1–2 per institution**. Cadence: ~Sept. https://www.searlescholars.net/
- **Rita Allen Foundation** — Scholars ($110K/yr up to 5yr); early-career, within ~4yr of first appointment; cancer, immunology, neuroscience, pain. Cit: any, US/Canada institution. **LIMITED SUBMISSION**. Cadence: LOI ~Sept/Oct. https://ritaallen.org/
- **Alfred P. Sloan Foundation** — Sloan Research Fellowships ($75K/2yr); tenure-track but untenured as of Sept 15 of the nomination year; fields include neuroscience and computational & evolutionary molecular biology. Cit: any, US/Canada. **Nomination only — department head nominates (~3–4 nominees per field per institution); no self-application.** Cadence: nomination window ~July 15 → Sept 15. https://sloan.org/fellowships/apply
- **David & Lucile Packard Foundation** — Packard Fellowships for Science and Engineering ($875K/5yr); assistant prof in first 3yr. **LIMITED SUBMISSION — 2 per institution**, invited institutions only. Cadence: institutional nomination ~Feb–March. https://www.packard.org/what-we-fund/science/
- **Arnold and Mabel Beckman Foundation** — Beckman Young Investigator ($600K/4yr); within first 3–4yr of tenure-track appointment; chemistry & life sciences, instrumentation/methods favored. Cit: any, US institution. Cadence: ~Aug LOI. https://www.beckman-foundation.org/programs/beckman-young-investigator/
- **Research Corporation for Science Advancement** — Cottrell Scholar Award ($100K/3yr); 3rd-year tenure-track, PUI/PhD institutions, strong teaching component; physics/chemistry/astronomy (limited biomed fit). https://rescorp.org/
- **W. M. Keck Foundation** — Medical Research + Science & Engineering programs; high-risk, ~$1M; **LIMITED SUBMISSION, invited only**, counsel-driven pre-proposal via the institution's research office. Cadence: concept papers ~Feb & Aug internal. https://www.wmkeck.org/
- **Chan Zuckerberg Initiative (CZI)** — Ben Barres Early Career Acceleration, Neurodegeneration Challenge Network (NDCN) Collaborative Pairs / Ben Barres, imaging & AI-for-science RFAs, "Essential Open Source Software for Science" (tools). Cit: any, international. CZ Biohub network is SF/Chicago/NY only (institutions outside those areas are not eligible for Biohub investigator program). Cadence: RFA-driven, watch the RFA page. https://chanzuckerberg.com/rfa/
- **James S. McDonnell Foundation** — Understanding Human Cognition, Understanding Dynamic & Multi-scale Systems (complex systems / networks). Cit: any, international. Cadence: periodic — currently between major calls, watch. https://www.jsmf.org/
- **Human Frontier Science Program (HFSP)** — Research Grants (Program & Early Career, **intercontinental team required**, ~$400K/yr/team for 3yr, novel interdisciplinary), Long-Term & Cross-Disciplinary Fellowships. Cit: any; team must span countries. Cadence: LOI ~late March. https://www.hfsp.org/
- **Wellcome Trust / Wellcome Leap** — Wellcome Leap runs bold time-limited programs (e.g., mental health, "Untangling Addiction", multi-channel measurement) with fast contracting; Wellcome Trust Discovery Awards (mostly UK/LMIC-eligible — check). https://wellcomeleap.org/ , https://wellcome.org/grant-funding
- **John Templeton Foundation / Templeton World Charity Foundation** — neuroscience of consciousness, "Diverse Intelligences", complexity, free will. Cit: any, international. Large grants, distinctive scope. https://www.templeton.org/
- **Damon Runyon Cancer Research Foundation** — fellowships + Damon Runyon–Rachleff Innovation Award (early faculty, cancer). Trainee-facing mostly.

### AI / computing / data science (foundations & nonprofits — company programs are in the next section)

- **Schmidt Sciences** (formerly Schmidt Futures) — AI2050 Fellows (Eric & Wendy Schmidt; early-career = within 10yr of PhD, and senior tracks; $300K–$500K/3yr for early-career; "hard problems in AI for a better 2050") — **closed nomination process, no open application**; Schmidt AI in Science Postdoctoral Fellowships (cohort programs at partner universities); Science of Trustworthy AI; Polymath Program (mid-career, high-risk). Cit: any, international. https://www.schmidtsciences.org/
- **Open Philanthropy** — AI safety & alignment, biosecurity & pandemic preparedness, "Career Development and Transition" funding; large and flexible, rolling. Cit: any. https://www.openphilanthropy.org/request-for-proposals/
- **Simons Foundation — Mathematical & Physical Sciences** — Collaboration Grants, Targeted Grants in MPS, **Simons Pivot Fellowship** (mid-career researchers making a substantive field change — relevant for a PI pivoting into multi-omics or a new method area, ~1yr full support + transition). Cit: any. https://www.simonsfoundation.org/mathematics-physical-sciences/
- **Mozilla Foundation / other "responsible AI" funders** — trustworthy and ethical AI; small, mission-specific. Only if the profile has an explicit fairness/ethics angle.
- **Patrick J. McGovern Foundation** — AI for humanity / data & society; program-driven, relationship-based.
- **Sloan Foundation — Technology** — "Better Software for Science", metascience, digital infrastructure. https://sloan.org/programs/digital-technology

### Aging / diabetes / other disease (scan when profile calls for it)

- **JDRF / Breakthrough T1D** — type 1 diabetes; large open RFAs including AI/data.
- **American Diabetes Association** — research grants.
- **Larry L. Hillblom Foundation** — aging & diabetes, California institutions only (drop otherwise).
- **Glenn Foundation for Medical Research** — biology of aging (via AFAR, above).
- **Alzheimer's Association / GBHI / BrightFocus** — see the AD section above.

## Industry research awards (tech / pharma / hardware)

These are corporate-sponsored academic research programs. Most are unrestricted gifts or sponsored research agreements rather than grants — different IP and reporting terms apply, but the application process is usually lighter than federal. Award sizes range from $25K cash + cloud credits up to $200K+ for multi-year academic-industry programs. Always good fits for AI/ML/computing-heavy labs.

**Important characteristics to flag in the digest:**
- Most require alignment with the company's stated research priorities for that cycle (re-published twice yearly for some, annually for others)
- Many include cloud credits, GPU allocations, or product/model access in addition to (or instead of) cash
- IP terms vary widely — some are pure gifts, others require company first-rights, right-of-first-negotiation, or co-publication review. **Always flag "route through your institution's Office of Sponsored Programs / OTC for IP review"** — a gift agreement and a sponsored-research agreement have very different terms.
- US institution status often required; some explicitly include international institutions
- Cash amounts are usually modest ($25K–$150K). Value is often the compute + the named company collaborator + the door it opens, not the dollars — weight accordingly against the profile's minimum-useful-award.
- Credit-only / compute-only programs (no cash) are near-zero-effort and pair well with a pending federal grant — list them but keep them in the low/glance tier unless the profile explicitly wants compute.

### Tech — AI / cloud / computing (cash + credits)

- **Amazon Research Awards (ARA)** — twice-yearly (Spring call ~March–May, Fall call ~Sept–Nov). Rotating themed calls: **Amazon 2030**, **AWS Agentic AI**, automated reasoning, ML, NLP, robotics, AWS AI, sustainability. Up to ~$80K unrestricted + $40K+ AWS credits + Amazon research contact. Cit: any (US + many international institutions). The "agentic AI for scientific discovery / health sciences" theme fits profiles in AI / health sciences. `amazon.science/research-awards/call-for-proposals`
- **Google Academic Research Awards (GARA)** — **new consolidated program that replaced the Research Scholar Program and the older Google Research Awards** (2024→). Up to $100K unrestricted + Google Cloud credits + a named Google research sponsor. Faculty worldwide, no fixed career-stage limit. **The topic list changes each cycle and can be narrow** (the 2026 cycle was quantum-computing-only, deadline Aug 7, 2026) — check the published themes before assuming a fit. Annual, application window ~mid-year → ~Aug. `research.google/programs-and-events/google-academic-research-awards/`
- **Google.org AI for Health / AI Collaboratives / Impact Challenges** — larger philanthropic grants for applied health AI; themed, periodic.
- **Google DeepMind** — academic partnerships and the DeepMind Fellowship / scholarships (mostly trainee-facing); research collaborations are relationship-driven.
- **Microsoft Accelerating Foundation Models Research (AFMR)** — Azure OpenAI + model credits + early access for academics; three goal areas incl. "accelerating scientific discovery". Cohort/rolling. **Now expanding under the Agentic AI Research and Innovation (AARI) initiative** — Grand Challenges + academic collaboration on agentic systems; watch for the AARI academic call. `microsoft.com/en-us/research/collaboration/accelerating-foundation-models-research/`
- **Microsoft Research Faculty Fellowship** — early-career (within ~5–7yr of faculty appt), ~$200K over 2yr. Nomination-based, ~1–2 nominees/institution → effectively LIMITED SUBMISSION. Annual, ~Sept. `microsoft.com/en-us/research/academic-program/faculty-fellowship`
- **Microsoft AI for Good / AI for Health** — Azure compute + cash, themed, rolling. `microsoft.com/en-us/ai/ai-for-good`
- **Meta (FAIR) research awards / RFPs** — periodic themed RFPs ("foundational AI", "responsible AI", systems, LLM evaluation); unrestricted gifts ~$50–100K. `research.facebook.com/research-awards`
- **OpenAI Researcher Access Program** — API credits (typically up to ~$25–50K equivalent) for published research; rolling. Also periodic themed RFPs (safety, agents, economic impact). `openai.com/form/researcher-access-program`
- **Anthropic AI for Science Program** — Claude API credits, **up to ~$50K/project** (expanded 2026 beyond biology to math/engineering/etc.); academic + nonprofit researchers, international eligible. **Rolling — applications reviewed the first Monday of each month.** Also **Claude for Science / Claude Team seats for scientists** (free/discounted subscriptions) and periodic themed tracks (e.g. rare disease). Credits, not cash. `anthropic.com/ai-for-science-program-rules`
- **Samsung Global Research Outreach (GRO)** — annual (call ~Jan, proposals ~March), ~$100K/1yr renewable; AI, health sensing, on-device ML. International eligible. `samsung.com/global/business/aits/main/gro/`
- **Sony Research Award Program** — **Focused Research Award** (up to $150K USD, collaborative research with a Sony team) + **Faculty Innovation Award** (up to $100K USD, pioneering independent research). PI must be a full-time faculty member/researcher eligible to supervise PhD students (assistant prof and up). Areas: AI, robotics, sensing, imaging, sustainability, entertainment tech. Annual; **application deadline ~mid-September** (2026 cycle: Sept 15). US + many international institutions. Sponsored research / gift — route via the institution's sponsored-programs office. `sony.com/en/SonyInfo/research-award-program/`
- **Qualcomm Innovation Fellowship** (trainee pairs) + Qualcomm faculty gifts.
- **Cisco Research** — grants & gifts, themed (AI, security, sustainability); rolling RFPs. `research.cisco.com`
- **Salesforce / Snowflake / Databricks academic programs** — mostly credits + data; occasional AI research gifts.
- **Toyota Research Institute (TRI)** — university research collaborations (ML, robotics, materials, human-centered AI); relationship-driven, not an open RFP.
- **J.P. Morgan AI Research Awards** — annual (~spring), themed around ML + finance/data; some healthcare/foundational tracks. `jpmorgan.com/technology/artificial-intelligence/research-awards`
- **Intel / IBM research collaborations & gifts** — discretionary; IBM also runs university programs (IBM-Illinois-style joint labs) periodically.

### Hardware / compute (in-kind — no cash, near-zero-effort, keep in low tier unless profile wants compute)

- **NVIDIA Academic Grant Program** — GPU compute (up to ~30,000 H100 GPU-hours) plus hardware for some tracks (up to 2 DGX Spark units). Three tracks when open: *AI Training & Model Development*, *Simulation & Modeling*, and *AI Inference, Agents & Systems Software* (agentic systems / distributed inference / LLMs — relevant for AI-systems profiles). **Status flip-flops:** nvidia.com has read "not accepting new applications" while university TTO feeds list an active cycle (e.g. an Oct 1 deadline) — check BOTH nvidia.com and a TTO feed before relying on a date. Also **NVIDIA Applied Research Accelerator Program**. `nvidia.com/en-us/industries/higher-education-research/academic-grant-program/`
- **AWS Cloud Credit for Research** / **AWS IMAGINE Grant** (nonprofits) / AWS Health Equity Initiative.
- **Google Cloud Research Credits** / Google Cloud Research Innovators.
- **Microsoft Azure for Research** / AFMR credits (above).
- **Oracle for Research** — cloud credits.
- **AMD University Program / Instinct GPU donations**; **Cerebras** and **Lambda** academic compute programs; **Hugging Face** community/academic compute (ZeroGPU, Enterprise for academia) — all worth a one-line mention for a compute-heavy foundation-model lab.
- **NAIRR Pilot** (National AI Research Resource, NSF-led) — allocations of compute + data + model access for US researchers; not a company program but belongs on this checklist. `nairrpilot.org`

### Semiconductors / systems consortia

- **Semiconductor Research Corporation (SRC)** — JUMP 2.0, GRC, AI Hardware (AIHW); consortium-style, multi-institution.

### Pharma / biotech industry–academic (for AD/ADRD, psychiatry, multi-omics translational angles)

- **Biogen** — investigator-initiated research + collaborations in Alzheimer's, MS, neuromuscular, neuropsychiatry; digital biomarkers. Route via medical affairs / research collaborations.
- **Eisai** — Alzheimer's (lecanemab); Alzheimer's biomarker & real-world-evidence collaborations.
- **Eli Lilly Research Award Program (LRAP)** — thematic cycles incl. neuroscience/AD and pain; also donanemab-adjacent AD work. `lillyresearchawards.com`
- **Genentech / Roche** — gRED / Roche research collaborations and the Genentech Innovation Fund; neuroscience & computational pipelines; Roche also runs postdoc fellowships and an "Applied Data Science" collaboration track.
- **Takeda, AbbVie, Bristol Myers Squibb, Johnson & Johnson (J&J Impact Ventures / WiSTEM2D), Sanofi (iAwards), GSK, Boehringer Ingelheim (incl. Grants4Targets), UCB, Amgen, Regeneron, Gilead (Research Scholars Program), Merck (MISP), Novartis, AstraZeneca, Bayer (Grants4Targets)** — each runs an investigator-initiated / independent-research-grant program, therapeutic-area-gated; search "<company> investigator initiated research" + the year. Neuro/psych and immunology programs are the most relevant here.
- **Novo Nordisk Foundation** — very large; Data Science Investigator grants, Challenge Programmes, and health-AI initiatives; funds internationally (not only Denmark). Worth a targeted check for data-science-in-health framing. `novonordiskfonden.dk/en/`

### University tech-transfer & open-innovation feeds (fast way to catch corporate RFPs with real dates)

Corporate research awards and open-innovation challenges are poorly indexed by web search but well-curated by university technology-transfer offices, which syndicate the same listings with deadlines. Check these every run and pull anything AI / ML / imaging / sensing / neuro / health-relevant:

- **The user's own institution's technology-transfer / commercialization office** — industry-opportunity and corporate-challenge listings. First stop; ask the user which institution.
- **Vanderbilt CTTC "Upcoming Deadlines / Industry Opportunities"** — `vanderbilt.edu/cttc/industry-collaborations/` — a well-maintained public list of corporate research awards and challenges (Sony, NVIDIA, J&J QuickFire, Pfizer RFPs, Bayer, P&G, Kimberly-Clark, …) with dates. The Vanderbilt-disclosed-technology entries don't apply to a PI without such a startup, but the open corporate awards do — treat it as a free national industry-RFP calendar.
- **Halo (`halo.science`)** — the platform behind many of those university-page listings; corporate R&D challenges (Pfizer, Bayer, P&G, Kimberly-Clark, etc.). Free researcher accounts; filter by field.
- **NineSigma**, **HeroX**, **yet2**, **IdeaConnection** — open-innovation challenge marketplaces; occasional AI / health / imaging challenges.
- **Grants.gov saved search + NIH Guide weekly email + NSF "upcoming due dates"** — the federal equivalents; set up standing alerts.
- **Cross-check every hit against the company's own program page** — TTO feeds lag, and a listed date is often a past cycle (e.g. NVIDIA's own page may say "closed" while a feed still lists it).

### Search / verification note for industry awards

Company cycles change frequently and closed calls stay indexed for months. When a snippet shows a "current" cycle, open the official page and confirm the deadline year explicitly. Many of these are gifts, not grants — always add the "OSP / OTC IP review" flag in the digest.

## Limited-submission / institutional-nomination programs

Many of the best foundation awards cap how many applicants an institution may put forward (often 1–2). These require an **internal competition through the institution's research office**, with an internal deadline typically **6–10 weeks before the sponsor deadline**. If one of these is a strong profile fit, the digest must flag it in the dedicated Limited Submission section (🏛️) and tell the PI to contact the institution's research office (limited-submissions staff) *now* — missing the internal deadline means missing the cycle entirely.

Recurring limited-submission programs (examples, mostly biomedical / quantitative science):

| Program | Sponsor | Typical institutional cap | Career stage |
|---|---|---|---|
| Pew Scholars in the Biomedical Sciences | Pew | 1 | Assistant prof, ≤3yr |
| Searle Scholars | Kinship Foundation | 1–2 | Assistant prof, 1st–2nd yr |
| Packard Fellowships for Science & Engineering | Packard | 2 (invited institutions) | Assistant prof, ≤3yr |
| Beckman Young Investigator | Beckman Foundation | often 1–2 | Tenure-track, ≤3–4yr |
| Rita Allen Foundation Scholars | Rita Allen | 1 | Early-career, ≤4yr |
| Sloan Research Fellowship | Sloan | 3–4 per field (chair nominates) | ≤6yr from PhD |
| Klingenstein-Simons Fellowship | Klingenstein Fund / Simons | varies | ≤4yr faculty |
| W. M. Keck Medical Research / Science & Engineering | Keck | 1, invited | any |
| Brain Research Foundation (SIA / Seed) | BRF | invited nominations | assoc/full (SIA), assistant (Seed) |
| Research Corporation Cottrell Scholar | RCSA | varies | 3rd-yr tenure-track |
| V Foundation V Scholar | V Foundation | often 1–2 | early-career |
| Vannevar Bush Faculty Fellowship | DoD | varies, invited | mid-career+ |

Always confirm the current year's cap on the institution's limited-submissions calendar — sponsors change the rules.

## Institutional programmes

Ask the user which institution they are at and search **that** institution's research-office pages (internal pilot / seed / bridge funding, clinical-translational pilots, centre pilots, AI/data-science seed funds, imaging- or core-facility pilots, limited-submission calendar). Do not carry over another institution's list.

## Search query strategy

For each source category, run 2-4 searches max. Better to do a few targeted queries than many broad ones. Combine the source-specific patterns above with the profile's top 2-3 keywords.

### Foundation search patterns

Foundations are under-indexed by generic "grants for X" searches. Go direct:

- `<foundation name> <program name> <current-year> deadline` — e.g. `BrightFocus Alzheimer's Disease Research 2027 LOI deadline`
- `<foundation name> funding opportunities` then `web_fetch` the opportunities/RFA page directly (most foundations keep a single canonical page)
- `<research area> foundation grant early career faculty <current-year>` — e.g. `computational neuroscience foundation grant assistant professor 2027`
- `<disease> foundation research grant RFP <current-year>` — e.g. `frontotemporal dementia foundation research grant RFP 2027`
- For limited-submission programs: also search `<institution> limited submissions <program name>` to see the internal deadline (e.g. `<institution> limited submissions Pew Scholars`)
- Cross-check against the institution's limited-submissions calendar and the InfoEd / Pivot-RP feed if reachable

For each foundation that survives the profile filter, `web_fetch` the program page and confirm: current-cycle deadline (and LOI date), award size, career-stage window, citizenship rule, indirect-cost cap, and whether it is limited submission.

### Industry award search patterns

Companies say "research award" / "call for proposals" / "request for proposals", not "grant":

- `Amazon Research Awards <call name> <current-year> call for proposals` (check both Spring and Fall)
- `Google Academic Research Awards GARA <current-year> deadline` (the Research Scholar Program is retired — do not cite it)
- `Microsoft AFMR <current-year>` and `Microsoft Agentic AI Research Innovation AARI academic call`
- `Microsoft Research Faculty Fellowship <current-year>`
- `Meta research RFP <topic> <current-year>`
- `Anthropic AI for Science program <current-year>` / `OpenAI researcher access program <current-year>`
- `Samsung Global Research Outreach <current-year> call`
- `Sony Research Award Program <current-year>`
- `NVIDIA academic grant program <current-year>`
- `<pharma company> investigator initiated research <therapeutic-area> <current-year>`
- `Novo Nordisk Foundation data science <current-year>`

Industry cycles change fast and closed calls stay indexed — open the official page and confirm the deadline **year** explicitly before listing.

### Federal search patterns (example only — replace the keywords by the confirmed profile's)

- `NIH <institute> R01 <keyword> <keyword> <current-year>`
- `NIH <initiative relevant to the field> open solicitations <current-year>`
- `NSF <program> <keyword>` / `NSF <directorate> solicitation <current-year>`
- `CDMRP <program> FY<current-year>`
- `ARPA-H open funding opportunity <field> <current-year>`

### Budgeting the run

Roughly 2–4 searches per source category. A full run is ~20–30 searches + ~10–15 `web_fetch` verifications. Prioritise: (1) NIH Guide, (2) the foundation lists that match the confirmed field, (3) NSF, (4) industry AI awards, (5) DoD/ARPA-H, (6) the user's institution's programmes + limited submissions. If time-boxed, always cover 1–3.

After each search, `web_fetch` the most promising 2–3 announcement pages to get accurate deadlines and eligibility before listing in the digest.