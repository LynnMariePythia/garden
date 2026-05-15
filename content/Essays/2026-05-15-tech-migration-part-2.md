---
title: "What the Living Systems Lens Actually Selects For"
date: 2026-05-15
tags: [tech-stack, living-systems, open-source, data-sovereignty, decentralization, coherence, nextcloud, quartz]
---

# What the Living Systems Lens Actually Selects For

*This is the second in a short series on my tech stack migration for Pythia Capital. The first essay, [[2026-05-04-security-by-design]], described the problem — layered SaaS, fragmented data, regulatory complexity, and the extractive architecture underneath all of it. This essay is about how I actually chose what to build with instead.*

---

A living system is not optimized for short-term efficiency. It is optimized for resilience, adaptability, and the ability to respond to its environment without losing coherence. When I talk about applying a living systems lens to technology selection, I mean something very specific: I am looking for the same qualities I look for in any living system. Can this component breathe? Can it adapt without collapsing? Does it hold its integrity under stress? Does it depend on a single point of failure?

Most SaaS stacks fail this test immediately. They are efficient in the way a factory farm is efficient — optimized for throughput at the expense of everything else that makes a system healthy. They extract value from the periphery and consolidate it at the center. The vendor is the center. You are the periphery.

This is not a conspiracy. It is just the logic of the extractive model operating faithfully according to its own design.

---

## The First Principle: Sovereignty Before Features

When I started evaluating options, I had one non-negotiable filter: I needed to own my data. Not in the marketing sense — not "your data is safe with us" — but in the literal sense that if the vendor disappeared tomorrow, my work would still exist, fully accessible, in formats I controlled.

This eliminated most of the obvious options immediately.

The second filter was modularity. Living systems are not monolithic. They are composed of specialized components that communicate across boundaries while maintaining their own integrity. A liver does not need to know how the lungs work at a detailed level — it just needs a clean interface. A good tech stack works the same way. Each tool does its job. The jobs are clearly defined. Nothing is dependent on everything else.

This is the opposite of the integrated SaaS suite, which sells you on seamless connection but delivers lock-in. The seams are the point. Seams are where adaptation happens.

---

## What I Actually Built

**Nextcloud** became the heart of the member workspace — vault.pythiacapital.io — handling file delivery, group organization, async communication, and project tracking through Talk, Deck, and Collectives. It is open source. The data lives on servers I chose, under policies I wrote. There is no vendor deciding tomorrow that my tier no longer includes a feature I built a workflow around.

To run it, I needed managed hosting for open-source software — and I could not find a single American company that offered what I needed at a reasonable price with the necessary skills. I had to go to Europe. That is not a complaint. It is a data point worth sitting with.

**Elestio** is the managed open-source hosting provider that made this stack possible. The customer service is outstanding. The costs are fair. I can add new open-source tools as I need them. And crucially — they price by capacity, not by person. As I scale, I pay more. That is how pricing should work. It aligns the vendor's incentives with mine. It does not punish growth or subsidize stagnation. Many open-source providers do not yet price this way, nor do they offer the breadth of tool choices. The smaller businesses like mine are out of luck with most of them. The open-source vendors that survive long-term will figure this out — the ones that solve for both sovereignty and viability, and do not assume every business worth serving is either large or venture-funded. Even that assumption may not hold. Just spend some time asking US-based tech entrepreneurs about open source technology...

My fully functional stack is demonstrably less expensive than comparable conventional options. Deal software alone can run thousands of dollars a year, and I am not convinced it is more secure than what I have built. The cost argument for extractive SaaS quietly assumes there is no alternative. There is. These comparisons do not even include the layered costs of managing regulatory, legal, security, and accounting complexity — costs that open-source architectures handle more cleanly by design.

I do not expect my costs to stay as low as they are now. They will increase as I grow. In the meantime, instead of spending my budget on walled-garden software with no data sovereignty and overpriced SaaS options, I can reserve capacity for new tools as I actually need them.

The learning curve was real. I will not pretend otherwise. But the learning curve of understanding your own infrastructure is categorically different from the learning curve of a vendor's proprietary interface. One builds capability. The other builds dependency.

**Quartz** powers the digital garden — garden.pythiacapital.io — as a static site. No database. No CMS with a login portal. No WordPress vulnerabilities quietly accumulating in the background. No cookies hunting people down with annoying pop-ups. I write in plain Markdown, in files I own, and the garden publishes from those files. It is my data. Backup is simple to understand. The publishing workflow is: finish in Typora, build, sync, done. That is the whole thing. The original setup was not easy — I had a real learning curve adjusting the open-source template and migrating years of blog posts because the formats were different. It is an ongoing education, but I can tell you I never felt this empowered when I was using walled-garden software.

There is something clarifying about a tool with no moving parts you do not understand.

