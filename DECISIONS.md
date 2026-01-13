# Strategic Decisions Log — bellabe.github.io & LeanOS

*Session: 2026-01-02*
*Status: FINALIZED*

---

## 1. UX/UI Critique: bellabe.github.io

### Context
- **User:** Potential clients, recruiters, technical peers
- **Goal:** Establish credibility, showcase work, generate advisory/consulting leads
- **Constraints:** Static Jekyll site on GitHub Pages

### Key Findings

| Severity | Issue | Recommendation |
|----------|-------|----------------|
| **Critical** | No photo — personal brand needs human element | Add professional photo to hero or about page |
| **Critical** | Contact CTA buried at page bottom in subtle gray | Make "Let's Talk" prominent in hero area |
| **Major** | Dual CTAs in hero ("View Projects" + "Read Writing") | Single CTA — pick one primary action |
| **Major** | Navigation too dense (6 items) | Move GitHub/LinkedIn to footer, keep 4 primary items |
| **Major** | LeanOS visually equal to other projects | Differentiate LeanOS as flagship (larger card, distinct styling) |
| **Minor** | Theme toggle mixed with nav links | Move to footer or floating corner |
| **Minor** | Empty state for Writing section | Remove until content exists |

### Summary Table

| Area | Assessment | Priority |
|------|------------|----------|
| Visual Hierarchy | ⚠️ Good but hero CTAs compete | Medium |
| Information Architecture | ✅ Clear, logical | - |
| Cognitive Load | ⚠️ Nav too dense, dual CTAs | Medium |
| Trust/Credibility | ❌ No photo, buried contact | Critical |
| Conversion Path | ❌ Contact CTA too subtle | Major |

### Recommended Actions
1. Add professional photo
2. Single hero CTA
3. Make contact prominent
4. Simplify nav (4 items max)
5. Differentiate LeanOS visually

---

## 2. LeanOS Placement Decision

### Decision: Dedicated `/leanos` Page on bellabe.github.io

**Rationale:**
- Current goal is consulting/advisory — LeanOS is proof of capability
- No maintenance overhead of second property
- All SEO authority compounds on one domain
- If LeanOS takes off, extraction to leanos.dev is trivial

**Revisit Trigger:** 5+ "how do I use LeanOS myself" inquiries per month

### Page Structure

```
/leanos
├── Hero
│   ├── Headline: "Run a business with AI infrastructure"
│   ├── Subhead: "63 skills. 12 agents. One operating system."
│   └── CTA: "Get Started Free" → GitHub
│
├── The Problem
│   └── Why headcount doesn't scale for founders/small teams
│
├── How It Works
│   ├── Visual: Skills architecture diagram
│   ├── Agents (orchestrators) → Skills (capabilities)
│   └── Goal-driven execution with 6-stage causal flow
│
├── What's Included
│   ├── Core (Free): 15 skills — reasoning, goal-setting, basic actions
│   └── Pro (Paid): 48 skills — sales, marketing, engineering, product
│
├── Proof
│   ├── "I run 2 businesses on this infrastructure"
│   ├── Chromly (FashionTech)
│   └── Detekta (RegTech)
│
├── Pricing
│   ├── Core: Free (MIT)
│   ├── Pro: $500 one-time OR $99/month
│   └── Implementation: $5K-$15K
│
├── For Whom
│   ├── Solo founders
│   ├── Small teams (2-5)
│   └── Operators who think in systems
│
└── CTA
    ├── Primary: "Get Core Free" → GitHub
    └── Secondary: "Get Pro" → Gumroad
```

---

## 3. LeanOS Product Strategy

### Decision: Open Core + Gumroad Delivery

**Model:** Two separate repos. Core is public (MIT). Pro is private, delivered via Gumroad.

### Repo Structure

#### `lean-os` (Public GitHub)

```
lean-os/
├── .claude/
│   ├── skills/
│   │   ├── reasoning-causal/
│   │   ├── reasoning-abductive/
│   │   ├── reasoning-inductive/
│   │   ├── reasoning-analogical/
│   │   ├── reasoning-dialectical/
│   │   ├── reasoning-counterfactual/
│   │   ├── action-descriptive/
│   │   ├── action-diagnostic/
│   │   ├── action-prescriptive/
│   │   ├── action-planning/
│   │   ├── action-decision/
│   │   ├── goal-setter/
│   │   ├── goal-tracker/
│   │   ├── foundations-market-intelligence/
│   │   └── foundations-problem-solution-fit/
│   └── agents/
│       ├── reasoning-gateway/
│       └── problem-solving-gateway/
├── docs/
│   ├── getting-started.md
│   ├── skills-reference.md
│   └── architecture.md
├── CLAUDE.md
├── README.md
└── LICENSE (MIT)
```

