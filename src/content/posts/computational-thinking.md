---
title: Computational Thinking
pubDate: 2025-09-14
---

## Part 1: The Genesis & Philosophy of Computational Thinking

### Beyond the Telescope

In a curriculum dedicated to the "Ways of Thinking in Informatics," the chapter on Computational Thinking often feels like it holds a special, almost holy status. Since Computer Science ostensibly revolves around computers, one might assume that Computational Thinking is simply the core objective of the entire discipline.

Here is the reality check: That assumption is partially false.

Computer Science is only conditionally about computers. The legendary computer scientist Edsger W. Dijkstra is famously attributed with the aphorism: "Computer science is no more about computers than astronomy is about telescopes." While the provenance of this quote is debated—Wikiquote marks it as disputed—the underlying sentiment remains structurally sound. Astronomy involves the development of high-performance instruments, yes, but the goal of the astronomer is not to build a telescope; it is to gain knowledge about the universe _using_ that telescope.

Similarly, Informatics does not have the sole objective of building powerful machines. We certainly have sub-disciplines dedicated to hardware and architecture, but the soul of the field lies elsewhere. Computational Thinking is indeed a core concern, but we must be careful not to elevate it to a mythical "silver bullet" status. It is essential, but it is nuanced. To understand it, we have to look at how we solve problems _with_ these machines, rather than just how the machines work. As Stephen Wolfram (the physicist behind WolframAlpha) once noted, the act of actually programming something inevitably allows one to do more exploration of the concept itself. It is a tool for thought, not just calculation.

### The Revival: Jeannette Wing and the Definition

The modern terminology was effectively resurrected in 2006 by Jeannette Wing. She published a seminal article titled "Computational Thinking" in the _Communications of the ACM_, one of the most influential journals in the field. While the concept had roots stretching back to the mid-20th century, Wing gave it a definition that stuck. She described it as a specific form of problem-solving competence: tackling complex problems through abstraction, algorithmic thinking, and decomposition so that they can be solved by (or with) a computer.

Wing’s definition is precise: It involves the thought processes required to formulate problems and their solutions so that the solutions are represented in a form that can be effectively carried out by an "information processing agent." This is a critical distinction. It implies that this mode of thinking transforms the conduct of every discipline. A professional with the ability to use computation effectively possesses a distinct "edge" over one who cannot. It is not just about writing code; it is about structuring reality in a way that code can manipulate it.

### The True Origin: Ada Lovelace’s Vision

To truly understand the depth of this concept, we have to look much further back than 2006—all the way to the 19th century. Augusta Ada King, Countess of Lovelace (born 1815), provides the first historical evidence of Computational Thinking. At the age of 17, she witnessed a demonstration of a partially finished automatic calculating machine and was immediately captivated. She met its creator, Charles Babbage, and wrote about seeing the "thinking machine" (or so it seemed) raising numbers to the 2nd and 3rd powers and extracting roots of quadratic equations.

Babbage and Lovelace began a collaboration that would define the pre-history of computing. Babbage focused on a machine far more complex than his previous "Difference Engine." He called it the **Analytical Engine**. Today, we can legitimately call this device the first concept of a "general-purpose computer." However, there was a massive gap in understanding between the inventor and the collaborator. Babbage viewed his projects essentially as increasingly complex calculators; his primary goal was to print mathematical tables quickly and precisely to avoid human error.

Ada Lovelace saw something else entirely.

In 1842, Lovelace translated an article by a French engineer who had summarized one of Babbage's lectures. During the translation process, she appended her own thoughts in the form of seven "Translator’s Notes." These notes were three times the length of the original article. They reveal that while Babbage was building a calculator, Lovelace had conceptually invented the computer. She discussed the potential for what we now call "nested loops" and, most importantly, the abstraction of moving from manipulating numbers to manipulating _symbols_.

In these notes, we find the first documented instance of Computational Thinking. Lovelace wrote: "The Analytical Engine has no pretensions whatever to originate any thing. It can do whatever we know how to order it to perform. It can follow analysis; but it has no power of anticipating any analytical relations or truths."

This quote is frequently cited to demonstrate that AI cannot be truly creative, but there is a second, more profound half to her observation. She noted that the engine is likely to exert an "indirect and reciprocal influence on science itself." By distributing and combining truths and formulas so they can be handled by the engine, the nature of scientific subjects is "thrown into new lights, and more profoundly investigated."

