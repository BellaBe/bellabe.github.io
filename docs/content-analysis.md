# Content Analysis: Personal vs Product Confusion

**Date:** 2026-01-23
**Issue:** Website reads as product marketing, not personal site

---

## The Problem

**URL:** bellabe.github.io (personal domain)
**Reads as:** LeanOS product landing page

The homepage no longer introduces Bella. It immediately pitches LeanOS.

---

## Current Content Map

### Homepage (index.html)

| Section | Content | Type |
|---------|---------|------|
| Hero | "Your AI starts from scratch every time" | **Product pitch** |
| Hero | "$3,450/month... LeanOS connects..." | **Product pitch** |
| Hero | "$500 once. 30-day money back." | **Product pitch** |
| Section 2 | "One System. Full Context." | **Product pitch** |
| Section 2 | Build / Sell / Operate cards | **Product features** |
| Section 3 | Recent Writing | Personal |
| Section 4 | Connect (GitHub, LinkedIn, X) | Personal |
| Footer | Services cross-link | Personal/Services |

**Verdict:** 80% product pitch, 20% personal

### LeanOS Page (leanos.html)

| Section | Content | Type |
|---------|---------|------|
| Hero | "Know Your Agent. Own Your Agent." | Product |
| What is LeanOS | 6 capability cards | Product |
| Example Skills | 3 concrete examples | Product |
| Why "Know Your Agent" | Transparency differentiator | Product |
| What's Included | Core vs Pro | Product |
| Pricing | $500, anchoring | Product |
| Who It's For | 3 personas | Product |
| Final CTA | Get Pro | Product |

**Verdict:** 100% product page (correct)

### Services Page (services.html)

| Section | Content | Type |
|---------|---------|------|
| Hero | "Technical Strategy for Non-Technical Founders" | Services |
| Cost of Waiting | Loss framing | Services |
| What You Get | 3 value props | Services |
| Investment | Pricing context | Services |
| Who It's For | 3 personas | Services |
| How It Works | Built on LeanOS | **Product tie-in** |
| About Me | Brief bio | Personal |
| Final CTA | DM on LinkedIn | Services |

**Verdict:** 85% services, 15% product tie-in

### About Page (about.html)

| Section | Content | Type |
|---------|---------|------|
| Header | Photo + "About Me" | Personal |
| The Journey | Career path | Personal |
| The Wall | Origin story | Personal |
| Now | Current thesis | Personal |
| Values | 3 values | Personal |
| Background | Bio bullets | Personal |
| What I'm Building | LeanOS + Services links | Personal/Product |
| Connect | Social links | Personal |

**Verdict:** 90% personal (correct)

---

## The Confusion

### Problem 1: Homepage Identity Crisis

**Current homepage says:**
- "Your AI starts from scratch every time" (LeanOS problem)
- "$3,450/month for a stack..." (LeanOS pitch)
- "See How It Works" → goes to LeanOS page

**A personal site homepage should say:**
- Who is Bella?
- What does she do/build?
- Why should I care about her?

### Problem 2: Redundant Content

**Homepage duplicates LeanOS page:**

| Topic | Homepage | LeanOS Page |
|-------|----------|-------------|
| Problem statement | ✓ "AI starts from scratch" | ✓ (implied) |
| Build/Sell/Operate | ✓ 3 cards | ✓ 6 cards |
| Price anchor | ✓ "$3,450/month" | ✓ "$3,450/month" |
| $500 once | ✓ hero proof | ✓ pricing section |
| CTA to LeanOS | ✓ twice | N/A |

**Result:** Visitor sees the same pitch twice. No progression.

### Problem 3: Personal Brand Erased

**Original homepage had:**
- "Bella Belgarokova" as H1
- "Building LeanOS" as context
- "Dubai-based. Building solo with AI leverage."

**Current homepage has:**
- No name visible until footer
- LeanOS problem as H1
- Product pitch as primary content

**The person disappeared.**

---

## Site Architecture Options

### Option A: Personal Site with Product Section (Current Intent)

```
bellabe.github.io/           ← About Bella, links to what she builds
bellabe.github.io/leanos     ← LeanOS product page
bellabe.github.io/services   ← Fractional CTO services
bellabe.github.io/about      ← Extended bio
bellabe.github.io/writing    ← Blog
```

**Homepage should be:** "This is Bella. Here's what she builds."
**LeanOS page should be:** Full product pitch (already correct)

### Option B: Product Site with Personal Section

```
bellabe.github.io/           ← LeanOS product landing
bellabe.github.io/about      ← About Bella (creator)
bellabe.github.io/services   ← Additional services
```

**Homepage should be:** LeanOS pitch (current)
**About should be:** Who built this

### Option C: Separate Domains

```
bellabe.github.io/           ← Personal site
leanos.dev/                  ← Product site (separate)
```

**Cleanest separation but requires new domain.**

---

## Recommendation

**Go with Option A: Personal Site with Product Section**

**Reasoning:**
1. Domain is `bellabe.github.io` — visitor expects personal site
2. Authority builds through person, not just product
3. Services require personal credibility
4. "Built in public" strategy needs personal presence

---

## Proposed Homepage Structure

```
HERO
├── "Bella Belgarokova" (name as H1)
├── "Building solo with AI leverage" (positioning)
├── "Dubai-based founder. Self-taught engineer." (context)
└── Connect links (GitHub, LinkedIn, X)

WHAT I'M BUILDING
├── LeanOS card (primary project)
│   └── Brief pitch + "Learn more" link
└── Services card (secondary, passive)
    └── Brief pitch + link

RECENT WRITING
└── 3 posts or placeholder

WHY FOLLOW
├── "Building in public" context
└── What you'll learn by following
```

**Key difference:** Homepage introduces Bella, then points to what she builds.
LeanOS page does the full product pitch.

---

## Content That Should Move

### FROM Homepage TO LeanOS Page Only

- "Your AI starts from scratch every time" (problem statement)
- Build / Sell / Operate cards (feature overview)
- "$3,450/month" anchor (pricing context)
- "$500 once. 30-day money back." (pricing proof)

### Keep on Homepage

- Recent Writing
- Connect links
- Brief intro to LeanOS (1-2 sentences max)
- Brief intro to Services (1-2 sentences max)

---

## Proposed Homepage Hero

```html
<section class="hero">
  <h1>Bella Belgarokova</h1>
  <p class="tagline">Building solo with AI leverage.</p>
  <p class="hero-label">Self-taught engineer. Dubai-based.
     Running 2 businesses with one AI system.</p>
  <div class="connect-links">
    <a href="https://github.com/BellaBe">GitHub</a>
    <a href="https://linkedin.com/in/bellabelgarokova/">LinkedIn</a>
    <a href="https://x.com/bellabelga">X</a>
  </div>
</section>
```

Then "What I'm Building" section with LeanOS and Services cards.

---

## Decision Needed

**Question for Bella:**

Is this site primarily:

**A) A personal brand site** that showcases LeanOS as your main project?
→ Homepage should introduce you, then link to LeanOS page

**B) A product landing page** for LeanOS that happens to be on your personal domain?
→ Current structure is correct, just needs About page prominence

The current confusion comes from trying to do both simultaneously on the homepage.
