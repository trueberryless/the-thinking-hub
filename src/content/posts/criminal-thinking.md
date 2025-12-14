---
title: Criminal Thinking
pubDate: 2025-11-02
---

## Part 1: The Criminal Mindset & Physical Vectors

### The Burglar’s Philosophy

When we talk about building secure systems, there is an aphorism that gets thrown around constantly in the security industry: "Think like a burglar." This isn't just a catchy phrase; it is the fundamental motivation behind understanding criminal thinking. As engineers and developers, we are trained to build things that work. We optimize for uptime, for throughput, for the "happy path" where the user clicks the right buttons and the database responds correctly. But that perspective is dangerous because it ignores the reality of entropy and malice. The idea that it is sufficient to implement a system well, without errors, and with thoughtful architecture is fundamentally challenged by the criminal mindset.

To truly secure a system, you have to invert your thinking. You cannot just ask, "How do I make this work?" You must ask, "How do I make this fail?" This concept is explored deeply in the "Mental Models & Security" framework, which argues that we need to adopt specific cognitive strategies to anticipate security problems before they manifest. These strategies include **Inversion** (looking at the problem backwards), **Second-Order Thinking** (asking "and then what?"), and **Probabilistic Thinking**.

These mental models act as the bridge between a "builder" and a "breaker." Builders operate under the assumption that technology works in the normal case. Criminal thinkers operate under the assumption that technology _will_ fail, or can be forced to fail. In cybersecurity, failing to plan for that failure isn't just an oversight; it is the core definition of negligence. We need to stop designing only for functionality and start designing for the inevitable breach.

### The ATM: A Public Vault with a Weak Interface

Let's ground this philosophy in a tangible example that has evolved over decades: the ATM. Fundamentally, an ATM is just a safe sitting in public. Physically "cracking" the safe itself is incredibly difficult. It usually requires heavy machinery, explosives, or ripping the entire unit out of the wall with a truck — methods that are loud, dangerous, and conspicuous. Because the vault is hard to break, criminal thinkers target the interface instead. It is significantly easier to intercept the data flow between the customer and the bank than it is to steal the physical cash.

This is where **Skimmers** come into play. A skimmer is a device added to the existing interaction hardware — the card reader and the keypad — to capture user data.

There is a fascinating nuance in how we design these interfaces that actually aids the attacker. Have you ever wondered why ATMs force you to type your PIN on a physical, rubberized keypad rather than a sleek touchscreen? It’s a security feature. If you used a touchscreen, software could log the coordinates of your tap (a software keylogger). Even more simply, the grease from your fingers would leave residual smudges on the screen, allowing a thief to shine a light on the glass and see exactly which numbers you pressed. By using a physical keypad, the system offloads authentication to the card itself without storing the PIN in an easily accessible software layer.

However, this physical separation creates a new vulnerability. Because the keypad is a distinct physical component, it can be manipulated. Attackers have developed overlay keypads — thin, realistic-looking plastic shells that sit directly on top of the real keypad. When you type your PIN, you are actually pressing the attacker’s buttons, which record the keystrokes and pass the pressure down to the real buttons below. The transaction works perfectly, but your PIN has been compromised.

We can see this vulnerability even without high-tech overlays. If you look closely at older keypads, you can sometimes see the PIN simply by observing the wear and tear. If the "1," "2," "3," and "4" keys are rubbed smooth while the rest are dusty, the PIN is almost certainly a permutation of those digits. This is the "Smoker’s Finger" effect: the physical evidence of digital secrets.

### The Vienna Case Study: What Was Missed?

A few years ago, a security researcher named Ben Tedesco uploaded a video that went viral. He was visiting St. Stephen’s Cathedral (Stephansplatz) in Vienna and spotted something off about an ATM. In the video, he grabs the green plastic housing surrounding the card slot and gives it a firm wiggle. With a bit of force, the entire plastic molding pops off. It was a 3D-printed replica containing magnetic read heads and a battery, designed to sit over the real slot and skim the magnetic stripe data as the card was inserted.

It was a great catch, but here is the terrifying detail that most people — including Tedesco at the moment — missed. He found the card skimmer, but he missed the second half of the apparatus.