Lovelace predicted that the mere act of automating mathematical processes would force scientists to see their own fields differently. This is the essence of Computational Thinking: the tool changes the user’s perception of the problem.

### The 20th Century Pillars: Papert and Wilson

Fast forward to 1980, and we meet Seymour Papert, a pioneer who linked this thinking to education. Papert argued that everyone uses procedures in everyday life—like giving directions to a lost motorist—but these are rarely reflected upon. In a computational environment (like his LOGO programming language), a procedure becomes a distinct "thing" that is named, manipulated, and recognized. Papert famously called **debugging** "the essence of intellectual activity," a perspective that reframes failure not as an error, but as the primary mechanism of learning.

Shortly after, in 1982, physicist Ken Wilson won the Nobel Prize. His contribution was the computational modeling of phase transitions in matter. Wikipedia’s entry on Wilson is telling; it lists his status as a "pioneer in using computers" _before_ his physical discoveries. Peter Denning, writing in 2017, noted that Wilson and his contemporaries used the term "Computational Science" to describe a new paradigm of science. They viewed computation not just as a tool, but as a third pillar of scientific inquiry, standing equal alongside Theory and Experiment.

### The Evolution of the Model: From Two A's to Three

When Jeannette Wing reintroduced Computational Thinking in 2006, and in subsequent talks around 2008, she initially boiled it down to the "Two A's": **Abstraction** and **Automation**.

This formulation aligns with a popular, yet historically flawed, model of rational problem-solving that dates back to the ancient Greeks: First, you understand the problem (Abstraction), and then you solve it (Automation). Henrik Gedenryd, in his dissertation "How Designers Work," deconstructed this idea. He showed that while the "First understand, then solve" model feels intuitively correct, it is empirically false.

This flawed "rational" view is perfectly encapsulated in the so-called **Feynman Algorithm**. Named after Nobel laureate Richard Feynman, the algorithm goes like this:

1.  Write down the problem.
2.  Think hard.
3.  Write down the solution.

This is, of course, a joke. It originated from Murray Gell-Mann, Feynman’s colleague, who described Feynman’s method this way to express admiration for his genius. The problem is that people took it seriously. It became a stand-in for the "genius view" of problem-solving. But if you asked Feynman himself, his process was nothing like that. It was iterative, parallel, opportunistic, and messy. He didn't "think then solve"; he used "new tricks" to change how he thought about the problem. As we discussed in Scientific Thinking regarding "cognitive artifacts," externalizing knowledge changes what we are capable of thinking.

Jeannette Wing’s "Two A's" (Abstraction -> Automation) sounded suspiciously like the Feynman Algorithm. It suggested a linear flow: model the world, then automate it. Critics pointed out that this ignored the iterative nature of real engineering and science.

Consequently, Wing updated her model. The "Two A's" became the "Three A's": **Abstraction**, **Automation**, and **Analysis**.

Crucially, she placed these three elements into a cycle.

1.  **Abstraction:** We model the problem to get a formulation we can automate.
2.  **Automation:** We let the "information processing agent" execute the solution.
3.  **Analysis:** We examine the results of that execution.

This analysis then feeds back into the Abstraction phase. The insights gained from the automation allow us to refine the model, fix the bugs, and improve the logic. We iterate. This cyclic view acknowledges that we often don't truly understand a problem until we have tried (and perhaps failed) to simulate or solve it computationally. This loop—Abstraction, Automation, Analysis—is the modern, robust definition of Computational Thinking.

---

_Next, we will look at how this thinking style triggered five distinct revolutions in science, and why FedEx might be faster than the internet._

## Part 2: The Five Revolutions & The New Science

### The Landscape of Change

If we accept that Computational Thinking isn't just "using a computer" but a fundamental shift in how we process reality, we have to look at the scale of that shift. It’s not just about doing math faster; it’s about changing what "doing math" actually means.

Matti Tedre, a Finnish computer scientist, delivered a lecture in 2019 that captured this perfectly. He postulated **five computing revolutions in science**. This framework is arguably the most comprehensive way to understand the impact of CT. It moves beyond the hardware and looks at the philosophical and sociological shockwaves.

#### 1. The Technological Revolution

