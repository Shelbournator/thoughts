---
title: "The Protocol of Maintenance: Fighting Entropy and Squeaky Brakes"
date: 2026-01-08 09:00:00 +0000
categories: [Build, Bike Mechanics]
tags: [maintenance, entropy, technical-debt, cycling, anti-fragility]
pin: false
math: false
mermaid: true
description: "Why preventative maintenance is the 'lazy' option, and how fixing a squeaky brake taught me the architecture of the rear wheel."
---

In my [last post]({% post_url 2026-01-07-the-art-of-bike-mechanics %}), I discussed the acquisition of the asset. Now, we move to **Operations**.

A commuter bike in London is a workhorse. It operates in a hostile environment of wet grit, road salt, and impact shocks. From a systems perspective, the bike is in a constant state of decay. Every mile ridden increases the **Entropy** of the system.

The goal of maintenance is not just "cleaning"; it is **Entropy Management**.

## The Paradox of Laziness

We often view maintenance as a chore—something that requires discipline to overcome our natural laziness.

But this framing is wrong.

If you analyze the total energy expenditure over the lifecycle of the asset, **Preventative Maintenance** is actually the "lazy" option.
*   **Scenario A (Maintenance):** 5 minutes of cleaning per week. Low effort.
*   **Scenario B (Neglect):** 0 minutes per week -> Catastrophic failure. High effort.

True laziness—efficiency—dictates Scenario A. What we call "laziness" (Scenario B) is actually just **High Time Preference**. It is the inability to delay gratification (the Marshmallow Test applied to mechanics).

We trade a small immediate gain (not servicing the bike) for a massive future cost (replacing components). In software terms, neglecting maintenance is simply taking out **Technical Debt**.

## The Operating System: Nested Loops

To manage this, I built a maintenance schedule. I treat this not as a "to-do list," but as a set of nested loops with different frequencies.

**Loop 1: The Integrity Check (Weekly)**
*   **Chain:** Wipe down and re-lube. (Prevents grinding paste forming).
*   **Tyres:** Check pressure. (Prevents pinch flats and reduces rolling resistance).
*   **Visual Audit:** Check for loose bolts or cracks.

**Loop 2: The Deep Clean (Monthly)**
*   **Wash:** Warm soapy water to remove salt and corrosive road dust.
*   **Inspection:** Check for wear on consumables (pads, chain).

**Loop 3: The Overhaul (6-12 Months)**
*   **Consumables:** Replace brake pads, cables, and housing.
*   **Truing:** Re-align wheels.

## Case Study: The Squeaky Brake

The schedule is the theory. The reality is that you learn when things annoy you.

Being sensitive to small changes in the system is crucial for maintenance - they are often early signals of failure.

Early on, I developed a squeak in the rear disc brake. Disc brakes work by pinching a rotor between two pads; if the rotor or pads get contaminated (oil, road grease), they screech.

**The Fix:** Cleaning with Isopropyl Alcohol.
**The Complexity:** To clean it properly, I had to take the wheel off.

This was my first time removing a wheel. In theory, it is simple: loosen the thru-axle, drop the wheel. In practice, the rear wheel is a **Complex Interface**.

The rear wheel doesn't just sit in the frame; it interfaces with the **Drive Chain**. The cassette (the cogs) sits inside the chain loop, and the derailleur (the gear shifter) sits underneath it.

> **Emergent Complexity**
>
> When you take the wheel off, the system loses tension. The chain goes slack. The derailleur swings.
>
> Putting it back requires navigating a 3D puzzle: aligning the disc rotor into the caliper slot, while simultaneously hooking the chain onto the cassette, while ensuring the axle threads line up.
{: .prompt-tip }

I struggled. I had to watch videos. I got grease everywhere.

I eventually found that the pads were glazed and I didn't have the right grit sandpaper to resurface them, so I replaced them entirely.

## The Anti-Fragility of Practice

Why does this matter?

Because I struggled with the rear wheel **in my living room**.

I learned the complexity of the cassette/derailleur interface in a warm, dry, low-stakes environment. I made mistakes, I dropped the chain, and I figured it out.

This is **Anti-Fragility**.

If I hadn't done this maintenance task, my first experience removing the rear wheel would likely have been **roadside**, in the rain, with a flat tire (hint: foreshadowing a future post).

By voluntarily engaging with the complexity now, I have reduced the "Shock" of a future failure. I have converted a potential crisis into a known procedure.

## Conclusion

## Conclusion: The Aristotelian Ladder

Maintenance looks like a cost, but it is actually an investment in **System Knowledge**.

Every time you touch the machine to clean it or fix a minor annoyance (like a squeak), you are climbing a hierarchy of knowledge that Aristotle outlined in his *Metaphysics*:

1.  **The User (*Empeiria*):** Knows *that* it works. They treat the machine as a Black Box.
2.  **The Operator (*Techne*):** Knows *how* it works. They can execute procedures to maintain the state of the system.
3.  **The Architect (*Architekton*):** Knows *why* it works. They understand the **Telos** (purpose) and the constraints that dictated the design.

Fixing the brake didn't make me a master mechanic, but it forced me to **reverse-engineer** the Architect's intent.

I didn't just see a lever; I saw the specific trade-off between leverage, cable tension, and pad clearance. I stepped out of the role of the User and caught a glimpse of the engineering logic that holds the system together.

Next time: The drive train starts making a grinding noise, and I learn the hard way about **Observability**.

## Conclusion: The Aristotelian Ladder

Maintenance looks like a cost, but it is actually an investment in **System Knowledge**.

Every time you touch the machine to clean it or fix a minor annoyance (like a squeak), you are building a mental model of how the components interact. You are climbing a hierarchy that Aristotle outlined in his *Metaphysics*:

1.  **The User (*Empeiria*):** Knows *that* it works. They rely on habit and experience. If the button fails, they are helpless because they lack the theory.
2.  **The Operator (*Cheirotechnes*):** The manual worker. They can act and repair, but they often work by rote or muscle memory, like "fire burning"—acting without necessarily knowing the cause.
3.  **The Architect (*Architekton*):** The master craftsman. They possess the *Techne*. They are wiser not because they can *do* more, but because they understand the **Causes** and the **Why**.

Fixing the brake didn't make me a master mechanic, but it pushed me briefly from User to Operator, and gave me a glimpse of the Architect's view. I didn't just see a lever; I saw the specific trade-off between leverage, cable tension, and pad clearance.

Next time: The drive train starts making a grinding noise, and I learn the hard way about **Observability**.
