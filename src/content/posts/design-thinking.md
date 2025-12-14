---
title: Design Thinking
pubDate: 2025-11-11
---

## Part 1: The Myth of the "Defined" Problem

To understand why modern software often frustrates us, we have to look at the failures first. We need to analyze why, despite decades of technical advancement, we still encounter interfaces that feel like they were designed by aliens for aliens. Before we get into the theory of Design Thinking, let's look at three specific examples that illustrate the landscape of "bad design." These aren't just aesthetic failures; they are structural failures in how we think about problems.

### The Functionality Monster and the Context Switch

Consider the classic "Bulk Rename Utility." This type of software attempts to solve a very specific, annoying problem: renaming a massive number of files in a file manager. For those comfortable with a Command Line Interface (CLI), this is trivial — provided you remember the correct regex or syntax for the Linux `rename` command. But for the average user, the CLI is a barrier. Early GUI developers saw this and decided to build visual tools. The result, however, is often a "monster" dialog box. Imagine a single window where a developer has attempted to cram every possible permutation of renaming logic — timestamps, numbering, extension handling, replacement strings — into one view.

The issue with these utilities isn't that they lack functionality; it’s that they prioritize the _existence_ of the function over the _human_ who uses it. This is the archetype of "Function Follows Function." The developer assumes that as long as the code can technically perform the task, the job is done. The layout, hierarchy, and clarity are afterthoughts, often decided by where a button happens to fit on the grid rather than where it makes cognitive sense. This points to a deeper issue in engineering culture: the technical capability and ease of implementation are valued higher than the cognitive cost paid by the user.

Then we have the issue of error messages. Straight up, error messages are a failure of design. Even "good" error messages are problematic because they force a hard context switch. When you are in the flow of work and a dialog pops up, you are forced to dump your current mental context to process the error. It is a violent interruption. Worse, the language often bleeds internal technical details into the user space. You might see a prompt asking if you want to "Mark as deleted" versus "Delete," a distinction that makes perfect sense in a database schema but zero sense to a user just trying to clear a file. The internal logic of the system forces its way to the surface, demanding to be understood, rather than the system understanding the user.

### High Stakes and "Dangerous" Design

Bad design isn't just about annoyance; it has a body count. In 2017, the USS John S. McCain collided with the Alnic MC, resulting in the deaths of ten sailors and over \$230 million in damages. That is roughly the total budget of a mid-sized European university. The subsequent investigation didn't just find human error; it found a systemic failure in the User Interface. The ship used a complex touch-screen navigation system that confused the operators.

This tragedy highlights a critical paradox in automation. We build systems to automate complex tasks, but when those systems malfunction or reach their limits, we hand control back to a human operator. The problem is that the operator, now out of the loop and relying on a confusing interface, is the least equipped person to handle that sudden spike in complexity. We cannot simply blame "user error" when the system itself is designed to provoke confusion.

### The Fallacy of the Problem-Based Approach

In Computer Science and engineering, we love the "Problem-Based" approach. It feels rigorous. We define a problem, we analyze it, and then we solve it. It aligns with the "Feynman Algorithm" of thinking: write down the problem, think very hard, write down the solution. This is deeply embedded in how we teach programming and project management. The classic Waterfall model is built on this foundation: you create a massive Requirements Document (often called a _Pflichtenheft_) that defines the problem in exhaustive detail. The assumption is that if we work hard enough on this document, we will arrive at a single, immutable, "true" definition of the problem.

The industry has historically relied on this document to answer all future questions during implementation. It assumes the problem exists independently of us, sitting there like a rock waiting to be measured. But reality disagrees. The Standish Group’s Chaos Report (2015) analyzed 50,000 projects and found that this problem-based, "define it first" approach doesn't just fail to guarantee success — it actually increases the risk of failure.

This is where the distinction between "Problem-Based" and "Solution-Based" (Agile) becomes critical. In a solution-based approach, we accept that we don't fully know the problem yet. We create iterations of solutions not just to fix the problem, but to _find_ the problem. The problem definition changes as we try to solve it.

### The Myth of the "Defined Task"

We need to challenge a core definition of Computational Thinking. Gerald Sussman defined it as "rigorous analysis and procedures for accomplishing a defined task efficiently." The trap here is the phrase **"defined task."**

