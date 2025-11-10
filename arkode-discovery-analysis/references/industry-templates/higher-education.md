# Higher Education Industry Template

## Purpose

This template provides examples and patterns specific to higher education institutions implementing HubSpot CRM for student recruitment, admissions, and related processes.

---

## Common Processes in Higher Education

### 1. Student Recruitment (Most Common)
**Inquiry → Application → Enrollment**

**Typical Scope:**
- Prospective student inquiry capture
- Recruitment officer follow-up and qualification
- Application submission and processing
- Admissions decision
- Enrollment confirmation

**Volume:** 100-5,000 inquiries per year (varies widely by institution size)

### 2. Student Retention & Advising
**Enrollment → Graduation**

**Typical Scope:**
- Academic advising touchpoints
- Early alert systems (at-risk students)
- Re-enrollment campaigns
- Student success tracking

### 3. Alumni Relations
**Graduation → Lifelong Engagement**

**Typical Scope:**
- Alumni database management
- Event invitations
- Career services
- Networking facilitation

### 4. Fundraising & Development
**Donor Cultivation → Gift**

**Typical Scope:**
- Prospect research
- Cultivation activities
- Campaign management
- Donor stewardship

**Note:** This template focuses primarily on **Student Recruitment** as it's the most common HubSpot use case.

---

## Typical Stakeholders in Student Recruitment

| Role | Typical Count | Responsibilities | Common Tools | Pain Points |
|------|---------------|------------------|--------------|-------------|
| Recruitment Officers (R.O.) | 5-15 | Manage inquiries, qualify prospects, guide through application | Email, phone, spreadsheet, SIS | No pipeline visibility, manual follow-ups, can't track activities |
| Admissions/Registration Admin | 2-5 | Process applications, evaluate credentials, make decisions, send acceptance letters | SIS, email, paper forms | Manual data entry, no integration with recruitment, delayed handoffs |
| Enrollment Management Director | 1-2 | Oversee recruitment strategy, monitor metrics, allocate resources | Spreadsheets, reports from SIS | No real-time metrics, manual report compilation, can't identify bottlenecks |
| IT/Systems Administrator | 1-3 | Maintain SIS, manage integrations, support tech issues | SIS backend, server access | Data silos between systems, manual exports/imports, integration requests backlogged |
| Marketing/Outreach Coordinator | 1-3 | Generate inquiries, manage campaigns, website | Website CMS, social media, email marketing | Can't track inquiry sources, no closed-loop reporting on campaign ROI |
| Academic Advisors | 10-30 | Student support, course planning, retention | SIS, email, paper files | Don't know recruitment status, late handoff from recruitment to advising |

---

## Sample AS-IS Process: Student Recruitment

This is a composite example based on common higher education patterns:

### Step 1: Prospective Student Submits Inquiry

- **Actor:** Prospective Student
- **Trigger:** Finds college website, clicks "Request Information"
- **Actions:**
  - Fills out web form (name, email, phone, program interest)
  - Clicks "Submit"
- **Tools/Systems:** College website form
- **Output:** Form submission sent to generic email inbox
- **Time:** 2-3 minutes (for student)
- **Dependencies:** Website form functioning
- **Pain Points:** No immediate confirmation, no tracking of submission

> "We get inquiries through the website form, but sometimes they go to spam and we don't see them for days." - Admissions Admin

### Step 2: IT Receives Form Notification

- **Actor:** IT Department (automated process)
- **Trigger:** Form submission
- **Actions:**
  - Form data sent to generic email inbox (admissions@college.edu)
  - Email includes inquiry details as plain text
- **Tools/Systems:** Website form backend, Email server
- **Output:** Email notification in shared inbox
- **Time:** Immediate
- **Dependencies:** Email server working
- **Pain Points:** Shared inbox creates confusion about who should respond

### Step 3: Admissions Admin Reviews Inbox (Batch Process)

