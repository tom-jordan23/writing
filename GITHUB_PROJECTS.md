# Tom Jordan's GitHub Projects - Technical Profile

**GitHub Profile:** https://github.com/tom-jordan23
**Affiliation:** University of Wisconsin - Madison
**Total Public Repositories:** 27
**Profile Stars:** 8 total across repositories

## Overview

Tom Jordan's GitHub portfolio reveals a technically diverse engineer with expertise spanning cybersecurity, AI/ML, humanitarian technology, and infrastructure automation. His work demonstrates a pattern of building practical tools and educational environments, often combining multiple technologies to solve real-world problems. Projects range from production-ready applications to experimental research, with a notable focus on:

- Zero Trust security architectures and modern authentication
- Natural Language Processing and AI/ML for humanitarian applications
- Infrastructure automation and containerization
- Knowledge graphs and information extraction
- Environmental monitoring and IoT systems

---

## Major Active Projects

### 1. **openrivercam** (Python)
**Updated:** November 24, 2025
**Status:** Active Development
**Description:** River monitoring station deployment using Raspberry Pi 5

**What It Does:**
Establishes automated field stations for continuous river observation combining computer vision, infrared imaging, and environmental sensors. The system runs NodeORC (open-source river observation) on solar-powered Raspberry Pi hardware for day-and-night monitoring.

**Technical Components:**
- Raspberry Pi 5 with integrated camera and IR capabilities
- Solar power system design
- GNSS/RTK surveying for precise geolocation
- Data collection and transmission pipelines
- LiveORC integration for remote data hosting

**Significance:** Demonstrates IoT deployment expertise and integration of embedded systems with environmental monitoring applications.

---

### 2. **cooking_mcp** (Python/Node.js)
**Updated:** September 22, 2025
**Status:** Production-Ready
**Description:** Model Context Protocol server for cooking experiments with multi-channel feedback

**What It Does:**
Production-grade MCP server that enables structured tracking of cooking experiments with automated feedback collection across multiple messaging platforms (Slack, Telegram, WhatsApp, SMS, Signal, Email). Uses Git-backed storage for version-controlled lab notebook entries.

**Technical Stack:**
- Model Context Protocol (MCP) implementation
- Multi-channel messaging integration
- YAML/Markdown data structure
- Git version control
- AI-enhanced recipe recommendations
- Zero-trust security architecture
- Deployment: Docker, Kubernetes, Render

**Significance:** Shows ability to build production-ready systems with modern protocols, comprehensive integrations, and enterprise-grade security.

---

### 3. **policydoodle** (Shell/HCL/Docker)
**Updated:** September 12, 2025
**Status:** Active
**Description:** Natural language policy document query system

**What It Does:**
Enables organizations to upload policy documents and query them using natural language instead of traditional search. Built on AnythingLLM for document ingestion and conversational retrieval.

**Technical Components:**
- AnythingLLM integration
- Infrastructure-as-code (Terraform)
- Docker containerization
- Render platform deployment
- Shell-based lifecycle management scripts

**Significance:** Practical application of RAG (Retrieval-Augmented Generation) for enterprise document management.

---

### 4. **ztlab** (HTML/Shell)
**Updated:** August 22, 2025
**Status:** Active & Functional
**Description:** Educational Zero Trust and SASE laboratory environment

**What It Does:**
Complete Docker-based learning environment simulating Secure Access Service Edge (SASE) architecture using open-source components. Designed for teaching Zero Trust networking principles.

**Architecture Simulation:**
- **Identity Management:** Zitadel (OAuth2/OIDC)
- **Zero Trust Network Access:** OpenZiti controller
- **Secure Web Gateway:** OPNsense with SSL/TLS inspection
- **Cloud Security Broker:** Cloud Custodian (policy-as-code)
- **Monitoring:** ELK Stack (Elasticsearch, Logstash, Kibana)
- **Network Zones:** External internet, DMZ, corporate internal, management networks

