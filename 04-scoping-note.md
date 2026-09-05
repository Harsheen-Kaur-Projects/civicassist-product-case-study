# Scoping note — CivicAssist v1

## What v1 actually is

CivicAssist v1 is a citation-grounded eligibility assistant for one clearly defined domain: for example, one family of education scholarships, rather than every government service at once.

Someone describes their situation in plain language and gets an answer based on a fixed set of sources. The answer shows where the information came from and when that source was last updated. If the sources don't actually cover the person's situation, the assistant says so instead of guessing. It also gives them a document checklist based on what they've told it.

Keeping the scope narrow is important here. My earlier eval harness project showed me how easily an AI system can start making things up when it goes beyond what the source actually supports. In that project, the model invented a 12–24 month eligibility rule that wasn't in the source material.

So for CivicAssist, I'd rather have a smaller system that I can properly ground and test than a broad one that tries to answer everything.

## In scope

- Eligibility questions for one domain, using a fixed and curated set of sources
- A source citation for every factual answer, including the source date
- A clear uncertainty state when the available sources don't directly answer the situation
- A document checklist based on the person's situation
- Free-text input, so people can explain their situation in their own words

## Deliberately out of scope

- Multiple domains at once — this brings back the same problem I saw in the eval harness: once the system has to work across lots of different sources, it's harder to control what evidence it is actually using.
- Live monitoring of source changes — useful eventually, but unnecessary for a first prototype.
- Handoff to a live agent — this could make sense for genuinely ambiguous cases, but v1 can still give people a clear next step and tell them what needs to be verified.
- Multiple languages — important for a real public facing product, but translation accuracy would need its own testing rather than being added on top of an already untested system.
- Accounts or saved information — v1 is a one-time eligibility check, not an application portal.
- Open web retrieval — the assistant only uses the curated sources for this version. Opening it up to the wider web would make it much harder to control what evidence the answer is based on.

## Rough phases

1. Curate the sources — choose the domain, collect the relevant documents, and keep track of which versions are being used. Everything else depends on getting this part right.
2. Build the basic Q&A flow — let someone describe their situation and return an answer with its source. First make sure the answers stay grounded before adding more complicated behaviour.
3. Add uncertainty handling — introduce the state for cases where the sources don't actually give us enough information to answer. This is the part most directly connected to what the eval harness exposed.
4. Add the document checklist — turn the information from the conversation into a situation-specific list of what the person needs.
5. Test and iterate — put the prototype in front of people and see whether they actually understand the uncertainty state, notice the sources, and know what to do when the answer isn't clear.