- **Actor:** Admissions Admin
- **Trigger:** Periodic check (usually morning and afternoon)
- **Actions:**
  - Opens admissions@college.edu inbox
  - Reviews new inquiry emails
  - Manually creates row in Excel spreadsheet "Master Inquiry List"
  - Copies inquiry details from email to spreadsheet
  - Determines which R.O. should receive based on program interest
  - Forwards email to assigned R.O.
- **Tools/Systems:** Outlook, Excel spreadsheet (on shared drive)
- **Output:** Email forwarded to R.O., row added to spreadsheet
- **Time:** 5-10 minutes per inquiry
- **Dependencies:** Admin availability, access to spreadsheet
- **Pain Points:** Manual data entry, batch processing causes delays (up to 4 hours), no automatic assignment

> "I check the inbox twice a day. If an inquiry comes in at 10 AM, it might not get assigned until 2 PM." - Admissions Admin

### Step 4: Recruitment Officer Receives Assignment

- **Actor:** Recruitment Officer
- **Trigger:** Forwarded email from Admin
- **Actions:**
  - Checks email
  - Reads inquiry details
  - Manually adds inquiry to personal tracking system (Excel or paper notes)
  - Plans to make first contact
- **Tools/Systems:** Email, personal Excel or notebook
- **Output:** R.O. aware of new inquiry
- **Time:** 5 minutes
- **Dependencies:** R.O. checking email
- **Pain Points:** No centralized tracking, can't see colleague workloads, no SLA enforcement

### Step 5: R.O. Attempts Initial Contact

- **Actor:** Recruitment Officer
- **Trigger:** R.O. availability (usually within 1-4 hours of assignment)
- **Actions:**
  - Looks up phone number in email
  - Calls prospective student
  - If no answer: Leaves voicemail
  - Sends manual follow-up email from personal email
  - Logs attempt in personal tracking system (not visible to others)
- **Tools/Systems:** Phone, Outlook, personal Excel
- **Output:** Contact attempt made and logged privately
- **Time:** 10-15 minutes per attempt
- **Dependencies:** R.O. availability, phone number valid
- **Pain Points:** No shared visibility, manual logging, no template for consistency, no automatic follow-up

> "I try to call within an hour if I can, but sometimes I'm in meetings or on calls with other students. I keep my own notes because the spreadsheet is too slow to update." - Recruitment Officer

### Step 6: Follow-Up Attempts (If No Initial Contact)

- **Actor:** Recruitment Officer
- **Trigger:** R.O. reminder (mental note or calendar reminder)
- **Actions:**
  - Checks personal tracking system for non-responders
  - Attempts contact again (phone or email)
  - Logs attempt manually
  - Repeats every 2-3 days (varies by R.O.)
- **Tools/Systems:** Phone, email, personal tracking
- **Output:** Additional contact attempts
- **Time:** 5-10 minutes per attempt
- **Dependencies:** R.O. remembering to follow up
- **Pain Points:** Inconsistent follow-up frequency, some inquiries fall through cracks, no automated reminders

> "I try to follow up 3 times, but honestly sometimes I forget. It's all manual." - Recruitment Officer

### Step 7: Contact Established (Two-Way Conversation)

- **Actor:** Recruitment Officer + Prospective Student
- **Trigger:** Student answers phone or replies to email
- **Actions:**
  - R.O. discusses student's goals, program interest, timeline
  - Answers questions about college, programs, costs
  - Sends informational materials via email
  - Updates personal tracking to "Contacted"
  - Updates Master Spreadsheet status (when has time)
- **Tools/Systems:** Phone, email, personal notes, spreadsheet
- **Output:** Relationship established, student informed
- **Time:** 20-45 minutes (conversation + follow-up)
- **Dependencies:** Student engagement
- **Pain Points:** Conversation details not shared with team, spreadsheet update delayed (not real-time)

### Step 8: Qualification & Nurturing

- **Actor:** Recruitment Officer
- **Trigger:** Ongoing relationship
- **Actions:**
  - Periodic check-ins via email/phone
  - Invites to campus tour, open house events
  - Sends program-specific materials
  - Manually tracks engagement in personal notes
  - Assesses readiness to apply
