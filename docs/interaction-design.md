# Interaction Design: Marketing Website

**Status:** Draft
**Created:** 2026-01-23
**Feature:** Homepage, LeanOS, Services conversion optimization

---

## User Journey

### Journey 1: Technical Founder → LeanOS Pro Purchase

**Persona:** Technical founder who can build but needs AI leverage/systems

| Stage | Trigger | Actions | Emotions | Pain Points | Opportunities |
|-------|---------|---------|----------|-------------|---------------|
| Aware | Google/LinkedIn/referral | Lands on homepage, scans hero | Curious, skeptical | "What is this?" | Hook with outcome, not product name |
| Consider | Clicks "Explore LeanOS" | Reads problem/solution, scrolls to pricing | Interested, evaluating | "181 skills means nothing to me" | Show concrete skill examples |
| Evaluate | Views pricing section | Compares Core vs Pro, checks GitHub | Calculating value | "Is this worth $500?" | Anchor against $200+/month alternatives |
| Act | Clicks "Get Pro" | Goes to Gumroad checkout | Ready to buy | Friction if Gumroad broken | Smooth checkout, money-back guarantee visible |
| Complete | Purchases | Gets repo access, starts using | Excited, maybe overwhelmed | "Where do I start?" | Onboarding email sequence |

### Journey 2: Non-Technical Founder → Services Inquiry

**Persona:** Non-technical founder with product idea, needs execution help

| Stage | Trigger | Actions | Emotions | Pain Points | Opportunities |
|-------|---------|---------|----------|-------------|---------------|
| Aware | Google/LinkedIn/referral | Lands on homepage, reads "Two Paths" | Curious, uncertain | "Am I technical or not?" | Clearer segmentation in copy |
| Consider | Clicks "View Services" | Reads problem framing, checks credibility | Hopeful, evaluating | "Is this person legit?" | Add social proof, case studies |
| Evaluate | Scrolls to pricing | Assesses $5k+ investment | Nervous about cost | "What exactly do I get?" | Add scope examples, timeline clarity |
| Act | Clicks LinkedIn DM | Opens LinkedIn, sends DM | Committed but friction | External redirect breaks flow | Add Calendly or direct form |
| Complete | Gets response | Schedules call | Relieved | Response time uncertainty | Auto-response with expectations |

### Key Moments

- **Aha Moment (LeanOS):** When visitor sees a concrete skill example and thinks "I could use that right now"
- **Aha Moment (Services):** When visitor reads "Built LeanOS in 2 months" and sees proof of execution capability
- **Friction Points:**
  - Homepage hero leads with name, not value
  - "181 skills" is abstract without examples
  - LinkedIn DM is high friction for services inquiry
  - No email capture for non-ready buyers
- **Delight Opportunities:**
  - Dark/light mode toggle shows technical attention to detail
  - Monospace aesthetic signals "built by a builder"
  - Price anchoring ($500 vs $200+/month) reframes value

---

## Task Flows

### Flow 1: Homepage → LeanOS Purchase

**Entry:** Direct URL, Google search, LinkedIn link
**Exit:** Gumroad checkout → purchase confirmation
**Preconditions:** None (cold visitor)

```
┌─────────────┐     ┌─────────────┐     ┌─────────────┐
│  Homepage   │────→│  LeanOS     │────→│  Pricing    │
│  Hero       │     │  Page       │     │  Section    │
└─────────────┘     └─────────────┘     └─────────────┘
      │                   │                   │
      │ [skip]            │ [not ready]       │ [buy]
      ▼                   ▼                   ▼
┌─────────────┐     ┌─────────────┐     ┌─────────────┐
│  Two Paths  │     │  GitHub     │     │  Gumroad    │
│  Section    │     │  (Core)     │     │  Checkout   │
└─────────────┘     └─────────────┘     └─────────────┘
```