For a task to be truly defined, the problem must be stable. It must be indisputable. This works for solving a quadratic equation, moving the Tower of Hanoi, or sorting a list of integers. These are what we call **"Tame Problems."** They are mathematically solvable, and their definitions don't change. But the moment you introduce humans into the equation, the idea of a "defined task" crumbles.

We have known this for decades. In their seminal 1986 paper, _A Rational Design Process: How and Why to Fake It_, Parnas and Clements admitted that determining detailed requirements is the hardest part of software design because the people commissioning the system usually do not know what they want. They are unable to tell us everything we need to know until they see the implementation progressing. The "requirements" are not a static target; they are a moving ghost.

### Wicked Problems vs. Tame Problems

If most problems aren't "Tame," what are they? In the late 1960s and early 70s, Horst Rittel and Melvin Webber coined the term **"Wicked Problems."** They were looking at social planning, but their findings map perfectly to modern software engineering.

A Wicked Problem is a problem you cannot understand until you have developed a concept of the solution. You cannot gather information meaningfully unless you understand the problem, but you can't understand the problem without information. It is a circular paradox. Unlike Tame Problems, Wicked Problems have no "stopping rule" — you don't stop because you solved it; you stop because you ran out of money, time, or patience.

Here is the deal with Wicked Problems:

- **No Definitive Formulation:** You cannot write a perfect specification for them.
- **No "True" or "False":** Solutions are only "better" or "worse."
- **One-Shot Operation:** Every attempt counts. You can't just reset the simulation without consequences (like implementing a social policy or deploying a live system).
- **Uniqueness:** Every Wicked Problem is essentially unique.

Henrik Gedenryd’s dissertation, _How Designers Work_, provides a perfect example of this. He describes a developer building spreadsheets for a CFO. The developer would build exactly what was asked for, and the CFO would look at it and say, "That's not what I wanted." It wasn't until the CFO saw the model that he could articulate what he actually needed. The early versions were not "waste"; they were necessary inquiries to discover the actual problem. The problem setting spanned the entire process.

### The Shift to Design Thinking

This brings us to the core realization: **If humans are involved, every problem is a Wicked Problem.**

Mathematical thinking works for Tame Problems. It relies on reduction and abstraction to create proofs. If we can model a phenomenon mathematically, we can wield the superpower of the "Proof." But this only covers a tiny fraction of the world. The rest of the world is messy, human, and wicked.

When we treat Wicked Problems as if they were Tame Problems — when we force them into a rigid Waterfall process or a strict Requirements Document — we fail. We see this in "Smart City" diagrams that depict traffic and energy flow but contain no actual humans. We are taming the problem by ignoring the variables that make it difficult. But those variables always come back to bite us. Requirement volatility is consistently cited as the core problem of software engineering. This volatility isn't a bug; it’s a feature of Wicked Problems.

Design Thinking, therefore, is not about making things pretty. It is the methodology we use to tame the wicked. It is the recognition that problem definition and problem solution must happen simultaneously.

---

_Coming Up in Part 2: We dive into the history of HCI, why "feature creep" is destroying your product, and the "Entanglement" theory that suggests we are no longer separate from our machines._

## Part 2: The Human-Centered Imperative & The History of "Clicking Things"

If Part 1 established that "Wicked Problems" are the true final boss of engineering, then Part 2 is about the weapon we chose to fight them. That weapon is Human-Computer Interaction (HCI). We can lay down a fundamental axiom right here, right now: **If humans are involved, every problem becomes a Wicked Problem.**

This isn't just a philosophical stance; it is a practical reality. Human needs are not independent variables. They are deeply entangled with context. If the context changes — say, a user moves from a quiet office to a noisy train — their needs change instantly. This volatility makes it impossible to create those "true" a priori problem formulations we love in engineering. The discipline that emerged around 1980 to tackle this volatility is HCI. It is effectively the scientific application of Design Thinking within computer science.

Andrea Bianci, a researcher in the field, once framed it perfectly: HCI focuses on designing interactive systems that are both productive and _pleasurable_. This is a massive expansion of the old "Form Follows Function" doctrine. It acknowledges that productivity isn't the only metric; the human experience of using the tool matters. The Association for Computing Machinery (SIGCHI) defines it as the discipline concerned with the design, evaluation, and implementation of interactive computing systems for human use. But even that definition is starting to creak under the weight of reality. As Ben Shneiderman noted back in 2011, HCI has grown from a small, rebellious group of researchers fighting for recognition into a community that impacts the daily lives of every human on earth.