To steal money, you need two things: the card data (PAN) and the PIN. The plastic overlay he removed only captured the card data. To get the PIN, the attackers had installed a micro-camera hidden in a molding strip directly above the keypad. This camera was angled perfectly to record the user's fingers as they typed. The attackers had covered all bases, and the hardware was designed to blend seamlessly into the machine's aesthetic. It is a perfect example of criminal competence: they didn't just hack the machine; they engineered a physical overlay that mimicked the industrial design of the bank's hardware.

### The Evolutionary Arms Race

The relationship between security engineers and criminals is a perpetual arms race. Every time we introduce a new defense, the "criminal thinker" finds a workaround.

When skimming became an epidemic, the industry moved from magnetic stripes to **EMV Chips**. The logic was that chips couldn't be cloned as easily as a magnetic stripe. Did this stop the criminals? No. It just changed their vector. We started seeing "Shimmers" — incredibly thin, flexible circuit boards that slide into the card slot _with_ the card, sitting between the chip and the reader to intercept the communication.

Then came "Deep Insert" skimmers. These are wafer-thin devices that are shoved deep inside the machine, completely invisible from the outside, utilizing tiny batteries and storage to harvest data for weeks.

As we moved to contactless (NFC) payments to avoid physical contact entirely, the attackers shifted again. We are now seeing Android malware like **NGate** that uses the NFC reader on a compromised phone to relay data from a victim's card in their pocket to an attacker's device, effectively cloning the card wirelessly. Or consider the "Ghost-Tap," where hackers exploit vulnerabilities in mobile payment protocols. The medium changes, but the methodology remains constant: find the input, intercept the data, monetize the access.

A critical piece of advice: If you ever spot a skimmer, do not pull a "Ben Tedesco" and rip it off yourself. Criminal gangs often monitor these devices from a parked car nearby to retrieve the data or the hardware. They can be extremely aggressive if they see you tampering with their livelihood. The correct move is to walk away and call the police.

### The "Lahore" Connection: Physical Meets Syntactic

We can categorize these attacks by their nature. Some are purely physical (glue on a cash dispenser), some are syntactic (SQL injection), and some are a hybrid.

A chilling example of a hybrid attack was discovered in the credit card terminals of a large discount grocery chain. Security teams found small, foreign circuit boards soldered inside the legitimate card readers. These weren't just storing data; they were equipped with GSM modems.

Every day, these devices would wake up, bundle the captured credit card numbers, and transmit them via the mobile network to a phone number in Lahore, Pakistan. The sophistication here is high: the attack was hardware-based, but the exfiltration was purely telecommunications.

The only reason this was discovered wasn't because of a software audit or a firewall alert. It was discovered because a security guard at the store noticed that his own cell phone was making that rhythmic "buzzing" interference noise you hear when a device is transmitting data nearby. He heard the interference near the checkout counter when no one was using a phone, realized something was broadcasting, and called the police. This incident underscores that criminal thinking is global, hardware-agnostic, and often invisible until a side channel — like audio interference — gives it away.

---

_Coming up in Part 2: We leave the hardware behind to profile the "Black Hat" — tracing their evolution from curious pranksters to the ruthless architects of the malware economy._

## Part 2: Profiling the Adversary – Motivations & The Malware Economy

### The Color of Intent

Before we can understand the attack, we have to understand the attacker. In the short history of computer science, we’ve developed a shorthand to categorize these actors based on the metaphorical color of their hats. It’s a bit of a cliché, but it’s useful for setting the stage.

You have your **White Hats**, the security professionals and researchers finding bugs to fix them. You have **Grey Hats**, who operate in the nebulous middle ground, perhaps breaking the law to reveal a vulnerability but without malicious intent. There are **Red Hats**, the vigilantes who actively attack the attackers. But for the purpose of "Criminal Thinking," we are almost exclusively interested in the **Black Hats**. These are the actors motivated by malice, profit, or political ideology.

