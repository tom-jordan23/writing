# How to Use Tom Jordan's Style Guides with AI Assistants

This guide explains how to integrate these style guides into different AI platforms and workflows.

---

## Option 1: ChatGPT Custom Instructions (Simplest)

**Best for**: Quick daily writing tasks, short pieces

**Setup**:
1. Go to ChatGPT Settings → Personalization → Custom Instructions
2. In "What would you like ChatGPT to know about you?":
```
I am Tom Jordan, solutions architect with:
- Open source contributions: OpenLDAP, OpenSSL
- Standards development: SAML, OIDC
- 20+ years mentoring higher ed open source community
- Emergency response: CAP SAR pilot, SIMS deployments (Hurricane Beryl/Grenada, Ebola #16/DRC, Hurricanes Helene/Milton)
- Multi-sector: Government emergency + higher education IT + humanitarian field deployment

My audiences: IT executives, IT technical staff, academic administrators, humanitarian leadership, field program managers, field technical staff.
```

3. In "How would you like ChatGPT to respond?":
```
Use Tom Jordan's writing style:
- Framework-based with specific examples (versions, costs, timelines)
- Acknowledge complexity + provide guidance
- Evidence from peer institutions/deployments
- Gentle historical context (especially Stoics - optional)
- Anti-oppressive: challenge power structures, center marginalized voices
- Cross-linguistic: avoid idioms, translation-friendly
- Warm, welcoming: "Everyone is welcome. You don't need to be perfect."

Adapt by audience:
- IT Executive: Strategic, ROI, concise
- IT Technical: Deep implementation, code examples
- Academic: Mission-first, consultative, shared governance
- Humanitarian Executive: Beneficiary-centered, principled
- Humanitarian Program: Operational steps, M&E, field-practical
- Humanitarian Technical: Offline-first, locally-repairable, open source

Always ask what audience before writing.
```

**Limitations**: ~1,500 character limit; doesn't capture full nuance

---

## Option 2: ChatGPT with File Upload (Recommended for longer pieces)

**Best for**: Articles, technical documentation, substantial writing

**Setup**:
1. Start new chat
2. Upload `STYLE_INDEX.md`
3. Upload relevant audience guide (e.g., `STYLE_IT_Technical.md`)
4. Prompt: "Write a [topic] for [audience] using the style guide provided"

**Advantages**:
- Full style guide available
- Can reference specific sections
- Can switch audiences mid-conversation

**Example conversation**:
```
You: [Upload STYLE_INDEX.md and STYLE_IT_Technical.md]
"Write a technical implementation guide for zero-trust architecture
for systems engineers at a research university. Use the style guide provided."

ChatGPT: [Writes using full IT Technical style, with code examples,
troubleshooting, peer-to-peer tone, etc.]

You: "Now create an executive summary version for the CIO"
[Upload STYLE_IT_Executive.md]

ChatGPT: [Adapts to strategic, concise IT Executive style]
```

---

## Option 3: Custom GPT (Best for repeated use)

**Best for**: Dedicated writing assistant you use regularly

**Setup**:
1. Go to ChatGPT → Explore GPTs → Create a GPT
2. Name: "Tom Jordan Writing Assistant"
3. Description: "Writes in Tom Jordan's style across multiple audiences"
4. Instructions (paste this):

```
You are a writing assistant that helps Tom Jordan write in his established style across different audiences.

# About Tom
Solutions architect with open source contributions (OpenLDAP, OpenSSL), standards development (SAML, OIDC), 20+ years mentoring higher education open source community, emergency response experience (CAP SAR pilot, SIMS deployments for hurricanes/Ebola, American Red Cross).

# Your Role
1. Ask what audience: IT Executive, IT Technical, Academic, Humanitarian Executive, Humanitarian Program, or Humanitarian Technical
2. Retrieve relevant style guide from knowledge base
3. Write using that guide's principles

# Core Style
- Framework-based thinking with specific examples
- Acknowledge complexity + provide guidance
- Evidence from peer institutions/deployments
- Gentle historical context (especially Stoics)
- Anti-oppressive: challenge power, center marginalized voices
- Cross-linguistic: avoid idioms, translation-friendly
- Warm: "Everyone welcome. You don't need to be perfect."

# Always Check
- Appropriate for audience?
- Framework-based and evidence-based?
- Translation-friendly language?
- Anti-oppressive and welcoming?
- Technology serves people?

Before writing, always ask: "What is your primary audience for this piece?"
```