**Significance:** Educational resource demonstrating complex security architecture concepts with practical, hands-on implementation.

---

### 5. **graph** (Python)
**Updated:** August 7, 2025
**Status:** Phase 1 Complete (12-phase roadmap)
**Description:** Knowledge graph extractor with multi-model support

**What It Does:**
Extracts entities and relationships from text to create knowledge graphs, supporting multiple AI models (OpenAI GPT, Anthropic Claude, local LLMs, spaCy) with benchmarking capabilities.

**Key Features:**
- Multi-model entity/relationship extraction
- Interactive Streamlit web interface
- Dynamic graph visualization with filtering
- Export formats: RDF, OWL, GraphML, JSON-LD, GEXF, Neo4j Cypher
- Performance benchmarking framework
- Docker Compose deployment

**Development Roadmap:**
12-phase plan covering data models, extractors, graph construction, export formats, benchmarking, interfaces, and optimization.

**Significance:** Sophisticated information extraction system demonstrating knowledge of NLP, graph databases, and model evaluation.

---

### 6. **graphrag** (Python)
**Updated:** August 1, 2025
**Status:** Active Development
**Description:** RAG + Knowledge Graph demonstration with multi-LLM support

**What It Does:**
Comprehensive application combining Retrieval-Augmented Generation with interactive knowledge graphs, enabling side-by-side comparison of responses from multiple LLM providers.

**Architecture:**
- **Frontend:** React with dark/light themes
- **Backend:** FastAPI
- **Databases:** Neo4j (graph), ChromaDB (vectors)
- **Models:** OpenAI, Anthropic, Ollama, HuggingFace
- **Document Support:** PDF, DOCX, TXT, MD, CSV, JSON, HTML
- **Deployment:** Docker, Kubernetes
- **Testing:** Unit, integration, regression coverage

**Significance:** End-to-end AI application demonstrating full-stack development, modern UI, multi-database architecture, and production deployment practices.

---

### 7. **openwebui** (Python/JavaScript)
**Updated:** August 21, 2025
**Status:** Active Development
**Description:** Personal AI assistant platform with GraphRAG and MCP

**What It Does:**
Containerized platform for prompt engineering, assistant development, and model evaluation across local and cloud AI models.

**Features:**
- Multi-model support (LightLLM, Ollama, cloud providers)
- Prompt laboratory with versioning and A/B testing
- GraphRAG knowledge enhancement
- Model Context Protocol (MCP) tool integration
- Real-time analytics and performance dashboards
- High-availability Kubernetes deployment

**Technology Stack:**
- React frontend
- LightLLM, Ollama for model serving
- PostgreSQL, Redis, Neo4j, Qdrant
- Docker Compose, Kubernetes, Helm
- Prometheus, Grafana monitoring

**Significance:** Production-ready AI development platform with comprehensive tooling and enterprise deployment capabilities.

---

## Security & Authentication Projects

### 8. **hybrid-auth-lab** (Shell)
**Updated:** July 1, 2025
**Status:** Active Development (8 commits)
**Description:** OAuth Device Flow for SSH authentication

**What It Does:**
Demonstrates integrating OAuth 2.0 Device Flow with Linux SSH, replacing traditional authentication with modern federated identity.

**Components:**
- OAuth Device Flow implementation
- Linux PAM integration
- Keycloak OAuth server (Docker)
- Active Directory federation via LDAP
- Ubuntu SSHD with OAuth PAM (Docker)
- Windows Server 2022 AD controller (QEMU)

**Features:**
- Centralized identity management
- MFA and conditional access support
- Complete quick-start guides
- Configuration import/export workflows

**Significance:** Bridges traditional IT infrastructure with modern authentication, showing deep understanding of identity protocols and Linux system integration.

---

### 9. **zt-info-model** (Markdown)
**Updated:** July 25, 2025
**Status:** Active (4 commits)
**License:** MIT
**Description:** Vendor-agnostic Zero Trust information model

