---
layout: post
title: "How LeanOS emerged from chaos"
date: 2026-02-03
description: "From fragmented tools to one system -- how building two products solo led to 40+ agents, 190+ skills, and an AI that operates a business"
reading_time: 6
tags: [founder, leanos, ai, startup, build-in-public]
image: /assets/images/a1-cover.png
leanos_ref: "README.md"
---

I am building two products from Dubai. Detekta (breach reporting for GCC financial institutions) and Chromly. Both in build stage. No employees. My previous co-founder was not executing, so I went solo.

When you build alone, you do not just write code. You run strategy, product, engineering, marketing, sales, and operations. All of it. And for each function, there is a tool. Confluence for documentation. Jira for project tracking. Linear for product. Notion for everything else.

Each tool works in isolation. Together, they form a system held together by your attention. Every morning starts the same way: rebuild context across tools before making a single decision.

I told myself this was normal. Cost of building. Every founder deals with this.

---

## The fragmentation tax

The subscriptions are not the real cost. The real cost is cognitive. The founder becomes the integration layer. Every decision that touches two functions -- a product spec that requires strategy context, a marketing plan that needs product positioning -- requires manually reconstructing context across tools.

Founders spend $4,700 to $22,000 per year on fragmented SaaS tools, according to 2026 industry benchmarks. But the financial number understates the problem. The actual cost is the 10-20 hours per week spent on manual operations between tools. Moving information. Rebuilding context. Translating outputs from one tool into inputs for another.

There is a growing market of vertical OS products trying to solve this. Vertical CRMs, vertical marketing platforms, vertical project management. But each one covers a single function. And each one requires significant investment to build, maintain, and scale. For a solo founder, buying five vertical OS products to replace five generic tools does not solve the architecture problem. It just changes the vendors.

---

## AI changed the equation, but not the way people think

In 2025, AI crossed a threshold. 74% of entrepreneurs now have AI as a core component of their startups. AI tools can handle junior development (80% of tasks), content writing (70%), customer support (60%), sales research (40%).

But here is what most people miss about working with generative AI.

There is always a layer between you and the model. The product interface. The prompt template. The system instructions. The context window limitations. Every AI product adds layers, and every layer reduces your ability to extract what you need from the model.

![Opaque vs Transparent: How different systems handle AI operations](/assets/images/a1-comparison.png)

Generative AI incorporates global knowledge. It has read the papers, the frameworks, the case studies. Extracting that knowledge at the quality level required to actually run a business -- not generate filler content, but produce analysis you can act on -- is high cognitive effort. It depends on how much context you can feed, how precisely you can direct the model, and how few layers sit between your intent and the output.

Most AI products optimize for ease of use. Lower the barrier. Simplify the interface. That works when you want a quick draft or a summary. It does not work when you need the AI to understand your business model, your customer segments, your competitive positioning, and your current strategic context -- all at once, in the same session.

This is where most people stop the analysis. They frame AI as "assistance." AI helps you write. AI helps you code. That framing misses the structural shift.

AI that assists is still you doing the work, with help. AI that *operates* runs business functions end-to-end with shared context. The difference: one computes what you ask, the other manages the function.

Nobody was building that. The "AI Business OS" category -- a system that covers strategy, product, engineering, sales, marketing, customer success, orchestration, and operations in one place -- did not exist.

---

## The false starts

My first attempt was MCP integrations with documentation split across Confluence and Notion. Claude Projects for context.

Every conversation started from zero. Twenty minutes copy-pasting context from different sources before the AI could do anything useful. The layer between me and the model was thick: scattered context, no continuity, no shared state.

I tried Notion as an all-in-one. It is a workspace, not an operating system. Good at storing information, not at operating across it.

I tried dedicated AI tools per function. Same fragmentation, different layer. Each tool was smart in its silo and useless across boundaries. And each one added its own layer between me and the underlying model.

The failed attempts taught me something: the problem was not the tools. The problem was the architecture. Separate databases. Separate contexts. Separate layers. No amount of integration fixes an architecture that separates what should be unified.

---

## One repo, shared context

Then Claude Code shipped Skills. An AI that reads files in a repository, executes code, and maintains context across a session. No product layer between you and the model. You talk to Claude directly, and it reads your files directly.

The hypothesis was simple: what if every business function was a skill file in the same repo? Not a SaaS integration. A directory. Not a product layer on top of AI. Plain markdown that the AI reads natively.

First skills: business foundations. In software engineering, you spend serious time defining foundations because they shape everything built on top. The early skills structured business model, segments, positioning, and goals. Not perfect, but the strategy structure was already lining up -- clean, organized, and referenced from one place.

Then came software architecture and product shaping. Requirements, specs, design system. Familiar territory for an engineer.

Then marketing and sales. Territory most software engineers avoid -- and for good reason. But the skills covered it: content strategy, channel scoring, outreach sequences, qualification frameworks. Functions I would not have built well on my own, operating from the same repo with full context.

The integration layer disappeared because there was nothing to integrate. The product layer disappeared because there was no product between me and the model.

![LeanOS Architecture: Agents and Skills operating across Strategy, Goals, Threads, Artifacts, and Research](/assets/images/a1-architecture.png)

190+ skills and growing. 40+ agents. 8 business domains:

- **Strategy:** Canvas holds business model, goals, reasoning
- **Product:** Requirements, specs, prioritization, design system
- **Engineering:** Frontend, backend, testing, architecture
- **Sales:** Prospecting, outreach, qualification, pipeline
- **Marketing:** Content, channels, campaigns, pattern library
- **Customer success:** Onboarding, health monitoring, retention, expansion
- **Orchestration:** Goals, briefs, cross-vertical coordination, tracking
- **Operations:** Thread execution, goal tracking, daily operations

Every skill is a readable markdown file. The architecture is Strategy (business context), Goals (strategic objectives), Threads (execution context), Artifacts (generated outputs), and Research (knowledge discovery) -- all operated by Agents and Skills. Everything references, nothing duplicates.

Today's session alone: built 110 persuasion patterns, mapped a PLG funnel, scored 8 distribution channels, allocated a time-based budget, and planned 32 content posts. From a terminal. Not chasing hype. Producing actual outputs that run the business.

---

## Why this exists

LeanOS exists because the architecture most founders use is wrong for solo businesses. Separate tools with separate contexts, each adding layers between you and the AI that could actually help.

The hypothesis proven over months of daily use: if everything lives in one repo as plain text, AI can operate across all business functions with shared context. No product layers to reduce quality. No context walls between functions. The founder goes from human middleware to reviewer of AI-operated workflows.

I built this for myself because I needed it. I still build on this system every day.

Core is free. MIT license. 15 skills covering reasoning and foundations. Clone the repo, read every skill file, decide for yourself.

Pro is the full system. 190+ skills. 40+ agents. 8 domains. $499 once. Not $5,000 per year.

If you are a founder spending more time moving context between tools than actually building -- this is what it looks like when you stop.

---

*Built on Claude Code. Operated daily. Still evolving.*