This is the most obvious layer. It’s about **speed**. We take known processes and accelerate them by orders of magnitude. Think of encryption or decryption. Historically, a "computer" was a human being who performed calculations. We moved from Human Computing to Machine Computing. This is essentially the "upgrading" of mathematics. However, this speed brings a side effect: We now have mathematical proofs generated by computers that are so complex that no single human can verify them manually. We trust the machine because the math is "known," but the scale is alien.

#### 2. The Methodological Revolution

Here, we start doing things that were previously impossible, not just slow. The classic example is the **Monte Carlo method**. This is a class of algorithms that rely on repeated random sampling to obtain numerical results. Before computers, you couldn't reasonably "simulate" randomness a million times to find a probability curve. Now, it's a standard method. Computational Science has emerged as a distinct methodology, sitting right next to the traditional scientific pillars of Theory and Experiment.

#### 3. The Epistemological Revolution

This is where it gets heavy. **Epistemology** is the branch of philosophy concerned with knowledge—"What can we know?"
Tedre argues that computation gives us a new way to interpret the world. Simulation becomes a valid path to knowledge. Previously, we observed the world or theorized about it. Now, we simulate it. If a simulation accurately predicts a phenomenon, we accept the simulation's rules as a form of truth. This is a **Representational Shift**, equivalent in human history to the invention of writing, the printing press, or the moving image. Code is now a valid way to represent knowledge.

#### 4. The Ontological Revolution

**Ontology** asks, "What exists?" Computational Thinking introduces new concepts and entities into our reality. We now treat "information processes" as fundamental building blocks of the universe. We explain biological phenomena (like DNA) as "code." We talk about the "state" of a system. These are computational metaphors that have become the actual descriptions of reality.

#### 5. The Sociotechnical Revolution

Finally, science itself has changed as a social activity. The lone genius is being replaced by massive, distributed networks. Tedre points to a physics paper with **5,154 authors**. The paper itself is 33 pages long; only the first nine pages describe the research. The rest is the list of authors. This scale of collaboration is only possible because of the communication and data-handling infrastructure provided by computing.

### Computational Thinking in the Wild

To ground these high-level revolutions, let's look at four concrete examples of how this thinking manifests in the real world.

#### Example 1: The Reset (The Engineer, The Physicist, and The Programmer)

There is an old joke that Jeannette Wing cites as a legitimate example of CT.
An engineer, a physicist, and a programmer are driving in a car. Suddenly, the car stalls and stops.
The Engineer says: "It must be the fuel injectors. The gas mixture isn't right."
The Physicist says: "No, clearly the cylinder head gasket has failed due to thermal expansion."
The Programmer looks at them and says: "I suggest we all get out, wait a few seconds, get back in, and then it should work."

Wing argues this isn't just a gag. It represents a specific computational strategy: **The Reboot**. A person thinking computationally understands that a complex system has an "internal state." If that state gets corrupted, you don't necessarily need to fix the physical component immediately; you need to reset the system to a "known, fresh state." It’s a valid, abstract solution to a physical problem.

#### Example 2: Shotgun Sequencing

This is the "poster child" for Computational Thinking in biology.
Shotgun sequencing is a method used for sequencing genomes. DNA strands are massive. You cannot just read them start-to-finish. In this method, the genome is cloned and then violently "shredded" into tiny, random fragments (about 1000 base pairs long). These small pieces are individually sequenced.
Then, the magic happens. A computer takes these millions of random, overlapping puzzle pieces and looks for patterns where the ends match. It reassembles the full sequence purely through pattern recognition algorithms.
This approach makes the impossible possible. It is only "thinkable" if you already know that a computer can handle the reassembly. If you didn't have CT, you wouldn't even attempt to shred the DNA, because you’d have no way to put it back together.

#### Example 3: The Earth-Sized Telescope (and FedEx)

When researchers photographed a Black Hole for the first time, they didn't use one telescope. They linked radio telescopes in Arizona, Spain, Mexico, Antarctica, and other locations to form a "virtual instrument" the size of the Earth (The Event Horizon Telescope).
Here is the data problem: The telescopes collected **5 petabytes** of data. That is roughly 5,000 years of MP3 music.
They needed to get this data to a central supercomputer to merge it. How do you move 5PB? The internet is too fast? No.
The researchers said: "What we actually do is, we take our hard drives and we FedEx them from place to place. This is much faster than any cable that you can ever find."
A 500kg crate of hard drives moving via airplane represents a data transfer rate of roughly 14GB/sec. This is a classic computational trade-off: Bandwidth vs. Latency. The "Ping" is terrible (it takes 24 hours to arrive), but the bandwidth is unbeatable. Understanding that physical logistics is just another form of data bus is pure Computational Thinking.

