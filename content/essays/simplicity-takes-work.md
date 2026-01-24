---
title: "Simplicity Takes Work"
tags: ["systems", "judgment"]
summary: "Why simple systems are not born but constructed, and how most complexity is not a technical failure but a cognitive one."
weight: 10
---
"The technician said the air conditioner was overcomplicated. \'Why can't they just make it simple? Why do they need to overcomplicate things?\'" He was right --- too many components, too many points of failure. But that wasn't because the designer wanted it that way. It's because designing something simple takes time and money. Cheap things are complex because no one could afford to make them simple.\
\
The physicist Blaise Pascal once apologized in a letter: \'I have made this letter longer than usual because I have not had time to make it shorter.\' That single line captures one of the hardest truths in engineering: simplicity isn't the absence of complexity --- it's what remains after you've done the hard work to understand and refine.\
\
Complexity is the natural state of any system. It appears whenever understanding is incomplete. Every workaround, every \'just in case\' condition, adds another layer. Ironically, many of those \'what if\' cases aren't special at all --- they're part of the business model. A well-designed system absorbs them into its normal flow. When that happens, you know simplicity has been achieved: not by denying complexity, but by giving it a natural place to live.\
\
I remember sitting through a presentation early in my career where an \'expert\' explained that physical systems, like springs, are smooth and continuous --- while software systems are full of exceptions and special cases. He said it as if that were an inevitable truth of software. But it isn't. That's not a property of software; that's a property of poor design.\
\
A well-structured system behaves like a continuous function. It doesn't fracture into a forest of conditionals and exceptions; it flows. The more your design mirrors the logic of the business, the fewer discontinuities you need to patch. The goal isn't to eliminate complexity, but to model it so cleanly that what others call \'edge cases\' are simply natural outcomes of the rules.\
\
Simplicity, then, is not the absence of detail --- it's the presence of clarity. You can only remove complexity from what you understand. Each simplification is a hypothesis about what can safely be discarded, and that hypothesis takes experience to form. That's why simple designs often look obvious in hindsight: every part fits so well it feels inevitable. But that illusion of inevitability is the mark of mastery. The novice builds complexity through enthusiasm; the expert removes it through understanding and discipline.\
\
The trouble is, simplicity costs time. It takes longer to design, align, and refine. It requires iteration, discussion, and the courage to revisit assumptions. That's why the cheapest systems are often the most complicated --- not because they're ambitious, but because they're unfinished. The work of simplification simply wasn't funded.\
\
Still, not all complexity is bad. Some domains demand it. Distributed caching, multi-layered access control, or real-time synchronization --- these problems are inherently difficult. Sometimes complexity is the only way to satisfy performance, security, or regulatory requirements. But even necessary complexity doesn't have to be opaque. A complex system can still be clear if it's well-structured, well-encapsulated, and reasoned about at the right granularity. Complexity and clarity are not opposites --- but clarity must always win.\
\
True simplicity doesn't emerge from minimalism; it comes from method. It grows out of good decisions, consistent reasoning, and hard-earned understanding.\
\
Proper encapsulation is one of the most critical parts. When it's missing, services call each other endlessly, passing around excessive data. Each change ripples across multiple modules that should have been independent. True encapsulation defines clear ownership, so each component is responsible for its own behavior and data, and can evolve without breaking its neighbors.\
\
The right granularity matters just as much. Get it wrong, and you'll suffer in two directions: too large, and you lose flexibility and scalability; too small, and you drown in orchestration and coordination. Performance can crumble when one small piece needs to scale separately but can't, or when a single business operation requires dozens of chatty service calls.\
\
The Open--Closed Principle (OCP) is another quiet hero of simplicity. When violated, every change demands code rewrites across multiple components, followed by endless meetings about rollout schedules and rollback plans. When respected, it allows systems to grow predictably --- extending behavior without constantly rewriting what already works.\
\
Choosing the right tools is another hallmark of mature simplicity. Reinventing a distributed cache instead of using Redis rarely leads to innovation; it leads to complexity, unreliability, and wasted effort. Similarly, storing large documents in a relational database might seem convenient --- until you realize that BLOB columns are slow, rigid, and hard to query. Tools matter, and simplicity depends on respecting what each tool is best at.\
\
Finally, understanding the business itself is the foundation. Every system reflects the clarity --- or confusion --- of the business it serves. Poorly understood domains lead to arbitrary restrictions, awkward APIs, and boundaries that don't align with real-world concepts. When the model of the business is clear, the software that mirrors it can be simple too.\
\
These principles sound ordinary, even boring --- but that's the point. Simplicity grows from fundamentals mastered over time, not from clever tricks. It can't be rushed or forced; it's distilled, not assembled.\
\
In architecture, the goal is rarely to build the best system. As Neal Ford and Mark Richards wrote in Fundamentals of Software Architecture, the goal is to build the least-worst system that meets its real constraints. That isn't cynicism; it's honesty. Perfect architectures exist only on whiteboards. Good ones make deliberate compromises and express them clearly.\
\
That's the same mastery that produces simple machines: knowing which trade-offs define the right shape for the problem, and shaping the system so that every part serves its purpose cleanly --- no more, no less.\
\
Complexity is what we start with. Simplicity is what we earn. It's the result of time, thought, and experience --- the art of writing a shorter letter when everyone else settles for a longer one.