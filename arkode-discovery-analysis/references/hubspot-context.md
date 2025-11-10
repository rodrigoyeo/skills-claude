# HubSpot Context for Discovery Analysis

## Purpose

This reference provides HubSpot-specific context to inform discovery analysis, helping identify gaps that HubSpot can address and understanding platform capabilities/limitations.

---

## HubSpot Core Capabilities

### Objects & Data Model

**Standard Objects:**
- **Contacts** - People (prospects, customers, partners)
- **Companies** - Organizations
- **Deals** - Opportunities in pipelines
- **Tickets** - Support/service requests
- **Custom Objects** - Industry-specific entities (available in Enterprise)

**Key Concept:** HubSpot is contact-centric. Everything revolves around people.

### Automation Capabilities

**Workflows:**
- Trigger-based automation (when X happens, do Y)
- Enrollment criteria (who/what gets automated)
- Actions: Send email, assign task, update property, create record, etc.
- Branching logic (IF/THEN)
- Delays (wait 1 day, wait until date, etc.)

**Sequences:**
- Sales-focused email sequences (personalized 1:1 emails)
- Manual enrollment (sales rep decides who to enroll)
- Auto-unenroll on reply
- Task reminders for sales team

### Communication Tools

**Email:**
- Marketing emails (mass sends, requires Marketing Hub)
- Automated emails (from workflows)
- One-to-one emails (logged in CRM)
- Email templates (reusable)
- Personalization tokens (dynamic content)

**Other Channels:**
- SMS (via integrations or workflows)
- Live chat (on website)
- Chatbots (automated conversations)
- Calling (VoIP integrated)

### Forms & Data Capture

**Forms:**
- Embedded on website
- Standalone pages
- Pop-ups
- Progressive profiling (ask different questions based on what you know)
- Field validation
- Auto-create contacts/deals

### Reporting & Analytics

**Dashboards:**
- Customizable widgets
- Real-time data
- Shareable with teams
- Multiple dashboards for different audiences

**Reports:**
- Standard reports (pre-built)
- Custom reports (build your own)
- Funnel reports (conversion analysis)
- Attribution reports (source tracking)

**Analytics:**
- Contact/company/deal analytics
- Email performance
- Form submissions
- Website traffic
- Pipeline analytics

---

## HubSpot Limitations to Consider

### Data Limits (By Tier)

**Free:**
- Limited contacts (1,000 marketing contacts)
- Basic features only
- No workflows (automation)

**Starter:**
- 1,000 marketing contacts
- Basic workflows
- Limited reporting

**Professional:**
- 2,000+ marketing contacts
- Full workflows
- Custom reporting
- Integrations

**Enterprise:**
- Unlimited contacts
- Advanced features
- Custom objects
- Dedicated support

**Discovery Question:** What HubSpot tier does client have or plan to purchase?

### Workflow Limitations