### Buxton’s Law and the Complexity Trap

Why is this focus on the human so critical right now? Because of a little thing called "Buxton’s Law." We all know Moore’s Law, which predicts the exponential growth of computing power and capacity. Buxton’s Law acts as the counterweight: while technology’s complexity and capacity skyrocket, **human capacity does not.** Our cognitive bandwidth is roughly the same as it was 50 years ago.

Technological artifacts — software, gadgets, and the "hidden" computers inside everything from washing machines to sex toys — have utilized Moore's Law to pack in more and more functions. This leads to an explosion of complexity in the User Interface. If the machine gets twice as complex every 18 months, but the user doesn't, you have a usability crisis. This necessitates a shift from "Can we build it?" to "Should we build it, and how?"

This perspective shifts the center of gravity from the technology to the life of the person using it. Historically, we called this "User-Centered Design," but even that term is problematic. "User" implies a person pressing buttons. But what about the person whose career is decided by an automated HR algorithm? They aren't "using" the software, but they are definitely affected by it. "Human-Centered Design" is better, but "Life-Centered Design" or "Humanity-Centered Design" might be where we need to land, acknowledging that our systems impact the environment and society at large.

We are also seeing a dark inverse of this principle today, often called "Enshittification" (a term coined by Cory Doctorow) or the "Rot Economy." This describes the lifecycle where platforms start by being good to users to gain critical mass, then abuse users to make things better for business customers, and finally abuse both to claw back value for shareholders. It is the deliberate degradation of the user experience for profit, a sign of what happens when Human-Centered Design is abandoned for profit maximization.

### The Three Waves of HCI

To understand where we are, we have to look at the "Waves of HCI." This history tracks how our relationship with the machine has morphed.

**The First Wave: Man-Machine Coupling.**
Back when computers were room-sized monoliths, HCI was about "Human Factors." It was physical. The focus was on the knobs, dials, and switches. How should the lights be arranged? What is the optimal keyboard layout (spoiler: it remained the typewriter layout)? How big must the font be on a CRT monitor so a specialist doesn't go blind? This era was about coupling an expert human to a machine to optimize throughput. It was industrial.

**The Second Wave: Cognitive Coupling.**
Then came 1981, the IBM PC, and the "Mother of All Demos." Suddenly, computers were on desktops in offices, used by non-specialists. The physical interaction wasn't the bottleneck anymore; the _mental_ interaction was. The Second Wave viewed the human and the computer as two information processors that needed to talk. The goal was to design tools that helped us "think better." This is where the desktop metaphor, files, folders, and the WIMP (Windows, Icons, Menus, Pointer) paradigm solidified.

**The Third Wave: Social and Entangled.**
Then the internet happened. Then mobile happened. Computers ceased to be tools for "defined tasks" and became the infrastructure of our social lives. We don't just "process information"; we hang out, we play, we create culture. This Third Wave recognized that technology is not external to us. We are now in an era of "Entanglement HCI," where we are inseparable from our devices. The technology is pervasive, embedded, and constant.

### Case Study: Honeywell vs. The Nest

Nothing illustrates the failure of old-school engineering thinking versus Design Thinking better than the Battle of the Thermostats.

Honeywell was the king of thermostats. For decades, they dominated the US market. But they fell victim to "Second Product Syndrome." This is a phenomenon where a successful company pours all its money into incrementally improving its existing cash cow rather than risking innovation. Over the years, Honeywell thermostats became complex beige boxes. They added a small computer inside, which meant they could add a small LCD screen and more buttons. They essentially took the same confusing interface and digitized it. It was powerful, programmable, and utterly hostile to the average human.

Then came Nest in 2011. It didn't look like a piece of industrial equipment; it looked like a piece of jewelry. It was a sleek, round glass dial. But the real revolution wasn't the shape; it was the interaction model. Nest didn't ask you to program a schedule on a tiny, low-res screen. It asked you to just turn it up when you were cold and down when you were hot. It _learned_ your habits. For the complex stuff, it offloaded the UI to a smartphone app, where the interface could be rich and intuitive.

