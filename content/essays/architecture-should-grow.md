---
title: "Architecture Should Grow, Not Mutate"
tags: ["architecture", "change"]
summary: "How irreversible decisions quietly accumulate, why “refactoring the whole thing” is rarely possible, and what it means for architecture to gain mass over time."
weight: 30
---
## The Open--Closed Principle at the Architectural Level

If I had a euro for every time someone called the Open--Closed Principle an architecture concept and then immediately started talking about classes and inheritance, I could fund a small cloud deployment.\
\
The truth is, the Open--Closed Principle (OCP) is one of the most misunderstood ideas in software. Most explanations stop where the code ends. But architecture---the stuff that's hard to change later---is exactly where OCP becomes most meaningful.\
\
The textbook definition says that software entities should be open for extension but closed for modification. At the code level, this often translates to "don't touch existing code; just subclass it." That's fine advice for small, stable units of logic, but architecture isn't a collection of classes---it's a collection of decisions. And those decisions, once made, are expensive to reverse. Architecture is, by definition, the part of the system that is hard to change later, so our real goal isn't to freeze it---it's to make sure that when change inevitably comes, it doesn't require rebuilding what already works.\
\
I learned this the hard way.\
\
I once inherited a "system" that was really just a patchwork of single-purpose scripts and small apps---each doing its job, none aware of the others. Whenever the business changed, we had to change dozens of these little fragments. Worse, they were chained together in fragile ways, so one small logic tweak triggered a rollout nightmare. We spent more time synchronizing releases than delivering value.\
\
Eventually, I had enough. The business unit running this Frankenstein stack had become strategically important, and I pushed for a complete redesign---a proper distributed system that could scale and adapt. The key idea was encapsulation: each service should own a specific role and evolve independently.\
\
But as I started designing the APIs, something still felt off. The design looked clean on paper but didn't feel resilient in practice---we were still too dependent on the shape of the data. That's when the realization hit: APIs should describe intent, not structure.\
\
Instead of saying "this account has property X," our requests began to say "this account needs to be treated this way." It was a subtle but powerful shift. Later, when other account properties required the same treatment or the rules became more complex, we didn't have to modify every service. Only the strategic ones that decided which accounts should be treated how needed to change. Everything else could simply be extended to handle the new case.\
\
The result was a system where each service was open to extending what it could do but closed to changing how it treated existing parameters. And when something went wrong, we had a simple fallback: just stop setting the new parameter. Deployments became calm and predictable again. No cross-team coordination. No cascading regressions.\
\
That was the first time I truly felt what the Open--Closed Principle means at the architectural level---systems that grow by addition, not by fear.\
\
When viewed this way, OCP stops being about immutability and becomes about additivity. A system is open for extension if new capabilities can be added through additive change, and closed for modification if existing behavior, integrations, and contracts remain intact. You can add a new endpoint without rewriting an old one. You can add a new event type without breaking existing consumers. You can introduce a new domain or module without refactoring the old ones to make it fit.\
\
When done well, a system doesn't resist evolution---it absorbs it. It grows like a tree: new branches sprout from stable trunks, each reaching further without disturbing what came before.\
\
This ties closely to what I once described as degrees of freedom---how every decision either frees or constrains a system's future movement. Too few degrees of freedom, and your system becomes rigid. Too many, and it becomes chaotic and unpredictable. OCP is what governs which freedoms to keep. It gives us the middle ground: open where extension is expected, closed where stability is required. In short, you can grow, but you cannot change what's already done.\
\
You can feel when an architecture violates this principle. A small change causes ripples across the entire system. A new feature needs five coordinated releases. A shared schema update breaks multiple services. Adding one new behavior forces you to revisit three old ones. These are all symptoms of a system that's "open" in the wrong places---too fragile to evolve safely.\
\
Ironically, the best architectures tend to follow OCP naturally because they reflect the structure of the business itself. Business domains evolve independently, and so should the systems that represent them. When your architecture mirrors your organization's logical structure, a business change becomes an architectural extension, not an architectural surgery. Each domain can grow internally without threatening the others. That's OCP in its purest form---local change with global stability.\
\
Of course, even the best systems need the occasional cleanup. Old endpoints must be retired; data flows refactored. That's not a violation of OCP---it's housekeeping, not mutation. But if every change demands a "refactor month," you're not extending; you're fighting your own design.\
\
A good architecture isn't one that never changes. It's one that can change without fear.\
\
As I often tell managers when they hesitate to invest in change:\
"Change is inevitable. We either welcome it and adapt early, on our terms---or we adapt when we must, the way we're forced to."\
\
The Open--Closed Principle is what lets us adapt early---gracefully, predictably, and with confidence that what worked yesterday will still work tomorrow.