# Usability testing

I wanted to see how people actually moved through the prototype, especially when the answer wasn't completely straightforward. I was less interested in whether they liked the screens and more interested in where they hesitated, misunderstood something, or expected the product to behave differently.

I tested the live Figma prototype with six people. Each session took around 15–20 minutes.

This was informal testing, not a representative user study. I treated the feedback as a way to catch problems in the prototype, rather than as evidence of how actual scholarship applicants would behave. The goal was mainly to catch problems in the flow, see where people misunderstood something, and find things I hadn't noticed myself.

## How I tested it

I started each session by saying:

> “This is an early prototype, not a finished product. I'm testing the design, not you if something's confusing, that's useful information. Think out loud as you go.”

I then gave them five tasks rather than walking them through the screens myself.

### 1. Starting from scratch

> “You want to find out if you qualify for this scheme. Show me what you'd do first.”

I didn't explain where to click. I wanted to see whether the starting point and the first question made sense on their own.

### 2. Reading the eligibility answer

> “Walk me through what this screen is telling you. Do you trust it? Why or why not?”

I watched whether they understood the answer, noticed the wording such as “Likely qualify,” and looked at the source behind it.

### 3. Trying an unclear case

I then gave them a more complicated situation involving two separate income gaps during the same year.

> “Try this one.”

This mattered because one of the main ideas behind CivicAssist is that the assistant shouldn't invent an answer when the available information doesn't clearly cover someone's situation.

### 4. Finding the documents

> “Now pull up what you'd need to submit.”

I wanted to see whether the checklist felt useful and whether people could understand why each document was being requested.

### 5. Final reaction

> “What does this do well, and what would make you not trust it?”

I also paid attention to things they didn't say out loud: hesitation, re-reading, looking for something that wasn't there, or trying to click something I hadn't intended them to click.

If someone missed something that I thought was obvious, I treated that as a design problem rather than a user mistake.

## What actually happened

| # | Screen | What happened | What I took from it |
|---|---|---|---|
| 1 | Screen 3 - uncertainty | “I did have to look twice at the orange one though, I thought it meant rejected.” | The uncertainty colour could easily be read as a negative outcome. |
| 2 | Screen 4 - checklist | Called this the most useful screen, but didn't notice the “Updated Mar 2026” date until I pointed it out. | Having the date there isn't enough if people don't actually see it. M3 needs stronger visual emphasis. |
| 3 | Screen 2 - cited answer | “‘Likely qualify’ made me wonder why it's not just saying yes. Then I saw the source and it made more sense.” | The wording creates some hesitation, but the citation helps explain why the answer isn't a simple yes. |
| 4 | Screen 3 - uncertainty | “I thought something had gone wrong, but then I read it properly. Maybe the colour is what threw me off.” | A second person had the same reaction. The wording itself wasn't the problem. |
| 5 | Screen 5 - source detail | Liked being able to check the actual rule, but said, “I probably wouldn't read all that legal text unless I had doubts.” | Good reason to keep the detailed source behind the main answer rather than putting it front and centre. |
| 6 | Screen 5 - source detail | Wanted a plain-language explanation alongside the legal text. | A useful improvement I hadn't considered. Worth adding later, but not something that blocks v1. |

## What I changed

The first clear change was the uncertainty state.

Two of the six people initially read the amber card as a rejection or something having gone wrong. Once they read the text properly, they understood that it meant the available information wasn't enough to give a confident answer.

I changed the uncertainty card from amber to a cooler slate tone. I kept the wording the same because the message itself was working once people read it.

This was a useful reminder that getting the wording right isn't enough if the visual treatment tells people something different at first glance.

I also kept the source and source update date visible on the relevant screens. The testing showed that people valued being able to verify the answer, but the update date was easy to miss. I didn't remove it or hide it; stronger visual emphasis is something the design still needs.

For the detailed source screen, I kept the full rule available rather than putting it directly into the main eligibility answer. People wanted to be able to check the source, but they didn't necessarily want to read all the legal text unless they had doubts.

## One problem I found in my own review

The testing also exposed a problem that wasn't really caused by the participants.

The complicated case on the uncertainty screen involved two income gaps. But the next checklist screen was shared with the normal path and only showed one income-gap document.

That meant the information wasn't being carried consistently through the prototype.

I fixed this by separating the two paths in the prototype:

- 4A — the normal case, with one income gap
- 4B — the more complicated case, with two income gaps

I also replaced the hidden demo click area with a visible second button:

“This is a bit more complicated”

That makes the choice explicit instead of expecting someone to discover an invisible interaction.

## Follow-up after the fixes

I showed the updated flow to two of the original participants.

This wasn't a second full testing round. I didn't give them the original tasks again, so I wouldn't treat it as equivalent to the first six sessions.

Both found the navigation clearer once the second button was visible. One also liked having an obvious option for the more complicated case.

It was only a small follow-up, but it was enough to tell me the change was clearer.

## What I learned

The biggest takeaway wasn't a particular colour or button.

It was that the prototype could contain the right information and still communicate the wrong thing.

The uncertainty state had the correct wording, but the colour made it look like a rejection. The source update date was present, but people didn't notice it. The detailed rule was available, but showing all of it at once would have made the main answer harder to use.

That's really what I want CivicAssist to get right: not just giving someone an answer, but being honest about how certain that answer is and showing them where it came from.

The testing helped me turn that idea into specific design decisions.