Honeywell was horrified. How could a startup outclass them in their own domain? To his credit, Honeywell CEO David Cote didn't just sue; he realized they had a cultural problem. He saw that in his consumer life, things were getting easier to use, but in his industrial sector, they were stagnant. Honeywell initiated a massive corporate pivot, embedding Design Thinking not just as a visual layer, but as a management philosophy. They built Design Studios and forced upper management to attend design workshops. They moved from a culture of "features" to a culture of "experience." The result? A massive turnaround in stock price and relevance.

### The ROI of Design

This isn't just about feeling good. There is hard data backing the "vibe." The Design Management Institute (DMI) tracks the "Design Value Index," a portfolio of design-centric companies. These companies — who treat design as a core strategy rather than a cost center — consistently outperform the S&P 500 by significant margins (often over 200%).

Design is not a luxury. It is not a coat of paint you apply at the end of the engineering process. It is a core component of business strategy. If you ignore it, you end up like the old Honeywell — rich, established, and waiting to be disrupted by a thermostat that actually knows what it feels like to be human.

---

_Coming Up in Part 3: We get into the gritty theory of "Inquiry" — why you have to build things to understand them — and the specific Heuristics you need to memorize to stop building garbage interfaces._

## Part 3: The Theory of Inquiry & Core Heuristics

We have established that the problems we face in modern engineering are "Wicked" and that Human-Computer Interaction is our primary weapon against them. But wielding this weapon requires more than just good intentions; it requires a fundamental shift in how we process information and a strict adherence to a set of operational laws. The execution of Design Thinking rests on a theoretical foundation that demands we look outside of computer science, accept the limitations of human perception, and embrace a chaotic, iterative path to the truth.

### The Interdisciplinary Requirement

You cannot design effective software if you only understand software. To build systems that function seamlessly for humans, you must possess a working knowledge of the hardware of the human being. This is why the field of Interaction Design is inherently interdisciplinary. It starts with the hard physiological constraints of our bodies. We need to understand how eyes perceive color to avoid poor contrast, we need to know the visual angle required for a font to be legible, and we must consider the physical posture of a user to prevent fatigue or repetitive strain injury.

Beyond physiology, we must delve into psychology. A designer needs to grasp the limits of human attention, how we parse visual hierarchies, and the finite capacity of our working memory. It even extends into organizational theory, asking how teams function and what workflows minimize error. Looking at the landscape of the field, we see a convergence of the hard sciences like engineering, the human sciences like psychology and sociology, and the artistic disciplines of graphic and industrial design. You do not need to be a PhD in all of these fields, but you must be able to communicate across their boundaries. You need to respect that a cognitive psychologist might understand the cognitive load of your navigation bar better than your senior backend engineer does.

### The Distorting Mirror

Engineers and computer scientists think differently than the rest of the population. A classic paper from 1990 confirmed that our mental models are fundamentally distinct; we prioritize efficiency, edge cases, and the mantra of "Faster, Cheaper, Smaller, More." When we build software based solely on our own mental models, the result is what we call a "Distorting Mirror." The technology ends up reflecting the creator’s mind rather than the user’s needs. If an alien archaeologist were to dig up our legacy keyboards and interfaces, they might deduce that humans possessed twenty fingers and a laser-sharp photographic memory.

To succeed, a product must stop being a distorting mirror and start reflecting the actual capabilities of the human using it. This requires a pivot from "Technology-Centered" design, which solves problems based on what the silicon can do, to "Human-Centered" design, which solves problems based on who is doing the work, and where, when, and why they are doing it. Critically, this often means ignoring what users explicitly say they want. Users are notoriously bad designers. If you ask them, they will request specific features that they think will solve their pain. If you observe them, however, you will see the messy reality of their workflow and the true underlying needs. As the apocryphal Henry Ford quote suggests, if he had asked people what they wanted, they would have asked for faster horses. Design Thinking requires you to look past the "horse" to see the desire for speed and efficiency.

### The Theory of Inquiry

The theoretical core of how we navigate this uncertainty comes from the concept of "Inquiry." The traditional "Feynman Algorithm" — write down the problem, think hard, write down the solution — fails spectacularly when applied to Wicked Problems. Instead, we look to John Dewey’s "Theory of Inquiry" and Donald Schön’s concept of the "Reflective Practitioner." Schön distinguishes between "reflection-in-action," which is the act of thinking while doing — tweaking the code as you write it because it just feels wrong — and "reflection-on-action," which is the analysis that happens after the fact.