- **Tools/Systems:** Email, phone, event registration system (separate), personal notes
- **Output:** Student progress toward application decision
- **Time:** Varies (weeks to months)
- **Dependencies:** Student responsiveness, R.O. bandwidth
- **Pain Points:** Hard to track engagement across multiple touchpoints, no automated event invitations, can't see who's "hot" vs "cold"

> "I have no idea if a student opened the email I sent or clicked on the campus tour link. I'm flying blind." - Recruitment Officer

### Step 9: Application Encouragement

- **Actor:** Recruitment Officer
- **Trigger:** Student indicates interest in applying
- **Actions:**
  - Provides application link/instructions
  - Explains required documents
  - Offers assistance with application process
  - Sets mental reminder to check if application submitted
- **Tools/Systems:** Email, application portal (separate system)
- **Output:** Student directed to apply
- **Time:** 15-30 minutes
- **Dependencies:** Application portal working
- **Pain Points:** Can't see if student started application, no automatic reminders if student doesn't complete

### Step 10: Application Submitted (System Transition)

- **Actor:** Prospective Student
- **Trigger:** Student completes and submits application
- **Actions:**
  - Student fills out application on portal
  - Submits application
  - Application data enters Student Information System (SIS)
- **Tools/Systems:** Application portal, SIS
- **Output:** Application record created in SIS
- **Time:** 30-60 minutes (for student)
- **Dependencies:** Application portal and SIS integration
- **Pain Points:** No confirmation to R.O. that application was submitted (they have to check SIS manually)

### Step 11: R.O. Discovers Application Submitted

- **Actor:** Recruitment Officer
- **Trigger:** Manual check of SIS or Master Spreadsheet
- **Actions:**
  - Logs into SIS periodically to see if students applied
  - Updates Master Spreadsheet when discovers application
  - Sends congratulations email to student
  - Notifies Admissions Admin (sometimes via email, sometimes in meeting)
- **Tools/Systems:** SIS, spreadsheet, email
- **Output:** R.O. aware of application, student acknowledged
- **Time:** 5 minutes per check
- **Dependencies:** R.O. remembering to check SIS
- **Pain Points:** Delay in discovering submission (sometimes days), manual discovery process, inconsistent student communication

> "I check the SIS every few days to see if my students applied. Sometimes I find out a week later." - Recruitment Officer

### Step 12: Handoff to Admissions Admin

- **Actor:** Recruitment Officer → Admissions Admin
- **Trigger:** R.O. awareness of application submission
- **Actions:**
  - R.O. emails Admin: "John Smith applied, please process"
  - R.O. may include context notes (optional, inconsistent)
  - Admin adds to application processing queue (separate spreadsheet)
- **Tools/Systems:** Email, multiple spreadsheets
- **Output:** Admin aware of application, added to queue
- **Time:** 5 minutes
- **Dependencies:** R.O. notifying admin, email received
- **Pain Points:** Manual handoff, context loss (R.O. notes not systematically transferred), duplicate tracking (inquiry spreadsheet + application spreadsheet)

### Step 13: Application Review & Processing

- **Actor:** Admissions Admin
- **Trigger:** Application in processing queue
- **Actions:**
  - Reviews application in SIS
  - Checks for completeness (all documents submitted)
  - Evaluates credentials against admissions criteria
  - If incomplete: Manually emails student requesting missing documents
  - If complete: Proceeds to decision
- **Tools/Systems:** SIS, email
- **Output:** Application evaluated
- **Time:** 20-45 minutes per application
- **Dependencies:** All documents submitted
- **Pain Points:** No automated document checklists, manual email requests, can't track which documents are missing in shared view

### Step 14: Admissions Decision

- **Actor:** Admissions Admin (or Committee for complex cases)
- **Trigger:** Complete application reviewed
- **Actions:**
  - Makes admissions decision (Accept, Deny, Waitlist)
  - Updates decision in SIS
  - Manually drafts decision letter (Word doc)
  - Emails or mails letter to student
  - Updates decision in Master Spreadsheet (sometimes)