**What It Does:**
Provides framework for understanding Zero Trust architecture across five operational pillars, documenting how components interact without vendor lock-in.

**Five Pillars:**
1. **Identity:** IdP, MFA, risk assessment, policy decisions
2. **Device:** MDM/EDR, inventory, posture assessment, trust scoring
3. **Network:** SDN, edge gateways, microsegmentation, flow monitoring
4. **Applications & Workloads:** App registry, access broker, WAF, runtime security
5. **Data:** Classification, tagging, encryption, DLP, storage enforcement

**Significance:** Educational resource for architects implementing Zero Trust, demonstrating systems thinking and security architecture expertise.

---

### 10. **ad-dc-vagrant** (PowerShell/Ruby)
**Updated:** June 30, 2025
**Status:** Active/Maintained
**Description:** Automated Active Directory domain controller with Packer/QEMU

**What It Does:**
Completely automated Windows Server 2022 VM creation with AD DS and LDIF user/group imports for lab environments.

**Features:**
- Windows Server 2022 with Desktop Experience
- AD configuration for test.wisc.edu domain
- LDIF-based user/group imports from OpenLDAP format
- VNC and RDP remote access
- Unattended installation (25-30 minutes)

**Requirements:**
- Packer v1.7.0+, QEMU with KVM
- 8GB RAM, 10GB disk space minimum

**Attribution:** Based on Stefan Scherer's packer-windows project (MIT license)

**Significance:** Infrastructure automation for complex Windows environments, useful for testing and development.

---

### 11. **wei-lab** (PowerShell/HCL)
**Updated:** July 14, 2025
**Status:** Early-stage
**Description:** Windows Environment Infrastructure test lab

**What It Does:**
Windows domain controller provisioning using Packer for infrastructure automation.

**Significance:** Infrastructure-as-code for Windows environments.

---

### 12. **wei_keycloak** (Shell)
**Updated:** April 9, 2025
**Stars:** 1
**Description:** Keycloak integration project

**Significance:** Identity and access management experimentation.

---

## AI/ML & NLP Projects

### 13. **reliefweb_nlp** (Python)
**Updated:** June 10, 2024
**Status:** Early-stage testing (5 commits)
**License:** Apache-2.0
**Description:** Humanitarian relief data analysis using NLP

**What It Does:**
Python application querying ReliefWeb database using GLIDE numbers (Global Disaster Identifier) with HuggingFace NLP models for analysis.

**Use Case:** Disaster response and humanitarian information management

**Significance:** Application of NLP to humanitarian sector, showing domain expertise beyond pure technical implementation.

---

### 14. **topic_explorer_ml** (Jupyter Notebook)
**Updated:** June 24, 2024
**Status:** Active exploration
**Description:** ML for humanitarian disaster response

**What It Does:**
Explores machine learning for:
- Generating disaster information summaries for response teams
- Extracting quantitative data (casualties, displaced persons)
- Creating enriched datasets for analytical applications

**Models Tested:**
- BART, T5, RoBERTa, DistilBERT
- Text summarization pipelines
- Question-answering against humanitarian texts

**Findings:**
- Summarization shows reasonable results
- Question-answering needs refinement
- Inference times: few seconds to 30+ seconds (batch processing viable)
- No fine-tuning on humanitarian datasets attempted yet

**Next Steps:**
- Fine-tuning with humanitarian datasets
- Exploring AWS Bedrock foundation models

**Significance:** Practical ML research with clear use case and honest assessment of limitations.

---

### 15. **humbert_test** (CSS/Jupyter Notebook)
**Updated:** June 10, 2024
**Status:** Experimental (8 commits)
**License:** Apache-2.0
**Description:** HumBert model experimentation from DEEP

**What It Does:**
Tests HumBert model with six notebooks covering:
- Summarization workflow
- Question pipeline processing
- Data extraction techniques
- Fine-tuning experiments
- Foundation models (basic and RAG approaches)

