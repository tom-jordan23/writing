# Tom Jordan's Writing Style: IT Technical Audience

**Target Audience**: Systems engineers, network architects, security engineers, DevOps practitioners, technical specialists
**Context**: Technical documentation, implementation guides, architecture deep-dives, technical blog posts
**Analysis Date**: November 24, 2025

---

## Executive Summary: Style Adaptation for Technical Practitioners

This style guide adapts Tom Jordan's core voice for technical practitioner audiences. The adaptation emphasizes **implementation depth over high-level strategy**, **specific configuration over general principles**, and **how-to guidance over why-to rationale**. Writing for technical audiences assumes high domain knowledge and values precision, completeness, and actionable specificity.

**Key shifts from base style**:
- **Technical depth intensified**: Specific commands, configurations, version numbers
- **Implementation focus**: Step-by-step guidance, troubleshooting, edge cases
- **Assumed knowledge**: Skip basics, dive into advanced topics
- **Code and configuration**: Include actual examples, snippets, scripts
- **Precision over brevity**: Longer articles acceptable if technically comprehensive

---

## I. VOICE AND AUTHORITY POSITIONING

### Authorial Persona

**Primary identity**: **Senior technical peer sharing battle-tested expertise**
- Fellow practitioner who has implemented this in production
- Architect who understands both theory and operational reality
- Experienced engineer who has debugged the edge cases
- Technical mentor sharing lessons learned
- Core belief: Complex technical problems are navigable through research and determined trial and error. "If you wanted something, you bought it broken and fixed it"—confidence that you can figure things out shapes peer-to-peer problem-solving approach

**Authority markers**:
- Higher education IAM leadership: Five-time InCommon BaseCAMP speaker (2020-2024), CACTI Chair for Internet2 (2020), InCommon Advisory Committee member (2024-2026)
- Trusted Access Platform expertise: Shibboleth and Grouper implementation and architecture for federated identity
- 20+ years leading IAM strategy at UW-Madison (R1 research university), supporting cross-institutional collaboration
- Open source implementation: OpenLDAP and OpenSSL deployment and community support in higher education contexts
- Federation standards: SAML and OIDC implementation enabling research and education collaboration
- Emergency communications: HAM radio technician (KD9QIA), digital modes (understanding RF, protocols, data communications)
- Emergency operations experience: Data center operations supporting university/county/state police coordination, critical infrastructure during emergencies
- American Red Cross international: Indonesia river monitoring (October 2025)—OpenRiverCam open source computer vision deployment with PMI/Delft University for flood early warning systems
- Search and rescue background: Civil Air Patrol mission pilot (2001-2005), multi-agency coordination, federal/state/local integration
- Specific implementation experience: "In our production environment," "When implementing this at scale," "During emergency operations..."
- Technical precision: Exact version numbers, command syntax, configuration parameters
- Framework mastery: Deep knowledge of NIST, STIG, CIS, emergency management protocols beyond surface level
- Community engagement: "In the InCommon community, we've found...", "Implementing Shibboleth at scale taught us..."
- War stories: "We discovered that...", "A common pitfall is...", "During the incident..."
- Tool-specific knowledge: Actual product experience, not vendor marketing
- Resilience expertise: Business continuity, disaster recovery, high-availability systems for emergency operations

**What changes from base style**:
- Much more technical detail
- Implementation-level specificity
- Troubleshooting and edge cases included
- Tool and vendor comparisons acceptable (with caveats about context)

### Relationship with Reader

**Reader positioning**: Peer-to-peer technical collaboration

**Assumptions about technical reader**:
- High domain literacy: Understands fundamentals; wants advanced knowledge
- Implementation-focused: Will actually use this guidance
- Detail-oriented: Wants completeness and accuracy
- Skeptical: Needs evidence, not assertions
- Tool-savvy: Familiar with standard toolchains and approaches

**Direct address**:
- "When you configure," "As you implement," "Before you deploy"
- "Your environment likely has," "You'll encounter," "You should validate"
- Assumes reader has technical agency and decision-making

---

## II. STRUCTURAL ADAPTATIONS

### Article Architecture for Technical Content

**Effective technical article structure**:

```markdown
# [Technical Topic]: Implementation Guide

**Environment**: [Specific platforms, versions, constraints]
**Prerequisites**: [Required knowledge, tools, access]
**Reading time**: X minutes

## Overview

[What this guide covers, scope, outcomes - 2-3 paragraphs]
[When to use this approach vs. alternatives]

## Technical Background

[Architecture principles or concepts - more depth than general audience]
[Framework or standard foundations]
[Why this approach vs. alternatives - technical rationale]

## Prerequisites and Environment

- Required tools and versions
- Access and permissions needed
- Baseline configuration assumptions
- Testing/staging recommendations

## Implementation Steps

### Step 1: [Specific Action]

[Detailed instructions with commands/config]
[Expected output or validation]
[Common issues and troubleshooting]

### Step 2: [Next Specific Action]

[Continue pattern]

## Configuration Examples

[Full config snippets, scripts, or code samples]
[Annotated with inline comments]

## Validation and Testing

[How to verify correct implementation]
[Test cases and expected results]
[Monitoring and observability]

## Troubleshooting

[Common issues and resolutions]
[Debugging approaches]
[Where to look when things fail]

## Performance and Optimization

[Tuning parameters]
[Scaling considerations]
[Resource utilization]

## Security Considerations

[Specific security implications]
[Hardening recommendations]
[Compliance mappings if applicable]

## References and Further Reading

[Official documentation links]
[RFCs, standards, technical specs]
[Related tools and approaches]
```