**Total Core:** 15 skills, 2 agents

#### `lean-os-pro` (Private GitHub)

**Pro is the FULL system — all 63 skills, all 12 agents.**

```
lean-os-pro/
├── .claude/
│   ├── skills/           (ALL 63 skills)
│   │   ├── reasoning-*/       (6)
│   │   ├── action-*/          (11)
│   │   ├── goal-*/            (2)
│   │   ├── foundations-*/     (10)
│   │   ├── sales-*/           (6)
│   │   ├── marketing-*/       (5)
│   │   ├── engineering-*/     (12)
│   │   ├── product-*/         (5)
│   │   ├── research-*/        (4)
│   │   ├── critique-ux-ui/
│   │   └── programming-python-excellence/
│   └── agents/           (ALL 12 agents)
│       ├── reasoning-gateway/
│       ├── problem-solving-gateway/
│       ├── sales-execution/
│       ├── marketing-execution/
│       ├── foundations-builder/
│       ├── product-manager/
│       ├── engineering-be-setup/
│       ├── engineering-fe/
│       ├── engineering-fe-shopify/
│       ├── engineering-testing/
│       ├── market-research/
│       └── knowledge-builder/
├── docs/
├── CLAUDE.md
├── INSTALL.md
└── README.md
```

**Total Pro:** 63 skills, 12 agents (complete system)

**Pro buyer just copies `.claude/` into their project — done.**

### Skills Split Summary

**Core = subset (free sample). Pro = superset (complete system).**

| Category | Core (Free) | Pro (Full) |
|----------|-------------|------------|
| **Reasoning** | 6 | 6 |
| **Action** | 5 | 11 |
| **Goal** | 2 | 2 |
| **Foundations** | 2 | 10 |
| **Sales** | — | 6 |
| **Marketing** | — | 5 |
| **Engineering** | — | 12 |
| **Product** | — | 5 |
| **Research** | — | 4 |
| **Critique** | — | 1 |
| **Programming** | — | 1 |
| **TOTAL** | **15 skills** | **63 skills** |

| Agents | Core | Pro |
|--------|------|-----|
| reasoning-gateway | ✓ | ✓ |
| problem-solving-gateway | ✓ | ✓ |
| sales-execution | | ✓ |
| marketing-execution | | ✓ |
| foundations-builder | | ✓ |
| product-manager | | ✓ |
| engineering-* (4) | | ✓ |
| market-research | | ✓ |
| knowledge-builder | | ✓ |
| **TOTAL** | **2 agents** | **12 agents** |

**Core skills included in public repo:**
- `reasoning-*` (6): causal, abductive, inductive, analogical, dialectical, counterfactual
- `action-*` (5): descriptive, diagnostic, prescriptive, planning, decision
- `goal-*` (2): setter, tracker
- `foundations-*` (2): market-intelligence, problem-solution-fit

### Pricing

| Tier | Price | Delivery |
|------|-------|----------|
| **Core** | Free | Public GitHub repo |
| **Pro** | $500 one-time | Gumroad → private repo invite |
| **Pro (subscription)** | $99/month | Gumroad → private repo invite |
| **Implementation** | $5K-$15K | Custom engagement |
| **Advisory retainer** | $2K-$5K/month | Ongoing support |

### User Journey

**Free path:**
```
1. Discover LeanOS (GitHub, blog, word of mouth)
         ↓
2. Clone lean-os (Core) — 15 skills, 2 agents
         ↓
3. Try reasoning, goal-setting, basic actions
         ↓
4. Hit limits: "I need sales/marketing/engineering skills"
         ↓
5. Upgrade to Pro
```

**Pro path:**
```
1. Purchase Pro on Gumroad ($500 or $99/mo)
         ↓
2. Get invite to lean-os-pro repo
         ↓
3. Copy .claude/ directory into project
         ↓
4. Done — all 63 skills, 12 agents ready
         ↓
5. (Optional) Book implementation help ($5K-$15K)
```

**Key:** Pro is the FULL system (superset). Pro buyers don't need Core.

### Gumroad Setup

**Product 1: LeanOS Pro (One-time)**
- Price: $500
- Delivery: Private GitHub repo invite (collect GitHub username at checkout)
- Includes: All 48 pro skills, 10 agents, updates for 1 year

**Product 2: LeanOS Pro (Subscription)**
- Price: $99/month
- Delivery: Private GitHub repo invite
- Includes: All pro skills + ongoing updates + priority support

**Fulfillment workflow:**
1. Buyer purchases on Gumroad
2. Gumroad webhook → collect GitHub username
3. Manual (initially) or automated invite to `lean-os-pro` repo
4. Buyer clones/pulls pro skills

