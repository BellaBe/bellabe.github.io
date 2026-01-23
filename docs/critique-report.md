# Critique Report: Marketing Website

**Date:** 2026-01-23
**Skills Applied:** critique-ux-ui, behavioral-science (AUDIT mode)

---

## Part 1: UX/UI Critique

### Context

- **User:** Technical founders, AI builders (Cursor/Replit users)
- **Goal:** Purchase LeanOS Pro ($500) or try Core (free)
- **Constraints:** Jekyll static site, monospace design system, dark/light mode

### First Impression (5-Second Test)

**Current homepage opening:**
```
Bella Belgarokova
Building LeanOS — AI Operating System for Founders
Know Your Agent. Own Your Agent.
```

**Problems:**
1. **Most prominent element is a name** — Should be value or outcome
2. **Purpose unclear without reading** — "AI Operating System" is abstract
3. **No emotional pull** — Describes what it IS, not what it DOES for me
4. **Competing taglines** — "Building LeanOS" AND "Know Your Agent" AND "AI Operating System"

**Proposed wireframe opening (from interaction-design.md):**
```
One System. Full Context.
AI OPERATING SYSTEM FOR FOUNDERS
Product. Engineering. Sales. Marketing. Customer Success. All connected.

┌────────────┐ ┌────────────┐ ┌────────────┐
│ 181 skills │ │ 30+ agents │ │ $500 once  │
└────────────┘ └────────────┘ └────────────┘
```

**Still has problems:**
1. **THREE headlines compete** — "One System", "AI Operating System", function list
2. **Chips add visual noise** — Stats without context aren't compelling
3. **No emotional resonance** — Still features, not transformation
4. **"Full context" is insider language** — Means nothing to newcomer

---

### Critical Issues

#### Issue 1: Feature Dumping Instead of Single Value Prop

**Observed:** We're trying to say everything:
- "One System. Full Context."
- "AI Operating System for Founders"
- "Product. Engineering. Sales. Marketing. Customer Success. All connected."
- "181 skills, 30+ agents, $500 once"
- "Know Your Agent. Own Your Agent."