- **Tools/Systems:** SIS, Word, email or postal mail
- **Output:** Student notified of decision
- **Time:** 15-30 minutes per decision
- **Dependencies:** Complete application
- **Pain Points:** Manual letter creation, no automatic notification to R.O. about decision, student may not receive email (spam)

### Step 15: Enrollment Confirmation (If Accepted)

- **Actor:** Student + Admissions Admin
- **Trigger:** Student accepts admission offer
- **Actions:**
  - Student submits enrollment confirmation (form or email)
  - Admin updates SIS to "Enrolled"
  - Admin sends welcome packet manually
  - Admin updates Master Spreadsheet
  - R.O. discovers enrollment via checking SIS or being told
- **Tools/Systems:** SIS, email, spreadsheet
- **Output:** Student enrolled, process complete
- **Time:** 10-20 minutes (admin work)
- **Dependencies:** Student action
- **Pain Points:** R.O. doesn't get automatic notification of successful enrollment (their "win"), no automatic celebration/thank you to R.O.

> "I find out my students enrolled when I happen to check the SIS or someone mentions it. It would be nice to get credit for my work." - Recruitment Officer

---

## Common Pain Points in Higher Ed Recruitment

### Visibility Issues

1. **Pipeline Status Blindness**
   - "Can't see where inquiries are in the process without asking"
   - "No dashboard showing how many inquiries are contacted, qualified, applied"

2. **No Workload Visibility**
   - "Can't see how many inquiries each R.O. is managing"
   - "No way to balance assignments fairly"

3. **Lost Context**
   - "When application comes in, we don't know the full conversation history"
   - "R.O. notes live in personal Excel, not shared"

4. **No Performance Metrics**
   - "Can't track R.O. response times"
   - "Can't measure conversion rates by program or R.O."

### Communication Issues

5. **Manual Follow-Ups**
   - "R.O.s manually track follow-up reminders (inconsistent)"
   - "No automated email sequences"

6. **Delayed Handoffs**
   - "Batch processing of inquiries causes 2-4 hour delays"
   - "Manual email handoff from R.O. to Admin when application submitted"

7. **No Student Status Updates**
   - "Students don't get application status updates automatically"
   - "Students email asking 'what's happening?' repeatedly"

### Data Quality Issues

8. **Multiple Data Entry**
   - "Inquiry data entered in spreadsheet, then later in SIS"
   - "Re-typing same information 2-3 times"

9. **Data Silos**
   - "Inquiry data in Excel, application data in SIS, no connection"
   - "Can't see full student journey in one place"

10. **Incomplete Records**
    - "Missing program interest, phone numbers, email addresses"
    - "No validation on web forms"

### Speed/Efficiency Issues

11. **Slow Initial Response**
    - "Average 2-4 hour delay before R.O. sees inquiry"
    - "Competitors may respond faster and win student"

12. **Manual Assignment Process**
    - "Admin manually assigns every inquiry (bottleneck)"
    - "Doesn't scale during peak season"

13. **Slow Application Processing**
    - "Takes 10-14 days to make admissions decision"
    - "Students accept other offers while waiting"

### Customer Experience Issues

14. **No Inquiry Confirmation**
    - "Students submit form and hear nothing (uncertainty)"
    - "May inquire elsewhere thinking form didn't work"

15. **Inconsistent Communication**
    - "Each R.O. has their own style, no templates"
    - "Some students get 5 touchpoints, others get 1"

16. **No Proactive Updates**
    - "Students have to call/email to ask about application status"
    - "Creates extra work for staff"

### Scalability Issues

17. **Can't Handle Volume Spikes**
    - "During peak season (Jan-Mar), system breaks down"
    - "Manual processes can't keep up"

18. **No Self-Service**
    - "Students can't check their own application status"
    - "Everything requires staff intervention"

### Reporting/Analytics Issues

19. **No Real-Time Metrics**
    - "Monthly reports compiled manually from spreadsheets"
    - "By the time we see data, it's too late to act"

20. **Can't Track ROI**
    - "Don't know which marketing channels produce best students"
    - "Can't attribute enrollments to specific campaigns"

