---
layout: post
title: "Why I Built an AI Operating System for Myself"
date: 2025-12-15
description: "From a failed London startup in 2014 to building LeanOS in Dubai - the real story of why systems beat co-founders"
reading_time: 8
tags: [founder, leanos, ai, startup]
leanos_ref: "CLAUDE.md"
---

I didn't set out to build an operating system. I was drowning.

But let me start at the beginning. The real beginning.

---

## London, 2014: The First Lesson

I moved to London with a startup idea and zero technical skills. Completely naive about what building a company actually meant.

Two gentlemen joined as co-founders. Respectable backgrounds - one from consultancy, another running a company that was doing okay. Their expectation was clear: I would handle execution. All of it.

One problem. We had no technical team member. Three people from business backgrounds trying to build a tech product.

The startup didn't work. But I learned something that took years to fully understand: **execution and people are the major bottlenecks.** Not ideas. Not market timing. Not funding.

I parked the startup dream and decided to learn coding myself.

---

## Dubai, 2025: Round Two

Two years ago I moved to Dubai. It's a place where you should build a business. The energy is different here.

Beginning of this year, I decided to try again. Joined an accelerator program in Oman. This time, I thought, I'll do it right.

The conventional wisdom: you need a co-founder. One handles engineering, one handles operations. Division of labor. Cover each other's weaknesses.

In May, a co-founder joined. She brought her own startup - or to be precise, an idea on air and some broken code from a previous team who'd worked on it for a year.

No documentation. 14 services scattered across Heroku. Deployment broken. Six months of someone else's work with no context for why anything was built the way it was.

Usually, no developer likes touching someone else's undocumented code. The moment you change one part, the whole thing falls apart. I spent months reverse engineering the project, creating stable documentation, trying to understand what existed before I could build on it.

I was also building Detekta - breach report generation for GCC financial institutions. Two products. One technical founder. Progress felt slow but steady.

Or so I thought.

---

## The Wake-Up Call

One conversation changed everything.

I met someone who'd joined an accelerator program a month prior. He said, casually: "Next week I will do sales."

One month in. Already selling.

We'd been on two projects for months. We hadn't attempted to sell either of them. Not once.

My co-founder's view: we should have working software before we try to sell it. Build first, sell later. It seemed reasonable at the time.

But when I started examining this assumption, I discovered something worse. On the "operations" side - the part that wasn't my responsibility - we had nothing. No strategy. No market research. No ICP. No prospect list. No positioning.

We weren't just not selling. We weren't prepared to sell.

Things that seem obvious now weren't obvious then. I'm a human being. This is a lesson learned.

---

## When Systems Replace People

I couldn't get what I needed from my co-founder. So I switched to generative AI. Read books. Watched podcasts. Started building the knowledge myself.

First attempt: MCP integrations. Documentation in Confluence and Notion. Claude Projects for context.

It was a headache. Every conversation started from zero. Twenty minutes copy-pasting context from different sources before the AI could help with anything useful.

Then Claude Code came out. Then Skills.

I moved everything into one repository. Plain markdown files. Strategy. Operations. Marketing. Sales. Engineering. All in one place, all referencing each other.

No duplication. No docs that don't bring value. Workflows orchestrated by agents and skills. Context window always has what it needs because everything lives together.

This became LeanOS.

The system isn't perfect. But it exists. It's operational. It helps me build and run two products simultaneously - something I couldn't do with a co-founder and scattered tools.

---

## What I Actually Learned

**2014 taught me:** Execution and people are bottlenecks. Having co-founders doesn't solve this. Sometimes it creates new bottlenecks.

**2025 taught me:** The era of "I need a co-founder for the business side" might be ending. AI can handle research, strategy documentation, content generation, prospect identification. Not perfectly. But consistently. Without misaligned incentives or different definitions of "progress."

**Building LeanOS taught me:** The friction isn't the AI. It's assembling context. Put everything in one place. Reference, don't duplicate. Let the system remember so you don't have to.

Every decision in LeanOS goes through 6 stages: Input, Hypothesis, Implication, Decision, Actions, Learning. Stage 6 is the point - learning feeds back into the system. When a similar situation comes up, there's a record. Not just what I decided, but why.

Sounds bureaucratic. Actually faster. Because I stopped re-deciding the same things.

---

## The Co-Founder Story

I'm sure my ex-co-founder has her own view. It might be right. It might be wrong. Time will tell.

What I know for sure: I'll continue this journey of exploration, curiosity, and building. The partnership didn't work, but the learning was worth it.

Some lessons you can only get by living them.

---

## The System That Emerged

LeanOS is now open source. It's a methodology implemented as Claude skills and markdown files - a way of thinking about decisions encoded into structure.

The architecture matters more than the code. Canvas holds strategy. Threads capture decisions. Skills execute. Artifacts store outputs. Everything references, nothing duplicates.

I built my personal operating system on top of it. Two products. Marketing. Sales prep. Engineering. All running through the same system.

Not perfect. Operational. Evolving.

---

*Built on Claude. Refined continuously. Still learning.*
