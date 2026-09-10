# Profile + CV refresh for LUNIT application

Date: 2026-09-09. Scope: 5 user-numbered items. Working repos:
`/home/nguyen/gh-profile` (profile README), `/home/nguyen/ngocdung03.github.io`
(Jekyll portfolio), `aio25-mix002/m01-p0102` (GitHub, remote only),
`ngocdung03/ADnewsHD` (GitHub + local clone), new peer dir `/home/nguyen/App_lunit`.

## Verified state (evidence)

| Claim | Evidence |
|---|---|
| Flask appears exactly once in profile README | `grep -rn -i flask /home/nguyen/gh-profile` → `README.md:192` (shields.io badge) |
| Flask already removed from portfolio site | `git log origin/main..HEAD` in `ngocdung03.github.io` → commit `efe480c "Remove Flask from skills list"`, unpushed |
| Portfolio has unrelated uncommitted work | `git diff --stat` → 4 files, all `Seoul` → `Seongnam`. Do not touch. |
| ADnewsHD highlighted in profile | `README.md` "Featured Research Code" section, `### 📰 [ADnewsHD]` block |
| `m01-p0102` is a Streamlit RAG chatbot | `rag_chatbot.py` (13 KB): LangChain `ConversationalRetrievalChain`, Chroma vector store, `lmsys/vicuna-7b-v1.5` under 4-bit NF4 BitsAndBytes, `bkai-foundation-models/vietnamese-bi-encoder` embeddings, `SemanticChunker`, `ConversationBufferMemory` |
| `m01-p0102` is org-owned, user is admin | `gh api repos/aio25-mix002/m01-p0102` → `permissions.admin: true`; contributors `hung-doan`, `DrJeys` |
| `dementia_can` has NO code or data | `ls -la /home/nguyen/dementia_can` → single subdir `research_proposal/` holding `proposal.tex`, `proposal.pdf`, 3 drawio PNGs. No `src/`, no data, no results. |
| Proposal content | `proposal.tex` §1–§10: CLSA Comprehensive Cohort n=30,000, non-mydriatic 45° TRC-NW8 fundus photography, incident dementia (ICD-10), 3 candidate pipelines (multimodal intermediate fusion; M2M transfer; segmentation-guided), no OCT/OCTA in CLSA |
| Canonical CV source | `/home/nguyen/App_aigen/application/NguyenNgocDung_CV.html` (15.7 KB) → PDF; site copy at `ngocdung03.github.io/files/NguyenNgocDung_CV.pdf`, site page `cv.html` |

## Decisions taken (user, 2026-09-09)

1. **CLSA dementia work is labelled a research proposal only.** No implied model,
   metrics, or trained artefact anywhere in CV/profile/site. Rationale: no code
   exists on disk; claiming otherwise would be fabrication.
2. **New LUNIT portfolio project = clinical RAG evaluation harness**, in
   `/home/nguyen/App_lunit/`, peer to `App_aigen/`. Closes the LLM/RAG gap named
   in `App_aigen/README.md` and matches LUNIT "Clinical Intelligence".

## Work items

### 1. Remove Flask
- Delete the Flask badge line `gh-profile/README.md:192`.
- Site already done (commit `efe480c`); nothing further.

### 2. Un-highlight + privatise ADnewsHD
- Delete the `### 📰 [ADnewsHD]` block from profile README "Featured Research Code".
- `gh repo edit ngocdung03/ADnewsHD --visibility private --accept-visibility-change-consequences`.
- Consequence to confirm with user: private repo loses public stars/forks/pages,
  and any link to it from the site breaks. Grep site for ADnewsHD first.

### 3. Rename + rewrite `m01-p0102` → `rag-chatbot-streamlit`
- `gh repo rename rag-chatbot-streamlit -R aio25-mix002/m01-p0102`.
- GitHub keeps a redirect from the old path; teammates' remotes keep working.
- Rewrite README: what it is, why RAG, architecture (loader → SemanticChunker →
  bi-encoder embeddings → Chroma → Vicuna-7B 4-bit → conversational chain),
  quickstart, Colab link, limitations. Keep existing setup instructions.
- Add repo description via `gh repo edit --description`.
- Add a highlight block in profile README.
- Attribution: shared team repo (`hung-doan`, `DrJeys`) — profile wording must say
  team project, not solo.

### 4. `/home/nguyen/App_lunit/` — LUNIT campaign dir
Structure mirrors `App_aigen/`:
```
App_lunit/
  README.md          campaign index
  jd.txt             role description as given
  research/role-fit.md   requirement-by-requirement evidence map
  application/       CV rewrite target
  project/clineval/  the clinical RAG eval harness (scaffold only today)
```
CV/profile/site edits from this item:
- Add "Research Proposals" entry: *Retinal Imaging and AI for Dementia Risk
  Prediction — CLSA Comprehensive Cohort* (2026), explicitly a proposal.
- Add `rag-chatbot-streamlit` under projects.
- Add LLM/RAG line to skills: LangChain, Chroma, Hugging Face Transformers,
  quantized inference. All backed by `m01-p0102` code — verified above.
- Do NOT add: PEFT/LoRA, MIMIC/OMOP/FHIR, agents. No evidence.

### 5. Portfolio site
- New `_projects/rag-chatbot.md` (order after existing 3).
- New `_projects/dementia-retinal-proposal.md` marked as proposal, or an
  "In progress / Proposals" block on `index.html` — choose the collection file so
  it renders with existing layout.
- Update `cv.html` skills + a proposals section.
- Leave the uncommitted Seoul→Seongnam diff untouched; commit separately.

## Status — 2026-09-10

All five items complete and verified.

The CV document was the one gap left open on 2026-09-09: `cv.html` on the site had been
updated but the CV *document* had not. Resolved by making
`App_lunit/application/NguyenNgocDung_CV.html` the canonical LUNIT-targeted copy (seeded
from the Aug 25 `App_aigen` version, which already carried the CHORALE metric correction),
retargeting it, rendering to PDF with headless chromium, and publishing to
`ngocdung03.github.io/files/`. The site's previous PDF dated 2026-08-18 and predated both
the correction and every addition here.

Known divergence, left alone deliberately: the site's `cv.html` page is thinner than the
PDF — it omits CHORALE, the CanAttend deployment, and the manuscripts in preparation. That
predates this work.

## Success criteria
- `grep -ri flask /home/nguyen/gh-profile` → no hits.
- `gh repo view ngocdung03/ADnewsHD --json isPrivate` → `true`.
- `gh repo view aio25-mix002/rag-chatbot-streamlit` resolves.
- No string in CV/profile/site asserts a trained dementia model or any metric.
- Both repos push clean; site builds (`bundle exec jekyll build`) if Ruby present.
