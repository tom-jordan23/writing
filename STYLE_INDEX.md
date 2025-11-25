# Tom Jordan Writing Style Guide - Master Index

**Purpose**: This index helps AI assistants select the appropriate style guide for your writing context.

## Quick Selection Guide

**Ask yourself**: Who is my primary audience?

- **IT Executives/CIOs/CTOs** → Use `STYLE_IT_Executive.md`
- **Systems engineers, architects, technical practitioners** → Use `STYLE_IT_Technical.md`
- **Provosts, deans, academic administrators** → Use `STYLE_Academic_University_Business.md`
- **NGO directors, humanitarian leadership** → Use `STYLE_Humanitarian_Executive.md`
- **Country directors, program managers, M&E leads** → Use `STYLE_Humanitarian_Program_Leadership.md`
- **Field ICT officers, technical coordinators in humanitarian contexts** → Use `STYLE_Humanitarian_Technical.md`
- **Direct reports, mentees, anyone you're coaching/developing** → Use `STYLE_Staff_Development.md`
- **General/uncertain audience** → Use base `STYLE.md`

## Core Authority Markers (All Guides)

Tom Jordan's credibility stems from:
- **Higher education IAM leadership**: Five-time InCommon BaseCAMP speaker (2020-2024), CACTI Chair for Internet2 (2020), InCommon Advisory Committee (2024-2026)
- **Trusted Access Platform**: Shibboleth and Grouper implementation and architecture for federated identity
- **Open source implementation**: OpenLDAP and OpenSSL deployment and community support
- **Standards development**: SAML and OIDC implementation in higher education contexts
- **Community mentorship**: 20+ years leading IAM strategy and building peer networks in higher education
- **Emergency response**: Civil Air Patrol SAR pilot (2001-2005), SIMS deployments (Hurricane Beryl/Grenada, Ebola #16/DRC), American Red Cross (Hurricanes Helene/Milton)
- **Emergency communications**: HAM radio technician (KD9QIA), digital modes for field operations
- **Field operations**: Agricultural aviation ground crew (mix rig and field team)
- **Multi-sector expertise**: Government emergency response + higher education IT + humanitarian field deployment

## Cross-Cutting Themes (All Guides Include)

1. **Historical Context**: Gentle connections to foundational principles and thinkers (especially Stoics)
2. **Anti-Oppressive Language**: Actively anti-racist, anti-classist, anti-sexist, anti-ableist; challenges power structures
3. **Cross-Linguistic Accessibility**: Translation-friendly, avoids idioms, internationally accessible
4. **Warmth and Human Connection**: Everyone is welcome; acknowledges difficulty; offers support

## Style Signatures Across All Contexts

- **Trust in figuring things out**: Core belief that complex problems are navigable through research and determined trial and error. "If you wanted something, you bought it broken and fixed it." Shapes everything—why acknowledge complexity while guiding, why share failures, why trust others to learn
- **Framework-based thinking**: Structured approaches (NIST, CHS, Sphere, etc.) provide scaffolding for figuring things out
- **Specific examples**: Concrete, actionable, tested guidance showing what others figured out
- **Acknowledgment of complexity**: "This is hard" + "here's how to navigate it" (hard but navigable)
- **Evidence-based**: Peer institutions, research, deployment experience (learn from others' problem-solving)
- **Humble service orientation**: Technology/writing serves people, not the reverse

## File Structure

```
# Quick integration
tojo_style.md                               # Single-URL condensed guide (all 8 audiences, ~500 lines)
                                            # Use: https://raw.githubusercontent.com/tom-jordan23/writing/main/tojo_style.md

# Detailed audience-specific guides
STYLE.md                                    # Base style guide (1,360 lines)
STYLE_IT_Executive.md                       # Strategic IT leadership (~700 lines)
STYLE_IT_Technical.md                       # Technical practitioners (~1,120 lines)
STYLE_Academic_University_Business.md       # Academic leadership (~885 lines)
STYLE_Humanitarian_Executive.md             # Humanitarian leadership (~865 lines)
STYLE_Humanitarian_Program_Leadership.md    # Field operations (~877 lines)
STYLE_Humanitarian_Technical.md             # Field technical (~1,423 lines)
STYLE_Staff_Development.md                  # Coaching & mentoring (~950 lines)

# Supporting frameworks (optional deep reading)
HISTORICAL_CONTEXT_FRAMEWORK.md
ANTI_OPPRESSIVE_LANGUAGE_ADDITIONS.md
CROSS_LINGUISTIC_STYLE_GUIDE.md
INCLUSIVE_LANGUAGE_REVIEW.md
LANGUAGE_ACCESSIBILITY_SUMMARY.md
```

## How to Use This with AI Assistants

### Quick Use (30 seconds):
**Paste this URL into any ChatGPT conversation**:
```
https://raw.githubusercontent.com/tom-jordan23/writing/main/tojo_style.md
```
Then say: "Write about [topic] for [audience] using Tom Jordan's style"

The condensed guide (tojo_style.md) includes all 8 audiences with routing logic.

### Detailed Use (for longer/complex work):
1. Upload this index file (STYLE_INDEX.md)
2. Upload the relevant audience-specific guide (e.g., STYLE_IT_Technical.md)
3. Prompt: "Write [topic] using the style guide provided, for [audience]"

### For ChatGPT Custom Instructions:
Use the condensed prompt (see `STYLE_PROMPT_CONDENSED.md`)

### For Custom GPT:
Upload all guides to knowledge base; GPT will retrieve relevant sections

### For API/Programmatic Use:
- Quick: Fetch tojo_style.md from GitHub raw URL
- Detailed: Use STYLE_INDEX.md to route to appropriate guide based on audience parameter

## Selection Decision Tree

```
START: What are you writing?

├─ Is it technical implementation guidance?
│  ├─ For corporate/enterprise IT? → STYLE_IT_Technical.md
│  └─ For humanitarian field contexts? → STYLE_Humanitarian_Technical.md
│
├─ Is it strategic/executive communication?
│  ├─ For IT/technology leadership? → STYLE_IT_Executive.md
│  ├─ For academic leadership? → STYLE_Academic_University_Business.md
│  └─ For humanitarian leadership? → STYLE_Humanitarian_Executive.md
│
├─ Is it operational/program guidance?
│  └─ For humanitarian field operations? → STYLE_Humanitarian_Program_Leadership.md
│
└─ Unsure/general audience? → STYLE.md (base)
```

## Key Adaptations by Audience

| Aspect | IT Exec | IT Tech | Academic | Hum Exec | Hum Program | Hum Tech | Staff Dev |
|--------|---------|---------|----------|----------|-------------|----------|-----------|
| **Depth** | Strategic | Deep technical | Mission-first | Strategic | Operational | Deep technical | Process-focused |
| **Length** | Concise | Comprehensive | Deliberative | Concise | Detailed steps | Comprehensive | Conversational |
| **Tone** | Decisive | Peer-to-peer | Consultative | Principled | Supportive | Problem-solving | Patient, encouraging |
| **Evidence** | Business metrics | Benchmarks | Peer institutions | Impact data | Field experience | Tested solutions | Personal stories |
| **Focus** | ROI, risk | Implementation | Mission alignment | Beneficiary impact | Team enablement | Appropriate tech | Growth, learning |

## Quick Reference: Avoid in ALL Contexts

**Idioms that don't translate**:
- "Low-hanging fruit" → "Easily achievable priorities"
- "Circle back" → "Return to this discussion"
- "Move the needle" → "Create measurable improvement"
- "Touch base" → "Meet" or "discuss"
- "Deep dive" → "Detailed analysis"

**Language choices**:
- Avoid: "elderly and illiterate" → Use: "based on age or literacy background"
- Avoid: "whitelist/blacklist" → Use: "allowlist/blocklist"
- Avoid: "master/slave" → Use: "primary/secondary" or "main/replica"
- Avoid: "sanity check" → Use: "validation check"

## Version Information

- **Created**: November 24, 2025
- **Based on**: Analysis of Tom Jordan's EdTech Magazine articles
- **Integrated**: Personal background, deployment experience, open source contributions
- **Frameworks**: Historical context, anti-oppressive language, cross-linguistic accessibility
- **Total guidance**: ~7,000 lines across all documents

## Questions for AI Assistant

Before writing, the AI should ask:
1. **Who is the primary audience?** (Select guide)
2. **What is the writing purpose?** (Article, memo, technical doc, etc.)
3. **What is the context?** (Crisis response, strategic planning, implementation, etc.)
4. **Any special considerations?** (Translation needs, accessibility requirements, etc.)

## Contact & Updates

These guides are living documents. As Tom's writing evolves or new contexts emerge, guides should be updated to reflect current voice and needs.