**Problem (Miller's Law):** Humans process 7±2 items. We're hitting 10+ distinct claims in the hero alone. Cognitive overload causes bounces.

**Recommendation:** ONE headline. ONE supporting line. ONE CTA.

---

#### Issue 2: No Problem-First Framing

**Observed:** We lead with solution features, not user pain.

**Problem (Loss Aversion):** Users need to feel the pain before caring about the cure. "181 skills" means nothing if I don't feel the problem first.

**Recommendation:** Lead with the problem they came here to solve.

---

#### Issue 3: Abstract Language

**Observed:**
- "AI Operating System" — What does that mean?
- "Full Context" — Context of what?
- "181 skills" — What's a skill?
- "Know Your Agent" — What agent?

**Problem (Concreteness):** Abstract language doesn't create mental pictures. Users can't imagine using this.

**Recommendation:** Use language users would use to describe their problem.

---

#### Issue 4: Stat Chips Don't Earn Attention

**Observed:** "181 skills | 30+ agents | $500 once" as scannable chips.

**Problem:** Stats without meaning. Why should I care about 181 skills? What does a skill do? You're asking me to trust numbers before you've earned my interest.

**Recommendation:** Stats come AFTER establishing value, not in hero.

---

### What's Actually Essential?

**The ONLY things that matter in first 5 seconds:**

1. **Who is this for?** → Technical founders / solo builders
2. **What problem does it solve?** → Running a business alone is hard / tools don't connect
3. **Why should I care NOW?** → Your AI is starting from scratch every time (loss frame)

**Everything else is noise until these are answered.**

---

## Part 2: Behavioral Science Audit

### Scoring (Landing Page Dimensions)

| Dimension | Score | Evidence |
|-----------|-------|----------|
| **Loss Framing** | 1/3 | "Not $200+/month" present but weak. No quantified loss, no pain agitation |
| **Social Proof** | 1/3 | "Built by creator, used daily" is vague. No peer companies, no numbers |
| **Scarcity** | 0/3 | None present |
| **Concrete Language** | 1/3 | Numbers present but abstract ("181 skills" — what's a skill?) |
| **Friction** | 2/3 | Single CTA present, but competing paths (LeanOS vs Services) |
| **Anchoring** | 2/3 | "$200+/month" anchor present but not vivid. "$3,450/month" from Canvas unused |

**Overall Score: 7/18** (Weak)

---

### Top 3 Gaps

#### Gap 1: Loss Framing is Absent

**Current:** "AI Operating System for Founders"
**Problem:** No pain. Why do I need an AI OS?

**What Canvas says the problem is:**
> "Technical founders lose context across fragmented tools. Product specs in Notion, sales in HubSpot, code in GitHub, customer data in Intercom. AI has to start from scratch every time because nothing is connected."

**Fix:**
```
BEFORE: "AI Operating System for Founders"
AFTER:  "Stop losing context across 10+ tools"
        or
        "Your AI starts from scratch every time. Fix that."
```

---

#### Gap 2: Social Proof is Generic

**Current:** "Built by the creator. Used daily to run real businesses."

**Problem:** No specificity. Who? What businesses? What results?

**What Canvas says:**
> "Running 2 businesses on LeanOS simultaneously"
> "Built LeanOS Pro in 2 months — 181 skills, 44 agents"

**Fix:**
```
BEFORE: "Built by the creator. Used daily to run real businesses."
AFTER:  "Built in 2 months. Running 2 businesses daily.
         Every feature tested in production."
```

Or better — get real user testimonials with specific results.

---

#### Gap 3: Anchoring is Weak

**Current:** "$500 once — not $200+/month in AI subscriptions"

**Problem:** $200/month is a weak anchor. Real cost is higher.

**What Canvas says:**
> "Your fragmented SaaS stack costs $3,450/month"
> "$300k+/year in specialists"

**Fix:**
```
BEFORE: "$500 once — not $200+/month in AI subscriptions"
AFTER:  "$500 once — not $3,450/month in SaaS tools
         or $300k/year in specialists"
```

---

### Behavioral Anti-Patterns Present

| Anti-Pattern | Where | Fix |
|--------------|-------|-----|
| **Stacking claims** | Hero has 5+ value props | One headline |
| **Generic proof** | "Used daily" | Specific: "2 businesses, 60 days" |
| **Feature-first** | Leads with "AI Operating System" | Lead with problem |
| **Friction neglect** | "Two Paths" creates choice paralysis | Default to primary path |

---

## Part 3: What We Forgot

### The Essential Story (Problem-Agitation-Solution)

**PROBLEM (What they feel):**
You're using 10+ tools that don't talk to each other. Notion for docs. HubSpot for sales. GitHub for code. Intercom for support. Your AI has to start from scratch every single time.

**AGITATION (Make it hurt):**
Every tool switch = lost context. You're paying $3,450/month for a stack that fragments your thinking. And competitors with connected systems are moving faster.

**SOLUTION (The transformation):**
One system where Claude sees your whole business. Product, engineering, sales, customer success — all connected. Your AI finally has the context to actually help.

**PROOF (Why believe):**
Built in 2 months. Running 2 businesses daily. Every skill tested in production.

**OFFER:**
$500 once. Yours forever. 30-day money back.

---

### Recommended Hero (Behavioral-Optimized)

```html
<section class="hero">
  <!-- PROBLEM - Loss Frame -->
  <h1>Your AI starts from scratch every time.</h1>

  <!-- AGITATION -->
  <p class="tagline">10+ tools. Context lost between each one.
     $3,450/month for a stack that fragments your thinking.</p>

  <!-- SOLUTION - One line -->
  <p class="hero-solution">LeanOS connects your entire business.
     Claude finally has the context to actually help.</p>

  <!-- CTA - Single, clear -->
  <div class="hero-links">
    <a href="/leanos" class="btn btn-primary">See How It Works</a>
  </div>

  <!-- Minimal proof -->
  <p class="hero-proof">$500 once. 30-day money back.
     Built in 2 months, running 2 businesses daily.</p>
</section>
```

**What's different:**
- ONE clear problem (not 5 competing claims)
- Loss frame FIRST (context lost, money wasted)
- Solution is the transformation (context → help) not the feature (181 skills)
- Stats/features come LATER (on LeanOS page, after interest established)
- CTA is exploratory ("See How It Works") not committal ("Get Pro")

---

## Part 4: Hierarchy Correction

### Current (Wrong)

```
1. Name (Bella Belgarokova)
2. Feature label (AI Operating System)
3. Tagline (Know Your Agent)
4. Stats (181 skills, 30+ agents)
5. CTAs
```

### Recommended (Behavioral)

```
1. Problem headline (Your AI starts from scratch every time)
2. Pain amplification ($3,450/month, context lost)
3. Solution promise (One system, full context)
4. Single CTA (See How It Works)
5. Minimal proof (Built in 2 months, running 2 businesses)
```

**Save for LeanOS page:**
- Stats (181 skills, 30+ agents)
- "Know Your Agent" differentiator
- Feature breakdowns
- Pricing details
- Five Functions framework

---

## Summary

| Area | Current | Recommended |
|------|---------|-------------|
| **Hero focus** | Features | Problem |
| **Language** | Abstract ("AI OS") | Concrete ("starts from scratch") |
| **Emotional pull** | None | Loss aversion |
| **Stats placement** | Hero | After interest |
| **CTA clarity** | Competing paths | Single path |
| **Social proof** | Generic | Specific |

### The One Thing We Forgot

**We forgot to make them feel the problem first.**

All the stats, skills, functions, agents — none of it matters until the visitor thinks "yes, that's my problem."

Lead with pain. Earn the right to talk about features.

---

## Next Steps

1. Rewrite homepage hero using Problem-Agitation-Solution structure
2. Move stats/features to LeanOS page (earned attention)
3. Strengthen social proof with specific claims
4. Update price anchor to $3,450/month (from Canvas)
5. Remove "Two Paths" choice paralysis — default to LeanOS, link to Services
