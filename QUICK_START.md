# Quick Start: Using Your Style Guides with AI

**Goal**: Get an AI assistant writing in your voice in under 5 minutes.

---

## Method 1: Single URL Paste (Fastest - 30 seconds)

**Best for**: Quick setup, any GPT chat, immediate use

1. **Copy this URL**:
   ```
   https://raw.githubusercontent.com/tom-jordan23/writing/main/tojo_style.md
   ```

2. **Paste into any ChatGPT conversation**

3. **Say**: "Write about [topic] for [audience] using Tom Jordan's style from this guide"

4. **Done!** The condensed guide (all 8 audiences) routes automatically.

**Example**:
```
[Paste URL]

Write a technical guide on Shibboleth federation for systems engineers
using Tom Jordan's style.
```

---

## Method 2: Detailed File Upload (2 minutes)

1. **Start a new ChatGPT conversation**

2. **Upload two files**:
   - `STYLE_INDEX.md` (this file helps route to the right guide)
   - `STYLE_IT_Technical.md` (or whichever audience you're writing for)

3. **Prompt**:
   ```
   Write a [topic] for [audience] using Tom Jordan's style from the uploaded guides.

   Include:
   - Framework-based approach
   - Specific examples (versions, costs, timelines)
   - Evidence from peer institutions or deployments
   - Open source recommendations
   - Warm, welcoming tone
   ```

4. **Done!** Review and iterate.

**Example prompt**:
```
Write a 1,500-word technical guide on implementing password-less
authentication for university faculty, targeting systems engineers.
Use Tom Jordan's style from the uploaded guides.
```

---

---

## Method 3: Claude Projects (Best for ongoing work)

1. **Create new Project** in Claude

2. **Upload all 8 style files**:
   - STYLE_INDEX.md
   - STYLE.md
   - All 6 STYLE_*.md files

3. **Set Project Instructions**:
   ```
   Help Tom Jordan write. Before starting, ask "What audience?"
   Then use the appropriate STYLE_*.md guide. Core principles:
   framework-based, specific examples, evidence-based, anti-oppressive,
   cross-linguistic, warm. Technology serves people.
   ```

4. **Start writing**: "Write a guide on [topic] for [audience]"

---

## Method 3: Custom Instructions (Daily use)

**ChatGPT Settings → Custom Instructions**

**"What would you like ChatGPT to know about you?"**:
```
Tom Jordan: solutions architect, open source contributor (OpenLDAP/OpenSSL),
SAML/OIDC standards developer, 20+ years higher ed open source mentor,
emergency responder (CAP SAR pilot, SIMS deployments, American Red Cross).

Audiences: IT executives, IT technical, academic, humanitarian.
```

**"How would you like ChatGPT to respond?"**:
```
Tom Jordan's style: Framework-based, specific examples, acknowledge
complexity, evidence-based, gentle historical context (Stoics optional),
anti-oppressive, cross-linguistic (no idioms), warm ("everyone welcome").

Ask audience first, then adapt: IT Executive (strategic/ROI),
IT Technical (deep implementation), Academic (mission/consultative),
Humanitarian (beneficiary-centered/offline-first).
```

---

## Quick Reference: What Changes by Audience

| Audience | Length | Depth | Tone | Key Focus |
|----------|--------|-------|------|-----------|
| **IT Executive** | 1,200-1,800 words | Strategic | Decisive | ROI, risk, competition |
| **IT Technical** | 2,500-4,000 words | Deep code | Peer | Implementation steps |
| **Academic** | 1,800-2,500 words | Mission-first | Consultative | Shared governance |
| **Humanitarian Exec** | 1,500-2,200 words | Principled | Values-driven | Beneficiary impact |
| **Humanitarian Program** | 2,500-3,500 words | Operational | Supportive | M&E, field steps |
| **Humanitarian Tech** | 3,000-5,000 words | Deep tech | Problem-solving | Offline, repairable |
| **Staff Development** | Conversational | Process | Patient, encouraging | Growth, learning |

---

## Essential Elements (Check Every Piece)

- [ ] **Framework-based**: NIST, CHS, Sphere, ISO (appropriate to context)
- [ ] **Specific**: Version numbers, costs, timelines, commands
- [ ] **Evidence**: Peer institutions, deployments, research
- [ ] **Open source**: When applicable, advocate for open source options
- [ ] **Historical context**: Optional Stoic connection if relevant
- [ ] **Anti-oppressive**: Who benefits? Who's excluded? Challenge power.
- [ ] **Cross-linguistic**: No idioms. Translation-friendly. Especially critical for humanitarian.
- [ ] **Warm**: "Everyone welcome. You don't need to be perfect. This is hard."

---

## Common Idioms to Avoid

Replace these always:

| ❌ Avoid | ✅ Use Instead |
|---------|---------------|
| "Low-hanging fruit" | "Easily achievable priorities" |
| "Circle back" | "Return to this discussion" |
| "Deep dive" | "Detailed analysis" |
| "Touch base" | "Meet" or "discuss" |
| "Move the needle" | "Create measurable improvement" |
| "Spin up" | "Start" or "launch" |
| "Kick off" | "Begin" or "start" |

---

## Test Prompt (Verify Your Setup)

Try this in your AI assistant:

```
Write a 500-word guide on two-factor authentication deployment
for university IT staff. Include specific technology recommendations
(open source preferred), implementation steps, and cost estimates.
Reference higher education context. Use warm, peer-to-peer tone.
```

**Check output has**:
- ✓ Specific tools (e.g., "FreeOTP, Duo, or Yubico")
- ✓ Version numbers and costs
- ✓ Step-by-step implementation
- ✓ Higher ed context ("peer institutions like Michigan")
- ✓ Open source advocacy
- ✓ No idioms
- ✓ Warm tone ("This can be challenging, but...")

---

## Troubleshooting

**Too generic?** → Upload full style guide, specify audience
**Wrong tone?** → Confirm correct audience guide, remind "peer-to-peer" or "consultative"
**Uses idioms?** → Remind "This will be translated. Avoid idioms."
**No frameworks?** → Prompt "Ground this in NIST framework" or "Reference CHS/Sphere"
**Too formal?** → Remind "Warm and welcoming. Everyone is welcome."

---

## File Locations

All files in: `/Users/tjordan/code/git/writing/`

**Start here**:
- `STYLE_INDEX.md` - Master index and routing
- `QUICK_START.md` - This file

**Audience guides** (pick one):
- `STYLE_IT_Executive.md`
- `STYLE_IT_Technical.md`
- `STYLE_Academic_University_Business.md`
- `STYLE_Humanitarian_Executive.md`
- `STYLE_Humanitarian_Program_Leadership.md`
- `STYLE_Humanitarian_Technical.md`
- `STYLE_Staff_Development.md`

**Supporting**:
- `STYLE.md` - Base style (all audiences)
- `STYLE_PROMPT_CONDENSED.md` - For custom instructions
- `AI_INTEGRATION_GUIDE.md` - Detailed platform instructions

---

## Next Steps

1. **Try Method 1** (file upload) right now with a test topic
2. **If you like it**, set up Method 2 (Custom GPT or Claude Project) for ongoing use
3. **For daily writing**, add Method 3 (Custom Instructions)
4. **Iterate**: First draft → refine tone → add examples → check translation-friendliness

---

## Remember

The AI has access to your full style - decades of open source work, standards development, emergency response deployments, and community mentorship. Just point it to the right audience guide and let it work.

**You don't need to be perfect. The AI will help you maintain consistency.**

Everyone is welcome to this process. Let's write clearly and serve people well.