**Significance:** Early-stage ML experimentation showing learning process.

---

### 16. **rag_example** (Python)
**Updated:** July 25, 2024
**Status:** Early-stage (2 commits)
**License:** GPL-3.0
**Description:** Local RAG demonstration with HuggingFace

**What It Does:**
Minimalistic RAG system demonstration:
- FAISS vector database creation
- Semantic similarity-based document retrieval
- HuggingFace transformers with PyTorch for generation
- Streamlit frontend interface

**Components:**
- `data/documents.txt` - sample corpus
- `scripts/create_vector_db.py` - FAISS indexing
- `scripts/retrieve_and_generate.py` - RAG pipeline
- `app/app.py` - Streamlit UI

**Significance:** Educational example of RAG fundamentals.

---

### 17. **utf-8** (Jupyter Notebook)
**Updated:** May 2, 2025
**Status:** Single commit
**Description:** UTF-8 to ASCII transliteration testing

**What It Does:**
Explores character encoding conversion techniques for converting non-ASCII UTF-8 characters to ASCII equivalents.

**Significance:** Data processing utility for text normalization.

---

### 18. **promptflow** (Python)
**Updated:** July 10, 2024
**Status:** Initial setup (1 commit)
**License:** Apache-2.0
**Description:** Promptflow experimentation in Jupyter

**What It Does:**
Personal exploration of Microsoft's Promptflow framework for building and evaluating LLM-based applications.

**Significance:** Learning new AI development frameworks.

---

## Infrastructure & Deployment Projects

### 19. **deployment_stuff** (Markdown)
**Updated:** August 21, 2025
**Status:** Active (2 commits)
**Description:** Remote IT/Engineering deployment checklists

**What It Does:**
Checklist and reference guide for IT professionals preparing for remote deployments.

**Contents:**
- README.md - project overview
- Electronics-Kit.md - equipment packing list

**Significance:** Practical knowledge capture from field deployment experience.

---

### 20. **essential_docker** (Dockerfile/Shell)
**Updated:** August 9, 2024
**Status:** Early-stage (3 commits)
**Description:** Dockerized Essential Architect

**What It Does:**
Containerizes Essential Architect application with build and run automation scripts.

**Significance:** Application containerization for architecture modeling tools.

---

### 21. **rcselect_redir** (Python)
**Updated:** February 3, 2025
**Status:** Operational (5 commits)
**Description:** Django redirect application for rcselect site migration

**What It Does:**
Simple Django application redirecting users from former rcselect site on Render to new IFRC-hosted location.

**Significance:** Production utility for platform migration.

---

## Standards & Documentation Projects

### 22. **porewg** (PlantUML)
**Updated:** May 9, 2025
**Status:** Active (4 commits)
**Description:** Profiling OpenID for Research and Education Working Group diagrams

**What It Does:**
Technical architecture documentation using UML diagrams for OpenID profiling in research/education institutions.

**Diagram Types:**
- Activity diagrams (user login)
- Class diagrams
- Component diagrams
- Registration sequence diagrams
- Use case diagrams

**Significance:** Participation in standards working group, technical architecture documentation.

---

### 23. **fabric_patterns** (Unknown language)
**Updated:** June 11, 2025
**Status:** Early-stage (4 commits)
**License:** GPL-3.0
**Description:** Pattern repository with cooking and disaster response components

**What It Does:**
Contains two directories:
- cooking_agent
- summarize_disaster

**Note:** Lacks README and detailed documentation

**Significance:** Potentially related to AI prompt patterns or workflow templates.

---

## Forked & Reference Projects

### 24. **game-of-life** (HTML)
**Updated:** June 10, 2016
**Status:** Forked from wakaleo/game-of-life
**Description:** Demo application for "Jenkins: The Definitive Guide" book

**Significance:** Reference project for CI/CD learning.

---

## Placeholder/Empty Projects

### 25. **writing** (No language specified)
**Updated:** November 25, 2025
**Status:** Current working repository (this analysis)