#### Example 4: The Monty Hall Simulation

Finally, we have the Monty Hall problem. You have three boxes (or doors). One has a prize (a pearl), two have nothing (peas). You pick a box. The host opens one of the _other_ boxes to reveal a pea. He asks: "Do you want to switch your guess to the remaining closed box?"

Intuitively, most people say it doesn't matter. It feels like a 50/50 split.
But if you write a simple simulation—a script that runs this scenario 10,000 times—you see the truth immediately. Switching wins 2/3 of the time. The simulation forces you to accept a mathematical reality that your intuition rejects.
However, as we will discuss later, the goal isn't just to trust the simulation. The ultimate goal is "Code as a way of understanding." By writing the code, you can actually see the logic: The variable determining which box the host opens becomes irrelevant to your winning chances if you stay, but crucial if you switch. The code reveals the structure of the logic itself.

### The New Scientist: The Research Software Engineer

This shift has created a new job description: The **Research Software Engineer**.
These are people who bridge the gap. They are scientists who think in code. The archetype for this is **Tim Berners-Lee**. On paper, he was a physicist at CERN. In reality, he was a computer scientist. He didn't invent the World Wide Web just for fun; he invented it to solve a specific information exchange problem between researchers. He applied computational concepts (hypertext, client-server architecture) to a sociological problem (scientific collaboration).

Jeannette Wing noted that this transformation is happening everywhere. Computational biology changes how biologists think. Computational game theory changes how economists think. It is not just a tool; it is a new language for every discipline.

---

_Next, we dive into the history of the "Act" of programming itself—how we went from "Writing" poetry for machines to the industrial "Engineering" of the NATO conference, and why the Waterfall model was doomed from the start._

## Part 3: A History of "The Act": From Writing to Engineering

### The Great Gap & The War Machines

After the visionary work of Charles Babbage and Ada Lovelace, the history of computing hit a pause button. Babbage was a brilliant inventor but a terrible communicator, and Lovelace died tragically young at 34, likely from cancer. Their ideas—the "Analytical Engine" and the first "program"—were largely lost to time, misunderstood by their Victorian contemporaries who only saw fancy calculators. It took nearly a century for the train to leave the station again, and unfortunately, it was war that fueled the engine.

The catalyst was the **Enigma**, a German machine used during World War II to encrypt communications. While not a computer in the modern sense (it was a highly specialized electromechanical cipher device), the Allied effort to break it birthed the modern computing era. This happened at **Bletchley Park**, where a team of British mathematicians and "computers" (the job title for humans who did calculations) worked to decrypt messages.

The "Bomb" (or Bombe) was the machine designed to crack Enigma. It wasn't a general-purpose computer; it was a beast built for one specific task: finding the daily settings of the Enigma machines. This project was critical—it is estimated that the work at Bletchley Park shortened the war by two to four years.

#### The Hidden Figures of Bletchley

The most famous figure here is **Alan Turing**, the father of theoretical computer science. He formalized the concept of the "General Purpose Computer" (the Turing Machine) and later laid the groundwork for AI with the Turing Test. But the history books often gloss over his team. **Joan Clarke** was a pivotal figure who worked alongside Turing on the Bomb. Because the job of "crypto-analyst" wasn't technically open to women, she was hired as a "Linguist," despite speaking no foreign languages. Her pay and rank reflected this bureaucratic fiction, not her actual contributions.

This is a recurring theme we need to address: The history of informatics is often told through a male lens, erasing the women who were foundational to the field. Just as we saw in _Scientific Thinking_ with the Viking warrior leader (who turned out to be a woman upon modern DNA analysis), computing history is full of "forgotten" women. Turing himself was later persecuted for his homosexuality, driven to suicide by state-mandated hormone "therapy"—a tragedy that highlights how society treated the architects of its own salvation.

### ENIAC: The First "Real" Computer