#### Happy Path
1. Visitor lands on homepage → sees value-focused hero
2. Clicks "Get LeanOS Pro" or scrolls to Two Paths → clicks LeanOS card
3. Reads problem/solution on LeanOS page → scrolls to pricing
4. Clicks "Get Pro" → completes Gumroad checkout
5. Receives repo access email → starts using

#### Error Paths
| Error | Trigger | Recovery |
|-------|---------|----------|
| Gumroad link broken | URL placeholder not replaced | Show fallback contact method |
| Visitor not ready | Needs more info | Email capture, GitHub Core as entry point |
| Price objection | $500 feels high | Emphasize lifetime ownership vs monthly drain |

#### States
| State | Entry Condition | Display |
|-------|-----------------|---------|
| Default | Page load | Full content, CTAs active |
| Scrolled | User scrolls 50%+ | Sticky nav appears with CTA |
| Mobile | Viewport < 768px | Collapsed nav, stacked layout |

---

### Flow 2: Homepage → Services Inquiry

**Entry:** Direct URL, Google search, referral
**Exit:** LinkedIn DM sent OR Calendly booked
**Preconditions:** None (cold visitor)

```
┌─────────────┐     ┌─────────────┐     ┌─────────────┐
│  Homepage   │────→│  Services   │────→│  Contact    │
│  Hero       │     │  Page       │     │  Section    │
└─────────────┘     └─────────────┘     └─────────────┘
      │                   │                   │
      │ [explore]         │ [compare]         │ [DM/book]
      ▼                   ▼                   ▼
┌─────────────┐     ┌─────────────┐     ┌─────────────┐
│  Two Paths  │     │  LeanOS     │     │  LinkedIn/  │
│  (Services) │     │  Cross-link │     │  Calendly   │
└─────────────┘     └─────────────┘     └─────────────┘
```

#### Happy Path
1. Visitor lands on homepage → identifies as non-technical founder
2. Clicks "View Services" from Two Paths section
3. Reads value props, scrolls to pricing context
4. Clicks contact CTA → books call or sends DM
5. Gets response within 24h → schedules discovery call

#### Error Paths
| Error | Trigger | Recovery |
|-------|---------|----------|
| LinkedIn redirect | External site friction | Add Calendly as primary option |
| Price uncertainty | "$5k+" feels vague | Add scope examples with price ranges |
| Trust gap | Not enough social proof | Add testimonials, case study snippets |

---

## Wireframes

### Screen: Homepage (Redesigned)

**Purpose:** Route visitors to correct path, communicate core value
**Entry:** Direct URL, search, referral
**Exit:** LeanOS page OR Services page

**Design Principle:** Use chips for stats to reduce visual load

```
┌─────────────────────────────────────────────────────┐
│  [Logo]                    [Nav] [Nav] [Get Pro]    │
├─────────────────────────────────────────────────────┤
│                                                     │
│         
  One System. Full Context.
  AI OPERATING SYSTEM FOR FOUNDERS                    │
│ Product. Engineering. Sales. Marketing. 
  Customer Success. All connected.                  │
│                                                     │
│   ┌────────────┐ ┌────────────┐ ┌────────────┐     │
│   │ 181 skills │ │ 30+ agents │ │ $500 once  │     │
│   └────────────┘ └────────────┘ └────────────┘     │
│                                                     │
│   [Get LeanOS Pro]  [Try Core Free]                 │
│                                                     │
│     Know Your Agent. Own Your Agent.                │
│                                                     │
│                                                     │
├─────────────────────────────────────────────────────┤
│                                                     │
│                    TWO PATHS                        │
│                                                     │
│   ┌─────────────────┐   ┌─────────────────┐        │
│   │ TECHNICAL       │   │ NON-TECHNICAL   │        │
│   │ FOUNDERS    ★   │   │ FOUNDERS        │        │
│   │                 │   │                 │        │
│   │ LeanOS Pro      │   │ Fractional CTO  │        │
│   │ AI you own      │   │ Done for you    │        │
│   │ $500 once       │   │ From $5k        │        │
│   │                 │   │                 │        │
│   │ [Get LeanOS]    │   │ [Learn More]    │        │
│   └─────────────────┘   └─────────────────┘        │
│                                                     │
├─────────────────────────────────────────────────────┤
│                                                     │
│                  RECENT WRITING                     │
│   (3 posts or "Building in public. Coming soon.")   │
│                                                     │
├─────────────────────────────────────────────────────┤
│                                                     │
│      [GitHub]  [LinkedIn]  [X]                      │
│                                                     │
│             © 2026 Bella Belgarokova                │
│                                                     │
└─────────────────────────────────────────────────────┘
```