5. Upload all style guide files to Knowledge:
   - STYLE.md
   - STYLE_INDEX.md
   - STYLE_IT_Executive.md
   - STYLE_IT_Technical.md
   - STYLE_Academic_University_Business.md
   - STYLE_Humanitarian_Executive.md
   - STYLE_Humanitarian_Program_Leadership.md
   - STYLE_Humanitarian_Technical.md
   - STYLE_Staff_Development.md

6. Conversation starters:
   - "Write a technical guide for..."
   - "Create an executive brief about..."
   - "Draft an academic memo on..."
   - "Write a humanitarian field SOP for..."

**Advantages**:
- All guides available automatically
- Persistent across conversations
- Can be shared with collaborators
- No repeated setup

---

## Option 4: Claude Projects (For Claude users)

**Best for**: Long-form writing, complex documents

**Setup**:
1. Create new Project in Claude
2. Add all style guide files to Project Knowledge
3. Set Custom Instructions:

```
You are helping Tom Jordan write in his established style.

Tom's background:
- Open source: OpenLDAP, OpenSSL contributions
- Standards: SAML, OIDC development
- Community: 20+ years mentoring higher ed open source
- Emergency response: CAP SAR pilot, SIMS deployments, American Red Cross

Before writing, ask: "What audience?" Then use the appropriate STYLE_*.md guide.

Core principles:
- Framework-based with specific examples
- Acknowledge complexity + provide guidance
- Evidence from deployments/peer institutions
- Gentle historical context (especially Stoics - optional)
- Anti-oppressive, cross-linguistic, warm
- Technology serves people

Always reference the uploaded style guides for detailed guidance.
```

**Advantages**:
- 200K context window (can handle all guides)
- Persistent across conversations
- Can upload drafts for revision

---

## Option 5: API Integration (For developers)

**Best for**: Automated writing workflows, bulk generation

**Pseudocode**:
```python
def get_style_guide(audience):
    """Route to appropriate style guide"""
    guides = {
        'it_executive': 'STYLE_IT_Executive.md',
        'it_technical': 'STYLE_IT_Technical.md',
        'academic': 'STYLE_Academic_University_Business.md',
        'humanitarian_executive': 'STYLE_Humanitarian_Executive.md',
        'humanitarian_program': 'STYLE_Humanitarian_Program_Leadership.md',
        'humanitarian_technical': 'STYLE_Humanitarian_Technical.md',
        'staff_development': 'STYLE_Staff_Development.md',
        'general': 'STYLE.md'
    }
    return read_file(guides[audience])

def write_in_style(topic, audience, additional_context=""):
    style_guide = get_style_guide(audience)

    prompt = f"""
    Write about {topic} for {audience} audience.

    Use Tom Jordan's writing style as defined in this guide:

    {style_guide}

    Additional context: {additional_context}

    Remember:
    - Framework-based thinking
    - Specific examples with details
    - Acknowledge complexity, provide guidance
    - Evidence-based
    - Anti-oppressive, cross-linguistic
    - Warm and welcoming tone
    """

    return call_llm_api(prompt)

# Usage
article = write_in_style(
    topic="zero-trust architecture implementation",
    audience="it_technical",
    additional_context="For research university with 50K users"
)
```

---

## Quick Reference by Platform

| Platform | Setup Time | Context Limit | Best For | Persistence |
|----------|------------|---------------|----------|-------------|
| Custom Instructions | 5 min | ~1,500 chars | Quick daily tasks | Permanent |
| File Upload | 1 min/chat | ~25K tokens/file | Single articles | Per conversation |
| Custom GPT | 15 min | All files | Repeated use | Permanent |
| Claude Projects | 10 min | 200K tokens | Long-form | Per project |
| API | 30 min setup | Full guides | Automation | Custom |

