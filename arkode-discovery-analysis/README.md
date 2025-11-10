# Arkode Discovery Analysis Skill

## What This Skill Does

This skill analyzes client discovery call transcripts and creates comprehensive **AS-IS Process Documentation + Gap Analysis** for HubSpot CRM optimization projects.

**Input:** Discovery call transcripts, sales brief, client industry
**Output:** 5,000-7,000 word analysis document with process flow, gaps, and prioritized opportunities
**Time:** ~1 conversation session (typically 50-100 turns)

---

## When to Use

- Starting the "clarity phase" of an Arkode process optimization project
- Client has completed discovery calls/interviews
- Need to document current state before designing TO-BE process
- First step in the Arkode 4-skill methodology

---

## Key Features

### 🎯 Evidence-Based Analysis
- **NO hallucination** - Everything grounded in transcripts
- Direct stakeholder quotes
- Assumptions clearly marked
- Gaps flagged when information missing

### 📊 Structured Output
- 15-25 detailed process steps
- 15-25 gaps across 7 dimensions
- 3-5 Quick Wins identified
- 5-8 baseline metrics
- Stakeholder matrix
- Prioritization matrix

### 🏭 Industry-Specific Context
- Templates for common industries (Higher Education, Healthcare, Professional Services, etc.)
- Real examples from past projects
- HubSpot-specific gap analysis
- Common patterns pre-identified