The shift from specialized machines like the Bomb to true "General Purpose Computers" happened with the **ENIAC** (Electronic Numerical Integrator and Computer). Commissioned for calculating artillery firing tables, it ended up being a programmable beast that could solve a wide array of problems. In the genealogy of modern computing, ENIAC is the root node. Everything we use today traces back to it.

But who programmed it?

The hardware was built by men, but the **ENIAC Six**—the first professional programming team in history—were women. In 1944, there were nearly 50 women working on the project, but six of them became the core operators. At the time, they were often dismissed as "refrigerator ladies" (models posing with appliances), but in reality, they were inventing the discipline of software engineering from scratch. They didn't have a manual. They had wiring diagrams.

### Phase 1: Programming as "Writing"

To understand the mindset of this era (1940s-1950s), you have to realize that **programming languages didn't exist**. There was no Python, no C, not even Assembly.

Programming the ENIAC meant physically connecting cables and setting switches. It was "operating at the open heart of the patient." The machine was completely exposed. To "program," you had to describe a narrative of what the electricity should do. The programmers wrote this narrative down as text—prose descriptions of the logic—and then translated that text into physical connections.

This era defined programming as **"Writing."**
Code was seen as a literary form, a story told to the machine. This philosophy persisted even as early languages emerged. Donald Knuth’s magnum opus, _The Art of Computer Programming_, enshrines this view: Code is a form of art, meant to be beautiful and elegant.

However, this "artistic" approach has a fatal flaw. It works great for calculating Bernoulli numbers or polynomials (linear mathematical tasks). It fails catastrophically when you introduce complex branching logic. If your "story" jumps around too much, it becomes unreadable. This led to the famous edict by Edsger Dijkstra in 1968: **"Go To Statement Considered Harmful."** He argued that using `GOTO` commands (which jump the program flow to a different line) creates "spaghetti code" that is impossible to maintain. The "Writing" metaphor was hitting a wall.

### Phase 2: The Software Crisis

By the 1960s, computers had evolved from room-sized calculators to mainframes like the **IBM 360**. These machines were powerful, and they were everywhere—banks, airlines, governments.

Suddenly, the industry faced a terrifying reality: **Software was becoming more expensive than hardware.**
The programs required to run these mainframes were so complex that a single "artist" couldn't write them. They couldn't even be fully mathematically described or tested. Projects ran over budget, missed deadlines, and were full of bugs.

Dijkstra (the "first nerd," who started counting at zero) described the crisis in 1972: "As long as there were no machines, programming was no problem at all; when we had a few weak computers, programming became a mild problem, and now that we have gigantic computers, programming has become an equally gigantic problem."

### Phase 3: The Pivot to "Engineering"

The industry needed a fix. In 1968, the NATO Science Committee organized a conference in Garmisch, Germany. The goal was to solve the software crisis.

Their solution was a fundamental shift in identity. They decided that software development should no longer be an art or a craft. It should be an **Engineering Discipline**.

This was a massive philosophical pivot. They wanted to industrialize code. The idea was to build software like we build bridges or cars:

1.  **Standardization:** Use interchangeable parts.
2.  **Hierarchy:** Managers oversee architects, who oversee coders.
3.  **Process:** Follow a strict, linear sequence of steps.

This decision birthed **Software Engineering** as a term and a profession. It rejected the idea of software as architecture (a design discipline) and embraced the factory model.

#### The Waterfall Model

The embodiment of this engineering mindset is the **Waterfall Model**.
It visualizes development as a cascade:

- Requirements Analysis → Design → Implementation → Verification → Maintenance.

The theory was seductive: You finish one phase completely, document it perfectly, and "hand it off" to the next team. It allows for centralization and clear management. It looks great on a Gantt chart.

There was just one problem: **It doesn't work.**

Winston Royce, the man often credited with inventing the Waterfall model in his 1970 paper, actually wrote the paper to say it was a bad idea! He included a diagram of the linear process and explicitly stated: "I believe in this concept, but the implementation described above is risky and invites failure."

He argued that software is inherently iterative. You discover new things about the problem _while_ you are coding the solution. A strict linear process forbids this learning. If you find a design flaw during implementation in a Waterfall model, it’s too late—you’ve already signed off on the Design phase.

### The Mythical Man-Month

The failure of this industrial "Construction" mindset was immortalized by Frederick Brooks, who managed the development of the OS/360 (the operating system for the IBM 360). It was the largest software project in history at the time, and it was a disaster of delays and bugs.