21. **No Funnel Visibility**
    - "Don't know where students drop off in the process"
    - "Can't identify bottlenecks with data"

---

## Sample Gap Analysis Output (Higher Education)

### 1. Visibility Gaps

| What Can't Be Seen | Who Needs Visibility | Business Impact | HubSpot Solution |
|-------------------|----------------------|-----------------|------------------|
| Real-time inquiry pipeline status | R.O.s, Management | Duplicate outreach, missed opportunities, can't manage workload | Deal pipeline with stages, real-time dashboard showing all inquiries |
| R.O. response times | Management | Can't enforce 1-hour SLA, slow responders unidentified | Report: Time to first contact (by R.O., by day) |
| Full student journey (inquiry → enrollment) | Everyone | Repeated questions, lost context, poor handoffs | Contact timeline showing all touchpoints across lifecycle |
| Application status visibility | Students, R.O.s | Students call repeatedly asking "what's happening?" | Automated status emails when stage changes + student portal |

### 2. Speed & Efficiency Gaps

| Process Bottleneck | Current Duration | Root Cause | Target Duration | HubSpot Solution |
|-------------------|------------------|------------|-----------------|------------------|
| Inquiry assignment | 2-4 hours (batch) | Manual review and forwarding by admin | < 5 minutes (instant) | Workflow: Auto-assign based on program interest + workload balance |
| First contact with inquiry | 2-6 hours | Delayed assignment + manual R.O. process | < 1 hour (SLA) | Workflow: Instant assignment + task created + notification sent |
| Follow-up tracking | Manual reminders per R.O. | Each R.O. manages own system | Automated | Workflow: If no contact in 2 days → auto-send follow-up email |
| Application processing | 10-14 days | Manual review, no prioritization, delays waiting for docs | 5-7 days | Ticket pipeline + automated status checks + document reminder emails |

### 3. Data Quality Gaps

| Data Issue | Current State | Business Risk | HubSpot Solution |
|------------|---------------|---------------|------------------|
| Duplicate data entry | Inquiry entered in Excel, later in SIS (2x entry) | Time waste, errors, frustration | HubSpot as source of truth, auto-create in SIS via integration (1x entry) |
| Incomplete contact info | 30% of inquiries missing phone or email | Can't reach students, lower conversion | Required fields on forms, validation rules (email format, phone format) |
| Data silos | Inquiry data (Excel), application data (SIS), no connection | Can't see full journey, reporting impossible | HubSpot synced with SIS, unified contact record |

---

## HubSpot Configuration Patterns for Higher Ed

### Common Objects Used

**Contacts:**
- Prospective students
- Current students (if tracking retention)
- Alumni (if using for alumni relations)
- Parents (sometimes)

**Companies:**
- High schools (recruitment territory tracking)
- Transfer institutions
- Employers (for workforce programs)

**Deals:**
- **Recruitment Pipeline:** Inquiry → Contacted → Qualified → Applied → Admitted → Enrolled
- **Fundraising Pipeline:** (if using HubSpot for development)

**Tickets:**
- Application processing (track documents, reviews, decisions)
- Transfer credit evaluations
- Student support requests (if using for retention)

**Custom Objects (Enterprise):**
- Applications (if not using deals)
- Courses/Programs
- Events (campus tours, open houses)

### Typical Properties

**Contact Properties:**
- Program(s) of Interest (multi-select)
- Student Type (First-time, Transfer, International, etc.)
- Entry Term (Fall 2024, Spring 2025, etc.)
- Inquiry Source (Web Form, Referral, Event, etc.)
- Recruitment Officer (assigned owner)
- Application Status (Not Started, In Progress, Submitted, etc.)
- Admissions Decision (Accepted, Denied, Waitlist, Pending)
- Enrollment Confirmed (Yes/No/Pending)

**Deal Properties:**
- Pipeline: Recruitment Pipeline
- Deal Stage: (maps to recruitment stages)
- Program Applied For
- Application Date
- Decision Date
- Expected Enrollment Date
- Deal Amount: (tuition value for forecasting)

