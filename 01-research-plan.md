# Research: MahaDBT and NSP

I looked at MahaDBT and the National Scholarship Portal (NSP) to understand where students can get stuck while trying to figure out scholarship or fee-concession eligibility.

I used publicly available documentation and reporting, and kept the findings tied to sources that someone else can check.

## Finding 1: Income doesn't always fit neatly into a category

MahaDBT has more than 68 schemes, with different income limits and eligibility categories. Many of these schemes require a Family Income Certificate for a particular financial year, issued by a Tahsildar or Sub-Divisional Officer. (Buddy4Study; DBIT's EBC scheme page)

The problem is that a certificate gives the system a fixed version of someone's financial situation. Real situations can be less straightforward: seasonal work, a parent between jobs, or income that changes during the year.

There isn't much room to explain that context.

For CivicAssist: I added free-text input (M4), so applicants can explain their situation instead of having to fit everything into predefined fields.

## Finding 2: It's not always clear whether a document is still valid

NSP's troubleshooting material says that there isn't one consistent rule for how long an income certificate remains valid. The requirement can vary by state, ministry, or district.

That creates uncertainty for applicants. A certificate that works for one scheme may not necessarily work for another, and it isn't always obvious when the requirement has changed. (Short Trick Science; NSP guidance)

There's also a timing problem. An income certificate can take around 7–15 days to issue, while a caste validity certificate can take 3–6 months. (MahaDocGuide)

So the question isn't just “Do I have the document?” It can also be “Is this version still acceptable?”

For CivicAssist: the source's last-updated date is shown next to the citation, so users have some context for how current the information is.

## Finding 3: A rejection and a system error can look the same

This was the finding that connected most directly to the problem that started this project.

During the MahaDBT 2.0 rollout, reporting showed that 2,246 applications in Vidarbha were stuck during 2025–26 because of portal errors. Students had to follow up with their colleges to try to get their applications moving again. (The Live Nagpur, “Thousands of SC/ST Students in Vidarbha Stuck Without Scholarships Due to MahaDBT Portal Errors,” May 2026)

NSP's error documentation also shows that things which look like a rejection to a user such as a blank dashboard or missing application can sometimes be caused by backend or synchronisation problems instead. (College Simplified)

From the applicant's perspective, those are very different situations:

“Was I rejected, or does the system just not know what's happening?”

That's the distinction I wanted CivicAssist to make visible.

For CivicAssist: M2 gives the assistant a separate uncertainty state. If the available evidence isn't enough to say that someone is ineligible, the product shouldn't turn that uncertainty into a rejection.

This is the main product lesson I carried over from my evaluation harness: when the system doesn't know, it shouldn't fill the gap with a confident answer.

## Finding 4: A generic checklist doesn't tell people what applies to them

NSP lists document mismatches among the reasons an application can be rejected. There are also third-party sites that help applicants work out which documents from the larger list actually apply to them. (NSPStatus; MahaDocGuide)

Knowing the full list of possible documents isn't the same as knowing which documents I need for my situation.

For CivicAssist: the checklist is based on what the applicant has described, and each item includes a reason for why it's needed.

The goal is to give someone a useful list for their situation, rather than another long checklist with everything on it.

## What these findings led to

The four findings pushed the product in a fairly consistent direction:

- Let people explain situations that don't fit neatly into predefined categories.
- Show where the information came from and how current it is.
- Separate “not eligible” from “there isn't enough evidence to tell.”
- Give people a document checklist that reflects their situation.

Those became the core requirements for the first version of CivicAssist.