This leads us to the concept of "doing for the sake of knowing." Consider how you solve a mechanical puzzle like a Rubik’s Cube. You rarely solve it by placing it on a table, staring at it, and calculating the algorithmic path in your head. You solve it by picking it up and twisting it. The physical action generates information. You try a move, observe the result, and that result informs your next move. In Design Thinking, the process of creating a prototype is not just about implementing a solution; it is a tool for understanding the problem itself. Every prototype is a hypothesis, and every failure is a data point.

This chaotic journey is famously visualized as the "Design Squiggle" by Damien Newman. The process begins on the left with a tangled, chaotic knot of lines, representing the "Research & Synthesis" phase where everything is noisy and uncertain. As you progress to the middle, the lines begin to straighten out as concepts form and patterns emerge. Finally, on the right, you achieve a single, straight line representing the final design and focused clarity. Unlike the rigid Waterfall model, Design Thinking is an open process where analysis, synthesis, and evaluation happen simultaneously. When you sketch a button, you are analyzing the layout, synthesizing a solution, and evaluating its aesthetic all at the same moment.

### Heuristics for Interactive Systems

With the theory established, we must turn to the hard rules — the "Heuristics" — that govern good interactive systems. These are the operational commandments for creating sanity in software.

The first and most critical heuristic is **Communication and Feedback**. The system must constantly talk to the user. This happens passively through "Affordance," where elements visually describe how they should be used, but also actively through feedback loops. If a user clicks something, the system must respond immediately. For short actions, a change in cursor or button state suffices; for longer actions, a progress bar is mandatory. The rule is absolute: never leave the user guessing "Did it work?"

This ties directly into the concept of **Affordance**, a term borrowed from industrial design. A physical door handle "affords" pulling, while a flat plate "affords" pushing. If you have to put a sign on a door saying "PUSH," the design has failed. In the digital realm, we simulate this. We use shadows and gradients to make buttons look raised, inviting a push. We use ridges on scrollbars to metaphorically suggest the grip of a bottle cap. If a non-clickable element looks like a button, you are effectively lying to your user.

**Structure and Consistency** form the backbone of a navigable system. We call this Information Architecture. Similar things must look similar, and different things must look different. The user should always be able to answer three questions: Where am I? Where did I come from? How do I get back? This requires internal consistency — if "Save" is a blue button on one page, it cannot be a red link on another — and external consistency, which means adhering to platform standards. Do not reinvent the wheel; if `Ctrl+C` means copy in every other application, making it "Clear All" in yours is an act of hostility.

We must also respect the limits of **Human Perception**. Humans are excellent at Recognition — seeing an icon and knowing what it is — but terrible at Recall — remembering a specific command name from memory. Good design relies on recognition, minimizing the cognitive load required to use the tool. This extends to readability, ensuring font sizes, contrast ratios, and color choices accommodate human biology.

Efficiency is governed by the **80\:20 Rule**. You should identify the 20% of features that users engage with 80% of the time and make those immediate, one-click actions. The remaining 80% of features, which are rarely used, should be tucked away in menus or secondary screens. The goal is to provide accelerators for power users while maintaining clear, uncluttered paths for beginners.

Finally, we must prioritize **Clarity and Control**. Every action needs a defined beginning and a clear confirmation of completion. But more importantly, we must prioritize "Undo" over error messages. An error message effectively tells the user, "You are stupid, stop." An Undo function tells the user, "Don't worry, explore, I have your back." By allowing users to reverse their actions, you give them the confidence to explore the system without fear of breaking it. If you must show an error, speak human language, not error codes. But the ultimate goal is to design a system where the error is impossible to commit in the first place.

### The Product Experience

Beyond the functional mechanics, we must address the "Product Experience," or the feel of the system. This is not just visual aesthetics; it is **Interaction Aesthetics**. Paul Hekkert defines this as the "gratification of senses," but in software, we often refer to it as "Pliability." Pliability describes the user's sense of shaping a malleable material. When you drag a file on a smartphone and the icons shift out of the way fluidly, that is pliability. It feels responsive, tight, and alive. This creates an emotional bond. If a tool makes a user feel smart and capable, they will love it. If it makes them feel stupid by throwing constant errors, they will hate it. The goal is to achieve a sense of joy and excitement — a feeling that the system is not just a tool, but an extension of the user's own intent.

---

_Coming Up in Part 4: The Practitioner’s Toolkit — Why you need to sketch (not prototype) 2,500 times, the difference between "Opportunity Seeking" and "Decision Making," and why your first idea is probably your worst._