### 26. **geo_stuff** (No language specified)
**Updated:** September 18, 2025
**Description:** "Geospatial odds and ends"
**Status:** Empty repository

### 27. **tojo.world** (JavaScript)
**Updated:** May 29, 2024
**Status:** No description or README available

---

## Technical Themes & Patterns

### Primary Technology Areas

**1. AI/ML & Natural Language Processing**
- Multi-LLM integration and comparison
- Knowledge graph extraction and visualization
- RAG (Retrieval-Augmented Generation) implementations
- Humanitarian NLP applications
- Model benchmarking and evaluation
- HuggingFace transformers expertise

**2. Zero Trust Security & Modern Authentication**
- SASE architecture simulation
- OAuth 2.0 Device Flow integration
- PAM (Pluggable Authentication Modules)
- Keycloak identity management
- Active Directory federation
- Vendor-agnostic security frameworks

**3. Infrastructure Automation**
- Docker containerization
- Kubernetes orchestration
- Terraform (Infrastructure-as-Code)
- Packer VM automation
- QEMU/KVM virtualization
- Windows Server automation (PowerShell)

**4. Data & Knowledge Management**
- Graph databases (Neo4j)
- Vector databases (FAISS, ChromaDB, Qdrant)
- Document processing (multiple formats)
- Git-backed data storage
- Policy-as-code implementations

**5. IoT & Environmental Monitoring**
- Raspberry Pi deployment
- Solar power integration
- Camera and sensor systems
- GNSS/RTK surveying
- Remote data transmission

### Development Patterns

**Consistent Approaches:**
- Docker-first development
- Comprehensive documentation (when mature)
- Multi-stage deployment options (dev, production, cloud)
- Open-source licensing (Apache-2.0, MIT, GPL-3.0)
- Infrastructure-as-code practices
- Testing frameworks (unit, integration, regression)
- Monitoring and observability (Prometheus, Grafana, ELK)

**Project Lifecycle:**
- Many early-stage experimental projects (1-5 commits)
- Several production-ready applications with comprehensive features
- Clear progression from experimentation to production
- Willingness to document limitations and next steps

**Technology Preferences:**
- **Languages:** Python (dominant), JavaScript/React, Shell scripting, PowerShell
- **Frameworks:** FastAPI, Django, Streamlit, React
- **Databases:** Neo4j, PostgreSQL, Redis, vector stores
- **Deployment:** Docker, Kubernetes, Render platform
- **AI/ML:** HuggingFace, OpenAI, Anthropic, local LLMs

### Domain Expertise

**1. Humanitarian Technology**
- ReliefWeb integration
- Disaster response data analysis
- GLIDE number systems
- Quantitative humanitarian metrics
- IFRC platform migration

**2. Cybersecurity**
- Zero Trust architecture
- SASE components
- Identity federation
- OAuth/OIDC protocols
- Network segmentation
- Policy enforcement

**3. Education & Research**
- University of Wisconsin affiliation
- OpenID for Research and Education (PORE WG)
- Educational lab environments
- Documentation for learning purposes

**4. Environmental Science**
- River observation systems
- Field station deployment
- Environmental sensor integration
- Geospatial data (implied)

---

## Contribution Activity

**Repository Statistics:**
- Total Stars Earned: 8
- Most Starred: wei_keycloak (1 star)
- Followers: 1
- Following: 11

**Activity Patterns:**
- Very recent activity (November 2025)
- Consistent project updates throughout 2024-2025
- Mix of long-term maintained projects and quick experiments
- Solo development on most projects (some show 2 contributors)

**Contribution to Other Repositories:**
- Limited data available from profile page
- One forked repository (game-of-life) suggests engagement with community projects

---

## Project Maturity Breakdown

**Production-Ready (Comprehensive documentation, deployment options, testing):**
- cooking_mcp
- openwebui
- graphrag
- graph (Phase 1 complete)
- ztlab
- hybrid-auth-lab