**Considerations:**
- Workflows trigger on property changes, form submissions, or manual enrollment
- Some triggers not available (e.g., can't trigger on "no activity in 30 days" in Starter)
- Workflow actions limited by tier
- Complex branching can get unwieldy (keep simple when possible)

### Integration Considerations

**Native Integrations:**
- HubSpot has 1,000+ native integrations
- Common: Salesforce, Gmail, Outlook, Slack, Zoom, WordPress, Shopify

**Custom Integrations:**
- API available (Professional+)
- Webhooks for real-time sync
- May require developer or middleware (Zapier, Make)

**Discovery Question:** What systems need to integrate with HubSpot?

### Reporting Limitations

**Considerations:**
- Some advanced reports require Professional/Enterprise
- Data retention limits on lower tiers
- Complex calculated fields may need custom properties
- Attribution tracking requires setup (UTM parameters, etc.)

---

## Identifying HubSpot Fit During Discovery

### Green Flags (HubSpot is Great Fit)

Listen for these signals that indicate HubSpot will solve problems well:

✅ **"We need better visibility into our pipeline"**
→ HubSpot's deal pipelines excel at this

✅ **"We're doing a lot of manual follow-ups"**
→ HubSpot workflows automate beautifully

✅ **"We can't track where leads come from"**
→ HubSpot's source tracking and attribution

✅ **"We need to segment our contacts better"**
→ HubSpot's lists and properties are powerful

✅ **"Our marketing and sales teams don't share data"**
→ HubSpot's unified platform solves this

✅ **"We want to send automated emails based on behavior"**
→ HubSpot workflows + email automation

✅ **"We need better reporting for leadership"**
→ HubSpot dashboards and reports

### Yellow Flags (Needs Consideration)

Signals that require careful planning:

⚠️ **"We need complex custom workflows"**
→ Assess if HubSpot's workflow builder can handle it (usually yes, but check)

⚠️ **"We need to integrate with legacy system X"**
→ Check if integration exists or if custom API work needed

⚠️ **"We have very specific industry data requirements"**
→ May need custom objects (Enterprise) or creative use of properties

⚠️ **"We need advanced forecasting and analytics"**
→ May need Enterprise tier or external BI tool

### Red Flags (HubSpot May Not Be Best Fit)

Signals that HubSpot might not be ideal:

🚩 **"We need complex quoting with product catalogs"**
→ HubSpot's quoting is basic; may need CPQ tool integration

🚩 **"We need advanced project management features"**
→ HubSpot is CRM, not PM tool; integrate with Asana/Monday

🚩 **"We need complex territory management and sales hierarchies"**
→ HubSpot is simpler than Salesforce here; assess fit

🚩 **"We need field service management"**
→ HubSpot doesn't do FSM; need integration

**Note:** Red flags don't mean don't use HubSpot - they mean "needs integration or workaround"

---

## Common HubSpot Use Cases by Industry

### Higher Education

**Typical Setup:**
- **Contacts:** Prospective students, current students, alumni
- **Deals:** Recruitment pipeline (inquiry → application → enrollment)
- **Pipelines:** Recruitment, Fundraising, Alumni Relations
- **Workflows:** Auto-assignment, follow-up sequences, application status updates
- **Integrations:** Student Information System (SIS), application platforms
- **Forms:** Inquiry forms, event registrations, scholarship applications

### Healthcare

**Typical Setup:**
- **Contacts:** Patients, providers, referring physicians
- **Deals:** Patient intake pipeline, partnership pipeline
- **Pipelines:** Patient Acquisition, Provider Relations
- **Workflows:** Appointment reminders, intake follow-ups
- **Integrations:** EMR/EHR (Epic, Cerner, etc.), scheduling systems
- **Forms:** Appointment requests, patient intake forms

### Professional Services

**Typical Setup:**
- **Contacts:** Prospects, clients, referral sources
- **Deals:** Sales pipeline (lead → proposal → client)
- **Pipelines:** New Business, Client Retention, Upsell
- **Workflows:** Proposal follow-up, contract renewals, referral requests
- **Integrations:** Accounting (QuickBooks), project management (Asana)
- **Forms:** Contact forms, consultation requests

### SaaS/Technology

**Typical Setup:**
- **Contacts:** Leads, trial users, customers
- **Deals:** Sales pipeline (lead → trial → paid customer)
- **Pipelines:** Sales, Customer Success, Upsell
- **Workflows:** Trial onboarding, product usage tracking, upsell triggers
- **Integrations:** Product (via API), billing (Stripe), support (Zendesk)
- **Forms:** Demo requests, trial signups, feature requests

---

## Key Questions to Ask During Discovery

### About Current CRM (if they have one)

1. **"What CRM are you using currently, if any?"**
   - Understand migration needs

2. **"What do you like about your current CRM?"**
   - Preserve what works

3. **"What frustrates you about your current CRM?"**
   - Identify gaps HubSpot can fill

4. **"How much data needs to be migrated?"**
   - Assess migration complexity

### About HubSpot Readiness

5. **"What HubSpot tier are you planning to use?"**
   - Understand feature availability

6. **"Do you have HubSpot already, or are you buying it?"**
   - Implementation vs. optimization

7. **"Who will be using HubSpot? How many users?"**
   - Understand user roles and license needs

8. **"Do you have technical resources for integrations?"**
   - Assess integration feasibility

### About Process Requirements

9. **"What's your average sales/conversion cycle timeline?"**
   - Inform pipeline stage design

10. **"How do you currently assign leads/inquiries?"**
    - Understand assignment logic needs

11. **"What reports do you need to see weekly/monthly?"**
    - Dashboard requirements

12. **"What integrations are must-haves?"**
    - Critical systems to connect

---

## HubSpot-Specific Gap Analysis Angles

When analyzing gaps, consider these HubSpot-specific solutions:

### Visibility Gaps → HubSpot Dashboards & Reports
**Example Gap:** "Management can't see pipeline status"
**HubSpot Solution:** Deal dashboard with pipeline stages, conversion rates, forecasting

### Efficiency Gaps → HubSpot Workflows
**Example Gap:** "Manual follow-up emails"
**HubSpot Solution:** Workflow: If no response in 2 days → auto-send follow-up email

### Data Gaps → HubSpot Properties & Validation
**Example Gap:** "Incomplete contact information"
**HubSpot Solution:** Required fields on forms, data validation rules

### Communication Gaps → HubSpot Notifications & Tasks
**Example Gap:** "Don't know when application submitted"
**HubSpot Solution:** Workflow: Deal stage change → create task + notification

### Customer Experience Gaps → HubSpot Automation
**Example Gap:** "No confirmation after form submission"
**HubSpot Solution:** Workflow: Form submission → instant confirmation email

### Scalability Gaps → HubSpot Automation
**Example Gap:** "Manual lead assignment doesn't scale"
**HubSpot Solution:** Workflow: Round-robin or criteria-based auto-assignment

### Reporting Gaps → HubSpot Analytics
**Example Gap:** "Can't track inquiry sources"
**HubSpot Solution:** UTM tracking, original source property, attribution reports

---

## HubSpot Implementation Complexity Indicators

Use these to assess complexity during gap analysis:

### Low Complexity (Standard HubSpot Features)
- Basic workflows (trigger → action)
- Standard properties (text, dropdown, date)
- Forms with standard fields
- Email templates
- Basic dashboards and reports
- Round-robin assignment

### Medium Complexity
- Multi-step workflows with branching
- Custom properties (calculated fields)
- Integration with common tools (Zapier, native integrations)
- Custom reports with multiple filters
- Multiple pipelines
- Progressive profiling forms

### High Complexity
- Custom objects (Enterprise feature)
- Complex API integrations (custom development)
- Data migration from legacy systems
- Multiple system integrations (orchestration)
- Complex scoring models
- Advanced attribution modeling

---

## Terminology Mapping

Help clients understand HubSpot concepts by mapping their language:

| Client Says | HubSpot Term | Explanation |
|-------------|--------------|-------------|
| "Lead" | Contact (in early stage) | Person in your database |
| "Opportunity" | Deal | Represents potential revenue in pipeline |
| "Status" | Deal Stage | Where deal is in pipeline |
| "Follow-up tasks" | Tasks | To-dos assigned to users |
| "Email campaign" | Marketing Email or Workflow | Mass email or automated sequence |
| "Sales funnel" | Pipeline | Visual representation of deal stages |
| "Lead source" | Original Source | Where contact first came from |
| "Custom field" | Custom Property | Additional data field you create |
| "Automation" | Workflow | Automated process/sequence |

---

## Discovery Output Considerations for HubSpot

When documenting AS-IS and gaps, keep in mind:

### Map Current Process to HubSpot Objects

As you document AS-IS steps, note which HubSpot object they relate to:
- **Contact creation** → Contacts object
- **Qualification** → Deal object + deal properties
- **Pipeline progression** → Deal stages
- **Follow-up** → Tasks + Workflows
- **Communication** → Email + Logged activities

This primes the TO-BE design.

### Note Integration Requirements Early

When documenting current systems, flag integration needs:
- Must integrate (critical data sync)
- Should integrate (efficiency gain)
- Nice to integrate (convenience)

### Identify Workflow Opportunities

As you document manual processes, flag automation opportunities:
- **Manual:** "R.O. sends follow-up email after 2 days"
- **Automation Opportunity:** Workflow automation

### Design Properties with Purpose

When documenting data captured, think about HubSpot properties:
- What's captured today?
- What format? (text, number, dropdown, date)
- Is it required?
- Who updates it?

---

## Common Patterns in HubSpot Implementations

### Pattern 1: Inquiry-to-Customer Pipeline

**Stages:**
1. New Inquiry
2. Contacted
3. Qualified
4. Proposal/Demo
5. Negotiation
6. Closed Won / Closed Lost

**Typical Workflows:**
- Auto-assign on creation
- Confirmation email on inquiry
- Follow-up sequence if no response
- Notification on stage change
- Task creation for manual steps

### Pattern 2: Automated Nurture Sequences

**Trigger:** Contact downloads resource / fills form / takes action
**Sequence:**
- Day 0: Immediate confirmation + resource delivery
- Day 2: Follow-up with related content
- Day 5: Case study or social proof
- Day 10: Offer demo/consultation

**Unenroll:** If contact replies or becomes customer

### Pattern 3: Round-Robin Assignment

**Trigger:** New deal/contact created
**Logic:**
- IF [criteria A] → Assign to Team A (rotate among team members)
- ELSE IF [criteria B] → Assign to Team B (rotate)
- ELSE → Assign to default owner

**Property:** "Last assigned user" (tracks rotation)

### Pattern 4: Status Update Notifications

**Trigger:** Deal stage changes
**Actions:**
- Update contact property (mirror deal stage)
- Send email to customer (status update)
- Create task for owner (next action)
- Notify team via Slack (visibility)

---

## Checklist for HubSpot-Informed Discovery

During discovery, ensure you capture:

- [ ] Current CRM (if any) and migration needs
- [ ] HubSpot tier client has or will purchase
- [ ] Number of contacts/deals expected
- [ ] Number of users (by role)
- [ ] Systems requiring integration
- [ ] Automation opportunities identified
- [ ] Reporting requirements noted
- [ ] Data capture needs documented
- [ ] Communication workflows mapped
- [ ] Pipeline stages conceptualized (preliminary)

This ensures TO-BE design can immediately translate to HubSpot configuration.