Brooks wrote _The Mythical Man-Month_, a book that remains the bible of software project management. His central law is devastating to the factory model:
**"Adding manpower to a late software project makes it later."**

Why? Because software isn't digging a ditch. If you have a ditch to dig, adding more people helps. In software, adding people increases the **communication overhead** quadratically. New people need to be trained, and they interrupt the work of the experienced people.
Brooks also described "Software Entropy": As time passes, a system becomes less and less well-ordered. Eventually, fixing bugs creates more bugs. The system wears out, not physically, but logically.

This realization—that you cannot "construct" software like a building—led us to the modern era. We had to abandon the idea of "Building" and embrace a new metaphor: "Growing."

---

_Next, we explore "Code as a Garden," why your codebase is likely a sick patient, and the cognitive science of how we actually read and understand this strange artificial language._

## Part 4: Growing Code, Decay, and The Cognitive Shift

### From Construction to Cultivation

If the "Waterfall" model was an attempt to treat software like a construction site—rigid, planned, and architectural—the modern era is defined by a realization that this model is fundamentally broken. We have moved from the metaphor of **Building** to the metaphor of **Growing**.

Software development is not about stacking bricks according to a blueprint that was finalized months ago. It is an organic process. The "Standish Group Chaos Report" (2015), which analyzed 50,000 projects, made this brutally clear: Linear processes fail. Iterative processes succeed.

This shift changes the definition of "Programming" again. It is no longer about "Writing" a story or "Constructing" a bridge. It is about **Gardening**. You plant a seed (a prototype), you water it (add features), you prune it (refactor), and sometimes you have to rip out weeds (debugging). As you move pieces on the board—Concept, Design, Model, Code—everything evolves simultaneously. You don't know exactly what the final tree looks like until it has grown.

### The Codebase as an Organism

In 2014, Kevin Simler published an influential essay titled "A Codebase is an Organism." He argued that the engineering metaphors we use (architecture, foundation, build) are actively harmful because they imply stability.
"The computer is a machine," Simler wrote, "but a codebase is an organism."

This biological view exposes the dual forces at play: **Growth** and **Decay**.
Just like a living thing, code that isn't actively maintained begins to rot. We call this "Bit Rot" or "Software Entropy," but the biological metaphor is more accurate: it's a sick patient. The role of the programmer shifts from "Architect" to "Nurse." We spend much of our time diagnosing symptoms, applying patches, and trying to keep the patient alive as it grows more complex and unwieldy.

### The Reality Check: "It Isn't Done Yet"

Despite our fancy new metaphors, the actual state of software engineering is arguably a disaster. If you browse communities like Reddit’s `/r/ProgrammerHumor`, you’ll see the collective trauma of the industry. We joke about "spaghetti code," "technical debt," and copying from Stack Overflow because deep down, we know our processes are fragile.

**Alan Kay**, a Turing Award winner and one of the fathers of object-oriented programming, offers a sobering critique. He argues that the computer revolution hasn't actually happened yet. We are still in the Stone Age.
Kay says: "The worst thing we could ever do is to pretend to the students that we know what [computer science] is... We should teach the students... that it isn’t done yet. It’s not even close to done."

Kay points out that we build massive systems (skyscrapers) using the methods suitable for small scripts (log cabins). We stack log cabins on top of each other and hope they don't collapse.
A prime example of this fragility is **NPM** (Node Package Manager). It is the largest software registry in the world, yet the average package depends on **683 other packages**.
This creates a "Dependency Hell" where security is impossible to guarantee.

- **Case in point:** The `ua-parser-js` library. It’s a tiny utility used by millions. In 2021, a malicious actor hijacked it and injected malware. Instantly, millions of systems worldwide were compromised.
- **The sobering stat:** For every 100 lines of code, there is likely an undiscovered bug. When you have millions of lines of dependencies you didn't write, the math is terrifying.

### The Cognitive Science of Coding

So, if the systems are complex and organic, how do humans actually understand them? This brings us to the cognitive science of programming, specifically the work of Australian researcher **Raymond Lister**.

Lister studies what happens in our brains when we read code. He identified a critical skill that is often ignored in education: **Code Tracing**.

#### The Three Stages of Understanding

Lister argues that programmers move through three cognitive stages:

1.  **Pre-Tracing:** The novice stage. You look at code and guess what it does based on variable names or comments, but you cannot mentally execute the logic. You are essentially "guessing."
2.  **Tracing:** You can manually simulate the computer in your head. You can take a piece of paper, track the variables, line by line, and calculate the output. This is the mechanical understanding of _how_ it works.
3.  **Post-Tracing:** This is expert-level. You look at a block of code and you don't need to run it line-by-line. You instantly recognize the _pattern_. You understand the _intent_ and the _function_ without doing the mental math.

#### The "Chunking" Phenomenon

This transition to Post-Tracing relies on **Chunking**.
It’s the same process as learning to read. When you learn a new script (like Cyrillic), you focus on the lines (curves vs. straights). Then you see letters. Then you see words. Eventually, you read whole sentences without looking at the letters.
In coding, a novice sees: `int i = 0; while (i < n) { ... i++ }`.
An expert just sees: "Loop n times."
This chunking allows experts to reason about abstract problems because their short-term memory isn't clogged with syntax details.

#### The "Variable Swap" Experiment

Lister demonstrated this with a simple experiment. Consider this logic (represented here in pseudo-code):

1.  Compare `y1` and `y2`. Put the smaller value in `y1` and the larger in `y2`.
2.  Compare `y2` and `y3`. Put the smaller value in `y2` and the larger in `y3`.
3.  Compare `y1` and `y2` again. Put the smaller in `y1` and the larger in `y2`.

**The Question:** What is the relationship between `y1`, `y2`, and `y3` at the end?

- **The Tracer** (Stage 2) will take specific numbers (e.g., 5, 2, 8), run them through, and say "It worked for these numbers." But they might miss the general rule.
- **The Post-Tracer** (Stage 3) looks at the structure and realizes: "This is a bubble sort network. It sorts the three variables from smallest to largest."

Lister found that students who could trace perfectly on paper often failed to answer the "big picture" question because they were stuck in the details. They couldn't see the forest for the trees.

### Code as a New Way of Understanding

This brings us back to the ultimate point of Computational Thinking.
Code is not just a way to tell a computer what to do. **Code is a way of understanding the world.**

When you reach the "Post-Tracing" level, code becomes a language for reasoning.
Recall the **Monty Hall** simulation from Part 2.
If you look at the code for that simulation, there is usually a line that defines which door the host opens:
`host_opens = a door that is NOT the player's pick AND NOT the prize door.`
Once you write that line, you realize something profound: **The host's choice is constrained.** The variable `host_opens` adds _information_ to the system because it cannot be random.
You don't even need to run the simulation anymore. Just _writing_ the code forces you to see the logic structure that makes switching the winning strategy.

This is the **Epistemological Revolution**. Just as we use calculus to talk about rates of change, we use code to talk about processes, states, and complex systems. As physicist Niels Bohr said, "Science is not to tell us about the universe, but to tell us how to talk about the universe."
Code is our new way of talking.

---

_Next, in the final part, we will demystify the "Algorithm"—separating the media's "Dark Side" fear-mongering from the mathematical "Light Side"—and break down the 5 Principles of Algorithmic Thinking._

## Part 5: Algorithmic Thinking: The Light, The Dark, and The Logic

### The Definition: What is an Algorithm?

Before we can master the five principles of algorithmic thinking, we need to agree on what an "algorithm" actually is. The term itself is ancient, deriving from the name of the 9th-century Persian scholar **Al-Chwarizmi** (Latinized as _Algorismi_), the same mind who gave us the term "Algebra."

While Wikipedia offers a functional definition, we need something more robust for computer science. An algorithm isn't just "code." A recipe for lasagna is an algorithm. A protocol for landing a plane is an algorithm. To qualify as a true algorithm in our context, a process must satisfy four strict criteria:

1.  **Unambiguous Action:** It must be a clear prescription for action. There is no room for interpretation. "Stir until it tastes good" is not an algorithm; "Stir for 30 seconds" is.
2.  **Finite Steps:** It must consist of a finite number of well-defined individual steps. It cannot run forever; it must eventually conclude.
3.  **Input/Output:** It must take a clear input (e.g., two numbers) and transform it into a clear output (e.g., the product of those numbers).
4.  **Substrate Independence:** Crucially, an algorithm works with or without a computer. You must be able to execute it with a pen and paper. If it requires a specific piece of silicon to exist, it’s an implementation, not an algorithm.