**Active Development (Functional with ongoing improvements):**
- openrivercam
- policydoodle
- ad-dc-vagrant
- zt-info-model

**Experimental/Learning (1-8 commits, limited documentation):**
- reliefweb_nlp
- topic_explorer_ml
- humbert_test
- rag_example
- utf-8
- promptflow
- wei-lab
- fabric_patterns

**Utility/Operational (Specific purpose, limited scope):**
- deployment_stuff
- rcselect_redir
- porewg
- essential_docker

**Placeholder/Empty:**
- geo_stuff
- writing

---

## Key Insights for Writing Style Documentation

### Technical Breadth
Tom demonstrates unusually broad technical range, comfortably working across:
- Backend (Python, FastAPI, Django) and frontend (React)
- Infrastructure (Docker, Kubernetes, Terraform)
- Windows (PowerShell, AD) and Linux (PAM, SSH)
- Databases (relational, graph, vector)
- AI/ML frameworks and protocols
- Hardware/IoT systems

### Problem-Solving Approach
Projects show pattern of:
1. Identifying practical problems (policy search, disaster response, authentication)
2. Experimenting with solutions (multiple notebooks, testing frameworks)
3. Building production implementations (comprehensive features, deployment)
4. Documenting for others (architecture diagrams, quick-start guides)

### Humanitarian Focus
Significant thread of applying technology to humanitarian challenges:
- Relief data analysis
- Disaster response summaries
- Environmental monitoring
- IFRC platform work

### Security Mindset
Deep understanding of modern security principles:
- Zero Trust architecture
- Defense in depth (multiple security layers in ztlab)
- Modern authentication protocols
- Vendor-neutral frameworks

### Practical Educator
Multiple projects serve educational purposes:
- Lab environments for teaching concepts
- Working group documentation
- Clear architecture diagrams
- Deployment checklists

### Engineering Maturity
Production projects show enterprise-grade practices:
- Comprehensive testing strategies
- High-availability deployment
- Monitoring and observability
- Configuration management
- Multi-environment support

---

## Significant/Interesting Projects (Highlighted)

**Most Technically Sophisticated:**
1. **graphrag** - Full-stack AI application with graph databases, multi-LLM support, comprehensive testing
2. **openwebui** - Production AI platform with GraphRAG, MCP, Kubernetes deployment
3. **graph** - Multi-model knowledge extraction with benchmarking framework

**Most Unique/Novel:**
1. **cooking_mcp** - Novel application of MCP protocol to cooking experiments with multi-channel feedback
2. **hybrid-auth-lab** - Modern OAuth integration with traditional Linux authentication
3. **openrivercam** - IoT river monitoring with solar power and IR capabilities

**Most Educational Value:**
1. **ztlab** - Complete SASE architecture simulation for learning
2. **zt-info-model** - Vendor-agnostic Zero Trust framework
3. **ad-dc-vagrant** - Automated Windows AD for testing

**Most Humanitarian Impact:**
1. **reliefweb_nlp** - Disaster response data analysis
2. **topic_explorer_ml** - Humanitarian summarization and extraction
3. **rcselect_redir** - IFRC platform migration utility

**Most Production-Ready:**
1. **cooking_mcp** - Enterprise security, multi-platform deployment
2. **openwebui** - High-availability Kubernetes deployment with comprehensive monitoring
3. **policydoodle** - Terraform infrastructure with multiple deployment options

---

## Technologies & Tools Inventory

**Programming Languages:**
- Python (primary)
- JavaScript/TypeScript
- Shell scripting
- PowerShell
- Ruby
- HCL (Terraform)
- PlantUML

**Frameworks & Libraries:**
- **Backend:** FastAPI, Django, Flask
- **Frontend:** React, Streamlit
- **AI/ML:** HuggingFace Transformers, PyTorch, spaCy
- **Testing:** Unit, integration, regression frameworks