It is also worth debunking a persistent stereotype right now: the image of the hacker as a lonely, hoodie-wearing guy in a basement is outdated and inaccurate. If you look at the history of notorious hackers, you find names like Susan Headley, Ying Cracke, and Kristina Vladimirovna Svechinskaya. The demographic is diverse, but the intent is what matters. In this industry, we try to avoid using the word "hacker" as a synonym for "criminal" because hacking is fundamentally just a creative engagement with technology. When that creativity is applied to theft or destruction, the correct terms are "Cybercriminal" or "Black Hat."

### The Evolution of the Hustle

If we trace the timeline of cyber threats, we see a distinct shift in motivation. In the early days, hacking was largely driven by curiosity, intellectual challenge, and a bit of ego. It was about seeing if you could get into a system just to prove it was possible. But as the internet matured, the "why" changed dramatically.

Today, malware is a business model. We often talk about "Internet Background Radiation" — the constant, low-level hum of automated attacks hitting every public IP address. This isn't personal; it's capitalism. Hackers make money by aggregating massive fleets of compromised home computers — bots — and leasing them out. They earn commissions for every piece of spyware or adware they successfully plant on an infected machine. As discussed in a 2021 TWiT podcast segment, this commercialization is the primary engine driving modern threats. The romantic idea of the lone genius has been replaced by the reality of the supply chain manager.

### The DDoS Timeline: From Pranks to Politics

A perfect illustration of this evolution is the history of Distributed Denial of Service (DDoS) attacks. Fifteen years ago, if you looked at a timeline of DDoS incidents, the motivations were chaotic. They were often "for the lulz" — kids testing scripts to knock a game server offline or just to see what would break. The attacks were characterized by a lack of clear purpose.

Over the last decade and a half, that randomness has hardened into strategy. The motivation shifted first to extortion — "pay us 5 Bitcoin or your e-commerce site stays down" — and then to political warfare. We now see massive spikes in traffic directed against gaming companies or media outlets that appear to be retaliation for sociopolitical stances. While it’s hard to prove attribution in real-time, the correlation between controversial public statements and massive packet floods is undeniable.

The scale has also become terrifying. Since 2008, the sheer volume of DDoS attacks has increased roughly 30-fold. We don't measure these campaigns in "attacks per day" anymore; we measure them in "attacks per hour." And thanks to the efficiency of modern tools, attackers can do more with less. A few years ago, you might have needed a botnet of 1,000,000 infected devices to cripple a target. Today, with smarter application-layer attacks and the assistance of generative AI to script complex attack vectors, you might achieve the same result with only 50,000 bots. The barrier to entry has lowered, but the destructive potential has skyrocketed.

### The Industrialization of Scamming

The profit motive has reshaped entire economies. As reported by the Guardian in October 2025, we are witnessing the rise of "cybercrime villages" in places like rural India. As traditional agricultural jobs vanish, entire regions are pivoting to call centers dedicated to global fraud.

This is "scamming as farming." The goal is to harvest capital from victims on the other side of the planet — stealing identities, draining bank accounts, and installing remote access trojans. This is a global information system with no corresponding global justice system. A scammer in a jurisdiction with lax enforcement faces almost zero risk of prosecution for defrauding a grandmother in Ohio. This accountability vacuum leads to bizarre outcomes, such as the rise of "glitterbombing" vigilantes like Mark Rober, who use engineering to exact the only form of justice available: pranking the scammers back. It’s entertaining, but it highlights a systemic failure of law enforcement to adapt to a borderless crime wave.

### Ransomware: The Predator of Infrastructure

The "start signal" for the modern era of high-stakes cybercrime was the emergence of Ransomware. This is the ultimate distillation of the criminal business model: encrypt the victim's data and sell them the decryption key.

Around 2016, we saw a massive wave of ransomware targeting hospitals. Why hospitals? Because they were the perfect "soft targets." They rely on immediate access to patient data to save lives, their IT infrastructure is often legacy and underfunded, and they have the money to pay.

The case of the Lukaskrankenhaus in Neuss, Germany, is a prime example. A virus infected their IT systems, forcing them to shut down nearly all digital operations. While they stated that patient data was safe due to backups, the hospital was effectively paralyzed, operating with severely limited functionality. This incident revealed a brutal truth: having a backup is not enough if the time required to restore that backup causes operational collapse.

