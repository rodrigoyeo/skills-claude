---
name: arkode-discovery-analysis
description: Analyzes client discovery calls to create AS-IS process documentation and gap analysis for HubSpot CRM optimization projects. Use this skill when starting the clarity phase of an Arkode process optimization engagement. Produces concise, evidence-based analysis with NO hallucination.
---

# Arkode Discovery Analysis

## Purpose

Transform discovery call transcripts into structured AS-IS + Gap Analysis documentation that identifies process inefficiencies and optimization opportunities for HubSpot CRM implementation.

**Single Deliverable:** Combined AS-IS + Gap Analysis document (5,000-7,000 words MAX)

**Keywords:** discovery analysis, AS-IS documentation, gap analysis, process optimization, HubSpot CRM, clarity phase, current state analysis

---

## When to Use This Skill

Use this skill when:
- Starting a new HubSpot process optimization project
- Client has completed discovery calls/interviews
- Need to document current state before designing TO-BE process
- Beginning the "clarity phase" of an Arkode engagement

**Do NOT use for:**
- TO-BE process design (use arkode-process-design skill)
- Creating implementation documents
- Executive presentations

---

## Critical Rules (Anti-Hallucination)

🚨 **STOP if user hasn't uploaded discovery transcripts**

**NEVER:**
- ❌ Invent stakeholder names, quotes, or process details
- ❌ Create generic "typical" processes without evidence
- ❌ Exceed specified word count limits
- ❌ Use vague language ("typically," "often," "usually")
- ❌ Add content beyond what's in transcripts

**ALWAYS:**
- ✅ Quote transcripts directly (use quotation marks)
- ✅ Mark assumptions clearly: `[ASSUMPTION: ...]`
- ✅ Flag missing information: `[CLARIFICATION NEEDED: ...]`
- ✅ Use client's exact terminology
- ✅ Stay within word count limits
- ✅ Base every statement on evidence from transcripts

---

## Required Inputs

Before proceeding, user MUST provide:
- [ ] Discovery call transcript(s) (.txt or .md format)
- [ ] Sales brief or client questionnaire (optional but helpful)
- [ ] Client industry

**If missing transcripts:** ASK for them. Do NOT proceed.

---

## Workflow (7 Steps)

### Step 1: Identify Client Industry

Ask user: **"What industry is this client in?"**

**Options:**
1. Higher Education (universities, colleges, training institutions)
2. Healthcare (hospitals, clinics, medical practices)
3. Professional Services (law firms, accounting, consulting)
4. Financial Services (banks, insurance, fintech)
5. SaaS/Technology (software companies, tech services)
6. Other (user specifies)

**Once answered:**
- Read `references/industry-templates/[industry].md` for context and examples
- Use this template as reference for common patterns in this industry
- DO NOT load template if industry is "Other" - work from transcripts only

---

### Step 2: Load Core Frameworks

Read these reference files in order:

1. **`references/as-is-framework.md`** - AS-IS analysis methodology
2. **`references/gap-analysis-framework.md`** - Gap analysis methodology
3. **`references/hubspot-context.md`** - HubSpot-specific considerations

**Note:** Only read what you need. If discovery is simple, you may not need all frameworks.

---

### Step 3: Analyze Discovery Transcripts

Extract from uploaded transcripts (with evidence):

**What to Extract:**
- Process steps (target: 15-25 steps - not more)
- Stakeholders (5-10 key people with roles)
- Pain points (8-12 specific, prioritized issues)
- Current tools/systems being used
- Direct quotes from stakeholders
- Current metrics/volumes (if mentioned)
- Edge cases or exceptions

**How to Extract:**
- Quote verbatim when possible
- Note who said what (role, not just name)
- Capture specific language (their terminology)
- Identify patterns across multiple stakeholders
- Note contradictions or uncertainties

**Flag Gaps:**
If transcripts don't cover something important, mark:
`[CLARIFICATION NEEDED: Timeline expectations not discussed]`

---

### Step 4: Create AS-IS Documentation

Follow structure in `assets/as-is-output-template.md`

**Required Sections with Word Limits:**

1. **Executive Summary** (150 words MAX)
   - What process is being analyzed
   - Key stakeholders
   - Top 3 challenges

2. **Stakeholder Matrix** (Table: 5-8 rows)
   - Role, Name, Responsibilities, Current Tools, Pain Points

3. **AS-IS Process Flow** (15-25 numbered steps)
   - Each step: 50-75 words max
   - Format: Actor, Trigger, Actions, Tools, Output, Time, Pain Points

