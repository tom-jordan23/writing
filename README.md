# Writing Style Documentation

This repository documents Tom Jordan's writing voice across professional contexts—IT, academic, humanitarian, and staff development.

## Quick Start

**For AI integration**: `https://raw.githubusercontent.com/tom-jordan23/writing/main/tojo_style.md`

Paste that URL into any GPT chat, say what you're writing and for whom, and the AI handles the voice.

**For detailed work**: Choose the relevant guide from the table below, upload it to your AI assistant, provide your key points.

## File Selection

| Audience | File | Focus |
|----------|------|-------|
| IT executives, CIOs, CTOs | `STYLE_IT_Executive.md` | Strategic decisions, ROI, risk management |
| Systems engineers, architects | `STYLE_IT_Technical.md` | Implementation details, technical depth |
| Academic administrators, deans | `STYLE_Academic_University_Business.md` | Mission alignment, shared governance |
| Humanitarian organization leadership | `STYLE_Humanitarian_Executive.md` | Beneficiary impact, humanitarian principles |
| Country directors, program managers | `STYLE_Humanitarian_Program_Leadership.md` | Field operations, M&E frameworks |
| Field ICT officers, technical coordinators | `STYLE_Humanitarian_Technical.md` | Appropriate technology, offline-first design |
| Direct reports, mentees, anyone you're coaching | `STYLE_Staff_Development.md` | Growth, learning, developmental conversations |
| General or mixed audience | `STYLE.md` | Base style applicable across contexts |

## What the Guides Capture

### Structure

Framework-based thinking—NIST for IT security, CHS/Sphere for humanitarian work, shared governance principles for academia. The frameworks provide scaffolding.

Example opening:
> "Zero-trust architecture—verifying every request regardless of network location—addresses the fundamental weakness of perimeter-based security. NIST SP 800-207 provides implementation guidance: define your protect surface, map transaction flows, build architecture, create policies, monitor and maintain."

Framework reference (NIST), em-dash clarification, specific guidance.

### Evidence

Not "use multi-factor authentication."

Instead: "TOTP-based MFA using FreeOTP (open source, works offline) or Duo ($3/user/month) provides stronger authentication than SMS. Tested with 50,000 faculty/staff at peer institutions—implementation timeline 4-6 months."

Version numbers, costs, timelines, peer institutions, deployment experience.

### Tone

Authoritative without arrogance. Acknowledges complexity—"This is challenging" not "This is simple." Shares uncertainty—"Here's what worked in our context; your mileage may vary."

### Language

Translation-friendly. Critical for humanitarian operations (field staff use Google Translate on SOPs) and international contexts. One idea per sentence, active voice, no idioms. "Easily achievable priorities" not "low-hanging fruit."

Not stylistic preference—operational necessity when unclear guidance affects beneficiary safety.

### Punctuation

High-frequency em-dash usage:
- "The protect surface—critical data and systems—requires strongest controls"
- "Zero-trust architecture—authentication for every request—replaces perimeter security"

Colons for lists and elaborations. Quotation marks for terms being defined. Serial commas.

### Warmth

"This work is hard. You're going to make mistakes. That's how learning happens. You don't need to be perfect."

Not corporate sterile. Human.

## Cross-Cutting Themes

Three frameworks integrated across all guides.

**Historical Context**: Optional connections to foundational principles. Stoic philosophy (dichotomy of control, amor fati), technical foundations (Saltzer & Schroeder 1975), humanitarian history (Solferino, Rwanda). Always framed as enrichment, never required. 1-2 paragraphs maximum.

**Anti-Oppressive Language**: Challenges systems of oppression—racism, classism, sexism, ableism. Questions who benefits and who's excluded. In humanitarian contexts, explicitly names colonialism and centers local leadership. In technical contexts, advocates open source and questions "best practices" (often code for "what well-funded US companies do").

**Cross-Linguistic Accessibility**: Avoids idioms, uses literal language, structures for machine translation. Especially critical in humanitarian field operations where unclear SOPs create safety risks.

## Background

The voice reflects specific professional experience:

