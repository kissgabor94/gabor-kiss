---
title: "The Right Amount of Control"
tags: ["leadership", "architecture", "judgment"]
summary: "Early in their careers, many architects mistake control for stability. This essay explores the moment that distinction breaks down — and what it means to move from controlling a system to truly understanding it."
weight: 55
---
When a symphony begins, the conductor doesn’t play a single note.
They guide tempo, phrasing, and flow — not through force, but through understanding. Each musician knows their part; the conductor keeps them aligned.

That’s what good architecture feels like when it works.
The system moves as one, not because it’s controlled, but because everyone understands how it’s meant to move.

Early in their careers, many architects mistake control for stability — I know I did.
It rarely starts from arrogance. More often, it begins with sincerity and frustration.
Most of us step into architecture after living through bad systems: [the tangled designs, the unpredictable dependencies](/essays/simplicity-takes-work/), the fragile code that breaks if you look at it wrong. We swear we’ll never let that happen again.
So when we finally get to design something ourselves, we grip tightly. [We over-specify, over-review](/essays/best-practices-as-models/), and try to protect the system from every possible failure. It feels like care, but underneath, it’s fear — the fear that if we don’t hold on, it’ll all collapse back into chaos.

True greatness, though, lies elsewhere.
Great architecture isn’t one that demands brilliance from everyone around it — it’s one that *tolerates the limitations of others.*
A well-architected system can absorb imperfect code, uneven skill, and the occasional bad day without losing coherence.
Control tries to prevent mistakes; understanding designs to survive them.
That’s the real turning point — the moment control transforms into guidance.

An architect who acts like a controller can keep the system stable only while their hands are on the levers. The moment they step away, drift begins.
But an architect who works like a gardener plants, nurtures, and shapes. They plan the landscape, enrich the soil, prune where needed, and protect when storms hit. The system grows not because someone controls it, but because its environment was designed to help it thrive.
A garden built that way doesn’t demand constant intervention — only steady, attentive care.

Of course, even in a well-tended garden, some plants need more care.
There are moments when tighter control is not only justified but necessary — when the team is inexperienced, when the deadline is brutal, when new technology or regulatory constraints raise the stakes.
But even then, control should serve as *closer mentoring*, not as takeover.
The architect’s task is to guide the design hand-in-hand, helping the team see *why* certain boundaries or structures matter, not to design *for* them.
Tighter control is still teaching — just with your sleeves rolled up.

There are, of course, things an architect *must* control — not out of ego, but out of duty.
The architect is responsible for keeping the system a whole, and that means applying control where it truly matters: at the boundaries between architecture and design.
[We review APIs and data models](/essays/shaping-the-problem/), because those are the contracts that define how the parts of the system fit together. We watch [architectural metrics](/essays/observability-makes-software-visible/) and cross-cutting qualities, because coherence doesn’t maintain itself.
We hold design reviews not as audits, but as early tests — to see whether the team has truly understood the purpose of their component and its role within the whole.
And when needed, we guide the testing strategy too, because perfect coverage means nothing if the tests don’t reflect what the system is *for.*
Like a gardener, we also shape direction. When a plant grows the wrong way, it’s corrected early, not punished later. The same goes for architecture — gentle adjustments at the right time keep the system healthy, without heavy intervention later.

Architecture, at its core, is communication.
The architect’s role is not to make every decision, but to make the intentions behind the system unmistakably clear.
The true product of architecture isn’t the system itself — it’s the [shared understanding](/essays/architecture-scales-down/) that allows the system to exist, evolve, and be maintained without its author standing over it.

Architecting defines the structure; designing fills it.
An architect identifies what components the system will consist of, how they relate to one another, what their responsibilities are, and what properties they must maintain.
The architect ensures that these intentions are clear enough for development teams to model them effectively in their own designs.
The developers, in turn, design and implement those components — they give shape and behavior to the abstractions.

If a component’s design fails to reflect its purpose, it undermines the health of the whole system. Changes won’t flow naturally; friction and inconsistency will spread.
That’s why architectural intent must be both well-defined and well-understood.

Finding the balance is the real work.
The goal is not to dictate decisions, but to help teams understand why each design decision exists — so they can own it.
By the end, developers shouldn’t just know what to build — they should know why it matters.
The architect’s influence must scale through comprehension, not authority.

Because just as they shape the system, they also shape the people who sustain it.
A well-architected system needs a well-formed team — one that understands its purpose, its trade-offs, its boundaries, and its rhythm.
Every decision the architect makes is an act of teaching. Every clear interface, every meaningful constraint, every explained choice strengthens the team’s ability to think in systems.
The goal is not only to build a stable structure, but to grow a group of people who can keep it alive.

A resilient system carries its imperfections gracefully.
Control over code fades the moment the architect looks away.
Control over understanding endures long after they’re gone.

That’s the real art of architecture — shaping flow without forcing it, enabling autonomy without losing coherence, until the architect’s role becomes as light as the conductor’s gesture — barely visible, yet felt everywhere.
And like a well-tended garden, the system will continue to grow with only steady care.

That’s the right amount of control.