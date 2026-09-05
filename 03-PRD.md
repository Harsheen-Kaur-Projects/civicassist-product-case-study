# Product requirements

These requirements came from the research, then got tested against the Figma prototype. One of the ideas also comes directly from an earlier project I built: an AI evaluation harness that caught a model making up an eligibility rule that wasn't in the source material.

The evidence labels mean:

- [Audit] — based on the findings in `01-research-plan.md`.
- [Eval] — came from the earlier AI evaluation harness.
- [Interview] — came from conversations while testing the Figma prototype.

| ID | Category | Requirement | Priority | Evidence |
|---|---|---|---|---|
| M1 | Core UI | Show the source behind every eligibility answer, including the relevant rule or clause. | Must | [Audit] Rules are spread across different scheme pages. [Interview] People used the source to check where an answer came from. |
| M2 | Core logic | If the sources don't clearly cover a situation, show uncertainty instead of calling it a rejection. | Must | [Audit] Portal errors and actual application problems can look the same. [Eval] The earlier eval harness caught the model inventing an eligibility rule. |
| M3 | Trust | Show the source's last-updated date next to the citation. | Must | [Audit] Document validity isn't always consistent across schemes. [Interview] One person didn't notice the update date until prompted. |
| M4 | Input | Let people describe their situation in their own words before asking them to choose a category. | Must | [Audit] Income situations don't always fit neatly into the available categories. |
| M5 | Output | Give a document checklist based on the person's situation, with a reason for each item. | Should | [Audit] Generic checklists don't always make it clear which documents apply. |
| M6 | Next steps | When the answer is uncertain, explain what the person can do next. | Should | [Audit] Some portal errors are recoverable, but the user isn't always told what to do. |
| L1 | Later | Let people save their information and come back later. | Later | Out of scope for v1. |
| L2 | Later | Let people compare their eligibility across different schemes. | Later | No strong evidence for this yet. I'd want to hear it from users first. |

## What changed after testing

The requirements started with the audit, but the prototype testing showed me where some of them needed more thought.

I tested the Figma prototype with six people. The source citation was useful, people understood that it was there so they could check the answer rather than just trust the assistant.

The uncertainty state was more interesting. The wording worked, but two people initially read the original amber card as an error or rejection. I changed it to a cooler slate colour without changing the meaning.

The testing also showed that including information isn't the same as making it noticeable. One person found the checklist useful but didn't notice the “Updated Mar 2026” date until I pointed it out. That led me to keep M3 as a requirement while treating its presentation as something that still needs improvement.

There was also a navigation issue during testing. An edge case involving two separate income gaps wasn't being carried consistently from one screen to the next. I fixed the flow by separating the normal case from the more complicated case and making that choice visible instead of relying on a hidden click area.

So these aren't just features I decided would be useful. They came from the research, and the testing helped me see where some of them needed to change.