#### Stat Chips
| Chip | Value | Purpose |
|------|-------|---------|
| Skills | 181 skills | Scope of capabilities |
| Agents | 30+ agents | Orchestration power |
| Price | $500 once | Value anchor |

#### Components Used
| Component | Purpose | State |
|-----------|---------|-------|
| Nav | Navigation + primary CTA | Default, mobile hamburger |
| Hero | Value proposition, stat chips, CTAs | Default |
| Stat Chips | Scannable key metrics | Default, hover tooltip |
| Two Paths Grid | Route by persona (LeanOS primary) | Default, hover highlight |
| Featured List | Recent writing | Default, empty state |
| Footer | Social links, copyright | Default |

#### Key Changes from Current
1. Hero leads with **"One System. Full Context."** value proposition
2. Stats moved to **chips** (181 skills, 30+ agents, $500 once) for scannability
3. "Know Your Agent" moved below CTAs as secondary message
4. Personal branding subtle at bottom
5. Two Paths shows LeanOS as **primary** (★ indicator)
6. Services CTA softened to "Learn More" (passive positioning)

---

### Screen: LeanOS Page (Redesigned)

**Purpose:** Convert technical founders to Pro purchase
**Entry:** Homepage CTA, direct URL, nav link
**Exit:** Gumroad checkout OR GitHub (Core)

**Design Principle:** Chips for stats, Five Functions for clarity