---

## 4. Implementation Phases

### Phase 1: Restructure (Week 1-2)

| Task | Status |
|------|--------|
| Create `lean-os` public repo with core skills | Pending |
| Create `lean-os-pro` private repo with pro skills | Pending |
| Write Core README + getting-started docs | Pending |
| Write Pro INSTALL.md | Pending |
| Set up Gumroad products (one-time + subscription) | Pending |
| Create `/leanos` page on bellabe.github.io | Pending |
| Update current `BellaBe/lean-os` repo (archive or redirect) | Pending |

### Phase 2: Launch (Week 3-4)

| Task | Status |
|------|--------|
| Publish Core repo | Pending |
| Publish `/leanos` page | Pending |
| Gumroad products live | Pending |
| Announce on LinkedIn | Pending |
| Write launch blog post | Pending |

### Phase 3: Validate (Month 2-4)

| Signal | Action |
|--------|--------|
| Core stars/forks growing | Double down on content marketing |
| Pro purchases happening | Validate pricing, gather feedback |
| Implementation requests | Productize implementation packages |
| No signal | Revisit positioning, distribution channels |

### Phase 4: Scale (Month 5+)

| Signal | Action |
|--------|--------|
| Pro converts well | Consider hosted version (SaaS) |
| Implementation dominates | You're a consulting business — own it |
| Community forming | Consider Discord, office hours |

---

## 5. Next Actions (Prioritized)

**Workflow:** `lean-os` already exists with all 63 skills. Create Pro as copy, then strip Core down.

| # | Action | Details | Status |
|---|--------|---------|--------|
| 1 | Create `lean-os-pro` private repo | New private repo on GitHub | Pending |
| 2 | Copy `lean-os` → `lean-os-pro` | Full copy (all 63 skills, 12 agents) | Pending |
| 3 | Clean `lean-os` (public) | Remove 48 pro-only skills, keep 15 core | Pending |
| 4 | Update `lean-os` README | Core-focused docs, link to Pro upgrade | Pending |
| 5 | Add `lean-os-pro` INSTALL.md | Simple: "Copy .claude/ to your project" | Pending |
| 6 | Set up Gumroad products | One-time ($500) + subscription ($99/mo) | Pending |
| 7 | Create `/leanos` page | Product landing on bellabe.github.io | Pending |
| 8 | Apply UX fixes to site | Photo, nav, CTAs per critique | Pending |
| 9 | Test Pro delivery flow | Purchase → invite → access works | Pending |
| 10 | Announce launch | LinkedIn + blog post | Pending |

### What to REMOVE from `lean-os` (public)

Delete these from public repo (keep only in Pro):
```
.claude/skills/
├── action-evaluative/
├── action-procedural/
├── action-validation/
├── action-risk/
├── action-constrain/
├── action-alignment/
├── foundations-business-model/
├── foundations-validation/
├── foundations-go-to-market/
├── foundations-funding/
├── foundations-regulatory/
├── foundations-retention-optimizer/
├── foundations-icp-generator/
├── foundations-value-proposition/
├── sales-*/                    (all 6)
├── marketing-*/                (all 5)
├── engineering-*/              (all 12)
├── product-*/                  (all 5)
├── research-*/                 (all 4)
├── critique-ux-ui/
└── programming-python-excellence/

.claude/agents/
├── sales-execution/
├── marketing-execution/
├── foundations-builder/
├── product-manager/
├── engineering-be-setup/
├── engineering-fe/
├── engineering-fe-shopify/
├── engineering-testing/
├── market-research/
└── knowledge-builder/
```

### What STAYS in `lean-os` (public)

```
.claude/skills/
├── reasoning-*/                (6 skills)
├── action-descriptive/
├── action-diagnostic/
├── action-prescriptive/
├── action-planning/
├── action-decision/
├── goal-setter/
├── goal-tracker/
├── foundations-market-intelligence/
└── foundations-problem-solution-fit/

.claude/agents/
├── reasoning-gateway/
└── problem-solving-gateway/
```

---

## Decision Log

| Date | Decision | Rationale |
|------|----------|-----------|
| 2026-01-02 | Dedicated `/leanos` page (not separate site) | Consulting is primary goal; compound SEO |
| 2026-01-02 | Open Core model (not full close) | Distribution + monetization balance |
| 2026-01-02 | Two repos (not monorepo) | Clean separation, simple permissions |
| 2026-01-02 | Gumroad delivery (not GitHub Sponsors) | Better checkout UX for one-time purchases |
| 2026-01-02 | 15 skills Core / 48 skills Pro | Reasoning + goals free; revenue-generating skills paid |

---

*This document is the source of truth for LeanOS product strategy.*
