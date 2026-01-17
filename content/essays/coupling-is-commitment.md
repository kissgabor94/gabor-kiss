---
title: "Coupling Is Not Evil — It’s a Commitment"
tags: ["judgment", "architecture"]
summary: "Why eliminating coupling is neither realistic nor desirable, and how the real architectural mistake is failing to recognize which commitments you are making permanent."
weight: 40
---
## When Best Practices Become Blind Practices

Software engineering has a habit of turning sound reasoning into slogans. "Loose coupling." "Composition over inheritance." "Microservices for everything." They sound modern and safe, so people repeat them without thought.\
\
This is how good ideas become lazy ones. It's easier to copy advice than to understand it. Following a slogan feels responsible --- nobody gets blamed for "best practices." But systems built on slogans inherit the same weakness: they look sensible on paper and collapse under real context.\
\
Architecture isn't a checklist. It's judgment --- choosing where to commit and where to keep options open. Repeating the right answer in the wrong place is still wrong.

## How "Loose Coupling" Became a Half-Truth

Coupling measures how tightly parts of a system depend on each other. Loose coupling means one part can change without breaking another. Tight coupling means changes ripple through connected components.\
\
That distinction was useful until it became gospel. The microservices movement spread the belief that loose coupling is always good, tight coupling always bad. What got lost is that independence has a cost --- more APIs to design, more latency to handle, more deployments to coordinate. The system spends more effort maintaining its flexibility than delivering value.\
\
The APIs themselves grow complex and verbose because every dependency must now be expressed explicitly. What used to be a function call inside one process becomes a documented contract with serialization, authentication, versioning, and monitoring. Each interaction becomes a small negotiation. Multiply that by dozens of services, and you have a distributed bureaucracy disguised as architecture.\
\
Loose coupling has benefits --- simpler testing, clearer ownership, faster parallel work. Tight coupling has technical advantages too: less overhead, better performance, simpler data flows. But those are engineering details. The real question is when each type of coupling serves the system's purpose. That's the level where most discussions stop short.\
\
Loose coupling only works when you already know what must stay stable. Without that understanding, it just creates optionality without direction.

## How Coupling Creates Stability

Coupling isn't a failure of design --- it's a statement of intent. It says: this relationship matters; these parts belong together.\
\
Think of a robotic arm. It can move, rotate, and reconfigure itself with remarkable freedom. But all that freedom depends on one absolute: the base is tightly coupled to the mounting point. Without that fixed anchor, the arm can't do anything precise --- it just spins aimlessly.\
\
Software is no different. Some parts need to move freely --- user interfaces, adapters, edge logic. Others must stay fixed --- the data models, transaction logic, domain rules that define what the system is. Those tightly coupled parts form the mounting point for everything else. Their stability is what lets the rest of the system evolve safely.\
\
And coupling isn't all-or-nothing. Systems are made of regions:
- Tightly coupled cores where performance, coherence, and identity live.
- Loosely coupled peripheries where experimentation, extension, and adaptation happen.

A well-designed system balances both. The tight core gives it structure; the loose edges give it reach. If everything is tightly coupled, the system becomes rigid. If nothing is, it loses shape entirely.\
\
Multiple services that always change together are not independent; they're one architectural unit disguised as many deployables. That's not a problem --- those services may still need to exist separately for scaling, security, or regulatory reasons --- but they should still be designed and evolved as a single cohesive whole. Recognizing and honoring that coupling simplifies design. Pretending it isn't there creates friction and fear.\
\
Coupling, applied consciously, turns chaos into coordination. It ties down the degrees of freedom we choose to fix, so the rest can move without risk.

## Coupling and the Shape of Change

In the end, coupling isn't just a technical choice --- it's a reflection of how the business itself expects to change. Every tightly bound part of the system declares, "this is stable; this is who we are." Every loose connection says, "this might evolve." Good architects align these boundaries with the business's own pace of change. Coupling, at its best, expresses trust --- trust that some decisions will hold so others can move freely. It's the backbone that gives change its shape.

## Closing Thought

Coupling is not evil. It's how we make architectural commitments.\
\
It defines where motion stops and meaning begins --- the deliberate connections that give a system both stability and purpose.