```
┌─────────────────────────────────────────────────────┐
│  [Logo]                    [Nav] [Nav] [Get Pro]    │
├─────────────────────────────────────────────────────┤
│                                                     │
│         AI OPERATING SYSTEM FOR FOUNDERS            │
│                                                     │
│     Know Your Agent. Own Your Agent.                │
│                                                     │
│   ┌────────────┐ ┌────────────┐ ┌────────────┐     │
│   │ 181 skills │ │ 30+ agents │ │ Full context│     │
│   └────────────┘ └────────────┘ └────────────┘     │
│                                                     │
│   Every prompt visible. Every skill modifiable.     │
│   $500 once — not $3,450/month in SaaS tools.       │
│                                                     │
│       [Get Pro]  [Try Core Free]                    │
│                                                     │
├─────────────────────────────────────────────────────┤
│                                                     │
│                 WHAT IS LEANOS?                     │
│                                                     │
│   One AI system for your entire business.           │
│   Claude sees everything. Context never lost.       │
│                                                     │
│   ┌─────────────────────────────────────────────┐  │
│   │  STRATEGIZE → CREATE → GROW → RETAIN → OPERATE │
│   │                    ↑_______|________|          │
│   │                      INTELLIGENCE              │
│   └─────────────────────────────────────────────┘  │
│                                                     │
├─────────────────────────────────────────────────────┤
│                                                     │
│                  THE PROBLEM                        │
│                                                     │
│   10+ tools. $3,450/month. Context lost between.    │
│   AI starts from scratch every time.                │
│   Your tools don't talk to each other.              │
│                                                     │
├─────────────────────────────────────────────────────┤
│                                                     │
│               EXAMPLE SKILLS                        │
│                                                     │
│   ┌──────────────┐ ┌──────────────┐ ┌──────────────┐│
│   │ SALES        │ │ ENGINEERING  │ │ MARKETING    ││
│   │              │ │              │ │              ││
│   │ outreach-    │ │ python-      │ │ content-     ││
│   │ personalizing│ │ codegen      │ │ repurposing  ││
│   │              │ │              │ │              ││
│   │ LinkedIn →   │ │ Spec →       │ │ 1 blog →     ││
│   │ personalized │ │ production   │ │ 5 LinkedIn,  ││
│   │ message      │ │ FastAPI      │ │ 10 tweets    ││
│   └──────────────┘ └──────────────┘ └──────────────┘│
│                                                     │
├─────────────────────────────────────────────────────┤
│                                                     │
│                WHAT'S INCLUDED                      │
│                                                     │
│   ┌─────────────────┐   ┌─────────────────┐        │
│   │ CORE (FREE)     │   │ PRO ($500)  ★   │        │
│   │                 │   │                 │        │
│   │ 15 skills       │   │ 181 skills      │        │
│   │ 2 agents        │   │ 30+ agents      │        │
│   │ Reasoning +     │   │ Full business   │        │
│   │ foundations     │   │ operations      │        │
│   │                 │   │                 │        │
│   │ [GitHub]        │   │ [Get Pro]       │        │
│   └─────────────────┘   └─────────────────┘        │
│                                                     │
├─────────────────────────────────────────────────────┤
│                                                     │
│                   PRICING                           │
│                                                     │
│              ┌─────────────────┐                    │
│              │                 │                    │
│              │  LEANOS PRO     │                    │
│              │                 │                    │
│              │    $500         │                    │
│              │     once        │                    │
│              │                 │                    │
│              │ Not $3,450/mo   │                    │
│              │ in SaaS tools   │                    │
│              │                 │                    │
│              │ Yours forever.  │                    │
│              │ 30-day refund.  │                    │
│              │                 │                    │
│              │ [Get Pro]       │                    │
│              │                 │                    │
│              │ Running 2       │                    │
│              │ businesses on   │                    │
│              │ LeanOS daily.   │                    │
│              └─────────────────┘                    │
│                                                     │
├─────────────────────────────────────────────────────┤
│                                                     │
│                  FOR WHOM                           │
│                                                     │
│   • Solo founders needing team capabilities         │
│   • Technical operators thinking in systems         │
│   • Claude users wanting reusable skills            │
│                                                     │
├─────────────────────────────────────────────────────┤
│                                                     │
│               NOT READY YET?                        │
│                                                     │
│   Join the build-in-public list.                    │
│   [Email input] [Subscribe]                         │
│                                                     │
├─────────────────────────────────────────────────────┤
│                                                     │
│              START BUILDING                         │
│                                                     │
│   Core is free. Pro is yours forever.               │
│   [Try Core Free]  [Get Pro]                        │
│                                                     │
├─────────────────────────────────────────────────────┤
│                                                     │
│   Non-technical? See services for implementation.   │
│                                                     │
└─────────────────────────────────────────────────────┘
```

#### Key Changes from Current
1. Added **"What is LeanOS?"** section immediately after hero
2. Added **"Example Skills"** section with concrete, tangible examples
3. Consolidated sections (removed redundant "Know Your Agent" separate section)
4. Added **email capture** for non-ready buyers
5. Improved social proof: "Built to ship 2 products in 60 days"
6. Reduced scroll fatigue by merging related sections

---

### Screen: Services Page (Redesigned)

**Purpose:** Convert non-technical founders to services inquiry
**Entry:** Homepage "View Services", nav link
**Exit:** Calendly booking OR LinkedIn DM

