# Reflection: from the eval harness to CivicAssist

Building the eval harness, the finding that stuck with me was how confident it sounded while being wrong, not hedged, not vague, just stated like fact.

It invented a 12–24 month eligibility rule that didn't exist anywhere in the source material, and presented it in exactly the same way it would've presented something that was true. Nothing in the answer gave you a reason to question it.

That's what I kept coming back to when I started designing CivicAssist. A product that gives confident answers is relatively easy to build. The harder part is deciding what happens when the evidence isn't enough — and making sure the product doesn't quietly fill in the gaps itself.

Screen 3, the “not a rejection, unresolved” state, is my attempt to move that idea from the model layer into the product itself. If someone's situation isn't clearly covered by the source, CivicAssist shouldn't guess. It should say that plainly, without making the person feel like they've done something wrong.

Unresolved versus rejected sounds like a small distinction when written down, but it's really the point of that screen.

The initial research looked at how real portals like MahaDBT and NSP handle these situations. Interviews came later, during usability testing: a couple of the PRD's requirements are tagged `[Interview]` because of what came up in those conversations. What I found was reassuring in the worst possible way: some of the same ambiguity already exists in the systems people are actually using. MahaDBT's 2.0 rollout left applications stuck because of portal issues, while NSP's troubleshooting guidance makes it clear that income certificate validity isn't governed by one consistent rule across every situation.

None of that is an AI hallucinating. It's the same basic problem showing up somewhere else, a system can leave someone with what looks like a definite outcome when the underlying situation is actually unclear.

## What testing actually showed

Everything above came from documentation. That's useful, but it's still me reading about a problem rather than watching someone run into it.

So I wanted to see what happened when someone looked at Screen 3 without me explaining what the colours or states were supposed to mean.

I ran six informal sessions. Two people initially read the amber uncertainty card as a rejection or an error.

One said:

> “I did have to look twice at the orange one though: I thought it meant rejected.”

Another said:

> “I thought something had gone wrong, but then I read it properly. Maybe the colour is what threw me off.”

Once they read the text, both understood what the screen meant. So the wording wasn't really the problem. The colour was creating the wrong impression before they got to the words.

I changed the uncertainty card from amber to a cooler slate tone and left the copy alone.

That was probably the most useful thing I learned from the testing: sometimes the problem isn't that the information is wrong or unclear. It's that the design is telling people something different before they have a chance to read it.

The same sessions also confirmed something I'd hoped was true but hadn't actually tested. People liked being able to check where the eligibility answer came from. At the same time, most weren't interested in reading the full legal text unless they had a reason to question the answer.

That made the current approach feel right: show the source, but don't put the entire source in the user's way. The detailed rule is there when someone wants to verify the answer, while the main screen stays focused on the actual decision they're trying to make.

The testing also caught a smaller issue I hadn't noticed myself. One person didn't notice the “Updated Mar 2026” date on the checklist until I pointed it out. It was technically on the screen, but that didn't mean it was doing its job.

That became another useful distinction for me. Putting information somewhere isn't the same as making it noticeable.

And that's probably the biggest connection between the eval harness and CivicAssist for me. In both cases, the goal isn't just to produce an answer. It's to make the limits of that answer visible enough that someone can actually make a sensible decision about whether to trust it.
