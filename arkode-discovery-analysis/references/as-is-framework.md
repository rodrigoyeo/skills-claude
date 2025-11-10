# AS-IS Process Analysis Framework

## Purpose

This framework guides the creation of current state (AS-IS) process documentation from discovery call transcripts.

---

## Analysis Principles

### 1. Evidence-Based Documentation
- Document what IS happening, not what SHOULD happen
- Capture reality, including workarounds and exceptions
- Quote stakeholders directly
- Note variations and inconsistencies

### 2. Appropriate Detail Level
- Granular enough to identify problems
- High-level enough to be understandable
- Target: 15-25 main process steps
- Sub-steps can provide detail without bloat

### 3. Multi-Perspective View
- Capture each stakeholder's experience
- Note where perspectives differ
- Identify information asymmetries
- Show handoff points between roles

---

## What to Extract from Transcripts

### Process Steps
For each step in the current process, identify:

**Core Elements:**
- **Step number and name** - Sequential, descriptive
- **Actor** - Who performs this (role, not just name)
- **Trigger** - What initiates this step
- **Actions** - What they do (be specific)
- **Tools/Systems** - What they use
- **Output** - What is created/delivered
- **Duration** - How long it takes
- **Dependencies** - What must happen first

**Pain Points:**
- What's frustrating about this step?
- Where do errors occur?
- What takes too long?
- What requires manual workarounds?

**Evidence Markers:**
- Direct quotes about this step
- Specific examples mentioned
- Frequency indicators ("every time," "daily," "often")

### Stakeholders
For each person/role involved:

**Identify:**
- Role/title
- Name (if mentioned)
- Responsibilities in this process
- Current tools they use
- Time spent on this process
- Pain points they experience
- What they wish they could see/do

**Quote Directly:**
Capture their frustrations in their own words:
> "I spend 2 hours every morning just checking if anyone responded to my emails."

### Current Systems & Tools
Document the technology landscape:

**List:**
- CRM (if any) - platform, usage level, limitations
- Spreadsheets - who maintains, what data, how shared
- Email - used for what workflows
- Paper/Forms - what still happens manually
- Other systems - ERP, SIS, project management, etc.

**Note:**
- Integration status (connected or siloed?)
- Data flow between systems
- Manual data entry/transfers
- Access/permission issues

### Process Metrics (Current State Baseline)
Find any quantifiable data:

**Volume Metrics:**
- How many instances per day/week/month?
- Seasonal variations?
- Growth trends?

**Timing Metrics:**
- Average processing time?
- Response time expectations?
- Wait times or delays?

**Quality Metrics:**
- Error rates?
- Customer satisfaction (if mentioned)?
- Completion rates?

**Efficiency Metrics:**
- Manual touchpoints count?
- Number of handoffs?
- Data re-entry instances?

---

## Process Documentation Structure

### Step Format (Target: 50-75 words per step)

```markdown
**Step [N]: [Descriptive Step Name]**

- **Actor:** [Role who performs this]
- **Trigger:** [What initiates this step]
- **Actions:**
  - [Action 1 - specific]
  - [Action 2 - specific]
  - [Action 3 - if applicable]
- **Tools/Systems:** [What they use]
- **Output:** [What is created/delivered]
- **Time:** [Duration]
- **Dependencies:** [What must happen first]
- **Pain Points:** [Problems with this step]

[Optional: Direct quote from transcript about this step]
```

**Example:**

**Step 5: Recruitment Officer Attempts Initial Contact**

- **Actor:** Recruitment Officer
- **Trigger:** Inquiry assigned in morning batch email
- **Actions:**
  - Check email for new inquiry notification
  - Open attached PDF form to see inquiry details
  - Manually create contact record in spreadsheet
  - Call prospective student's phone number
  - If no answer, send manual email from Outlook
  - Log attempt in spreadsheet
- **Tools/Systems:** Email (Outlook), Excel spreadsheet, Phone
- **Output:** Contact attempt logged, possible conversation
- **Time:** 10-15 minutes per inquiry
- **Dependencies:** Morning batch email sent by IT
- **Pain Points:** No visibility if someone else already contacted them, manual data entry, no automatic follow-up