The attackers realized that public infrastructure was a goldmine. By 2019, the target list expanded to city governments. New Orleans had to declare a state of emergency following a cyberattack that crippled the police department, courts, and emergency medical services.

The human cost of this is not theoretical. In 2020, a patient in Germany died after being diverted to a different hospital because the nearest facility was in the midst of a ransomware lockout. The delay in treatment proved fatal. This tragedy underscores the danger of viewing IT security as a cost center rather than a safety requirement. When organizations like Sony (in 2007) or local hospitals decide that "hardening the database costs $10 million, but the breach only costs $1 million," they are making a business calculation that ignores the catastrophic reputational and human damage that modern black hats can inflict.

---

_Coming up in Part 3: We examine the "Opportunity" that lets these attacks happen — from the persistence of "Zero Day" vulnerabilities and bad code to the looming threat of AI-generated exploits._

## Part 3: The Opportunity Landscape – Zero Days, Policy Failures, and AI

### The Window of Vulnerability

If motivation is the "why" and malware is the "how," then opportunity is the "when." A central concept in understanding this opportunity is the **Zero Day**. This term refers to a software vulnerability that is unknown to the vendor or the public, meaning there is effectively zero days of warning before an attack could theoretically happen. In the hands of a Black Hat, a Zero Day is a master key. But the opportunity doesn't close the moment a vulnerability is discovered; it often widens due to the sluggishness of human response.

Consider the case of **Heartbleed**, a critical vulnerability discovered in the OpenSSL cryptographic library in 2014. OpenSSL is the bedrock of secure internet communication, used by approximately two-thirds of all web servers at the time. The bug allowed anyone on the internet to read the memory of systems protected by the vulnerable versions, potentially exposing passwords, encryption keys, and user data.

When Heartbleed was announced, the fix was released simultaneously. In a perfect world, the story ends there. But in the real world, the announcement was just the starting gun for a race between administrators patching their servers and criminals scanning for vulnerable targets. The technical fix was instant; the deployment was agonizingly slow. One year after the vulnerability was disclosed, fewer than 50% of the affected servers in Germany had been patched. Two years later, tens of thousands of systems were still bleeding. This illustrates a critical failure in the security lifecycle: solving the problem mathematically does not solve it operationally. Millions of systems remain vulnerable simply because they are running legacy software that no one bothers to update.

### The Myth of Calculated Risk

Historically, organizations have rationalized this sluggishness through cold financial calculus. A notorious example from 2007 involves a security executive at Sony, who essentially argued that if hardening a legacy database costs $10 million, but the cost of notifying customers after a breach is only $1 million, the valid business decision is to accept the risk of the hack. This "calculated negligence" was the industry standard for a long time.

That logic has now collapsed. The cost of a breach is no longer just the immediate cleanup bill. Today, we have regulatory hammers like the GDPR (General Data Protection Regulation) in Europe, which mandate that personal data must be protected according to the "state of the art." The penalties for negligence are now astronomical. For instance, the Greek mobile operator COSMOTE was fined €6 million after a hack exposed customer data. Beyond the fines, there is the devastating loss of reputation. In the modern tech economy, trust is a currency. When companies lose customer data, they lose that trust, and the market punishes them far more severely than the cost of a firewall upgrade.

### The AI Double-Edged Sword

The opportunity landscape is shifting again with the rise of **Generative AI**. This technology acts as an accelerant for both sides of the security equation. On one hand, we are seeing a massive influx of "Bad Code" generated by AI assistants. Studies suggest that a significant percentage of code produced by tools like GitHub Copilot contains security vulnerabilities. When developers blindly trust AI-generated snippets without rigorous auditing, they are baking flaws into their software supply chain at a speed we haven't seen before.

On the other side, Black Hats are using the same tools to sharpen their attacks. AI can write convincing phishing emails, generate polymorphic malware that changes its code to evade detection, and even help script complex exploits. While the security industry sometimes reacts with panic, the reality is undeniable: AI lowers the barrier to entry for cybercrime. It allows less skilled attackers to operate with the sophistication of advanced groups, effectively democratizing the ability to cause chaos.

