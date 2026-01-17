---
title: "From Code to Systems: The Three Levels of Thinking That Define Technical Growth"
tags: ["architecture", "systems"]
summary: "Why many architectural debates fail before they start — not because of disagreement, but because participants are reasoning at different conceptual levels without realizing it."
weight: 10
---
When I started coding, I didn't use functions, I just couldn't wrap my head around them.  
I copied entire blocks of code whenever I needed something twice, changed a few variables, and hoped it would still work. It usually did - until it didn't.  

Back then, my world was made of lines, braces, and the desperate joy of watching something compile.  
I thought I was learning to program, but what I was really learning was how to think. I just didn't realize it yet.  

Over the years, I noticed that every big step in my career wasn't about learning a new language, framework, or tool.  
It was about learning to see more while holding fewer details in my head.  
That's what abstraction really is - the ability to understand more by focusing on less.  

I've come to believe that most technical people grow through three levels of abstraction - three ways of seeing the same work.  
Each level changes how you define problems, what you optimize for, and what you see as "success."

## Level 1 - The Implementer

The Implementer thinks in code.  
They care about syntax, loops, and making things run. Their world is concrete - they see systems as collections of files and functions.  

They ask: "How do I make this work?"  

They value correctness, feedback, and visible progress.  
And that's not a bad thing - it's the foundation everything else is built on.  

Example: When given a new feature, the Implementer jumps straight to the editor and starts typing. They see the task as something to make happen.  

Strengths: Pragmatic, efficient, resourceful.  
Growth edge: Tends to optimize locally - "this function," "this sprint," "this issue" - without yet seeing the ripple effects.

## Level 2 - The Designer

The Designer thinks in modules and boundaries.  
They start asking: "How can I build this so others can extend or debug it later?"  

They think about coupling, cohesion, and naming. Patterns begin to matter - not for elegance, but for communication.  
They realize code isn't just for machines; it's a language between humans.  

Example: The Designer looks at that same feature and asks where it should live, how to isolate concerns, and how to make testing easy.  

Strengths: Clarity, long-term maintainability, empathy for future maintainers.  
Growth edge: Still focused on this system - not yet questioning its role in the broader landscape.

## Level 3 - The Architect

The Architect thinks in systems, flows, and trade-offs.  
They ask: "How does this decision affect everything else - today, next month, and a year from now?"  

They think in terms of latency, consistency, resilience, cost, and organizational design.  
They see systems as living organisms - constantly evolving, never "done."  

Example: The Architect might question whether the feature even belongs in this service, or whether it should exist at all.  
They care not only about correctness, but about consequence.  

Strengths: Holistic vision, anticipation of change, clear communication across disciplines.  
Growth edge: Risks abstraction drift - forgetting the reality of implementation if they stay too far above ground for too long.

## How the Levels Work Together

These levels aren't rungs on a ladder you climb and leave behind.  
They're perspectives that coexist - each vital in its own way.  

A great architect still needs to think like a designer and implementer when the situation demands it.  
When debugging production at 2 a.m., abstraction collapses - everyone becomes an Implementer again.  
When designing new domain boundaries, the same architect must think like a Designer to express the idea cleanly in code.  

Likewise, strong Implementers and Designers keep architects honest.  
They expose when abstractions leak, when designs get in the way of real work, and when "elegance" becomes fragility.  

You can think of the three levels as lenses, not ranks:  
- The Implementer's lens gives precision.  
- The Designer's lens gives structure.  
- The Architect's lens gives direction.  

Teams that combine all three perspectives build systems that are both beautiful and battle-tested.

## Identifying Where You Are

I only know two types of developers: those with impostor syndrome, and those riding the Dunning-Kruger high.  
The funny part is that most of us oscillate between those two states two or three times a day.  
That's normal - it's just what growth feels like when your mind is stretching to a new level of abstraction.  

You can usually tell where someone operates by the kinds of questions they ask:  
- "How do I make this work?" → Implementer  
- "How should I structure this?" → Designer  
- "What are the trade-offs here?" → Architect  

Most of us live somewhere between two levels - and that's fine.  
The key isn't to climb as fast as possible, but to know which lens you're using, and when it's time to switch.

## Moving Between Levels

Growth doesn't happen automatically.  
To move up a level, you must change the questions you ask yourself.  
From Level 1 → Level 2:  
- Read code written by others - especially frameworks. Ask why they made those design choices.  
- Seek design reviews, not just code reviews.  
- Practice turning messy code into modular, self-contained components.  

From Level 2 → Level 3:  
- Study distributed systems and system-design trade-offs.  
- Read post-mortems; they're lessons written in hindsight.  
- Learn to connect technical choices to business impact.  
- Talk to people outside engineering - product, operations, even finance. Architecture lives in those conversations too.  

At every stage: Don't chase abstraction for its own sake. It's only valuable if it helps you see further.

## Closing Reflection

I didn't become an architect when I got the title.  
I became one when I stopped asking "How do I build this?"  
and started asking "What will this decision look like two years from now?"  

Each level teaches a new way to see - code, structure, and system.  
You can't skip any of them. But you can choose how far you climb.  

So, which level are you thinking at today?