---

## Recommended Workflow

**For most writing**:
1. Create Custom GPT with all guides uploaded
2. Use for 90% of writing tasks
3. For edge cases, upload additional context files to conversation

**For occasional use**:
1. Set up Custom Instructions with condensed prompt
2. Upload full guide when needed for major pieces

**For team/collaboration**:
1. Create Custom GPT and share link
2. Everyone on team uses same assistant
3. Consistent voice across all team writing

---

## Testing Your Setup

After setup, test with this prompt:

```
Write a 500-word technical implementation guide about deploying
two-factor authentication for university faculty, targeting IT systems
engineers. Include:
- Specific technology recommendations
- Implementation steps
- Cost estimates
- Open source options
- Reference to higher education context
```

**Check the output for**:
- [ ] Technical depth (specific tools, versions, commands)
- [ ] Framework-based approach (NIST, etc.)
- [ ] Open source advocacy
- [ ] Higher education context (peer institutions)
- [ ] Specific costs and timelines
- [ ] Step-by-step implementation
- [ ] No idioms (translation-friendly)
- [ ] Warm, encouraging tone

If missing these elements, adjust your setup or provide more explicit instructions.

---

## Troubleshooting

**"Output too generic"**:
- Upload full style guide, not just condensed prompt
- Explicitly state audience at start
- Ask for specific examples with version numbers/costs

**"Wrong tone"**:
- Verify correct audience guide loaded
- Remind: "Use the peer-to-peer technical voice from the guide"

**"Too academic/formal"**:
- Remind: "Write with warmth and accessibility. Everyone is welcome."

**"Missing framework approach"**:
- Prompt: "Ground this in NIST framework" (IT) or "CHS/Sphere" (humanitarian)

**"Uses idioms"**:
- Remind: "This will be translated. Avoid idioms. Use clear, literal language."

---

## Maintaining Your Setup

**When to update**:
- Your writing evolves
- New deployment experience to reference
- New frameworks/standards emerge
- Audience needs change

**How to update**:
- Edit the relevant STYLE_*.md file
- Re-upload to Custom GPT / Claude Project
- Update Custom Instructions if needed
- Test with sample prompt

**Version control**:
- Keep style guides in Git repository
- Tag versions (v1.0, v1.1, etc.)
- Note major changes in commit messages
- Consider dated backups for major revisions

---

## For Collaborators

If others will write in your voice:

1. **Share Custom GPT** (easiest):
   - Create GPT as described above
   - Set visibility to "Anyone with link"
   - Share link with collaborators

2. **Provide style guide package**:
   - `STYLE_INDEX.md` (start here)
   - Relevant audience guide(s)
   - `STYLE_PROMPT_CONDENSED.md` (quick reference)
   - This integration guide

3. **Train on examples**:
   - Provide 3-5 pieces you've written
   - "This is good" / "This is off-brand"
   - Let them upload examples with style guide

---

## Advanced: Multi-Pass Writing

For important pieces:

**Pass 1 - Draft**: Upload relevant guide, ask for draft
**Pass 2 - Refine tone**: "Make this warmer and more welcoming"
**Pass 3 - Add examples**: "Add 2 specific examples with version numbers and costs"
**Pass 4 - Check translation**: "Remove any idioms. Make this work for machine translation."
**Pass 5 - Anti-oppressive check**: "Review this for power dynamics. Are we centering marginalized voices?"

---

## Getting Help

If output doesn't match expected style:
1. Check you're using correct audience guide
2. Provide example of your actual writing for comparison
3. Be explicit: "This is too formal. Use the warm, peer-to-peer tone from the guide."
4. Upload multiple guides if writing for multiple audiences
5. Ask for specific revisions: "More technical depth" or "More strategic framing"

The guides are comprehensive—the AI should be able to replicate your voice closely if you direct it to the right guide and provide clear audience context.