### Typical Pipelines & Stages

**Recruitment Pipeline:**

| Stage | Entry Criteria | Exit Criteria | Typical Duration | Automated Actions |
|-------|----------------|---------------|------------------|-------------------|
| 1. New Inquiry | Form submitted | R.O. makes first contact attempt | 1 hour | Auto-assign to R.O., send confirmation email, create task |
| 2. Attempting Contact | First contact attempted | Contact reached (two-way convo) | 1-5 days | Follow-up emails at Day 1, 3, 5 if no response |
| 3. Contacted | Conversation established | Qualified or disqualified | 1-3 days | Send program info email, create follow-up task |
| 4. Qualified | Meets criteria, interested, realistic timeline | Moved to nurture OR applied | 2-8 weeks | Weekly nurture emails, event invitations |
| 5. Nurturing | Engaged but not ready to apply | Applied OR disqualified | Ongoing | Automated email sequence, event reminders |
| 6. Application Started | Student started application | Application submitted OR abandoned | 1-2 weeks | Reminder emails if not completed within 7 days |
| 7. Application Submitted | Application in SIS | Decision made | 1-2 weeks | Confirmation email, assign to Admin, status update emails |
| 8. Admitted | Acceptance sent | Enrolled OR declined | 2-4 weeks | Acceptance email, welcome packet, enrollment instructions |
| 9. Enrolled (Won) | Enrollment confirmed | N/A (closed) | N/A | Congratulations email, onboarding sequence |
| 10. Not Enrolled (Lost) | Disqualified OR declined admission | N/A (closed) | N/A | (Optional: Exit survey, re-engagement campaign later) |

### Typical Workflows

**Workflow 1: Inquiry Processing & Assignment**
- Trigger: Form submission (web inquiry form)
- Actions:
  - Create contact (if new) or update (if existing)
  - Create deal in "New Inquiry" stage
  - Assign to R.O. based on program interest (rotating within program team)
  - Send instant confirmation email to student
  - Create task for R.O.: "Contact [Name] - New Inquiry"
  - Set task due: 1 hour from now (SLA)

**Workflow 2: Follow-Up Sequence (No Response)**
- Trigger: Deal stage = "Attempting Contact" for 2+ days
- Enrollment criteria: Last contact date is null OR > 2 days ago
- Actions:
  - Day 2: Send follow-up email #1 (friendly, "still interested?")
  - Day 4: Send follow-up email #2 (different angle, program highlight)
  - Day 7: Send follow-up email #3 (final attempt, "let us know if timing changes")
  - Day 10: Update deal stage to "On Hold - Unresponsive"
  - Exit workflow if contact responds (reply to email) or R.O. logs activity

**Workflow 3: Application Abandoned Reminder**
- Trigger: Deal stage = "Application Started" for 7+ days
- Actions:
  - Day 7: Email reminder to student: "We noticed you started your application..."
  - Day 10: Create task for R.O.: "Call [Name] - app not completed"
  - Day 14: Final reminder email
  - Day 21: Move to "Application Abandoned" stage

**Workflow 4: Application Status Updates**
- Trigger: Deal stage changes
- Actions:
  - Stage → "Application Submitted": Email: "We received your application!"
  - Stage → "Under Review": Email: "Your application is being reviewed"
  - Stage → "Admitted": Email: "Congratulations! You've been accepted"
  - Each stage change: Notify assigned R.O. (task or internal notification)

### Typical Integrations

**Student Information System (SIS):**
- Common SIS: Anthology (formerly Campus Management), Ellucian (Colleague, Banner), Jenzabar, PowerSchool
- Integration type: Bidirectional API sync
- Data synced:
  - HubSpot → SIS: Contact info, inquiry source, R.O. notes
  - SIS → HubSpot: Application status, decision, enrollment status, student ID
- Trigger: Real-time (webhooks) or scheduled (daily sync)