### The Admin Gap

We often blame the "end-user" for security failures — the receptionist who clicked a link or the grandfather who shared his password. But we need to turn that scrutiny toward the professionals. System administrators and IT staff are often assumed to be the "strong link," but research challenges this.

Two scientific studies from the environment of TU Wien investigated how well system administrators actually understand the security measures they deploy. The titles alone — _On the Usability of Deploying HTTPS_ and _If HTTPS Were Secure, I Wouldn’t Need 2FA_ — point to the problem. The findings were concerning: not only were there significant knowledge gaps among the professionals, but the security products themselves suffered from massive usability issues.

If the tool for configuring a secure server is confusing, the administrator will likely misconfigure it. This is a "System 2" failure. It’s not just that people are lazy; it’s that the complexity of modern infrastructure has outpaced the usability of our management tools. When we say "humans are the weakest link," we must include the architects and administrators in that statement. A poorly designed interface for a firewall is just as dangerous as a weak password.

---

_Coming up in Part 4: We dive into the psychology of the "Human Factor," exploring how distance emboldens attackers and how Social Engineering hacks the human operating system._

## Part 4: The Human Factor – Social Engineering & The Identity Crisis

### Distance as a Weapon

One of the most powerful enablers of criminal thinking is a concept that predates the internet entirely: distance. It is a well-documented psychological phenomenon that it is easier to be cruel, aggressive, or destructive when you don't have to look your victim in the eye. We see this in the toxicity of anonymous online comment sections, but in the realm of cybersecurity, this distance transforms crime into a game.

Hackers operate remotely, far removed from the tangible consequences of their code. A chilling demonstration of this was the famous remote hacking of a Jeep Cherokee by researchers Charlie Miller and Chris Valasek. In their demonstration, they didn't just tamper with the radio; they killed the engine while the car was driving down a highway. In the video documentation of the hack, you can hear the researchers laughing as the driver struggles with a dead vehicle. To them, sitting comfortably miles away with their laptops, it was an intellectual triumph — a successful execution of code. To the driver, it was a terrifying loss of physical control. This emotional disconnect allows attackers to perform dangerous acts with the casual demeanor of someone playing a video game, making the threat landscape far more volatile than traditional physical crime.

### Professionals Target People

There is a saying by security guru Bruce Schneier: "Amateurs tend to attack machines, whereas professionals target people." This brings us to the domain of **Social Engineering**, which is arguably the most reliable way to breach a complex system. Why spend months trying to crack 256-bit encryption when you can just ask the receptionist for the password?

Social engineering is the art of manipulating people into breaking their own security rules. In pop culture, this is often depicted as a hacker guessing a password because it’s the name of the target’s dog. While that happens (reconnaissance into private lives is real), the reality is often much more physical and immediate. It exploits our social norms. For example, if you are walking towards a secure office door carrying a heavy box, and you ask the person in front of you to "hold the door," they almost certainly will. In that moment, their desire to be polite overrides their training to prevent "tailgating." You are now inside the building, and the firewall doesn't matter anymore.

The industry is full of legends who specialize in this. Jason E. Street is a notorious penetration tester who has given talks at DevCon detailing how he breaks into banks and secure facilities not with code, but with a smile and a clipboard. He exploits the fact that people want to be helpful. Similarly, a photo of Eric Corley (founder of _2600_ magazine) captures the essence of this "low-tech" hacking. In the image, he is simply working a payphone, yet through sheer verbal manipulation, he once managed to get a Taco Bell to shut down all their registers for five minutes and convinced a KMart manager to patch him into the store-wide PA system so he could announce that "everything in Aisle 6 is free." Even security experts are vulnerable; Youtuber Max Fosh demonstrated that he could infiltrate a security convention, proving that the very people who mock end-users for being the "weakest link" are just as susceptible to a clipboard and a confident demeanor.

### The "Stupidity" Paradox

We frequently blame end-users for security breaches, labeling them as the "weakest link" in the chain. This is a lazy and dangerous simplification. It is like a driver in a traffic jam complaining about traffic, failing to realize they _are_ the traffic.

