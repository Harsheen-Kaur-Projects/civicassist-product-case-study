Author Harsheen Kaur

LinkedIn: https://www.linkedin.com/in/harsheen285/

GitHub: https://github.com/Harsheen-Kaur-Projects

# CivicAssist — Public-Service AI Product, Requirements to Prototype

CivicAssist came out of a problem I found while working on my AI evaluation harness.

The harness caught a model confidently inventing a 12–24 month eligibility rule that didn't exist in the source material. That made me think beyond the model itself: if an AI system doesn't actually have enough evidence to answer, what should the product do?

CivicAssist is my attempt at answering that question.

It's a citation-grounded eligibility assistant that I took from research and product requirements through to a clickable prototype and usability testing.

## Prototype

- **Figma prototype:** https://www.figma.com/proto/tU6K6R6hvXXKYm8HMV4Vhw/CivicAssist-screens?node-id=1-9&p=f&t=LlvvjTxW30p9H4c9-1&scaling=min-zoom&content-scaling=fixed&page-id=0%3A1&starting-point-node-id=1%3A9

- **Figma design file:** https://www.figma.com/design/tU6K6R6hvXXKYm8HMV4Vhw/CivicAssist-screens?node-id=0-1&t=uWaoyOeys430rxkP-1

## What's here

- `01-research-plan.md` — Research and documentation audit covering MahaDBT and the National Scholarship Portal (NSP).
- `02-persona-journey-map.md` — The persona and user journey built from the research.
- `03-PRD.md` — Product requirements, tied back to specific research findings.
- `04-scoping-note.md` — What I chose to include in v1, and what I left out.
- `05-usability-testing-plan.md` — The testing plan and findings from six informal sessions.
- `06-reflection.md` — What I learned from connecting the product work back to the original evaluation problem.
- `screens/civicassist-screens.html` — The HTML reference I used while building the Figma screens.

## How I approached it

The research started with a documentation audit of MahaDBT and the National Scholarship Portal rather than interviews. I looked for problems that were actually documented — things like applications getting stuck, uncertainty around income certificate validity, and applicants being given generic reasons for rejection.

That gave me evidence that these problems exist. It didn't tell me what it feels like to deal with them as an applicant, or what someone actually does when the system gives them an unclear answer. That's an important limitation of this first round.

I then built a small prototype around one idea: the assistant should be able to show when the evidence isn't enough to give a definite answer.

The usability testing was first-hand. I ran six informal sessions with friends using the live prototype. One thing I wouldn't have caught from the documentation showed up pretty quickly: two people initially read the amber uncertainty screen as a rejection/error screen before reading the text.

That changed the design. I kept the wording but changed the visual treatment to a cooler slate tone, and updated the Figma prototype and HTML reference.

## Status

The research, persona, PRD, and MVP scoping are complete.

The prototype has also been tested through six informal usability sessions, and the findings are documented in `05-usability-testing-plan.md` along with the design changes I made.

`06-reflection.md` documents what I learned from the process and how CivicAssist connects back to the original AI evaluation problem.

## License

This project is licensed under the MIT License.