```
┌─────────────────────────────────────────────────────┐
│  [Logo]                    [Nav] [Nav] [Get Pro]    │
├─────────────────────────────────────────────────────┤
│                                                     │
│                FRACTIONAL CTO                       │
│                                                     │
│   Technical Strategy for Non-Technical Founders     │
│                                                     │
│   CTO-level decisions + AI-powered execution.       │
│   Projects from $5k. Not $150k/year salary.         │
│                                                     │
│   [Book a 15-min Call]  [Or explore LeanOS]         │
│                                                     │
├─────────────────────────────────────────────────────┤
│                                                     │
│               THE COST OF WAITING                   │
│                                                     │
│   Every month without technical leadership =        │
│   features shipped wrong, debt compounding,         │
│   competitors gaining ground.                       │
│                                                     │
├─────────────────────────────────────────────────────┤
│                                                     │
│                 WHAT YOU GET                        │
│                                                     │
│   ┌──────────────┐ ┌──────────────┐ ┌──────────────┐│
│   │ Technical    │ │ AI-Powered   │ │ Built for    ││
│   │ Strategy     │ │ Execution    │ │ Independence ││
│   │              │ │              │ │              ││
│   │ Architecture,│ │ Faster than  │ │ No lock-in.  ││
│   │ stack, road- │ │ agencies.    │ │ Everything   ││
│   │ map planning │ │ AI workflows │ │ transferable ││
│   └──────────────┘ └──────────────┘ └──────────────┘│
│                                                     │
├─────────────────────────────────────────────────────┤
│                                                     │
│                PROJECT EXAMPLES                     │
│                                                     │
│   ┌──────────────┐ ┌──────────────┐ ┌──────────────┐│
│   │ MVP Build    │ │ Tech Audit   │ │ AI Strategy  ││
│   │ $8-15k       │ │ $5k          │ │ $5-10k       ││
│   │              │ │              │ │              ││
│   │ 6-8 weeks    │ │ 2 weeks      │ │ 4 weeks      ││
│   │ Full product │ │ Architecture │ │ AI roadmap + ││
│   │ launch-ready │ │ review +     │ │ implementa-  ││
│   │              │ │ action plan  │ │ tion plan    ││
│   └──────────────┘ └──────────────┘ └──────────────┘│
│                                                     │
├─────────────────────────────────────────────────────┤
│                                                     │
│                   ABOUT ME                          │
│                                                     │
│   [Photo]  Built LeanOS Pro in 2 months.            │
│            181 skills, 30+ agents.                  │
│                                                     │
│            Self-taught engineer. UK background.     │
│            Dubai-based. AdTech, FinTech, HealthTech.│
│                                                     │
│            I think in systems. I build with         │
│            precision. I care about leverage.        │
│                                                     │
├─────────────────────────────────────────────────────┤
│                                                     │
│                  LET'S TALK                         │
│                                                     │
│   Book a 15-minute discovery call.                  │
│   No pitch. Just questions to see if we're a fit.   │
│                                                     │
│   [Book Call on Calendly]                           │
│                                                     │
│   Prefer async? DM "CTO" on LinkedIn.               │
│                                                     │
├─────────────────────────────────────────────────────┤
│                                                     │
│   Technical founder? LeanOS might be what you need. │
│                                                     │
└─────────────────────────────────────────────────────┘
```

#### Key Changes from Current
1. Primary CTA changed from LinkedIn DM to **Calendly booking**
2. Added **"Project Examples"** section with scope/price clarity
3. Enhanced About section with **photo and proof of work**
4. LinkedIn DM offered as **secondary async option**
5. Clearer investment framing with concrete project types

---

## Component Specifications

### Component: Stat Chip

**Type:** Atom
**Purpose:** Display key metrics in scannable, compact format to reduce visual load

#### Anatomy
```
┌─────────────────┐
│  181 skills     │
└─────────────────┘
```

#### Props
| Prop | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| value | string | Yes | — | The stat value (e.g., "181") |
| label | string | Yes | — | The stat label (e.g., "skills") |
| variant | string | No | "default" | Visual variant (default, accent, muted) |

#### States
| State | Visual Change | Trigger |
|-------|---------------|---------|
| Default | Subtle border, monospace text | Initial |
| Hover | Slight background highlight | Mouse hover |
| Focus | Focus ring | Keyboard navigation |