## Part 4: The Practitioner’s Toolkit

We have spent a lot of time on the philosophy of the "Wicked Problem" and the history of HCI. Now we need to look at the actual mechanics of doing the work. If Design Thinking is an "Open Process" where analysis, synthesis, and evaluation happen simultaneously, how do you actually structure your day? How do you move from a vague sense of a problem to a shipped product without falling into the trap of building the wrong thing?

The first hurdle you will face is your own brain. In design theory, we talk about the concept of the **Primary Generator**. This is the technical term for that first, lightning-bolt idea you get when you hear a problem description. You know the feeling: a client describes a need, and immediately, a solution pops into your head. It feels like intuition, or experience, or even genius. But in the context of Wicked Problems, this primary generator is dangerous. These early ideas act as blinders, creating a tunnel vision that forces you toward a specific solution before you have actually understood the problem.

To truly embrace an open design process, you have to learn to "kill your darlings." A great example of this comes from a group of students who created the game _And Yet It Moves_. The initial concept relied on a specific mechanic where the player would "fling" the mouse to rotate the world 90 degrees. It was their primary generator, the core hook they were excited about. But during prototyping, it became clear that this mechanic turned the game into a test of dexterity rather than a puzzle platformer. It was only by discarding their original "genius" idea that they were able to uncover the better game underneath — a game that eventually launched on the Nintendo Wii. You must actively seek uncertainty at the beginning of the process. You have to climb the hill of ambiguity rather than rushing for the first comfortable solution.

This approach is exemplified by Graham Whiteley’s work on the "Sheffield Arm." Whiteley started with a whimsical goal: he wanted to build a better mechanical arm for an animatronic drinking robot in his favorite pub. His first thought was to use existing medical prosthetics, but he quickly found them totally unsuitable. Instead of trying to force the existing solution to fit, he embarked on a process of **Research through Design**. He didn't write a specification; he built sketches. He built prototype after prototype, creating physical objects that he could put into the hands of surgeons and osteopaths.

What happened next is key: the experts didn't just look at diagrams; they manipulated the physical prototypes with their hands, using their tacit, embodied knowledge to give feedback like "this joint is too stiff" or "this needs more resistance." By "moving all horses at once" — building, testing, and analyzing simultaneously — Whiteley ended up creating a breakthrough in bionics that went far beyond a pub robot. He didn't solve the problem by defining it first; he defined the problem by trying to solve it.

### The Blur of Analysis and Synthesis

In a traditional engineering workflow, you might have a phase for requirements gathering followed by a phase for design. In Design Thinking, these blur together. We use tools like **Personas** and **Scenarios**, but not as bureaucratic paperwork. A Persona is not just a demographic checklist; it is a tool to keep the user present in the room. Our brains are wired to remember people, not lists of requirements. If you can say "This feature will confuse Martha," you are accessing a much faster, more empathetic mode of evaluation than if you reference "User Requirement 4.2."

Similarly, Scenarios are narratives. They are stories about people using your system to achieve a goal. Writing a scenario forces you to deal with the timeline of interaction, the context, and the inevitable "edge cases" where things go wrong. It creates a context where non-functional requirements become visible. You aren't just listing features; you are simulating the reality of the usage.

### The Art of Sketching

The most potent tool for this simultaneous analysis and synthesis is **Sketching**. Do not confuse this with drawing art. In design, a sketch is a tool for thinking. Bryan Lawson calls it the "thinking pen." Designers often say they cannot "speak" or think about a problem without a pencil in hand. The sketch is a conversation between the designer and the problem. You draw a line, and that line asks a question. You draw another, and it answers it.

Crucially, sketching is distinct from prototyping. The difference lies in the intent. You sketch to explore; you prototype to decide. A sketch is cheap, fast, and disposable. It is low-fidelity by design. The "roughness" of a sketch is a feature, not a bug, because it invites interpretation. If you show someone a polished, pixel-perfect mockup, they will critique the font choice. If you show them a rough pencil sketch, they will critique the concept.

Consider the case of the software _ProfCast_. The creators generated over **2,500 sketches** before they settled on the final design. That number seems absurd until you realize that sketching is fast. It is a volume game. You sketch to get the bad ideas out of your system, to explore the impossible, and to find the unexpected connections. If you are precious about your sketches, you are doing it wrong. You should be willing to throw them away instantly. This is where modern "Vibe Coding" — using AI to generate throwaway interactive snippets — can actually be useful. If you treat the code as disposable as a napkin sketch, it becomes a powerful tool for inquiry. But if you start trying to ship that code, you have moved from sketching to bad engineering.