### Paragraph Construction

**Target length**: 3-6 sentences (can be longer than base style for technical completeness)
**Pattern**: Concept-Detail-Example-Implication

**Example**:
> "Microsegmentation in zero-trust implementations requires careful planning of Layer 7 policies. In our environment, we use Palo Alto Networks' application-based policies combined with user identity from Active Directory to create fine-grained access controls. A typical policy might allow only specific applications (e.g., port 443 for HTTPS) from authenticated users in the 'DataScience' AD group to reach the research data enclave at 10.20.30.0/24, while denying all other traffic. This approach allows us to maintain the principle of least privilege while supporting complex workflows that span multiple systems."

**What's different**:
- Specific vendor/product mentioned with context
- Actual configuration details (ports, IP ranges, AD groups)
- Concrete example embedded
- Still maintains the principle-to-practice flow

### Technical Depth Calibration

**Go deeper on**:
- Architecture patterns and trade-offs
- Configuration specifics with actual parameters
- Version compatibility and migration paths
- Performance characteristics and bottlenecks
- Security implications and threat models
- Integration patterns and APIs
- Troubleshooting and debugging approaches

**Can skip or minimize**:
- Business justification (they're already bought in)
- Basic concept explanations (assume knowledge)
- Executive-level strategic context
- Budget and ROI discussions

---

## III. LANGUAGE AND VOCABULARY

### Technical Precision

**Version specificity**:
- "Windows Server 2022 with TPM 2.0"
- "Python 3.11+ (3.12 recommended for performance improvements)"
- "NIST SP 800-207 (August 2020 revision)"
- "OpenSSL 3.0.x (not 1.1.x due to deprecation)"

**Configuration precision**:
- Actual parameter names: `max_connections=100`
- File paths: `/etc/nginx/sites-available/default`
- Command syntax: `sudo systemctl restart nginx.service`
- API endpoints: `POST /api/v2/auth/token`

**Architectural precision**:
- Layer numbers: "Layer 7 application policies," "Layer 3 routing"
- Protocol specifics: "TLS 1.3 with forward secrecy," "OAuth 2.0 with PKCE"
- Architectural patterns: "event-driven architecture," "microservices with service mesh"

### Technical Vocabulary Clusters

**Infrastructure**:
- Bare metal, hypervisor (ESXi, KVM, Hyper-V), container runtime (Docker, containerd, CRI-O)
- Infrastructure as Code (Terraform, Ansible, Pulumi)
- Configuration management, drift detection, immutable infrastructure

**Security**:
- Threat modeling, attack surface, lateral movement, privilege escalation
- Defense in depth, least privilege, separation of duties
- SIEM, EDR, XDR, SOAR
- CVE, CVSS, CWE, exploit chains

**Networking**:
- BGP, OSPF, VxLAN, segment routing
- East-west traffic, north-south traffic
- MTU, TCP window size, buffer bloat
- Software-defined networking, network function virtualization

**Development/DevOps**:
- CI/CD pipeline, GitOps, infrastructure as code
- Blue-green deployment, canary releases, feature flags
- Observability (metrics, logs, traces), SLI/SLO/SLA
- Container orchestration, service mesh, API gateway

### Code and Configuration Examples

**Include actual code/config when relevant**:

```yaml
# Example nginx configuration for zero-trust proxy
server {
    listen 443 ssl http2;
    server_name api.example.edu;

    # Require client certificate (mutual TLS)
    ssl_client_certificate /etc/nginx/ssl/ca-chain.pem;
    ssl_verify_client on;
    ssl_verify_depth 2;

    location /api/ {
        # Verify JWT in addition to mTLS
        auth_request /auth;
        proxy_pass http://backend:8080/;

        # Pass identity headers
        proxy_set_header X-Client-CN $ssl_client_s_dn;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
    }

    location = /auth {
        internal;
        proxy_pass http://auth-service:9000/verify;
        # Additional auth validation
    }
}
```

**Annotation style**:
- Inline comments explaining non-obvious choices
- Note security implications
- Highlight configuration trade-offs
- Point out common mistakes

---

## IV. RHETORICAL STRATEGY FOR TECHNICAL CONTENT

### Technical Problem-Solution Pattern

**Primary pattern**: **Problem → Architecture → Implementation → Validation**

**1. Problem definition** (technical, not business)
- Specific technical challenge
- Constraints and requirements
- Why existing approaches fall short
- Edge cases or complications

*Example*:
> "Implementing zero-trust architecture in higher education networks presents unique challenges due to the diversity of endpoint devices, the need to support legacy research equipment that can't be easily updated, and the requirement for guest network access that maintains acceptable security postures. Traditional NAC solutions struggle with the variety of authentication methods required across these use cases."

**2. Architecture and approach**
- Design principles applied
- Technology choices and rationale
- Architecture diagrams if helpful
- Trade-offs acknowledged

**3. Implementation details**
- Step-by-step guidance
- Configuration examples
- Integration points
- Testing approach

**4. Validation and operations**
- How to verify correctness
- Monitoring and alerting
- Troubleshooting guide
- Operational considerations

### Types of Technical Evidence

**What technical audiences find credible**:
- **Actual implementation experience**: "In production for 18 months across 50,000 endpoints"
- **Performance data**: "Reduced authentication latency from 250ms to 45ms"
- **Comparative testing**: "Benchmarked three solutions; here's what we found"
- **Open source/community validation**: "Widely adopted pattern in CNCF projects"
- **Standards compliance**: "Implements NIST 800-207 requirements including..."

**Technical authorities**:
- RFCs and internet standards
- NIST publications (with specific control mappings)
- STIG and CIS benchmarks (with specific rule IDs)
- CVE databases and security advisories
- Vendor technical documentation (official, not marketing)
- Open source project documentation
- Conference presentations and academic papers (occasionally)

---

## V. IMPLEMENTATION-FOCUSED WRITING

### Step-by-Step Guidance

**Effective technical steps**:

```markdown
### Step 3: Configure Identity Provider Integration

1. **Generate service account credentials** in your IdP:
   ```bash
   # For Azure AD
   az ad sp create-for-rbac --name zero-trust-gateway \
     --role contributor \
     --scopes /subscriptions/{subscription-id}
   ```

   Save the output JSON; you'll need `appId`, `password`, and `tenant`.

2. **Configure the gateway authentication module**:

   Edit `/etc/zt-gateway/idp.conf`:
   ```ini
   [azuread]
   tenant_id = your-tenant-id
   client_id = your-app-id
   client_secret = your-password
   authority = https://login.microsoftonline.com/{tenant}
   ```

3. **Validate IdP connectivity**:
   ```bash
   sudo zt-gateway test-auth --provider azuread
   ```

   Expected output:
   ```
   [OK] Successfully authenticated test user
   [OK] Retrieved group memberships
   [OK] Token refresh working
   ```

4. **Common issues**:
   - **Error: "Invalid client secret"**: Ensure no trailing whitespace in config
   - **Error: "Insufficient permissions"**: Service principal needs `User.Read.All` and `Group.Read.All` permissions in Azure AD
   - **Timeout errors**: Check firewall rules allow outbound HTTPS to `login.microsoftonline.com`
```

**Key elements**:
- Numbered steps with clear actions
- Actual commands with syntax
- Expected outputs for validation
- Troubleshooting for common failures
- Security notes where relevant

### Architecture and Design Patterns

**Technical architecture discussion**:

```markdown
## Architecture: Defense-in-Depth for Zero-Trust

Our implementation uses a layered approach:

1. **Network Layer** (L3/L4):
   - Microsegmentation via VxLAN overlays
   - Default-deny posture with explicit allow rules
   - Segment routing for traffic steering

2. **Application Layer** (L7):
   - Reverse proxy with mTLS (nginx with custom auth module)
   - API gateway for service-to-service (Kong with JWT validation)
   - Per-request authentication and authorization

3. **Identity Layer**:
   - Centralized IdP (Azure AD) with MFA enforcement
   - Service mesh identity (Istio with SPIFFE/SPIRE)
   - Short-lived credentials (1-hour JWT expiry, 8-hour refresh limit)

4. **Data Layer**:
   - Encryption at rest (LUKS with TPM-sealed keys)
   - Encryption in transit (TLS 1.3 minimum)
   - Field-level encryption for sensitive data (AES-256-GCM)

**Trade-offs**:
- Higher latency (avg +30ms per request due to auth overhead)
- Increased operational complexity (more components to monitor)
- Better security isolation (breach impact limited to single segment)
- Improved audit trail (complete request attribution)
```

**What's different from general audience**:
- Specific technologies and protocols named
- Layer-specific details provided
- Quantified performance impact
- Trade-offs explicitly technical

---

## VI. TECHNICAL SIGNATURES AND PATTERNS

### Technical Opening Patterns

**Problem-focused openings**:
- "Implementing [X] at scale reveals challenges not apparent in lab environments, particularly [specific issue]"
- "The standard approach to [X] using [Y] breaks down when [specific constraint], requiring [alternative]"
- "When migrating from [legacy] to [modern], three critical issues arise: [A], [B], and [C]"

**Architecture-focused openings**:
- "Zero-trust network architecture relies on several core components working in concert: [list]. This guide focuses on [specific component] and its integration points."
- "Microsegmentation can be implemented at multiple layers—network (L3/L4), application (L7), or both. Our approach uses [X] because [technical rationale]."

### Technical Explanation Patterns

**Concept → Mechanism → Implementation**:

> "Zero-trust eliminates network location as a trust factor. This requires authenticating and authorizing every request, regardless of source network. In practice, we implement this using a reverse proxy that validates JWT tokens on every API call, combined with mutual TLS to verify client identity at the transport layer."

**Compare and contrast**:

> "Traditional VPN approaches (IPsec or SSL VPN) grant network-level access once authenticated, allowing lateral movement. By contrast, application-level access control via zero-trust proxies grants access only to specific services, preventing lateral movement even after initial authentication."

**Technical definition with em-dash**:

> "The protect surface—the minimal set of critical resources requiring direct protection—should be as small as possible to reduce complexity. In our environment, this includes the identity provider (Azure AD), the certificate authority (HashiCorp Vault), and the policy engine (Open Policy Agent), totaling fewer than 20 services versus thousands of downstream applications."

### Code and Configuration Patterns

**Annotated configurations**:

```python
# Policy enforcement example using Open Policy Agent
package authz

import future.keywords.if
import future.keywords.in

# Default deny - explicit allow required
default allow = false

# Allow if user has required role AND resource access
allow if {
    # Verify JWT signature and claims
    token.valid

    # Check role membership
    required_role := data.role_mappings[input.resource]
    required_role in token.payload.roles

    # Check resource-level permissions
    permission := data.permissions[input.resource][input.action]
    permission.allowed

    # Additional context: time-based access
    time_allowed(data.access_windows[required_role])
}

# Time-based access control helper
time_allowed(window) if {
    current_hour := time.clock(time.now_ns())[0]
    current_hour >= window.start
    current_hour < window.end
}
```

**What makes this effective**:
- Actual working code (not pseudocode)
- Inline comments explain logic
- Shows practical policy enforcement
- Demonstrates framework usage (OPA)

---

## VII. TROUBLESHOOTING AND OPERATIONAL GUIDANCE

### Troubleshooting Section Pattern

```markdown
## Common Issues and Resolutions

### Issue: Authentication failures after IdP token refresh

**Symptoms**:
- Users disconnected every 60 minutes
- Logs show: `ERROR: Token validation failed - exp claim in past`

**Root cause**:
Clock skew between gateway and IdP servers exceeding tolerance (default 60s).

**Resolution**:
1. Verify time synchronization:
   ```bash
   timedatectl status
   # Ensure NTP sync is active
   ```

2. Increase clock skew tolerance (if NTP sync not possible):
   ```ini
   # /etc/zt-gateway/auth.conf
   [jwt]
   clock_skew_tolerance = 300  # 5 minutes
   ```

3. Monitor clock drift:
   ```bash
   # Add to monitoring
   ntpq -p  # Check NTP peer status
   ```

**Prevention**:
- Configure NTP on all infrastructure systems
- Alert on clock drift >10s
- Use hardware timekeeping (PPS) for critical systems

---

### Issue: Performance degradation under load

**Symptoms**:
- Auth latency increases from 50ms to 2000ms+
- Gateway CPU at 100%
- Connection pool exhaustion errors

**Root cause**:
Synchronous LDAP queries blocking request processing.

**Resolution**:
1. Enable async LDAP queries with caching:
   ```ini
   [ldap]
   async_queries = true
   cache_ttl = 300  # 5 minute cache
   cache_size = 10000  # entries
   ```

2. Scale horizontally (add gateway instances):
   ```bash
   # Deploy additional gateways behind load balancer
   # Ensure session affinity not required (stateless design)
   ```

3. Monitor cache hit rate:
   ```
   zt-gateway metrics | grep ldap_cache_hit_rate
   # Target: >80% hit rate
   ```
```

**Key elements for troubleshooting sections**:
- Specific symptoms (logs, errors, behavior)
- Root cause identified
- Step-by-step resolution
- Prevention/monitoring guidance
- Performance metrics and targets

---

## VIII. SECURITY AND COMPLIANCE DEPTH

### Security-Specific Content

**Threat modeling**:
```markdown
## Threat Model Considerations

**Attack vectors addressed**:
1. **Compromised credentials**: Mitigated by short-lived tokens (1hr), MFA requirement
2. **Lateral movement**: Prevented by microsegmentation, per-request auth
3. **Privilege escalation**: Limited by RBAC, just-in-time access, audit logging

**Residual risks**:
- **IdP compromise**: Single point of failure; mitigate with monitoring, MFA for admins
- **Token theft**: Tokens valid for 1hr; consider shorter lifetime for high-value resources
- **Insider threat**: Audit logging and anomaly detection required

**Compliance mappings**:
| Control | NIST 800-53 | CIS v8 | Implementation |
|---------|-------------|---------|----------------|
| MFA enforcement | IA-2(1) | 6.3 | Azure AD Conditional Access |
| Session management | AC-12 | 4.3 | 1-hour JWT expiry |
| Audit logging | AU-2 | 8.2 | Centralized to Splunk |
| Least privilege | AC-6 | 5.4 | OPA policy engine |
```

### Specific Control Implementation

**Technical control details**:

```markdown
## STIG Compliance: RHEL 8

### V-230221: Disable USB storage

**STIG Rule**: RHEL-08-040080
**Severity**: CAT II
**CCI**: CCI-001958

**Implementation**:
```bash
# Blacklist USB storage module
echo "install usb-storage /bin/true" > /etc/modprobe.d/usb-storage.conf

# Prevent module load
echo "blacklist usb-storage" >> /etc/modprobe.d/blacklist.conf

# Unload if currently loaded
modprobe -r usb-storage
```

**Validation**:
```bash
# Should return nothing if properly disabled
lsmod | grep usb_storage
```

**Exceptions**: Research systems requiring USB data acquisition - documented exception in RMF package.
```

---

## IX. PERFORMANCE AND SCALABILITY

### Performance-Focused Content

**Benchmarking and tuning**:

```markdown
## Performance Characteristics

### Baseline Performance (single gateway instance)

**Test environment**:
- Hardware: 8 vCPU, 16GB RAM, 10Gbps NIC
- Load: 1000 concurrent users, 10,000 req/sec
- Auth: JWT validation + LDAP group lookup

**Results**:
| Metric | p50 | p95 | p99 |
|--------|-----|-----|-----|
| Auth latency | 45ms | 120ms | 250ms |
| Throughput | 9,800 req/sec | - | - |
| CPU utilization | 65% | 85% | 92% |
| Memory | 8.2GB | 9.1GB | 9.8GB |

### Tuning Recommendations

**For latency optimization** (target p95 < 100ms):
1. Enable LDAP caching (5min TTL): -40ms p95
2. Use connection pooling: -15ms p95
3. Enable HTTP/2: -10ms p95

**For throughput optimization** (target 15k req/sec):
1. Horizontal scaling (3 instances): +13k req/sec
2. Async processing for logging: +1.5k req/sec
3. Kernel tuning (`net.core.somaxconn=4096`): +500 req/sec

### Scaling Patterns

**Horizontal scaling** (recommended):
- Stateless design allows simple load balancing
- Add instances as needed
- Linear scalability up to ~50k req/sec (tested)

**Vertical scaling** (limited effectiveness):
- CPU-bound workload benefits from more cores
- Diminishing returns above 16 vCPU
- Memory not typically bottleneck (<16GB under heavy load)
```

---

## X. INTEGRATION AND INTEROPERABILITY

### Integration Patterns

**API and integration guidance**:

```markdown
## Integration with External Systems

### SIEM Integration (Splunk)

**Log forwarding configuration**:
```ini
# /etc/zt-gateway/logging.conf
[syslog]
enabled = true
host = splunk-hec.example.edu
port = 8088
protocol = https
format = json

[events]
auth_success = true
auth_failure = true
policy_violation = true
performance_degradation = true
```

**Splunk HEC event format**:
```json
{
  "time": 1699564800,
  "host": "zt-gateway-01",
  "source": "zt-gateway",
  "sourcetype": "zero-trust:auth",
  "event": {
    "action": "authentication",
    "result": "success",
    "user": "tjordan@wisc.edu",
    "source_ip": "10.1.2.3",
    "resource": "/api/v2/data",
    "latency_ms": 47,
    "auth_method": "azuread_jwt"
  }
}
```

**Splunk queries for monitoring**:
```spl
# Authentication failure rate
index=security sourcetype="zero-trust:auth" result=failure
| timechart span=5m count

# Anomalous access patterns
index=security sourcetype="zero-trust:auth"
| stats dc(resource) as unique_resources by user
| where unique_resources > 20
```

### Service Mesh Integration (Istio)

**Configuration for east-west traffic**:
```yaml
apiVersion: security.istio.io/v1beta1
kind: PeerAuthentication
metadata:
  name: default
  namespace: production
spec:
  mtls:
    mode: STRICT  # Require mutual TLS

---
apiVersion: security.istio.io/v1beta1
kind: AuthorizationPolicy
metadata:
  name: data-api-authz
  namespace: production
spec:
  selector:
    matchLabels:
      app: data-api
  rules:
  - from:
    - source:
        principals: ["cluster.local/ns/frontend/sa/webapp"]
    to:
    - operation:
        methods: ["GET", "POST"]
        paths: ["/api/v2/*"]
    when:
    - key: request.auth.claims[role]
      values: ["data-scientist", "analyst"]
```
```

---

## XI. EXAMPLE TRANSFORMATIONS

### Base Style (General IT Audience):
> "Zero-trust architecture acknowledges that infiltration points don't determine ultimate targets—once inside a network, threat actors tend to move laterally. Implementation requires several key components: identity verification, device assessment, policy enforcement, and continuous monitoring."

### Technical Practitioner Adaptation:
> "Zero-trust architecture eliminates network location as a trust boundary, requiring authentication and authorization at the application layer for every request. Our implementation uses nginx as a reverse proxy with custom Lua modules for JWT validation (HS256 algorithm, 1-hour expiry), integrated with Azure AD as the IdP. Device posture assessment occurs via endpoint agent (Jamf for macOS, Intune for Windows) that reports compliance status to the policy engine (Open Policy Agent). Per-request latency overhead averages 30-45ms in production (p95: 120ms), with horizontal scaling supporting up to 15,000 req/sec per gateway instance."

**What changed**:
- Specific technologies named (nginx, Lua, Azure AD, Jamf, Intune, OPA)
- Technical details (JWT algorithm, token expiry, implementation method)
- Performance characteristics (latency numbers, throughput capacity)
- Architecture specifics (reverse proxy, endpoint agents, policy engine)
- Removed high-level "why" explanation
- Added operational metrics

---

## XII. VALIDATION CHECKLIST FOR TECHNICAL WRITING

Before finalizing technical content, verify:

**Technical accuracy**:
- [ ] Commands and syntax verified in test environment
- [ ] Version numbers current and specified
- [ ] Configuration examples tested and working
- [ ] Performance claims based on actual measurements
- [ ] Security implications reviewed

**Completeness**:
- [ ] Prerequisites clearly stated
- [ ] Edge cases and limitations documented
- [ ] Troubleshooting guidance included
- [ ] Validation/testing steps provided
- [ ] References to official documentation

**Usability**:
- [ ] Step-by-step guidance is unambiguous
- [ ] Code/config examples are copy-pasteable
- [ ] Expected outputs shown for validation
- [ ] Common errors anticipated and addressed
- [ ] Operational considerations covered

**Technical depth**:
- [ ] Assumes appropriate baseline knowledge
- [ ] Provides sufficient detail for implementation
- [ ] Explains technical trade-offs
- [ ] Addresses security and performance
- [ ] Links to deeper technical resources

**Style consistency**:
- [ ] Maintains Tom's framework-based thinking
- [ ] Uses active voice and strong verbs
- [ ] Includes specific examples and evidence
- [ ] Acknowledges complexity appropriately
- [ ] Peer-level technical voice maintained

---

## Conclusion: Technical Writing for Practitioners

Writing for technical audiences requires **depth, precision, and completeness over brevity**. Technical practitioners value specificity, actual implementation experience, and comprehensive coverage of edge cases. They are skeptical of assertions without evidence and appreciative of battle-tested guidance.

Tom Jordan's base style adapts well to technical audiences because it already emphasizes:
- Framework-based approaches (which technical audiences appreciate as architecture)
- Specific examples (which scale to code/config examples)
- Acknowledgment of complexity (which becomes troubleshooting and edge cases)
- Pragmatic realism (which becomes operational considerations)

**The technical version of your voice is**: The senior engineer who has implemented this in production, debugged the edge cases, optimized the performance, and can guide peers through the same journey with specific, tested, actionable guidance.

---

## XIII. HISTORICAL CONTEXT AND FOUNDATIONAL THINKING

### A Gentle Historical Awareness

*This section is completely optional enrichment. You don't need to know any of this history to write excellent technical documentation. But connecting current practice to foundational principles can sometimes deepen our understanding and help us make better design decisions.*

When we design systems today, we're building on decades of hard-won lessons from those who came before us. The principles we apply—defense in depth, least privilege, separation of concerns—weren't invented yesterday. They emerged from real systems that failed, real breaches that hurt people, and real engineers learning what works under pressure.

**Consider these connections** (when relevant and helpful):

- **Saltzer & Schroeder's 1975 principles** ("The Protection of Information in Computer Systems") established design principles we still use: economy of mechanism, fail-safe defaults, complete mediation, least privilege, separation of privilege, least common mechanism, psychological acceptability. Zero-trust architecture implements many of these principles at scale.

- **The Unix philosophy** (Thompson, Ritchie, McIlroy) emphasized doing one thing well, composability, and text as a universal interface. Modern microservices architecture and container orchestration echo these principles—small, focused services communicating via well-defined interfaces.

- **End-to-end argument** (Saltzer, Reed, Clark 1984) established that certain functions can only be correctly implemented end-to-end, not in intermediate layers. This principle guides our API design, encryption practices (encrypt at the application layer, not just transport), and distributed system design.

- **ARPANET's design principles** (1969-1989) prioritized resilience through decentralization and redundancy. When we design for high availability and disaster recovery today, we're applying lessons learned from building networks that could survive partial failures—originally motivated by Cold War concerns, now essential for business continuity.

These aren't abstract academic concepts—they're practical wisdom from engineers who built systems that had to work under real constraints, often with much less capable hardware and networks than we have today. When we implement microsegmentation, we're applying lessons learned from decades of network breaches. When we use infrastructure-as-code, we're building on lessons from configuration drift causing countless incidents.

**For the Stoically inclined** (completely optional):

Technical work offers rich opportunities for practicing Stoic principles:

- **Dichotomy of control** (Epictetus): We control our code quality, documentation clarity, and testing rigor. We don't control production incidents, upstream bugs, or vendor timelines. Focus energy where we have agency.

- **Amor fati** (Marcus Aurelius): Incidents and failures are inevitable in complex systems. Embrace them as learning opportunities. Blameless postmortems and psychological safety allow growth from failure.

- **Premeditatio malorum** (Seneca): Pre-mortem exercises, failure mode analysis, chaos engineering—these are Stoic practices applied to engineering. By imagining failure scenarios, we prepare better and reduce their emotional impact.

- **Sympatheia** (interconnection): Our systems connect to others' work. Upstream dependencies, downstream consumers, operational teams, end users—we're part of a larger technical ecosystem. Design with empathy for those who will operate, maintain, and depend on our systems.

The Stoics would have made excellent SREs—they understood that systems fail, that we control only our response, and that building resilience requires both technical rigor and emotional equanimity.

---

## XIV. ANTI-OPPRESSIVE LANGUAGE AND JUSTICE IN TECHNOLOGY

### Technology as Liberation or Control

Every technical choice either opens doors or closes them. Who gets to participate in technology? Who gets excluded by our design decisions? These aren't political questions—they're engineering requirements that affect real people's lives.

**Questions for technical decisions:**

**Who can build and contribute?**
- Does our tool require expensive licenses, or is it open source?
- Do our docs assume computer science degrees, or do we teach concepts?
- Is our community welcoming to different backgrounds and approaches?
- Do our contribution guidelines create barriers based on cultural communication styles?

**Who can use what we build?**
- Does our interface require high-end devices, or does it work on older hardware?
- Does our application assume high-bandwidth connectivity?
- Does our design work with assistive technologies?
- Do we require phone numbers for 2FA (excluding people without phones or with limited plans)?

**Who do our systems serve?**
- Does our algorithm perpetuate existing biases in training data?
- Does our "optimization" optimize for profit or for people?
- Does our automation replace human judgment in ways that harm vulnerable people?
- Do we build surveillance infrastructure that disproportionately targets marginalized communities?

### Examples in Technical Practice

**Authentication design:**
- ❌ "SMS-based 2FA (cheap and easy)" → excludes people without phone plans or in areas with poor SMS delivery
- ✅ "TOTP-based 2FA with backup codes" → works offline, no phone plan required, more accessible globally

**Performance optimization:**
- ❌ "Optimize for latest Chrome on desktop (our primary users)" → excludes mobile users, older devices, different browsers
- ✅ "Progressive enhancement: works on all browsers, enhanced features where supported" → serves everyone, better experience for those with capable devices

**Documentation:**
- ❌ "Assumes familiarity with Kubernetes concepts" → excludes people new to cloud-native
- ✅ "Explains concepts with links to deeper learning; includes glossary" → welcomes learners while serving experts

**Infrastructure choices:**
- ❌ "Cloud-only, requires high bandwidth" → excludes humanitarian field work, low-bandwidth contexts, sovereignty concerns
- ✅ "Cloud-native but also deployable on-premises; works offline; data sovereignty respected" → serves more contexts, more resilient

### Open Source as Anti-Oppressive Practice

Open source software democratizes technology access. Proprietary software requires money; open source requires only knowledge and effort—both of which can be shared. When we contribute to open source, document our work clearly, and welcome newcomers, we're making technology more accessible.

**But**: Open source communities can still be oppressive through gatekeeping, hostile communication, unwelcoming contribution processes, and burnout culture. Being open source doesn't automatically make us just.

### Accessibility is Engineering

Accessibility isn't a "nice to have"—it's engineering rigor. Building for screen readers, keyboard navigation, low-bandwidth networks, older devices, and diverse cognitive styles makes our systems better for everyone. The curb-cut effect: accommodations for disabilities improve usability for all.

**Technical accessibility practices:**
- Semantic HTML and ARIA labels (not just visual styling)
- Keyboard navigation support (not just mouse/touch)
- Color contrast and non-color indicators (not color alone)
- Captions and transcripts for video content
- Progressive enhancement (works without JavaScript)
- Responsive design (works on small screens)
- Low-bandwidth modes (works on slow connections)
- Clear error messages (helps everyone)

### Writing with Anti-Oppressive Awareness

**Center diverse perspectives:**
- Don't assume "everyone" uses MacOS, high-end hardware, fast internet, or speaks English fluently
- Include examples from different contexts (not just US tech companies)
- Feature contributors and users from marginalized communities
- Acknowledge when our experience is limited to specific contexts

**Challenge assumptions:**
- "Best practices" often mean "what works at well-funded US tech companies"
- "Industry standard" often means "what dominant vendors sell"
- "Professional" often encodes white, Western, male communication styles
- "Meritocracy" often ignores different starting points and barriers

**Name systems and power:**
- Surveillance capitalism, not just "data-driven personalization"
- Algorithmic discrimination, not just "unintended bias"
- Digital colonialism, not just "expanding internet access"
- Labor exploitation in supply chains and data annotation work

**Use inclusive language:**
- "They" instead of "he" for generic developers
- "Staff" or "workforce" rather than "manpower"
- "Allowlist/blocklist" rather than "whitelist/blacklist" (clearer and not racially coded)
- "Primary/secondary" rather than "master/slave" in technical contexts

---

## XV. CROSS-LINGUISTIC AND GLOBAL ACCESSIBILITY

### Writing for Global Technical Communities

Technical communities span every language and culture. When we write clearly for machine translation, we make our documentation accessible to engineers worldwide. When we avoid idioms and cultural assumptions, we respect linguistic diversity and make our content more usable.

This isn't just courtesy—it's **operational necessity**. Documentation gets translated. APIs get called from everywhere. Systems run on every continent. Code comments get read by international teams.

### Writing for Translation and International Audiences

**Clear, literal technical language:**
- Simple sentence structure (one main clause per sentence)
- Active voice ("configure the parameter" not "the parameter is configured")
- Specific verbs ("stop the service" not "kill the service")
- Standard technical terminology (international English, not regional slang)

**Avoid idioms and figurative language:**
- ❌ "Let's tackle the low-hanging fruit" → ✅ "Let's address the easiest improvements first"
- ❌ "This will bite you later" → ✅ "This will cause problems later"
- ❌ "Boilerplate code" → ✅ "Template code" or "standard initialization code"
- ❌ "Sanity check" → ✅ "Validation check" or "verify correct operation"

**Avoid cultural-specific references:**
- ❌ "Like NFL draft picks" → ✅ "Selected in order of priority"
- ❌ "Monday morning quarterback" → ✅ "Analyze decisions after the fact"
- ❌ "Going postal" → ✅ "System failure" or "outage"

**Technical idioms to avoid:**

| Avoid | Use Instead |
|-------|-------------|
| "Spin up containers" | "Start containers" or "launch containers" |
| "Bake in security" | "Include security from the design phase" |
| "Fire off requests" | "Send requests" or "initiate requests" |
| "Hammer the API" | "Send high-volume requests to the API" |
| "Nuke the database" | "Delete all records" or "drop the database" |
| "Kick off the pipeline" | "Start the pipeline" or "trigger the pipeline" |
| "Kill the process" | "Stop the process" or "terminate the process" |
| "Bulletproof code" | "Robust code" or "resilient code" |

### Writing for Machine Translation

**Test your documentation** using Google Translate, DeepL, or other services:

1. Translate to 2-3 languages (e.g., Spanish, French, Japanese)
2. Translate back to English
3. Check if technical meaning preserved
4. Revise sentences that translate poorly

**Good for translation:**
> "Configure the authentication parameter in the configuration file. Set the value to `enabled`. Restart the service for changes to take effect."

**Translates poorly:**
> "You'll want to flip the auth switch in your config—just set it to enabled and bounce the service."

### International Conventions in Technical Writing

**Dates:** Use ISO 8601 format (YYYY-MM-DD) or spell out month
- ✅ "2025-11-24" or "November 24, 2025"
- ❌ "11/24/25" (ambiguous: US vs. international format)

**Times:** Use ISO 8601 with timezone
- ✅ "14:30 UTC" or "2025-11-24T14:30:00Z"
- ❌ "2:30 PM EST"

**Numbers:**
- Large numbers: Use spaces or underscores as separators
  - ✅ "1,000,000" or "1_000_000"
  - ❌ Different conventions (European: 1.000.000)
- Decimal: Be explicit about notation
  - ✅ "3.14 (decimal point)" when precision matters

**Currency:** Always specify currency code
- ✅ "100 USD" or "$100 USD"
- ❌ "$100" (which dollar?)

**Measurements:**
- Provide both metric and imperial when relevant
- ✅ "Maximum cable length: 100 meters (328 feet)"
- Consider metric-first (more universal): "100m (328ft)"

### Code Comments and Documentation

**Comments in code should also be translation-friendly:**

```python
# Good for translation:
# Check if the user has permission to access this resource
# Return 403 Forbidden if permission denied
if not has_permission(user, resource):
    return 403

# Harder to translate:
# Bail out if user doesn't have the juice to access this
if not has_permission(user, resource):
    return 403
```

**API documentation:**
- Use clear, standard HTTP terminology
- Avoid jargon like "ping the endpoint" → "send request to the endpoint"
- Include request/response examples (code is universal)
- Provide error messages in English (standardized) but structure for localization

### Language Justice as Technical Practice

**Linguistic accessibility is social justice:**
- English dominance in tech excludes brilliant people
- Machine translation costs shouldn't prevent collaboration
- Local languages should be primary in local contexts
- Documentation translation enables participation

When we write clearly for machine translation, we:
- Reduce barriers for non-English speakers
- Enable collaboration across language boundaries
- Respect linguistic diversity
- Distribute technical knowledge more equitably

---

## FINAL INTEGRATION: Technical Writing That Welcomes Everyone

The best technical documentation is:
- **Precise and complete** (serves experts)
- **Clear and accessible** (welcomes learners)
- **Translation-friendly** (works globally)
- **Justice-oriented** (considers who's included/excluded)
- **Connected to foundations** (respects those who came before)

You don't have to be perfect. You don't have to know everything. But being aware of these dimensions—historical foundations, social justice, linguistic accessibility—makes us better technical communicators and more thoughtful engineers.

Everyone is welcome here. Everyone has something to contribute. Let's build technology that reflects that.