This distinction is vital: **Algorithms are abstract; Programs are concrete.**
An algorithm is the pure logic; a program is that logic frozen into a specific language (like Python or C) to run on specific hardware.

### The Power of Scale: Linear vs. Binary Search

To see why algorithmic thinking matters, let's look at a classic problem: Searching for a specific CD in a collection that is sorted alphabetically by band name.

**Method A: The Linear Search**
You start at the left end of the shelf. You look at the first CD. Is it the one you want? No. You move to the next. You repeat this until you find it.

- **The Math:** If you double the number of CDs, the time it takes to find your target also doubles (on average). The effort grows **linearly** with the dataset size.

**Method B: The Binary Search**
You go straight to the middle of the shelf. You look at the CD. Is the band name "Zappa"? You are looking for "Beatles." "Beatles" comes before "Zappa."
You now know, with absolute certainty, that the CD is in the _left_ half of the shelf. You can ignore the entire right half. You then go to the middle of the left half and repeat the process.

- **The Math:** Every time you make a check, you eliminate 50% of the remaining possibilities. If you double the number of CDs, you only need to add **one single extra step** to the search process. The effort grows **logarithmically**.

This difference is the "Scalability" principle in action. For 10 items, the difference is negligible. For 10 billion items, Linear Search is impossible, while Binary Search is instant.

### The Devil is in the Details

However, understanding the _concept_ of Binary Search is easy. Implementing it is a nightmare.
Because algorithms must be "unambiguous" and handle all edge cases, humans are terrible at writing them correctly.

In 1983, researcher R. Lesuisse conducted a study on Binary Search. He examined 20 implementations of the algorithm found in published educational articles.
**The result:** Only 5 out of 20 were correct.
15 of them contained subtle bugs—usually "off-by-one" errors (e.g., excluding the middle item incorrectly) or failing to handle empty lists. This proves that high-level conceptual understanding (Abstraction) is not enough; you need rigorous precision (Specification) to make it work.

### The PR Problem: The "Dark Side" of Algorithms

In the public sphere, the word "Algorithm" has acquired a sinister vibe. It has become a placeholder for "opaque system that oppresses me."
If you search Google News for "Algorithm," you find headlines asking: "Are algorithms sexist?" "Do algorithms control our lives?"

We can think of this as the **Dark Side** vs. the **Light Side**.

- **The Dark Side:** Algorithms that determine creditworthiness, police patrols, or job applications. These are often "Black Boxes" where biases in data (Machine Learning) are codified into rules that affect human lives without accountability.
- **The Light Side:** The algorithms that route logistics so supermarkets have food, the code that compresses video so you can stream movies, or the search tools that organize the world's information.

The media often conflates "Algorithm" with "Machine Learning" (AI).

- **Classic Algorithms** (Symbolic AI) are rules we write. We know exactly how they work (e.g., Binary Search).
- **Machine Learning** (Sub-symbolic AI) involves systems that _learn_ their own rules from data.

When people are angry at "The Algorithm," they are usually angry at the opaque results of Machine Learning, not the sorting logic of Computer Science. However, as computer scientists, we own both.

### The Framework: The 5 Principles

So, how do we master this thinking style? Stefan Szeider breaks down Algorithmic Thinking into five distinct pillars. These are the mental tools we use to tame complexity.

1.  **The Principle of Specification:** Before we solve, we must define. We need to describe the problem and the goal with mathematical precision, removing all ambiguity.
2.  **The Principle of Decomposition:** "Divide and Conquer." We break a massive, scary problem into tiny, manageable sub-problems that we can solve individually.
3.  **The Principle of Abstraction:** We hide the messy details. We create models that ignore the irrelevant parts of reality so we can focus on the core structure (like using a map instead of a satellite photo).
4.  **The Principle of Scalability:** We don't just solve for today's data. We ask: "What happens if the inputs grow to infinity?" We design for efficiency at scale (like choosing Binary Search over Linear).
5.  **The Principle of Reduction:** We don't reinvent the wheel. We try to transform our new problem into an old problem that we already know how to solve.

These five principles are the DNA of the discipline. They transform us from people who just "write code" into people who "solve problems."

---

_This concludes the transformation of the Computational Thinking lecture notes. The five parts cover the history, philosophy, practice, cognitive science, and algorithmic foundations of the field._