Sketching is not limited to paper. One of the most famous sketches in tech history was a block of wood. Jeff Hawkins, the creator of the Palm Pilot, walked around for weeks carrying a piece of wood cut to the size of his proposed device. He would pull it out of his pocket to "check his schedule." He would tap on the wood with a "stylus" (a chopstick). He used this physical roleplay to understand the form factor. He discovered that people interacted with the device differently depending on whether he handed it to them vertically or horizontally. He learned about the ergonomics and the social acceptability of the device before writing a single line of code or soldering a single circuit. This is the essence of a sketch: it costs nothing, but it generates massive insight.

We can also do "Interaction Sketches" using video. In one example, designers wanted to test a concept for smart toy cars. Instead of building complex robotics, they simply filmed standard toy cars being moved by magnets under a table. This "Wizard of Oz" approach allowed them to test the _experience_ of the interaction without solving the engineering challenges first. They could ask "Is this fun?" before asking "How do we build it?"

### Mental Models and the Delete Button

Finally, all of this sketching and modeling is aimed at one goal: aligning the system with the user’s **Mental Model**. A mental model is the internal theory a user builds about how your system works. These models are often based on superstition and guesswork rather than facts.

A classic example is the "Clear" button on a calculator. Many people press the "C" button multiple times before starting a new calculation. Why? Because on some older calculators, pressing "C" once only cleared the last entry, while pressing it twice cleared the whole memory. Users formed a defensive mental model: "Pressing it many times is safe." Even though modern calculators rarely work this way, the behavior persists.

Your job as a designer is to create a system that helps the user build a correct mental model. You do this through consistency, clear feedback, and logical grouping (Grids). If your design is erratic, the user will form a superstitious, defensive model. If your design is consistent and transparent, the user will form a confident, robust model. You are not just building a product; you are teaching the user how to understand it.

---

_Coming Up in Part 5: The traps that ruin everything — Featuritis, Solutionism, and the dark world of Deceptive Patterns._

## Part 5: The Traps of Modern Design

We have covered the theory, the history, and the toolkit. Now we have to talk about how it all goes wrong. Even with the best intentions and a stack of Personas, projects frequently derail. They usually fall into one of three specific traps: Featuritis, Solutionism, or the ethical void of Dark Patterns. Understanding these traps is the only way to avoid building software that people hate.

### The Trap of Featuritis

The most common disease in software development is Featuritis, also known as Feature Creep or Software Bloat. It is the uncontrolled growth of functionality. We often assume that adding a feature adds linear value to a product, but the complexity of the user interface tends to grow quadratically with the number of functions. Remember the "Bulk Rename Utility" we discussed in Part 1? That monstrous dialog box didn't happen because the developers were malicious; it happened because they likely started with a simple tool and kept adding "just one more thing" until the interface collapsed under its own weight.

There is a perverse incentive structure driving this. Media outlets compare products using feature tables, forcing companies to tick boxes to remain competitive. Marketing departments demand new bullet points for the next release. But the most dangerous pressure comes from the users themselves. Peter Sikking, in a conversation on the Chaosradio podcast, compared users to children in a candy store: they will always say "yes" to more features, even if the sugar rush eventually gives them a stomach ache. For a developer, adding a feature is the path of least resistance. It is quantifiable work. Removing a feature, or spending weeks refining an existing one to be simpler, is much harder to justify to a project manager. It often looks like a step backward, even if it is the only way to save the product.

This leads to what Kathy Sierra calls the Featuritis Curve. There is a "Happy User Peak" where capability meets usability. Push past that, and the user experience falls off a cliff. The tragedy is that when users encounter bloated software, they rarely blame the software. They say, "I am too stupid for this," or "I am not technical enough." When a user says they are too stupid to use your tool, what they are actually saying is that your tool has become so complex that the cognitive load required to operate it outweighs the value it provides. Sierra suggests that we must stop listening to what users _say_ they want and start listening to the motivation behind their requests. We have to trust ourselves enough to say no.