**Application Platform:**
- Common platforms: Common App, ApplyTexas, institution's own portal
- Integration type: One-way (application → HubSpot)
- Data synced: Application submission, completion status
- Trigger: Webhook when application submitted

**Email Marketing (if not using HubSpot Marketing):**
- If using separate email tool: Mailchimp, Constant Contact
- Integration: Sync contact lists
- Note: Often migrate to HubSpot Marketing to consolidate

**Event Management:**
- Common tools: EMS, Eventbrite, custom systems
- Integration: Sync event registrations
- Creates contact + logs activity in HubSpot

### Typical Reports & Dashboards

**R.O. Dashboard:**
- My open inquiries (by stage)
- My tasks due today
- My response time (avg)
- My conversion rate (inquiry → application)

**Management Dashboard:**
- Total inquiries (this month vs last month)
- Inquiry sources (breakdown)
- Pipeline by stage (funnel visual)
- Team response time (avg, by R.O.)
- Conversion rates (inquiry → app → enrollment)
- Forecast (expected enrollments based on pipeline)

**Reports:**
- Inquiry Source Report (which channels perform best)
- Conversion Funnel (where drop-offs occur)
- Response Time Report (by R.O., by day of week)
- Program Interest Report (which programs generate most inquiries)
- Enrollment Forecast (based on historical conversion rates)

---

## Quick Wins for Higher Education

These are common high-impact, low-complexity improvements:

1. **Instant Inquiry Confirmation Email**
   - Impact: Improves student experience, sets expectations
   - Complexity: 30 min to set up workflow + template

2. **Auto-Assignment of Inquiries**
   - Impact: Eliminates 2-4 hour delay, removes admin bottleneck
   - Complexity: 1-2 hours to configure assignment logic

3. **Pipeline Dashboard for Management**
   - Impact: First-time real-time visibility into recruitment
   - Complexity: 1 hour to build dashboard

4. **Automated Follow-Up Sequence**
   - Impact: Ensures no inquiry falls through cracks, saves R.O. time
   - Complexity: 2-3 hours to build workflow + email templates

5. **Application Status Update Emails**
   - Impact: Reduces student anxiety, reduces "where's my app?" calls
   - Complexity: 2 hours to build workflow + templates

---

## Higher Education Terminology

| Common Term | HubSpot Mapping | Notes |
|-------------|-----------------|-------|
| Inquiry | Contact in early stage | Person who expressed interest |
| Prospect | Contact in "Qualified" stage | Actively considering enrollment |
| Applicant | Deal in "Application Submitted" | Has submitted application |
| Admit/Accepted Student | Deal in "Admitted" stage | Offered admission |
| Enrolled Student | Deal in "Enrolled (Won)" stage | Confirmed enrollment |
| Lead Source | Original Source property | Where inquiry came from |
| Program of Interest | Custom property (multi-select) | Academic program(s) student interested in |
| Entry Term | Custom property (dropdown) | Semester/term student plans to start |
| Recruitment Officer | Contact Owner | Assigned R.O. in HubSpot |
| SIS | External System Integration | Student Information System |

---

## Common Mistakes to Avoid (Higher Ed)

### ❌ Don't:
- Use "Leads" object (use Contacts)
- Create one deal per contact for recruitment (creates clutter; use contact properties + pipeline)
- Over-complicate stages (keep to 7-10 max)
- Forget to integrate with SIS (creates duplicate data entry)
- Ignore mobile experience (students primarily on phones)
- Send too many automated emails (email fatigue)

### ✅ Do:
- Use Contacts for students, Deals for recruitment pipeline
- Keep stage names simple and student-centric
- Plan SIS integration from day one
- Test emails on mobile devices
- Segment email sequences by program interest
- Set up reporting before go-live (establish baselines)

---

## This Template's Use

When analyzing discovery transcripts for a higher education client:

1. **Reference this template** for common patterns
2. **Look for similar pain points** (but use client's specific language)
3. **Use the sample AS-IS** as a structural guide (but document client's actual process)
4. **Adapt, don't copy** - every institution is unique
5. **Quote the client**, don't quote this template

This template provides context, not a script.
