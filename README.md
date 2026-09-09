# Can AI Models Evaluate Resumes Objectively?

**A structured comparison of Claude, ChatGPT, and Gemini as resume reviewers**

---

## Research Question

When given identical inputs, do AI models evaluate resumes on consistent criteria — or do they optimise for the output they produced?

---

## Method

Three resume variants for the same candidate were generated using Claude, ChatGPT, and Gemini, each tailored for a **Market Intelligence Analyst** role. All three covered identical underlying experience; the differences were structural and framing-level — opening sentence, skills placement, section labelling, and curation of less-relevant roles.

The generation was controlled: every model received the **same six-prompt sequence** (spot the flaws → rewrite for impact → ATS boost → craft the hook → upgrade experience → format fix), working from the same source history. The full prompt text is in [`prompts-used.md`](./prompts-used.md).

Each model was then shown all three finished resumes and asked a single question:

> *"Of these 3 resumes, which would you choose for a Market Intelligence Analyst role?"*

Each model evaluated its own output alongside the other two **without being told which it had written.**

**Evidence in this folder:**
- Source input: [`Source_LinkedIn_Profile.pdf`](./Source_LinkedIn_Profile.pdf) (attached to all three models)
- Resumes: [`Claude_Resume.pdf`](./Claude_Resume.pdf) · [`ChatGPT_Resume.pdf`](./ChatGPT_Resume.pdf) · [`Gemini_Resume.pdf`](./Gemini_Resume.pdf)
- Full model responses: [`transcript-claude.md`](./transcript-claude.md) · [`transcript-chatgpt.md`](./transcript-chatgpt.md) · [`transcript-gemini.md`](./transcript-gemini.md)
- Underlying project (the posting datasets referenced in the resumes): [LinkedIn-Market-Analysis](https://github.com/Shiv-1801/LinkedIn-Market-Analysis) — first search (4,949 postings) plus the "August Update" second scrape

---

## The Three Resumes, Side by Side

Every model was working from the same career history. What differed was how each chose to frame it:

| Dimension | Claude (Resume 3) | ChatGPT (Resume 1) | Gemini (Resume 2) |
|-----------|-------------------|--------------------|--------------------|
| **Opening line** | Leads with *evidence*: "Built a market intelligence pipeline that scraped, classified, and segmented 4,949 LinkedIn job postings across 10 countries — independently, from research question to deployed live tool" | Leads with *positioning*: "Market Intelligence Analyst specialising in competitive intelligence, industry trends, market sizing, and data-driven research" | Leads with *bridge framing*: "Market Intelligence Analyst bridging custom Python web-scraping pipelines… to transform raw web data into executive insights" |
| **Skills placement** | Bottom of page | Bottom of page | Front-loaded, immediately after summary |
| **Project section label** | "Projects" | "Projects" | "Market Intelligence Projects" |
| **Digital Marketing Intern role** | Retained (Chennai Super Kings, 15M+ followers) | Retained | **Dropped** — curated out as marketing noise |
| **Social-media metrics in experience** | Retained (1.25M+ follower growth, 800M+ impressions) | Retained, reframed toward analysis | Stripped out |
| **AI-native tools named** | Explicit — "Claude (workflow integration, prompt engineering, RAG)" | Named in skills | Named in skills |
| **Postings-count claim** | 4,949 (first search) | 4,949 + 3,897 (first search + August Update) | **"8,800+"** (combined total of both searches) |

---

## Results

| Model | Picked | Primary Reasoning |
|-------|--------|-------------------|
| **Claude** | Its own (Resume 3) | Strongest MI credential in the opening line; only version naming AI-native tools explicitly |
| **ChatGPT** | Its own (Resume 1) | Experience section most effectively bridges digital-marketing background to MI; scored its version 9.5/10 across 9 dimensions |
| **Gemini** | Its own (Resume 2) | Aggressive curation of irrelevant roles; skills front-loaded above experience; explicit "Market Intelligence Projects" label |

**All three models picked themselves. None picked a competitor's output.**

---

## Key Findings

**1. Self-preference bias — present and unanimous**
Each model, blind to authorship, ranked its own resume first. The bias was consistent across all three systems.

**2. Convergent synthesis (unprompted)**
Claude and ChatGPT independently recommended the *same* hybrid without seeing each other's answers: take Claude's evidence-led opening sentence, build ChatGPT's experience architecture around it, and apply Gemini's curation logic (drop the social-media metrics, strip the marketing noise). Neither was asked to synthesise — both arrived there on their own. Gemini did not propose a hybrid; it defended its own version outright.

**3. A shared flag — that was actually a false positive**
Both Claude and ChatGPT independently flagged the same figure in Gemini's version: its "8,800+ job postings," which both read as a round-number credibility risk. ChatGPT put it plainly: *"round-number claims get scrutinised in analyst interviews."* Neither was prompted to check anything; both landed on the same caution unprompted.

But the flag was wrong. "8,800+" is the true combined total — the original 4,949-posting search plus a second "August Update" scrape (~3,897 more), together ~8,846 — all documented in the project's public repository ([LinkedIn-Market-Analysis](https://github.com/Shiv-1801/LinkedIn-Market-Analysis)). The attached LinkedIn profile mentioned only the first search's 4,949, so the two reviewing models saw a larger, rounder number they couldn't verify and advised against it. Gemini's figure reflected the fuller dataset and was sound; the reviewers were being cautious without the context to know it.

The lesson cuts both ways: two models will independently converge on flagging an aggregate they can't verify, and that shared instinct can be confidently wrong. A reviewer without your receipts penalises your most complete number precisely because it's the one they can't see behind.

**4. Evaluation criteria differed by model**
- **Claude** prioritised: opening-line evidence, AI-native skill visibility
- **ChatGPT** prioritised: experience-section narrative, recruiter readability, precision of claims
- **Gemini** prioritised: structural choices — skills placement, section labelling, ruthless curation

All three treated the opening sentence as the primary signal, but weighted everything else differently.

---

## Inference

Self-preference bias is present and consistent across all three models. But the bias does not preclude useful analysis: both Claude and ChatGPT acknowledged weaknesses in their own output and identified specific strengths in the others. The convergent hybrid recommendation — arrived at independently — suggests the models are applying partially overlapping criteria beneath the surface-level disagreement.

The more useful output of this experiment is not *"which resume wins"* but the **evaluation frameworks each model revealed through its reasoning.** Read together, the three transcripts function as three different expert lenses on the same document, and the places where two of them converge unprompted are the strongest signal of what to weigh. That convergence is a strong signal, not an infallible one: where Claude and ChatGPT agreed on flagging the "8,800+" figure, they agreed *and* were wrong (see Finding 3). Convergence tells you where to look, not always what the answer is.

The resume ultimately submitted was a hybrid nobody wrote: assembled from what each model got right and warned against in the others.

---

## Limitations

- Single candidate, single target role — findings are not generalisable
- Models may have been influenced by stylistic patterns in their own training outputs
- No human-recruiter baseline for comparison
- Authorship was hidden but not adversarially controlled; a stronger design would randomise resume order and labels across multiple trials

---

## Tools

Python · Prompt engineering · Structured comparison design