When we look at security failures, we often find that the "user error" was actually a design failure. Remember the ATM keypad discussed in Part 1? If the keys are worn down, revealing the PIN, that isn't the user's fault; it's the fault of the system administrator who failed to replace the hardware. If a user chooses a weak password, it's often because the system didn't enforce a better policy or provide a usable password manager.

A tragic example of this "blame the user" mentality failing is the **WannaCry** ransomware outbreak. When the news broke that a massive cyberattack was encrypting computers worldwide, panic set in. People were terrified. In their desperation to protect themselves, thousands of Android users rushed to the Google Play Store and searched for "WannaCry Protection." They downloaded the top results, thinking they were being responsible.

The tragic irony was that these apps were fake. Malware authors had anticipated the panic and flooded the store with "protection" apps that were actually malware themselves. The users were infected not because they were reckless, but because they were trying to be safe in an ecosystem that failed to protect them. The media's incompetent reporting on the technical details only fueled the fire, driving people straight into the arms of the attackers.

### The Crisis of Digital Identity

Perhaps the deepest systemic failure we face today is the lack of a verifiable digital identity. The internet was built without an identity layer. We have no standard, global way to prove who we are online. Instead, we have a fragmented mess of "Login with Facebook," "Login with Google," and hundreds of isolated user accounts.

This fragmentation forces users to manage impossible numbers of credentials, leading to password reuse and identity theft. But the consequences are getting far more severe with the advent of Deepfakes. Because we cannot cryptographically prove our identity in a standard way, we rely on our senses: "I see your face on the video call, I hear your voice, therefore it is you."

That heuristic is now obsolete. In a staggering case from Hong Kong, a finance worker at a multinational firm was invited to a video conference call with the company's Chief Financial Officer (CFO). The worker joined the call and saw the CFO and several other colleagues he recognized. They discussed a confidential transaction, and the CFO instructed him to transfer 200 million Hong Kong dollars (approx. €20 million).

The worker made the transfer. It was only later that he discovered the truth: everyone else on that video call was a deepfake. The attackers had used publicly available footage to reconstruct the faces and voices of the executive team in real-time. The worker wasn't negligent; he was overpowered by a technological reality that our identity systems are not equipped to handle. Until we solve the problem of digital identity verification, "seeing is believing" will remain a critical vulnerability.

---

_Coming up in Part 5: The final frontier — how billions of cheap, unsecure IoT devices are creating a zombie army, and why we might need a "Center for Disease Control" for the internet._

## Part 5: The IoT Apocalypse & A New Defense Paradigm

### The Landfill of Unsecured "Smart" Junk

While the security industry loves to hyperventilate about Artificial Intelligence, the most immediate and pervasive threat isn't a super-intelligent rogue AI. It’s your toaster. Or your cheap webcam. Or that Wi-Fi-connected fish tank thermometer. We are living through the explosion of the **Internet of Things (IoT)**, and frankly, it is a security disaster.

We need to make a sharp distinction here. When you buy a high-end "always-on" device like a Google Home or Amazon Echo, you are generally buying into a managed ecosystem. These companies have security teams, and crucially, they push firmware updates. If a vulnerability is found, it gets patched.

The danger lies in the "long tail" of cheap electronics. The market is flooded with white-label "smart" devices produced by manufacturers that act like mayflies — they exist for a year or two to flood the market with cheap hardware, and then they vanish. These devices are sold with no plan for software maintenance. They have hardcoded passwords (often just "admin/admin"), open Telnet ports, and unpatchable firmware. Once a vulnerability is discovered in one of these "zombie" devices, it is there forever.

This creates a terrifying dynamic: we are filling our homes and offices with millions of tiny, powerful computers that are permanently vulnerable. And because the people buying them are regular consumers, not sysadmins, these devices are almost never monitored. They just sit there, connected to the internet, waiting to be conscripted.

### Mirai and the Million-Bot Army

The wake-up call for this threat was the **Mirai Botnet** in 2016. Mirai didn't attack sophisticated servers; it scanned the internet for those cheap IoT devices — digital video recorders (DVRs) and IP cameras — and tried default usernames and passwords. It worked terrifyingly well.