### ⚖️ Optimized for Context Limits
- Lean SKILL.md (500 lines)
- Progressive reference loading (load only what's needed)
- Strict word count limits (no bloat)
- Won't hit Claude.ai max length

---

## How to Use

### Step 1: Prepare Your Files

Gather discovery materials:
- Discovery call transcript(s) (.txt or .md format)
- Sales brief or client questionnaire
- Any existing process documentation

### Step 2: Start Conversation

In Claude.ai or Claude Code:

```
Use the arkode-discovery-analysis skill to analyze discovery calls for [Client Name]'s [Process Name] process.

Industry: [Higher Education / Healthcare / Professional Services / etc.]
```

Upload your transcript files.

### Step 3: Claude Analyzes

The skill will:
1. Load industry template for context
2. Load AS-IS and gap analysis frameworks
3. Analyze your transcripts (evidence-based)
4. Create AS-IS documentation (15-25 steps)
5. Conduct gap analysis (7 dimensions)
6. Prioritize opportunities (Quick Wins, Core, Strategic)
7. Deliver complete analysis document (5,000-7,000 words)

### Step 4: Review & Iterate

- Claude delivers the analysis document
- Review for accuracy
- Request clarifications or additions
- Claude updates based on feedback

### Step 5: Next Phase

Take the output to **arkode-process-design** skill for TO-BE design.

---

## What You'll Get

### Deliverable: Complete Analysis Document

**Sections included:**
1. Executive Summary (150 words)
2. Stakeholder Matrix (5-10 people)
3. AS-IS Process Flow (15-25 detailed steps)
4. Information Flow Analysis
5. Current State Challenges (8-12 issues)
6. Current State Metrics (5-8 KPIs)
7. Gap Analysis (7 dimensions, 15-25 total gaps)
8. Opportunity Prioritization Matrix
9. Recommended Next Steps (Quick Wins + Core Improvements)

**Length:** 5,000-7,000 words (concise, actionable)

**Quality:** 100% evidence-based, no invented content

---

## Skill Architecture (How It Works)

### Progressive Loading Strategy

```
SKILL.md (500 lines - always loaded)
    ↓
Industry Template (600 lines - loaded based on user input)
    ↓
AS-IS Framework (1,500 lines - loaded when needed)
    ↓
Gap Analysis Framework (1,500 lines - loaded when needed)
    ↓
Quality Checklist (loaded before delivery)
```

**Total context:** ~10,000 tokens
**Remaining for conversation:** 190,000 tokens
**Result:** Won't hit max length limits

### Files Structure

```
arkode-discovery-analysis/
├── SKILL.md (Main instructions)
├── references/
│   ├── as-is-framework.md (AS-IS methodology)
│   ├── gap-analysis-framework.md (7-dimension framework)
│   ├── hubspot-context.md (HubSpot-specific considerations)
│   ├── quality-checklist.md (Pre-delivery verification)
│   └── industry-templates/
│       └── higher-education.md (Industry-specific examples)
└── assets/
    └── as-is-output-template.md (Exact output format)
```

---

## Industries Supported

### Currently Available Templates

1. **Higher Education** ✅
   - Student recruitment, admissions, enrollment
   - Based on real higher ed projects (e.g., Bermuda College)

### Coming Soon

2. Healthcare
3. Professional Services
4. Financial Services
5. SaaS/Technology

### Other Industries

For industries without templates, Claude works purely from your transcripts (no template context loaded).

---

## Anti-Hallucination Features

### 🚨 Safeguards Built-In

- **Required evidence:** Won't proceed without transcripts
- **Direct quotes:** Uses stakeholder's actual words
- **Marked assumptions:** `[ASSUMPTION: ...]` tags
- **Flagged gaps:** `[CLARIFICATION NEEDED: ...]` tags
- **No generic content:** Everything client-specific
- **Word count limits:** Forces prioritization (no bloating)
- **Quality checklist:** 50+ verification points before delivery

---

## Example Usage

**User:**
```
Use arkode-discovery-analysis skill to analyze discovery calls for Riverside University's student recruitment process.

Industry: Higher Education

[Uploads 3 discovery call transcripts]
```

**Claude:**
1. Loads higher-education.md template
2. Loads AS-IS framework
3. Analyzes transcripts
4. Extracts 22 process steps
5. Identifies 18 gaps across 7 dimensions
6. Creates prioritization matrix
7. Identifies 4 Quick Wins
8. Delivers 6,200-word analysis document

**Output Document Includes:**
- Executive summary of recruitment process challenges
- 5 stakeholder profiles (R.O.s, Admins, Director, IT, Marketing)
- 22-step AS-IS process (inquiry → enrollment)
- 18 gaps categorized by dimension
- 4 Quick Wins (instant confirmation emails, auto-assignment, dashboard, follow-up automation)
- 5 Core Improvements (integration with SIS, automated status updates, etc.)
- Baseline metrics (200 inquiries/month, 4-6 hour response time, 35% conversion)

**Time to complete:** 1 conversation session

**Next step:** TO-BE design with arkode-process-design skill

---

## Tips for Best Results

### ✅ Do This

- **Upload complete transcripts** - More context = better analysis
- **Specify industry** - Loads relevant template
- **Include sales brief** - Provides additional context
- **Be specific about process scope** - "Student recruitment" not "everything"
- **Review and iterate** - Request clarifications if needed

### ❌ Avoid This

- **Don't skip transcripts** - Skill requires evidence
- **Don't expect generic "best practices"** - Analysis is client-specific
- **Don't request TO-BE design** - That's a separate skill
- **Don't expect exhaustive lists** - Skill prioritizes (15-25 gaps max)

---

## What Happens Next

After this skill delivers the analysis:

### Option 1: Review with Client
- Share analysis document with client
- Validate accuracy
- Gather additional context
- Update document if needed

### Option 2: Proceed to TO-BE Design
- Use arkode-process-design skill
- Input: This analysis document
- Output: Optimized TO-BE process for HubSpot

### Option 3: Iterate
- Request additional analysis
- Explore specific gaps deeper
- Add clarifications

**This skill does NOT:**
- Design TO-BE processes (use arkode-process-design)
- Create swimlane diagrams (use arkode-swimlane-mapping)
- Create implementation documents (use arkode-implementation-master)
- Create client presentations (separate skill or manual)

---

## Troubleshooting

**Issue:** "I don't have discovery transcripts"
- **Solution:** Skill requires transcripts. Conduct discovery calls first or provide interview notes.

**Issue:** "Output is too generic"
- **Solution:** Provide more detailed transcripts. Skill is evidence-based; more evidence = more specific analysis.

**Issue:** "Missing my specific industry"
- **Solution:** Select "Other" as industry. Claude will work purely from your transcripts without template.

**Issue:** "Document is incomplete"
- **Solution:** Run quality checklist. Ask Claude to verify all sections present.

**Issue:** "Need more gaps identified"
- **Solution:** Skill limits to 15-25 prioritized gaps (not exhaustive). Focus on Quick Wins and Core Improvements.

---

## Contact & Support

**Created by:** Arkode
**Part of:** Arkode Process Optimization Methodology (4-skill suite)
**Version:** 1.0

**Related Skills:**
- arkode-process-design (Skill 2 - TO-BE design)
- arkode-swimlane-mapping (Skill 3 - Visual process maps)
- arkode-implementation-master (Skill 4 - Implementation documents)

---

**Ready to analyze your first project? Upload transcripts and let's go!**