#### CSS Implementation
```css
.stat-chip {
  display: inline-flex;
  align-items: center;
  gap: var(--space-1);
  padding: var(--space-2) var(--space-3);
  border: 1px solid var(--color-border-secondary);
  border-radius: var(--radius-sm);
  font-family: var(--font-mono);
  font-size: var(--font-size-sm);
  color: var(--color-text-secondary);
  background: var(--color-bg-secondary);
}

.stat-chip:hover {
  background: var(--color-bg-tertiary);
  border-color: var(--color-border-primary);
}

.stat-chip-value {
  font-weight: var(--font-weight-semibold);
  color: var(--color-text-primary);
}
```

#### HTML Structure
```html
<div class="stat-chips">
  <span class="stat-chip">
    <span class="stat-chip-value">181</span> skills
  </span>
  <span class="stat-chip">
    <span class="stat-chip-value">30+</span> agents
  </span>
  <span class="stat-chip">
    <span class="stat-chip-value">$500</span> once
  </span>
</div>
```

#### Responsive Behavior
| Breakpoint | Layout |
|------------|--------|
| Desktop (>768px) | Horizontal row, centered |
| Mobile (<768px) | Wrap to 2 rows if needed |

---

### Component: Nav CTA Button

**Type:** Atom
**Purpose:** Persistent conversion path in navigation

#### Anatomy
```
┌─────────────────────┐
│    [Get Pro]        │
└─────────────────────┘
```

#### Props
| Prop | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| label | string | Yes | "Get Pro" | Button text |
| href | string | Yes | "#pricing" | Target URL |
| variant | string | No | "primary" | Button style |

#### States
| State | Visual Change | Trigger |
|-------|---------------|---------|
| Default | Primary color, white text | Initial |
| Hover | Darker background | Mouse hover |
| Active | Pressed state | Click |
| Mobile | Hidden in hamburger | Viewport < 768px |

#### CSS Addition (main.css)
```css
.btn-nav {
  padding: var(--space-2) var(--space-4);
  font-size: var(--font-size-xs);
  margin-left: var(--space-4);
}
```

---

### Component: Skill Example Card

**Type:** Molecule
**Purpose:** Make abstract skill counts tangible with concrete examples

#### Anatomy
```
┌─────────────────────────┐
│ [CATEGORY LABEL]        │
│                         │
│ Skill Name              │
│                         │
│ Description of what     │
│ this skill does in      │
│ concrete terms.         │
│                         │
└─────────────────────────┘
```

#### Props
| Prop | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| category | string | Yes | — | Category label (Sales, Engineering, etc.) |
| name | string | Yes | — | Skill name |
| description | string | Yes | — | What the skill does |

#### States
| State | Visual Change | Trigger |
|-------|---------------|---------|
| Default | Card with subtle border | Initial |
| Hover | Slight lift, border highlight | Mouse hover |

#### HTML Structure
```html
<div class="skill-card">
  <span class="card-label">{category}</span>
  <h3>{name}</h3>
  <p>{description}</p>
</div>
```

---

### Component: Email Capture

**Type:** Molecule
**Purpose:** Capture leads from non-ready buyers

#### Anatomy
```
┌─────────────────────────────────────┐
│                                     │
│  Not Ready Yet?                     │
│                                     │
│  Join the build-in-public list.     │
│                                     │
│  ┌─────────────────┐ ┌──────────┐  │
│  │ Email           │ │Subscribe │  │
│  └─────────────────┘ └──────────┘  │
│                                     │
└─────────────────────────────────────┘
```

#### Props
| Prop | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| heading | string | No | "Not Ready Yet?" | Section heading |
| description | string | No | "Join the build-in-public list." | Description text |
| buttonText | string | No | "Subscribe" | Submit button text |
| formAction | string | Yes | — | Form endpoint URL |

#### States
| State | Visual Change | Trigger |
|-------|---------------|---------|
| Default | Input + button visible | Initial |
| Loading | Button shows spinner | Form submitted |
| Success | "Thanks! Check your email." | Submission success |
| Error | Error message below input | Submission failed |

---

### Component: Project Example Card

**Type:** Molecule
**Purpose:** Clarify service scope and pricing for non-technical founders