Mirai amassed an army of hundreds of thousands of hijacked devices. When the controllers gave the order, this swarm launched a Distributed Denial of Service (DDoS) attack of unprecedented scale against Dyn, a major DNS provider. The result? Huge chunks of the internet, including Twitter, Netflix, and Reddit, simply vanished for users across the US and Europe.

Since then, the problem has only metastasized. A 2023 threat intelligence report from Nokia revealed that the number of IoT devices engaged in botnet-driven DDoS attacks skyrocketed from 200,000 to approximately **1 million devices** in a single year. The graph of IoT attacks in 2022 mimics the exponential curve of malware growth in general. Today, the majority of malware activity isn't targeting your laptop; it's targeting your smart infrastructure. We have inadvertently built a global supercomputer for criminals, powered by our own cheap gadgets.

### The "Creepy" Factor: When the Hacker is in the Bedroom

The threat isn't just about DDoS attacks knocking websites offline; it is deeply personal. These devices often include cameras and microphones, and they are frequently installed in our most private spaces.

There is a horrifying, well-documented case involving a Ring camera installed in a children’s bedroom. The parents put it there for safety. A hacker managed to compromise the device. The parents later reviewed the footage to find the hacker playing the eerie song _"Tiptoe Through the Tulips"_ through the camera's speaker. When the eight-year-old girl in the room stopped and asked, "Who's there?", the hacker replied: **"It's Santa. It's your best friend."**

This is the nightmare scenario. It has become so prevalent that the FBI issued warnings about "Swatting" attacks originating from compromised smart home devices.

Simultaneously, we are seeing a massive erosion of trust. Consumers are starting to realize that "smart" often means "spy." Stories of smart TVs serving intrusive ads or an LG washing machine seemingly uploading 11GB of traffic to the internet have made people skeptical. As one tech commentator noted, trust is the hardest thing to earn and the easiest to lose. We are approaching a tipping point where users might simply refuse to connect these appliances, turning "smart" features into dead silicon.

### "Click Here to Kill Everybody"

Security expert Bruce Schneier argues that the term "Cybersecurity" is becoming obsolete. We should just call it "Security." Why? Because everything is a computer now. Your car is a computer with wheels. Your pacemaker is a computer in your chest. Your power grid is a distributed computer system.

This means that software vulnerabilities now have kinetic consequences. We are moving from a world where a hack means "data loss" to a world where a hack means "physical harm."

Compounding this is the "Snyk 2023 AI Code Security Report," which highlights a dangerous feedback loop. 96% of development teams are now using AI coding tools to write software faster. However, over half of those teams report that these AI tools consistently generate insecure code. We are using machines to write bad code faster than humans can audit it, deploying it into critical infrastructure that controls the physical world.

### A New Model: The CDC for Cyber

So, how do we fix this? The lecture proposes a radical shift in how we think about digital safety: **The Public Health Model.**

In the 19th century, we didn't solve cholera by telling everyone to "just be more careful" with their water. We solved it by building sewage systems and establishing public health institutions. We need a similar approach for the internet.

Imagine a **Center for Disease Control (CDC) for Cybersecurity**.
Instead of blaming the user, this institution would operate at a systemic level. Its responsibilities would include:

- **Epidemiology:** Tracking the spread of malware and vulnerabilities like a biological virus.
- **Regulation & Certification:** Just as you can't sell a toaster that explodes, you shouldn't be allowed to sell a webcam that can't be patched. This body would test and certify hardware before it hits the shelves.
- **Public Warnings:** Issuing authoritative alerts about specific dangerous products (e.g., "Do not buy Brand X Baby Monitor").
- **Hygiene Education:** Moving beyond "make a strong password" to teaching genuine digital literacy and resilience.

We cannot "firewall" our way out of this individually. Resilience comes from systemic changes — automated backups, incident response protocols, and diversity in software ecosystems to prevent monoculture failures. We need to stop treating security as a feature and start treating it as a prerequisite for civilization, backed by policy, law, and robust institutions.

This brings us to the edge of technology and into the realm of governance. But that is a story for the next chapter: **Policy Thinking**.

---

_This concludes the "Criminal Thinking" blog series. Thanks for reading!_
