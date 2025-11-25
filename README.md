# Writing Style Documentation

This repository contains comprehensive style guides for replicating Tom Jordan's writing voice across different professional audiences.

## Background

These guides analyze writing patterns, voice, and approach based on published work and professional experience including:
- Open source contributions (OpenLDAP, OpenSSL)
- Standards development (SAML, OIDC)
- Higher education open source community mentorship
- Emergency response deployments (Civil Air Patrol, SIMS, American Red Cross)
- Multi-sector experience (government emergency response, higher education IT, humanitarian field operations)

## File Selection

Choose the guide that matches your primary audience:

| Audience | File | Focus |
|----------|------|-------|
| IT executives, CIOs, CTOs | `STYLE_IT_Executive.md` | Strategic decisions, ROI, risk management |
| Systems engineers, architects | `STYLE_IT_Technical.md` | Implementation details, technical depth |
| Academic administrators, deans | `STYLE_Academic_University_Business.md` | Mission alignment, shared governance |
| Humanitarian organization leadership | `STYLE_Humanitarian_Executive.md` | Beneficiary impact, humanitarian principles |
| Country directors, program managers | `STYLE_Humanitarian_Program_Leadership.md` | Field operations, M&E frameworks |
| Field ICT officers, technical coordinators | `STYLE_Humanitarian_Technical.md` | Appropriate technology, offline-first design |
| General or mixed audience | `STYLE.md` | Base style applicable across contexts |

## Using with AI Assistants

The simplest approach:

1. Upload the relevant style guide file to your AI assistant (ChatGPT, Claude, etc.)
2. Provide your topic and key points
3. Ask the AI to write using the uploaded guide

Example prompt:
```
Write about [topic] for [audience] using the uploaded style guide.

Key points:
- [point one]
- [point two]
- [point three]

Length: [word count or approximate length]
```

The guide contains the voice, tone, structure, and approach patterns. You provide the content direction.

## Core Style Characteristics

All guides share these foundations:

**Structure**: Framework-based thinking with clear hierarchical organization. NIST, CHS, Sphere, or other established frameworks provide scaffolding.

**Evidence**: Specific examples with version numbers, costs, timelines, and citations. Peer institutions for higher education contexts, deployment experience for humanitarian contexts, production implementations for technical contexts.

**Tone**: Authoritative without arrogance. Acknowledges complexity while providing practical guidance. Warm but not informal.

**Language**: Translation-friendly—avoids idioms and culturally-specific metaphors, particularly critical in humanitarian and international higher education contexts.

**Values**: Technology serves people. Centers marginalized voices. Challenges power structures. Open source advocacy when appropriate.

## Key Adaptations by Audience

**IT Executive**: Strategic framing, business impact, concise presentation suitable for senior leadership review. ROI and risk mitigation emphasized.

**IT Technical**: Implementation depth, command syntax, configuration examples, troubleshooting guidance. Peer-to-peer technical voice.

**Academic**: Mission-first framing, respect for shared governance, consultation rather than direction. References to peer institutions and educational research.

**Humanitarian Executive**: Beneficiary-centered decision making, humanitarian principles non-negotiable, resource constraints openly acknowledged.

**Humanitarian Program**: Operational specificity, M&E integration, field team perspective, partner coordination emphasis.

**Humanitarian Technical**: Appropriate technology principles—offline-first, locally repairable, low power consumption, open source preferred. Constraint-driven design.

## Cross-Cutting Frameworks

Three themes integrated across all guides:

**Historical Context**: Optional connections to foundational principles and thinkers. Stoic philosophy applied to professional challenges (dichotomy of control, amor fati, sympatheia). Always framed as enrichment, never required knowledge.

**Anti-Oppressive Language**: Actively challenges systems of oppression—racism, classism, sexism, ableism. Questions who benefits and who is excluded from technical decisions. Centers community voice over external expertise in humanitarian contexts.

**Cross-Linguistic Accessibility**: Avoids idioms that fail in translation. One idea per sentence, active voice, specific verbs. Critical in humanitarian field operations where unclear guidance affects beneficiary safety.

## Common Issues

**Output feels too generic**: Upload the full style guide file rather than relying on summary prompts. Specify the audience explicitly.

**Wrong tone for audience**: Verify you uploaded the correct audience-specific guide. IT Executive and IT Technical guides produce significantly different output despite covering similar topics.

**Uses problematic idioms**: Remind the AI that content may be translated—request literal, clear language particularly for humanitarian or international higher education contexts.

**Missing framework grounding**: Explicitly request framework integration—"ground this in NIST controls" or "reference CHS indicators."

## Additional Resources

`STYLE_INDEX.md` provides detailed comparison across guides and routing logic.

`QUICK_START.md` offers step-by-step setup for common AI platforms.

`AI_INTEGRATION_GUIDE.md` covers platform-specific implementation (Custom GPT, Claude Projects, API integration).

`STYLE_PROMPT_CONDENSED.md` provides abbreviated guidance for character-limited contexts.

## File Organization

Total documentation: approximately 7,000 lines across all guides.

Base style guide (`STYLE.md`): 1,360 lines analyzing core patterns.

Six audience-specific adaptations: 700-1,400 lines each, depending on context complexity.

Supporting frameworks and integration guides: 200-500 lines each.

## Maintenance

These guides represent patterns observed as of November 2025. Writing evolves with experience—particularly as deployment contexts, technology standards, and professional focus shift over time.

Update guides when:
- New deployment experience adds relevant context
- Professional role or focus changes
- New frameworks or standards become relevant
- Audience needs shift
- Language usage evolves

Version control through git enables tracking changes and reverting if needed.

## Note on Use

The style captured here reflects specific professional background and values. When using these guides, consider whether the voice fits your context. The technical patterns (structure, evidence, clarity) transfer broadly. The specific authority markers (deployment experience, standards work, community leadership) are contextual to this particular professional history.

If writing for audiences unfamiliar with the background, you may need to establish credibility through different evidence sources while maintaining the structural and tonal patterns.