Consider the cautionary tale of AltaVista. Before Google, AltaVista was a dominant search engine. In an attempt to not "patronize" the user or limit their options, they added everything to the homepage: specialty searches, hierarchical indices, news tickers, and advanced search forms. They offered maximum choice, which resulted in maximum cognitive overload. Google arrived with a single text box and a single button. They understood the principle of Simplicity. As industrial design legend Dieter Rams famously put it, good design is "as little design as possible." It is about omitting the unessential to let the essential speak.

### The Trap of Solutionism

The second trap is Solutionism. This is the fancy term for the "when you have a hammer, everything looks like a nail" problem. It describes the tendency to view every problem as a nail that can be hammered down with the latest technology. We see a problem and immediately assume the solution is an app, a blockchain, or a touchscreen, without asking if that technology is actually appropriate for the context.

This brings us back to the tragedy of the USS John S. McCain. The investigation into the collision revealed that the shift from physical throttles to touchscreens was a primary factor in the disaster. Under normal conditions, a touchscreen is fine. But under the extreme stress of a collision course, the lack of physical **affordance** became fatal. A physical lever tells your hand where it is without you looking at it. A touchscreen demands your visual attention. The feedback from the fleet was unanimous: "Just give us the throttles."

This is a clear case where Design Thinking would have saved lives. If the engineers had focused on the human need (controlling a massive ship under high cognitive load) rather than the technological capability (we can put this on a screen), they would have kept the physical controls. We are seeing a similar correction in the automotive industry right now. After years of burying climate controls in sub-menus on touchscreens, manufacturers like Volkswagen are bringing back physical buttons. They realized that taking your eyes off the road to adjust the temperature is fundamentally bad design, no matter how modern the dashboard looks.

### The Trap of Dark Patterns

If Featuritis is negligence and Solutionism is naivety, then Dark Patterns are malice. These are user interface design patterns that are carefully crafted to trick users into doing things they didn't mean to do. This is often called "Deceptive Design." As a designer, you wield significant power over human behavior, and using that power to manipulate users is an ethical failure.

We see this everywhere in "Cookie Banners." You land on a site, and there is a massive, bright green button that says "Accept All." If you want to reject them, you have to find a tiny, grey, unstyled link that says "Preferences," navigate through three sub-menus, and manually toggle off individual vendors. The design uses color theory and visual hierarchy to exhaust the user into submission. This is not an accident; it is a calculated decision to prioritize data collection over user intent.

Krisztina Szerovay’s "UX Knowledge Base" visually documents these patterns, showing how interfaces use confusing language ("double negatives"), hidden costs, and forced continuity to exploit human psychology. In Europe, many of these patterns are now illegal, but the mindset persists. A good designer must resist the pressure to implement these patterns. If you are tricking your user, you aren't designing; you are scamming.

### The "User" Problem

Finally, we need to address the language we use. Throughout this series, we have used the word "User." But as the old industry joke goes, only two professions refer to their customers as "users": drug dealers and IT professionals. The term is problematic because it implies passivity. A "user" is someone who takes what is given to them. It strips the human of their agency and complexity.

When we view people as "users," we start to treat them like the dog in the famous "IT Crowd" style cartoons — stupid, inept, and needing to be heralded through the process. We create error messages that treat them like children. We assume they read every word of our instructional text (they don't). We assume they care about our database schema (they don't).

Jonathan Nightingale from Mozilla once satirized this attitude by rewriting a browser error message to say: "You have hurt the internet's feelings." It was a joke, but it highlighted how ridiculous our communication often is. We bombard people with technical jargon and meaningless choices because we forget there is a human on the other side of the screen.

We should shift our vocabulary. Some suggest "Actor" or "Stakeholder." Others prefer simply "Human." Whatever word you choose, the goal is to remember that the person on the other end is not a metric to be optimized or a receptacle for your features. They are a person trying to get something done.

### Conclusion

Design Thinking is not a magic wand. It is a rigorous, messy, and difficult process of aligning technology with human needs. It requires you to be humble enough to kill your best ideas, patient enough to sketch two thousand iterations, and brave enough to say "no" to feature creep.

The goal is not to make users fascinated by your technology. As the saying goes, "Users want to be empowered by technology, not awed by it." If you can build a system that makes the human feel powerful, competent, and in control, you have succeeded. If you build a system that makes them feel stupid, no matter how many features it has, you have failed.

---

_This concludes the Design Thinking series. Go forth and design for humans._