#### Anatomy
```
┌─────────────────────────┐
│                         │
│ Project Type            │
│ $X,XXX                  │
│                         │
│ X weeks                 │
│                         │
│ Description of what's   │
│ included in this        │
│ project type.           │
│                         │
└─────────────────────────┘
```

#### Props
| Prop | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| title | string | Yes | — | Project type name |
| price | string | Yes | — | Price or range |
| timeline | string | Yes | — | Duration estimate |
| description | string | Yes | — | What's included |

---

## Design Tokens (New)

| Token | Value | Usage |
|-------|-------|-------|
| --color-accent-highlight | var(--color-text-accent) | Emphasized words in headlines |
| --space-card-internal | var(--space-4) | Internal padding for new card types |
| --radius-skill-card | var(--radius-md) | Skill example cards |

---

## Open Questions

- [ ] Email capture service? (Buttondown, ConvertKit, Gumroad follow) — Owner: Bella
- [ ] Calendly vs other booking tool for Services? — Owner: Bella
- [ ] Case studies/testimonials available for Services page? — Owner: Bella

---

## Implementation Priority

### Phase 1: Critical Fixes (This Week)
1. **Homepage hero rewrite** - Lead with "Unified Context" value prop, not personal brand
2. **Correct agent count** - Update "30+" to "44" everywhere
3. **Add nav CTA button** - Persistent "Get Pro" in navigation
4. Fix Gumroad URL placeholder (when ready)

### Phase 2: High Impact (Next 2 Weeks)
5. **Add "What is LeanOS?" section** with Five Functions framework
6. **Add "Example Skills" section** with 3 concrete examples
7. **Add email capture** for non-ready buyers
8. **Update price anchor** from "$200+/month" to "$3,450/month"
9. **De-emphasize Services** (passive positioning per Canvas)

### Phase 3: Polish (Following 2 Weeks)
10. Add "Project Examples" section to Services
11. Improve social proof text
12. Mobile optimization refinements

---

## Canvas-Aligned Content Updates

### Corrected Stats
- **44 agents** (not 30+)
- **181 skills** (correct)
- **6 capability buckets**: Build, Sell, Serve, Plan, Grow, Think

### Primary Value Proposition (from Canvas 07-uvp)
"Run your entire business with one AI system. Product. Engineering. Sales. Marketing. Customer Success. All connected. Claude follows the context."

### Price Anchors (from Canvas)
- Current: "$200+/month in AI subscriptions"
- **Better: "$3,450/month fragmented SaaS stack → $500 once"**
- Alternative: "$300k+/year in specialists → $500 once"

### Messaging Hierarchy
1. **Primary: Unified Context** - "One system. Full context. Better AI results."
2. **Secondary: Know Your Agent** - "Every prompt readable. Every skill modifiable."
3. **Tertiary: Ownership** - "$500 once. Yours forever. No lock-in."

### Five Functions Framework
```
STRATEGIZE → CREATE → GROW → RETAIN → OPERATE
                 ↑__________|__________|
                       INTELLIGENCE
```
- **Build:** Code generation, design systems, product specs
- **Sell:** Outbound, inbound, campaigns, partnerships
- **Serve:** Onboarding, health, retention, expansion
- **Plan:** Market research, business model, GTM strategy
- **Grow:** Activation, conversion, viral mechanics
- **Think:** 6 reasoning modes, 11 structuring schemas

### Segment Priorities (from Canvas 04-segments)
| Segment | Priority | Revenue Stream |
|---------|----------|----------------|
| Technical Founders | **PRIMARY** | LeanOS Pro |
| AI Builders (Cursor users) | **PRIMARY** | LeanOS Pro |
| Non-Technical Founders | Secondary | Services (PASSIVE) |

### Services Positioning (from Canvas)
**Status:** Passive. Not actively marketed. Inbound from authority only.
- De-emphasize on homepage "Two Paths"
- Services page should feel premium/exclusive
- "Available for select clients" not "Book a call"

---

## Next Steps

1. Review this design with stakeholder (Bella)
2. Prioritize implementation phases
3. Create HTML/CSS changes following existing design system
