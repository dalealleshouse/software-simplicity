# Software Simplicity

## What is Complexity
- Considered next to testing and reasoning, simplicity is more important than
    either. An investment in simplicity, is often the better choice because it
    will facilitate all future attempts to understand the system — attempts of
    any kind. - Ben Moseley and Peter Marks
- (Software design is) a craft… and it has a lot to do with valuing simplicity
    over complexity — Barbara Liskov
- We need to build simple systems, if we want to build good systems — Rich
    Hickey 
- The only way to write complex software that won’t fall on its face is
    to hold its global complexity down, to build it out of simple parts — Eric
    S.  Raymond
- Simple can be harder than complex: You have to work hard to get your thinking
    clean to make it simple. But it’s worth it in the end because once you get
    there, you can move mountains. — Steve Jobs
- Simplicity is a prerequisite for reliability.— Edsger Dijkstra 
- The price of reliability is the pursuit of the utmost simplicity— Tony Hoare

Every programmer should aim to write the simplest possible program which solves
the problem.

Everyone talks about the need for simplicity, but never asks the question, "what
is simple?".

"Debugging is twice as hard as writing the code in the first place. Therefore,
if you write the code as cleverly as possible, you are, by definition, not smart
enough to debug it." - Brian Kernighan

No Silver Bullet — Essence and Accidents of Software Engineering - Fred Brooks

> Much of the complexity that [a programmer] must master is arbitrary
> complexity, forced without rhyme or reason by the many human institutions and
> systems to which his interfaces must conform. 

Fred Brooks

> Essential Complexity - is inherit in, and the essence of, the problem (as seen
> by the user)

> Accidental Complexity - Complexity with which the development team would not
> have to deal in the ideal world (complexity arising from performance issues
> and from suboptimal language and infrastructure)

Ben Moseley and Peter Marks

The goal is to remove accidental complexity via smart architecture and choice of
tools

Complex code is different than complicated code
- Complex - has a measurable level of complexity (cyclomatic complexity, etc...)
- Complicated - Psychological Complexity - Is the code hard to understand
    * Completely subjective
- Familiarity does not equate to simplicity 
- Complicated code becomes uncomplicated via research
- Complex code will always be complex until it's re-written
- Making complicated code less complex will not necessarily make it less
    complicated.

The math behind software complexity is just a measure to quantify. It is not
necessary to understand it to reduce complexity.

## Simplicity is Hard
> Simplicity is the most intensely intellectual of the XP values. To make a
system simple enough to gracefully solve only today's problem is hard work. -
Kent Beck

> I didn't have time to write a short letter, so I wrote a long one instead -
attributed to many different great thinkers

> e n’ai fait celle-ci plus longue que parce que je n’ai pas eu le loisir de la
faire plus courte. - Pascal

Agile Doctor "high quality costs three times as much up front but is 40% cheaper
in the long run"
- Find this chart

No control over software you must consume (3rd party libs, legacy, etc...)
    * The software "we" write makes up a surprisingly small portion of the
        system

## Measuring Complexity
if you can't measure it, you can't manage it.

A Complexity Measure, Thomas J. McCabe - First attempt to measure - cyclomatic
complexity
- Correlation coefficient of .8 between complexity and defect density

One of the tragedies of software engineering is that, in industry at least,
we've successfully avoided the metrics-based quality revolution that transformed
manufacturing. 

When measuring complexity, it is important to look holistically at coupling,
cohesion, SQL complexity, use of frameworks, and algorithmic complexity.

- Coupling Ratio - ratio between efferent & total coupling 
- LCOM4 algorithm
- Cyclomatic Complexity
    * Measures the number of "linearly independent paths" through a piece of
        code
    * unique path where we count loops only once
    * control flow graph
        - Node = computation
        - Edge = transfer of control between nodes
        - M = E - N + 2
        - Complexity = (number of edges) - (number of nodes) + 2
    * simply count the number of of if, while, for, and case statements
    * Shortcomings
        - Not all statements contribute equally to complexity
        - Does not properly weight complexity caused by nested
        - No accounting for cognitive complexity
- NPath
    * acyclic execution path
    * unique path through the code
- Coupling and cohesion of modules

## Principals

Blindly following rules leads to complexity
- DRY
- SOLID
- Composition over inheritance

Simplicity is somewhat subjective
    - Justice Potter's definition of pornography: "I know it when I see it"

- The fewer the parts, the simpler the program
- Separating from general to specific is simplifying
- Simplicity is tantamount to brevity

I conclude that there are two ways of constructing a software design: One way is
to make it so simple that there are obviously no deficiencies and the other way
is to make it so complicated that there are no obvious deficiencies.— Tony Hoare

[Software simplicity] demands the same skill, devotion, insight, and even
inspiration as the discovery of the simple physical laws which underlie the
complex phenomena of nature. It also requires a willingness to accept objectives
which are limited by physical, logical, and technological constraints, and to
accept a compromise when conflicting objectives cannot be met. — Tony Hoare

# Why Complex?

- There is no single development, in either technology or in management
    technique, that by itself promises even one order-of-magnitude improvement
    in [software] productivity, in reliability, in simplicity. — Fred Brooks

- The one thing you can be sure of is when you get any number of people
    together, they will disagree. Topics of disagreement include the problem,
    the solution, and the implementation of the solution.
    - Framing in this way is silly. The are multiple dynamic problems as seen by
        different people in the system.

- Any meaningful program will become complex over time

- It's impossible for simplicity to spring from simple thinking
    - No magic bullets


- A programming language is low level when its programs require attention to the
    irrelevant. — Alan Perlis


One of the main intentions of React is to abstract away the DOM. However, React
provides refs for those cases where you may need to interact with the DOM. To do
so, of course, you must understand how to interact with the DOM. This means that
the abstraction has failed. In fact, it introduces the additional complexity of
having to understand how to “escape” React to interact with the DOM.

The latest and greatest introduces chaos
- Dale's law of software entropy - if you have a ball of mud, it's not the
    fault of the tools, it's the fault of the team
- Programmers are not to be measured by their ingenuity and their logic but
    by the completeness of their case analysis. — Alan Perlis


if the core value you deliver is technology, it is rarely a good idea to adopt
tools that your best developers don’t want to work with.

our industry right now is far too worried with following the lead of the big
tech giants to realize that sometimes their tools don’t add a lot of value to
our projects.

A lot of developers right now seem to be so obsessed with the technical wizardry
of it all that they can’t step back and ask themselves if any of this is really
needed.

Our answer to the growing complexity of doing business cannot be adding
complexity to the development process – no matter how elegant it may seem.

We must find ways to manage complexity by simplifying the development process.
Because even though managing complexity is our second most important
responsibility, we must always remember the most important responsibility of
software developers: delivering value through working software.
https://www.simplethread.com/software-complexity-killing-us/
