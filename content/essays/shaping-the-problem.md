---
title: "Shaping The Problem"
tags: ["judgment", "models", "architecture"]
summary: "Why painful tradeoffs are often a sign of a poorly modeled problem — not a hard decision."
weight: 65
---
Every architect eventually faces a design decision that feels uncomfortably tight. The options are clear, the tradeoffs well understood — yet choosing any of them feels like accepting damage in a different direction. One option strains performance, another complicates the model, a third invites operational risk.

Tradeoff analysis explains why the discomfort appears. It maps the consequences, clarifies the tensions, and gives structure to the choice.

But sometimes, even with all the analysis in front of you, something still feels off. Not with the options — with the shape of the decision itself.

That quiet discomfort is worth listening to.

It hints that the problem may have been framed too soon, too rigidly, or too narrowly. In many organizations, once something is diagrammed or written into an ADR, it acquires an unintended weight. Boundaries that were meant to be tentative become fixed. Decisions that were meant to guide exploration become commitments.

And then the tradeoffs look worse than they need to be.

This led me to a realization that reshaped how I think:

The quality of the tradeoffs is feedback on the quality of the model. Painful tradeoffs may signal a poorly shaped problem — or they may reflect constraints we cannot move. Either way, the tradeoffs are telling us something true.

This reframing changed everything for me. Tradeoff analysis wasn’t a final step anymore. It became the quiet compass that accompanies the shaping of the problem.

As I model a system, I find myself doing something akin to exploring a problem space. Early paths are hypotheses, not commitments, and walking them back is part of the process, not a failure. A direction looks promising, so I follow it a little. If the consequences grow into something sharp or unwieldy, I step back and explore a different branch. The point isn’t to wander — it’s to let the structure of the problem reveal itself before I freeze it into form.

Each small adjustment to a boundary changes the landscape of tradeoffs. A constraint added here removes unnecessary freedom. A responsibility moved there reduces conceptual noise. Sometimes a difficult concern belongs not in the service design at all, but in technology built specifically to handle it — a database for integrity, a message broker for coordination, a workflow engine for ordering and retries.

These moves aren’t formal steps. They are ways of loosening the frame so the problem can settle into a shape that fits the domain.

And this shaping continues until the tradeoffs soften — until the choice that once felt forced begins to feel natural. The decision hasn’t become easier. The problem has become clearer.

Of course, not all pain disappears. Some constraints are simply immovable: budget, deadlines, regulatory rules, the strange but necessary nature of the business itself. Sometimes the walls around us are real, and the least-worst option is genuinely all we can choose.

But more often than we expect, the walls were drawn by us — too early, too confidently, without enough exploration. And when we reshape the boundaries, the decision space changes with them.

That is why tradeoff analysis works best not as a moment, but as a continuous thread. Not the end of the journey, but the instrument that guides it.

Architecture is choosing the least-worst set of tradeoffs. That remains true.

But we serve our systems better when we let the problem evolve before we freeze it, so that the tradeoffs themselves can reveal the shape the solution is meant to take.

Architecture is choosing the least-worst set of tradeoffs — but only after shaping the problem so the tradeoffs reveal the direction the system can truly follow.