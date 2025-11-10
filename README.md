# Arkode Skills Repository

## Overview

This repository contains Arkode's custom Claude skills for HubSpot process optimization projects. These skills systemize our methodology, ensuring consistent, high-quality deliverables across all client engagements.

---

## Arkode Skills

### 🔍 **arkode-discovery-analysis** (Skill 1 of 4)
**Purpose:** Analyze discovery calls → Create AS-IS + Gap Analysis
**Input:** Discovery transcripts, industry
**Output:** 5,000-7,000 word analysis with process flow, gaps, and Quick Wins
**Status:** ✅ Complete

[View Skill →](./arkode-discovery-analysis/)

---

### 📧 **arkode-client-email**
**Purpose:** Write professional, consistent client emails
**Input:** Email type, recipient, context
**Output:** On-brand email (updates, proposals, meetings, etc.)
**Status:** ✅ Complete

[View Skill →](./arkode-client-email/)

---

### 📋 **arkode-template-skill**
**Purpose:** Template for creating new Arkode skills
**Input:** N/A (copy and customize)
**Output:** Structured skill directory
**Status:** ✅ Template ready

[View Skill →](./arkode-template-skill/)

---

## Coming Soon

### 🎨 **arkode-process-design** (Skill 2 of 4)
**Purpose:** Design optimized TO-BE process for HubSpot
**Input:** AS-IS + Gap Analysis
**Output:** Complete TO-BE design document
**Status:** 🚧 Planned

---

### 🗺️ **arkode-swimlane-mapping** (Skill 3 of 4)
**Purpose:** Create visual process maps (Miro-ready)
**Input:** TO-BE design
**Output:** Swimlane diagram specification
**Status:** 🚧 Planned

---

### 📊 **arkode-implementation-master** (Skill 4 of 4)
**Purpose:** Create Master Implementation Document (Excel)
**Input:** TO-BE + Swimlane
**Output:** Complete HubSpot configuration guide
**Status:** 🚧 Planned

---

## Arkode Methodology (4-Skill Suite)

```
Discovery Calls
    ↓
[Skill 1] arkode-discovery-analysis
    ↓
AS-IS + Gap Analysis Document
    ↓
[Skill 2] arkode-process-design
    ↓
TO-BE Process Design
    ↓
[Skill 3] arkode-swimlane-mapping
    ↓
Visual Process Map
    ↓
[Skill 4] arkode-implementation-master
    ↓
Master Implementation Document
    ↓
HubSpot Configuration & Launch
```

---

## Quick Start

### For Arkode Team Members

1. **Install skills in Claude.ai:**
   - Download the skill folder you need
   - Zip it
   - Upload to Claude.ai as custom skill

2. **Or use in Claude Code:**
   ```bash
   # Copy skill to your skills directory
   cp -r arkode-[skill-name] ~/.claude-code/skills/
   ```

3. **Start using:**
   ```
   Use arkode-discovery-analysis to analyze [client project]
   ```

### Creating New Arkode Skills

1. Copy `arkode-template-skill/` directory
2. Rename to `arkode-[category]-[function]`
3. Edit SKILL.md following the template
4. Add references, assets as needed
5. Test thoroughly

---

## Documentation

- **[ARKODE_SKILLS_FRAMEWORK.md](./ARKODE_SKILLS_FRAMEWORK.md)** - Strategy and business areas
- **[ARKODE_QUICKSTART.md](./ARKODE_QUICKSTART.md)** - How to get started
- **[SKILL1_SUMMARY.md](./SKILL1_SUMMARY.md)** - Skill 1 architecture details
- **[agent_skills_spec.md](./agent_skills_spec.md)** - Technical skills specification

---

## Resources

- **skill-creator/** - Meta skill for creating skills (from Anthropic)
- **.claude-plugin/** - Plugin configuration

---

## Naming Convention

All Arkode skills follow this pattern:

```
arkode-[category]-[function]
```

**Categories:**
- `client-*` - Client-facing communications
- `project-*` - Project management workflows
- `discovery-*` - Discovery and analysis
- `process-*` - Process design
- `implementation-*` - Implementation documents

**Examples:**
- `arkode-client-email`
- `arkode-discovery-analysis`
- `arkode-process-design`

---

## Contributing

### Adding a New Skill

1. Use `arkode-template-skill` as starting point
2. Follow naming convention
3. Include README.md in skill folder
4. Test with real project
5. Document in this README

### Adding Industry Templates

For discovery-analysis skill:
1. Create new file in `arkode-discovery-analysis/references/industry-templates/`
2. Follow `higher-education.md` structure
3. Include real examples from past projects
4. Update skill documentation

---

## Support

**Internal Team:** Ask in #arkode-skills Slack channel
**Documentation:** See individual skill READMEs

---

**Version:** 1.0
**Last Updated:** November 2025
**Maintained by:** Arkode Team