> "By the time I see the inquiry in my email, it could be hours old. I have no idea if it's been contacted already." - Recruitment Officer

### Consolidation Guidelines

**When to combine steps:**
- Sequential actions by same person with no waiting
- Tightly coupled sub-tasks
- Example: "Open email" + "Read email" + "Forward email" = "Process incoming email"

**When to separate steps:**
- Different actors involved
- Significant time gap between actions
- Decision points
- Handoffs
- Example: Don't combine "Submit form" (customer) + "Review form" (staff)

---

## Information Flow Analysis

### Data Sources
Identify where information currently lives:

**Common Sources:**
- CRM database (if exists)
- Spreadsheets (who owns, where stored)
- Email inboxes
- Paper forms
- Legacy systems
- Personal notes/memory ("tribal knowledge")
- External systems (vendor platforms, government databases)

### Data Movement
Map how information flows (or doesn't):

**Questions to Answer:**
- How does data move from source A to source B?
- Is it automated or manual?
- How often does it sync?
- What gets lost in translation?
- Where does data need to be re-entered?

**Red Flags:**
- "I export from System A and import to System B"
- "Someone emails me the spreadsheet"
- "I manually type it into..."
- "I have to ask [person] for that information"

### Data Quality Issues
Identify data problems:

**Common Issues:**
- **Incomplete:** Missing required fields
- **Inconsistent:** Different values for same thing
- **Duplicate:** Same record in multiple places
- **Stale:** Out-of-date information
- **Inaccessible:** Can't find when needed
- **Unstructured:** Free-text instead of structured fields

---

## Current State Challenges Framework

### Challenge Categories

Organize pain points into these categories:

1. **Visibility Issues**
   - What can't stakeholders see that they need to?
   - What requires asking someone else?
   - What can't be tracked or reported?

2. **Speed/Efficiency Issues**
   - What takes too long?
   - What's manual that should be automated?
   - Where do requests sit in queue?

3. **Communication Issues**
   - Where do handoffs fail?
   - What requires meetings/calls that shouldn't?
   - What notifications are missing?

4. **Data Quality Issues**
   - Where is data incomplete?
   - Where is re-entry required?
   - What validation is missing?

5. **Customer Experience Issues**
   - Where do customers face delays?
   - What creates confusion?
   - Where do customers repeat information?

6. **Scalability Issues**
   - What breaks with more volume?
   - What are single points of failure?
   - What can't grow without adding headcount?

7. **Reporting/Analytics Issues**
   - What can't be measured?
   - What questions can't be answered?
   - What reports require manual compilation?

### Challenge Documentation Format

| Category | Specific Issue | Business Impact | Frequency | Affected Stakeholders |
|----------|----------------|-----------------|-----------|----------------------|
| Visibility | Can't see inquiry status without asking | Delays in response, duplicate outreach | Daily | Recruitment Officers (5), Management (2) |

---

## Analysis Best Practices

### Listen for Signal Words

**Frustration signals:**
- "It's difficult to..."
- "We can't see..."
- "I have to check..."
- "There's no way to..."
- "It would be helpful if..."

**Frequency indicators:**
- "Usually" (indicates variation - probe deeper)
- "Sometimes" (inconsistent process)
- "Always" (possible automation opportunity)
- "Never" (gap or constraint)

**Workaround signals:**
- "What I do is..."
- "I've created a spreadsheet that..."
- "We have a system where..."
- "The unofficial process is..."

### Mark Uncertainties

When transcripts are unclear, mark it:

**Assumptions:**
`[ASSUMPTION: Inquiries are assigned round-robin, but not explicitly stated]`

**Gaps:**
`[CLARIFICATION NEEDED: Timeline for response not mentioned in discovery]`

**Contradictions:**
`[NOTE: R.O. said "within 1 hour" but Admin said "by end of day" - needs clarification]`

### Use Client Terminology

Capture their exact language:
- If they call it "inquiry," don't say "lead"
- If they say "programs," don't say "products"
- If they use acronyms, use the same acronyms
- If they have status names, use those exact names

This ensures the document resonates with stakeholders.

---

## Edge Cases & Exceptions

Don't just document the "happy path." Identify:

**Exception Scenarios:**
- What happens when normal process can't be followed?
- How are unusual situations handled?
- What manual overrides exist?
- What escalation paths are used?

**Example Edge Cases:**
- International students (different requirements)
- Transfer students (different evaluation process)
- Late applications (rushed process)
- Incomplete information (waiting/follow-up process)

Document these separately:

```markdown
### Edge Cases

**Scenario 1: Incomplete Inquiry Form**
- Current handling: R.O. manually emails to request missing info
- Frequency: ~20% of inquiries
- Pain point: No tracking of follow-up status

**Scenario 2: Transfer Credit Evaluation**
- Current handling: Manual review by academic admin, 5-10 days
- Frequency: ~30% of applicants
- Pain point: Delays enrollment decision, no visibility into evaluation status
```

---

## Baseline Metrics Table

Even if metrics are rough estimates, document them:

| Metric | Current Value | How Measured | Data Quality |
|--------|---------------|--------------|--------------|
| Inquiries per month | ~200 | Manual count in spreadsheet | Low (estimated) |
| Average response time | 4-6 hours | Not measured | Unknown |
| Inquiry-to-application rate | ~40% | Manual calculation quarterly | Medium |
| Application-to-enrollment | ~60% | SIS report | High |
| R.O. time per inquiry | 30-45 min total | Estimated | Low |

This establishes baseline for measuring TO-BE improvement.

---

## Common Patterns to Recognize

### Pattern: Email as Task Management
**Signals:**
- "I keep emails in my inbox as reminders"
- "I flag emails I need to follow up on"
- "I search my sent folder to see if I contacted them"

**Problem:** No shared visibility, things get missed, no automation possible

### Pattern: Spreadsheet as Database
**Signals:**
- "I maintain a spreadsheet of..."
- "I track [data] in Excel"
- "Someone emails me the updated spreadsheet"

**Problem:** No real-time sync, version control issues, manual updates

### Pattern: Tribal Knowledge
**Signals:**
- "I just know that..."
- "We have to ask [person] about..."
- "It's not written down anywhere"

**Problem:** Single point of failure, inconsistent execution, onboarding difficulty

### Pattern: Manual Follow-Up
**Signals:**
- "I set a reminder to follow up"
- "I check back in a few days"
- "I send reminder emails"

**Problem:** Time-consuming, inconsistent, doesn't scale

### Pattern: Status via Meetings
**Signals:**
- "We discuss status in our weekly meeting"
- "I ask in standup if anyone's heard from..."
- "We review the list together"

**Problem:** Delayed visibility, synchronous requirement, inefficient

---

## Final Checklist for AS-IS Documentation

Before considering AS-IS complete, verify:

- [ ] 15-25 main process steps documented
- [ ] Each step has all required elements (actor, trigger, actions, etc.)
- [ ] 5-10 stakeholders identified with roles and pain points
- [ ] Current tools/systems listed
- [ ] Direct quotes from transcripts included
- [ ] Information flow mapped (where data lives and moves)
- [ ] 8-12 specific challenges identified across categories
- [ ] Baseline metrics documented (even if rough)
- [ ] Edge cases noted
- [ ] Assumptions and gaps clearly marked
- [ ] Client's terminology used consistently
- [ ] Total AS-IS section: 3,000-4,000 words

---

## What NOT to Include in AS-IS

❌ **Solutions or recommendations** (save for TO-BE)
❌ **Generic best practices** (without connection to transcripts)
❌ **Invented details** (only what's in transcripts)
❌ **Idealized processes** (document reality, not aspirations)
❌ **Technical jargon** (unless client used it)
❌ **Exhaustive detail** (prioritize signal over noise)