- Higher education IAM community leader: Five-time InCommon BaseCAMP speaker (2020-2024), CACTI Chair for Internet2 (2020), InCommon Advisory Committee (2024-2026)
- Trusted Access Platform expertise: Shibboleth and Grouper implementation and architecture for federated identity
- 20+ years leading IAM strategy at UW-Madison (R1 research university), supporting cross-institutional collaboration across the UW System
- Open source implementation: OpenLDAP and OpenSSL deployment and community support in higher education contexts
- Federation standards: SAML and OIDC implementation enabling research and education collaboration
- Emergency response: Civil Air Patrol SAR pilot (2001-2005), Surge IM Officer with IFRC, IM and ITT Officer with American Red Cross International Services, SIMS deployments (Hurricane Beryl/Grenada, Ebola #16/DRC), American Red Cross (Hurricanes Helene/Milton, Indonesia river monitoring October 2025)
- Emergency communications: HAM radio technician (KD9QIA), digital modes for field operations
- Field operations: Agricultural aviation ground crew (mix rig and field team)
- Multi-sector: government emergency response, higher education IT, humanitarian field operations

This background shapes the voice—federated identity expertise, peer-to-peer community building, open source advocacy, appropriate technology principles, framework-based thinking, field-tested solutions.

Farm background shapes core belief: "If you wanted something, you bought it broken and fixed it"—trust in your ability to address the unknown through research and determined trial and error. This isn't just repair culture; it's fundamental confidence that complex problems are navigable. Explains why the voice acknowledges complexity while providing guidance, shares failures openly, and trusts others to figure things out.

Solution evaluation always considers financial and environmental costs: total cost of ownership (not just acquisition price), power consumption, e-waste impact, carbon footprint, operational sustainability. Repair extends equipment life and reduces waste. Newest isn't always best when considering full lifecycle costs.

Your writing draws on different experience. The structural patterns (framework-based, evidence-driven, translation-friendly) transfer. The specific authority markers don't.

## Example: Voice Transformation

**Generic AI output**:
> "Implementing zero-trust architecture is important for modern security. Organizations should consider this approach. It requires careful planning."

**After applying STYLE_IT_Executive.md**:
> "Zero-trust architecture addresses a fundamental shift—perimeter-based security assumes internal users are trustworthy, an assumption that fails when credential theft provides threat actors initial access. Implementation requires three decisions: defining your protect surface (critical data requiring strongest controls), selecting architecture approach (NIST SP 800-207 provides frameworks), and planning migration (peer institutions report 12-18 months). Initial investment: $200K-$500K depending on infrastructure. ROI comes through reduced breach impact—Ponemon data shows $4.24M average breach cost, making this risk mitigation rather than technical upgrade."

What changed: Framework reference (NIST), specific timelines (12-18 months), peer evidence, cost ranges, ROI data, em-dash clarifications, strategic framing.

## Common Issues

**Output feels generic**: Upload the full guide file, not a summary. Specify audience explicitly.

**Wrong tone**: Verify correct audience guide. IT Executive and Staff Development produce very different output.

**Uses idioms**: Remind the AI content may be translated. Humanitarian and international contexts require literal language.

**Missing framework grounding**: Request explicitly—"ground this in NIST controls" or "reference CHS indicators."

## File Organization

**Single-URL integration**: `tojo_style.md` (condensed, all audiences)

**Base analysis**: `STYLE.md` (1,360 lines analyzing core patterns)

**Audience adaptations**: 7 guides, 700-1,400 lines each

**Integration**: `QUICK_START.md`, `AI_INTEGRATION_GUIDE.md`, `STYLE_INDEX.md`

**Frameworks**: `HISTORICAL_CONTEXT_FRAMEWORK.md`, `ANTI_OPPRESSIVE_LANGUAGE_ADDITIONS.md`, `CROSS_LINGUISTIC_STYLE_GUIDE.md`

Total: ~8,000 lines.

## Using with AI Assistants

Upload relevant guide or paste URL. Provide topic and key points. AI handles voice, structure, evidence patterns.

For human writers: Read guides to see patterns, practice applying them, get feedback.

For teams: Shared Custom GPT or Claude Project ensures consistent voice.

## Maintenance

These guides capture patterns as of November 2025. Writing evolves with experience—new deployments, shifting focus, emerging frameworks. Update when context changes.

The voice in 2030 won't match 2025 exactly. That's growth. The structural patterns persist (framework-based, evidence-driven, warm, accessible). The specific examples and contexts shift.

## For Those Developing Their Own Voice

You don't need to copy this voice. These guides enable replication by AI or consistent team output. Your voice should reflect your experience and values.

Take what's useful—framework-based structure, specific evidence, translation-friendly language, warmth.

Leave what doesn't fit—your authority comes from different experience, your tone might differ, your values might emphasize different dimensions.

The `STYLE_Staff_Development.md` guide is for anyone on this journey. Your voice matters. Your perspective fills gaps. Everyone is welcome.

## Contributing

See `CONTRIBUTING.md`. The bar is "does this make the guides more useful?" not bureaucratic requirements. Fork, improve, submit PR.

---

**Repository**: https://github.com/tom-jordan23/writing
**Quick integration**: https://raw.githubusercontent.com/tom-jordan23/writing/main/tojo_style.md
**Version**: 1.0 (November 2025)