**Infrastructure & Deployment:**
- Docker, Docker Compose
- Kubernetes, Helm
- Terraform
- Packer
- QEMU/KVM
- Vagrant

**Databases & Storage:**
- **Graph:** Neo4j
- **Vector:** FAISS, ChromaDB, Qdrant
- **Relational:** PostgreSQL
- **Cache:** Redis
- **Search:** Elasticsearch
- **Storage:** Git-backed data

**AI/ML Platforms:**
- OpenAI GPT models
- Anthropic Claude
- Ollama (local LLMs)
- LightLLM
- HuggingFace Hub
- Microsoft Promptflow

**Security & Identity:**
- Keycloak
- Zitadel
- OAuth 2.0 / OIDC
- Linux PAM
- Active Directory
- OpenZiti

**Monitoring & Observability:**
- Prometheus
- Grafana
- ELK Stack (Elasticsearch, Logstash, Kibana)

**Networking & Security:**
- OPNsense
- Cloud Custodian
- SDN concepts
- Microsegmentation

**Cloud Platforms:**
- Render
- AWS (Bedrock mentioned)

**Hardware/IoT:**
- Raspberry Pi 5
- Solar power systems
- Camera systems (IR capable)
- GNSS/RTK surveying equipment

**Protocols & Standards:**
- Model Context Protocol (MCP)
- OAuth 2.0 Device Flow
- OpenID Connect
- LDAP
- GLIDE (disaster identification)

---

## Recommendations for Writing Style Documentation

This GitHub portfolio should inform Tom's writing style documentation in several ways:

### 1. Technical Communication Style
Tom likely writes with:
- **Clarity over jargon** - READMEs are accessible while technically accurate
- **Practical focus** - Documentation emphasizes "what it does" and "how to use"
- **Honest assessment** - Explicitly notes limitations and future work
- **Architecture-first thinking** - Often includes diagrams and system overviews

### 2. Problem-Solving Narrative
Writing likely follows pattern:
1. Identify concrete problem
2. Explore potential solutions (often multiple approaches)
3. Build practical implementation
4. Document for reproducibility
5. Acknowledge limitations and next steps

### 3. Audience Awareness
Projects show adaptation to different audiences:
- **Educators** (ztlab, zt-info-model)
- **Developers** (production apps with comprehensive docs)
- **Field workers** (deployment checklists)
- **Standards bodies** (PORE WG diagrams)

### 4. Domain Integration
Writing likely integrates:
- Technical precision from engineering background
- Humanitarian awareness from relief sector work
- Security mindset from Zero Trust expertise
- Systems thinking from architecture projects

### 5. Documentation Patterns
When mature projects include:
- Quick-start guides
- Architecture overviews
- Deployment options (multiple environments)
- Troubleshooting sections
- Explicit requirements
- Next steps/roadmaps

### 6. Learning Journey Transparency
Multiple experimental projects suggest comfort with:
- Documenting work-in-progress
- Sharing learning process
- Publishing incomplete explorations
- Building on others' work (proper attribution)

---

## Summary

Tom Jordan's GitHub profile reveals an engineer with exceptional technical breadth, spanning AI/ML, cybersecurity, infrastructure automation, and humanitarian technology. His work demonstrates:

- **Production capability:** Several enterprise-ready applications with comprehensive testing and deployment
- **Educational commitment:** Multiple lab environments and documentation projects for teaching complex concepts
- **Humanitarian focus:** Consistent thread of applying technology to disaster response and relief work
- **Security expertise:** Deep understanding of Zero Trust, modern authentication, and defense-in-depth
- **Full-stack competency:** Comfortable across backend, frontend, infrastructure, databases, and hardware
- **Practical problem-solving:** Projects address real-world challenges with working implementations
- **Learning mindset:** Willingness to experiment, document findings, and iterate

The portfolio shows progression from experimentation to production-ready systems, with honest documentation of both successes and limitations. This technical foundation should inform writing style analysis, particularly around clarity, practical focus, systems thinking, and integration of domain expertise.
