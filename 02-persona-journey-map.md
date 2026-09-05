# Persona and journey map

This persona is based on the problems identified in `01-research-plan.md`. Ananya is a working persona, not someone I interviewed, so the details here are meant to represent a realistic user situation rather than describe a real individual. A few specific behaviors referenced later, like checking a source before trusting an answer or missing the update date until it was pointed out are drawn from real conversations during usability testing, tagged `[Interview]` in `03-PRD.md`. The persona itself is still a composite, not a real person.

## Ananya Sharma, 20

Ananya is a final-year undergraduate student living in Navi Mumbai. She's applying for a MahaDBT scholarship to help cover her college fees.

She has already started looking through the MahaDBT and NSP websites, but she's finding it difficult to tell what actually applies to her. The information is spread across different pages, the wording is fairly formal, and some of the requirements aren't very clear until she starts thinking about her own situation.

Her main concern is making a mistake in the application and finding out later that she was missing something.

A few things are making that harder:

- Her family's income hasn't been completely consistent during the year, so she's not sure how neatly it fits into the income requirements. *(Finding 1)*
- She has an income certificate already, but isn't sure if it's still valid for the scheme she's applying for. *(Finding 2)*
- She's seen scholarship applications get stuck because of portal errors, without it being clear whether there was actually a problem with the application. *(Finding 3)*
- The document lists are long, and she isn't sure which ones she actually needs to submit. *(Finding 4)*

## The journey

### 1. Trying to figure out what applies

She starts with Google, MahaDBT and NSP, looking for the scholarship that matches her category and college.

She can find the information, but it takes some effort to piece it together. There are lots of scheme pages and different requirements, and it's not always obvious which details matter for her.

**CivicAssist:** She starts by describing her situation instead of trying to work out the right category first. The assistant uses that information to narrow down what may apply.

### 2. Checking whether she qualifies

Once she has a possible scheme, she wants to know whether her particular situation fits the rules.

This is where a simple yes/no answer isn't always enough. For example, if her family's income changed during the year, she needs to know whether that affects the requirement and what the actual rule says.

**CivicAssist:** The answer is tied to a specific source and clause, with the source's last-updated date shown alongside it. She can see what the answer is based on rather than having to take it on trust.

### 3. Running into something the rules don't explain

She then reaches a situation where the available information doesn't give a clear answer.

Maybe there were two separate gaps in family income during the year, but the published rule only talks about one. At this point, a normal system might still force the situation into a yes or no answer.

That creates a bigger problem: is she actually not eligible, or does the system just not have enough information to tell?

**CivicAssist:** Instead of turning an unclear case into a rejection, the assistant shows that the answer is uncertain and explains what she can do next.

### 4. Working out what to submit

After that, she still needs to gather her documents.

The general checklist has more items than she expects, and she's tempted to collect everything just to be safe. She doesn't want to leave something out and have her application rejected later.

**CivicAssist:** The checklist is based on the situation she has described. Each document has a short explanation of why it's needed, so she can understand the list instead of just ticking boxes.

## What this journey tells me

Ananya's situation points to a fairly simple product direction:

- Let people explain their situation in their own words.
- Show the source behind an eligibility answer.
- Make the difference between “not eligible” and “not enough information” obvious.
- Show when the source was last updated.
- Give people a document list that is relevant to their situation.
- Give them something useful to do when the answer isn't clear.
