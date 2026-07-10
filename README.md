# 426-project-JandJ

### Team name: JandJ

### Team Roster

| Email                | GitHub Username |
| :------------------- | :-------------- |
| jkaros@umass.edu.com | sh34v3          |
| jjpark@umass.edu     | rainwater75     |

### Domain Review

The domain your team wants to simulate (what kind of system is this?)
The scalability problem this domain faces (what would make a single server insufficient?)
Why this domain is meaningful from a Computing for the Common Good standpoint (who benefits when the system works well, and who is affected when it does not?)

Option 1: AnkiTeacher Share

Anki is a widely used spaced repetition software that allows flashcard decks to be easily shared. The application tracks retention statistics for each card individually and can help students optimize their learning by economizing their reviews and hone in on what current understandings are not solidifying. Presently, Anki is mostly accessible for mature learners with autodidatic skills and metacognitive understanding of their learning. The user needs to be able to formulate cards, and then upon failure identify "why" they don't understand a given card, learn more, simplify, and then reformulate. These skills are advanced usually not well developed enough in teenagers and younger populations. To do so, they likely would need periodic attention from their teacher. A potential project could be a web application that allows a teacher to create "classrooms" for students to participate in. The teacher could distribute Anki decks to their students at an appropriate pace. A small addon for Anki could be created that gathers repetition statistics for each individual card and send it back to the web application. The teacher could then analyze these statics on a student basis--"what is this person not retaining well"--or on a card basis--"which cards are not being retained well by all". This would allow the teacher to refine the delivery of their material while also tracking student progress and mastery. In the case of wide use of this application, a distributed system would certainly be necessary as to allow concurrent access of content.

Option 2: TOPA matching

The state of Massachusetts very recently passed the Tenant Opportunity to Purchase Act (TOPA). When a landlord decides to sell a multi-family rental building, the tenants living there are given the first opportunity to buy it before it can be sold to an outside private developer or investor. Furthermore Tenants are allowed to pass (or assign) their "right of first refusal" (RFR) to a local housing authority, a land trust, or an affordable housing non-profit (the assignee). The asignee then buys the building and keeps the current tenants in place.

While this is certainly beneficial for tenants, it's very difficult to approach the process of passing RFR to an assignee.

TOPA laws operate on incredibly tight legal deadlines. In most jurisdictions, when a landlord announces an intent to sell, tenants usually have a narrow window (often just 30 to 45 days) to legally form a tenant association, vote, and file an official "Statement of Interest."

If they decide to assign their rights, the assignee has a limited timeframe (frequently 60 to 90 days) to match the outside buyer's appraisal, secure funding, and close the deal. Real estate transactions involving non-profits or public funds rarely move that fast, and missing a deadline by even one day forfeits the tenants' rights entirely.

To exercise or assign TOPA rights, a solid majority of households in the building must actively cooperate. Getting dozens—or hundreds—of neighbors to agree on a single path forward is a massive community-organizing challenge.

A web application that allows Tenants to quickly organize and to collectively communicate, vote, and file a statement of interest, while also helping match a group of tenants appropriate asignees.