4. **Information Flow Analysis** (200-300 words)
   - Where data lives
   - How it moves (or doesn't)
   - Data quality issues

5. **Challenges Summary** (Table: 8-12 issues)
   - Category, Issue, Impact, Frequency, Affected Stakeholders

6. **Current State Metrics** (Table: 5-8 baseline KPIs)
   - What can be measured today (even if poorly)

**Total AS-IS Section: 3,000-4,000 words**

---

### Step 5: Conduct Gap Analysis

Analyze across 7 dimensions using `references/gap-analysis-framework.md`:

1. **Visibility Gaps** - What can't stakeholders see?
2. **Speed/Efficiency Gaps** - What's too slow or manual?
3. **Data Quality Gaps** - Where is data incomplete/inconsistent?
4. **Communication Gaps** - Where do handoffs fail?
5. **Customer Experience Gaps** - Where do customers struggle?
6. **Scalability Gaps** - What breaks under volume?
7. **Reporting Gaps** - What can't be measured?

**Constraint:** Identify 15-25 total gaps across all dimensions
- Focus on HIGH IMPACT gaps
- Prioritize over exhaustive listing
- Use evidence from transcripts

**Output:** One table per dimension (3-5 gaps each)

**Total Gap Analysis Section: 2,000-3,000 words**

---

### Step 6: Prioritize Opportunities

Create Impact/Complexity Matrix:

| Opportunity | Impact | Complexity | Priority | Category |
|-------------|--------|------------|----------|----------|
| [Description] | H/M/L | H/M/L | 1-5 | [Category] |

**Categorize:**
- **Quick Wins** (High Impact + Low Complexity) → Priority 1
- **Core Improvements** (High Impact + Med Complexity) → Priority 2
- **Strategic Investments** (High Impact + High Complexity) → Priority 3
- **Easy Additions** (Med/Low Impact + Low Complexity) → Priority 4
- **Deprioritize** (Med/Low Impact + High Complexity) → Priority 5

**Identify:**
- 3-5 Quick Wins
- 3-5 Core Improvements
- 2-4 Strategic Investments

---

### Step 7: Quality Check & Deliver

Before delivering, verify using `references/quality-checklist.md`:

**Required Checks:**
- [ ] Industry template loaded and used as reference
- [ ] All data sourced from transcripts (no invented content)
- [ ] Executive summary ≤ 150 words
- [ ] 15-25 process steps (not more, not less)
- [ ] 8-12 challenges identified
- [ ] Direct quotes included with quotation marks
- [ ] Assumptions marked with [ASSUMPTION: ...]
- [ ] Gaps marked with [CLARIFICATION NEEDED: ...]
- [ ] Output matches template format
- [ ] Total document 5,000-7,000 words
- [ ] All 7 gap dimensions analyzed
- [ ] Opportunities prioritized in matrix

**If any check fails:** STOP and fix before delivering.

---

## Output Specifications

**Format:** Markdown document

**Structure:**
```
# AS-IS Process Analysis & Gap Identification
## [Client Name] - [Process Name]

### Executive Summary
[150 words]

### Stakeholder Matrix
[Table]

### AS-IS Process Flow
[15-25 detailed steps]

### Information Flow Analysis
[200-300 words]

### Current State Challenges
[Table with 8-12 issues]

### Current State Metrics
[Table with 5-8 KPIs]

### Gap Analysis

#### 1. Visibility & Transparency Gaps
[Table with 3-5 gaps]

#### 2. Speed & Efficiency Gaps
[Table with 3-5 gaps]

[... continue for all 7 dimensions]

### Opportunity Prioritization Matrix
[Table]

### Recommended Next Steps
- Quick Win 1: [Description]
- Quick Win 2: [Description]
- Core Improvement 1: [Description]
- Core Improvement 2: [Description]
```

**Length Constraints:**
- Executive Summary: 150 words
- Each process step: 50-75 words
- Information Flow: 200-300 words
- Gap Analysis per dimension: 300-500 words
- **Total Document: 5,000-7,000 words (FIRM LIMIT)**

---

## After Completion

**Deliver to user:**
1. The AS-IS + Gap Analysis markdown document
2. Summary statement: "Discovery analysis complete. Ready for TO-BE design phase."

**User's next step:**
→ Take this document to **arkode-process-design** skill for TO-BE design

**DO NOT:**
- Automatically proceed to TO-BE design
- Create implementation documents
- Generate swimlane diagrams
- This skill ONLY does discovery analysis

---

## Example Usage

**User:** "I need to analyze discovery calls for a university recruitment process. Here's the transcript..."

**Claude:**
1. "What industry is this client in?" → User: "Higher Education"
2. Loads `industry-templates/higher-education.md`
3. Loads AS-IS framework
4. Analyzes transcript
5. Extracts 20 process steps
6. Identifies 10 pain points
7. Creates AS-IS documentation (4,000 words)
8. Conducts gap analysis across 7 dimensions
9. Prioritizes 15 opportunities
10. Delivers complete 6,500-word document
11. "Analysis complete. Ready for TO-BE design."

---

## Resources

### Reference Files (Load as Needed)
- **Framework:** `references/as-is-framework.md` (AS-IS methodology)
- **Framework:** `references/gap-analysis-framework.md` (Gap analysis)
- **Context:** `references/hubspot-context.md` (HubSpot specifics)
- **Template:** `references/industry-templates/[industry].md` (Industry examples)
- **Quality:** `references/quality-checklist.md` (Final verification)

### Assets
- **Output Template:** `assets/as-is-output-template.md` (Exact format)

### When to Load What
- **Always load:** Industry template (if not "Other")
- **Load when needed:** AS-IS framework (if unfamiliar with methodology)
- **Load when needed:** Gap analysis framework (for gap dimensions)
- **Load before delivery:** Quality checklist (final verification)

---

## Troubleshooting

**"I don't have discovery transcripts"**
→ STOP. Ask user to provide them. Do NOT proceed without evidence.

**"Transcript is vague or incomplete"**
→ Mark gaps clearly with [CLARIFICATION NEEDED: ...] throughout document

**"Client is in unusual industry"**
→ Select "Other" and work purely from transcripts without template

**"Process is very complex (50+ steps)"**
→ Consolidate steps. Group sequential actions by same person.
→ Target: 15-25 high-level steps with sub-actions

**"I'm generating too much content"**
→ STOP. Check word counts. Cut ruthlessly to stay within limits.
→ Quality > Quantity. Prioritize insights over exhaustive lists.

**"Not sure what's a 'gap'"**
→ Load `references/gap-analysis-framework.md` for examples

---

## Notes

- This skill focuses on ANALYSIS, not DESIGN
- Output is INPUT for next skill (arkode-process-design)
- Conciseness is critical - clients want insights, not novels
- Evidence-based only - no generic best practices without context
- When in doubt, ask user for clarification rather than assume