**Cloudflare Pages** hosts the marketing site — edge.pythiacapital.io — and manages the redirects from the old domain. Cloudflare is not perfectly decentralized, but it sits at the edge of the network by design, not the center. It distributes rather than consolidates. That is the right directional choice, even if it is not the final answer.

**Whereby** replaced Zoom for live calls. Thirty seconds to share a link. No downloads. No account required for guests. No AI assistant quietly transcribing conversations into someone else's data lake. I still write setup instructions, but now because my clients are not accustomed to things working simply — not because the tool is broken.

**Buttondown** handles email delivery — nothing more. I did not want an email platform that was also a CRM, a landing page builder, a course platform, and an "audience monetization suite." I wanted a tool that sends email reliably and does not make itself the center of the operation. Buttondown does that.

It is not open source, but it carries the ethos. Analytics can be connected — they are off by default, and I leave them off. I will find another way to market than invading people's privacy and calling it growth strategy. Buttondown is GDPR-friendly by design, not by compliance department. If all proprietary software companies operated this way, we would not need GDPR regulation in the first place. The regulation exists because the defaults are wrong everywhere else.

I use Substack too — it is a reasonable way to meet people and reach a wider audience. But it is not my primary space, and it is not where I anchor my work. Platforms like Substack and Gumroad offer what looks like a small-business-friendly package: built-in audience, email list included, regulatory complexity handled for you. And they do deliver on that. But you pay in fee structures that extract heavily from every transaction. The "free" or "easy" option is almost always the most extractive one when you look at the full picture. So yes, I pay more for Buttondown directly. I pay less elsewhere. And the people building these tools need to eat — that calculation matters to me. A financially viable, ethically structured vendor is more resilient than a free platform running on venture capital patience.

**Stripe** handles payments for both services, cleanly separated from everything else. No payment data touching the member workspace. No Stripe having opinions about my content delivery architecture. Clean handoff at the transaction point, then member access handled through Nextcloud group permissions.

This is not a comprehensive list. The stack is still evolving, and I expect it to keep evolving. That is the point of building on modular, open foundations — you can add, replace, and refine without dismantling everything else.

---

## The Pattern Underneath the Stack

If you look at what these tools have in common, the pattern is not obvious from a features comparison chart. They are not always the cheapest options, especially when many bundled SaaS products look cheaper on the surface and easier to use. They are not the most feature-rich. They are not the ones most frequently recommended in SaaS review forums.

What they share is this: each one is designed to do a specific job well, hold its integrity independently, and stay out of the way of everything else. None of them require me to build my whole operation inside their walls. None of them get more powerful as I become more dependent on them — which is the inverse of how extractive platforms work.

This is what modularity looks like in practice. It is not glamorous. It is just durable.

---

## What the Living Systems Lens Is Not

I want to be clear about something, because this framing gets misunderstood. Applying a living systems lens to technology does not mean choosing the artisanal, the slow, or the ideologically pure. It does not mean sacrificing for the greater good. It means asking a different set of questions than the standard evaluation criteria.

The standard questions are: What does this cost? What features does it have? Does it integrate with the other tools I use? These are fine questions. They just do not surface the structural risks — the lock-in, the dependency concentration, the points of fragility that only become visible when the system is under stress.

The living systems questions are: Where does the value go? Who holds the data? What happens when this component fails or changes its terms? What would I need to rebuild if this disappeared? How does this interact with the regulatory environment I am actually operating in?

Those questions produce very different answers.

I might suggest to executive teams, both large and small, to stop delegating infrastructure decisions to IT consultants without first understanding the strategic, operational, regulatory, and security implications of those choices. Investors will be happier long-term. Companies will waste far less of their funding on outdated technologies and processes. During uncertain times, entrepreneurs with a clearer understanding of these nuances can outcompete venture-backed businesses with far less capital.

---

## The Longer Arc

I am still learning this stack. Some things are more friction than I expected. Some things are less. The Nextcloud infrastructure required real attention to get right — file locking issues, security configurations, app compatibility decisions. There were weeks where I questioned whether this was worth the trouble.

It was. Not because everything works perfectly, but because the trouble is mine. When something breaks, I understand why. When I fix it, I own the solution. When I make a decision about what goes where, that decision reflects my actual priorities rather than a vendor's product roadmap.

This is what data sovereignty feels like from the inside. Not frictionless. Just honest.

The next essay in this series will look at how this same architecture — modular, sovereignty-first, edge-distributed — maps directly to how I think about investment coherence. The patterns are the same. The principles travel.

---

*This is the second in a short series for my digital garden exploring technology migration through a living systems lens. The first essay is [[2026-05-04-security-by-design]]. The series connects to my broader work at [The Pythia Scrolls](https://edge.pythiacapital.io/scrolls), where these same principles are applied to investment research.*

---

Enjoy this? Get the Coherence Lab Letter delivered to your inbox → [subscribe](https://buttondown.com/LynnMarie?tag=Garden)
