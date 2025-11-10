# Arkode Skill Template

This template is specifically designed for creating Arkode business operation skills.

## Quick Start

1. **Copy this directory** and rename it following the pattern: `arkode-[category]-[function]`
   - Examples: `arkode-client-proposal`, `arkode-project-estimate`, `arkode-team-standup`

2. **Edit SKILL.md** and replace all bracketed placeholders:
   - Update the `name` in YAML frontmatter to match your directory name
   - Write a clear, specific `description`
   - Fill in all `[REPLACE]` and `[TODO]` sections

3. **Add optional resources** as needed:
   - Create `scripts/` for Python/Bash automation
   - Create `references/` for documentation to reference
   - Create `assets/` for templates, logos, or files to use in output

4. **Delete unused sections** - Not every skill needs all sections

5. **Test the skill** - Use it in real scenarios and iterate

## Directory Structure Options

### Minimal Skill (Just Instructions)
```
arkode-skill-name/
└── SKILL.md
```

### With References (Company Knowledge)
```
arkode-skill-name/
├── SKILL.md
└── references/
    ├── arkode-services.md
    └── arkode-pricing.md
```

### With Assets (Templates/Logos)
```
arkode-skill-name/
├── SKILL.md
└── assets/
    ├── arkode-logo.png
    └── proposal-template.docx
```

### Full Skill (Everything)
```
arkode-skill-name/
├── SKILL.md
├── scripts/
│   └── calculate_estimate.py
├── references/
│   ├── services-catalog.md
│   └── pricing-tiers.md
└── assets/
    ├── arkode-logo.png
    └── email-signature.html
```

## Best Practices for Arkode Skills

1. **Be Specific in Descriptions** - The description determines when Claude uses the skill
2. **Include Real Examples** - Show actual Arkode scenarios
3. **Document Brand Standards** - Ensure consistency across all skills
4. **Keep it Updated** - Skills should evolve with your business
5. **Test Before Rolling Out** - Always validate with real use cases

## Need Help?

Refer to the main repository's ARKODE_SKILLS_FRAMEWORK.md for guidance on:
- Prioritizing which skills to build
- Information gathering checklist
- Skill naming conventions
- Quality standards
