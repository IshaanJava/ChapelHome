# Chapel Home — team guide

Independent student project; not affiliated with UNC.

## Run and maintain
No build step or dependencies are required. From the project root run:

    python3 -m http.server 8000 --directory dist

Open http://localhost:8000. Hash routes support Home, Explore, property detail, comparison, review submission, and About / Research. Source files: dist/index.html (shell), style.css (design), app.js (behavior), data.js (replaceable data).

Change the working name in data.js at CHAPEL_DATA.brand; also change the default HTML title and metadata if renaming. Edit properties and reviews in data.js. Preserve unique IDs and review-to-property IDs. Unknowns must stay null, not 0. Numeric property rent is a researched monthly amount, with basis and source to be documented before using it; distance is miles with a stated campus destination and method. Those numeric filters appear only when the property data supplies values. Do not copy historical self-reported rent into a current property price.

Current property sources (accessed November 7, 2026):
- Lark official overview: https://larkchapelhill.com/one-sheet/
- Lark features: https://larkchapelhill.com/features/
- Stratford Hills amenities: https://stratfordhillsapts.com/amenities/

Amenities are provider-reported, not independently verified. The homepage hero is an original illustration. Property cards and details use downloaded photos credited to property websites. Prices and numeric distances are deliberately not supplied. Five real properties appear: Lark, Stratford Hills, Union Chapel Hill, Bell Chapel Hill, and Mill Creek Condominiums. The user-provided Vivek and Maheb accounts are paraphrases, not direct quotes or invented demo reviews. Residence dates, lease status, topic ratings, and numeric rent were not supplied. Obtain permission for public attribution before expanding beyond this private prototype.

## Working features
- Responsive navigation, keyboard focus states, labeled forms, semantic headings and comparison table.
- Search by name or general location; supported housing-type and amenity filters; most-reviewed and recently-reviewed sorts. Unknown dates do not pretend to be recent. Numeric rent/distance filters and sorts appear when data exists; lease/sublease filtering appears when accounts supply status.
- Property details, transparent sources, unknown values, structured review topics, and checklist.
- Comparison for up to three properties (five currently supplied).
- Required-field validation, local reviews, local review flags, usability feedback, JSON export, and explicit local-data deletion confirmation.
- Unlisted-property submissions are retained for export, without inventing a researched property page.
- localStorage persistence when available, with honest session-only fallback messaging when unavailable.

## Simulated or limited
No backend, accounts, residency verification, public posting, shared database, moderation inbox, or automatic notification. Flags and feedback stay in the submitting browser. Checklist ticks reset on navigation. localStorage can be cleared by browser settings; export data to keep it. The two source accounts are not representative evidence. No aggregate star ratings or consensus claims are calculated. Do not use invented experience text in actual usability submissions; testers without experience can inspect the form or use a clearly marked test entry, then clear it.

## Before a public launch
Implement a shared database and API, server-side validation, submission consent and privacy/retention rules, human moderation and reporting workflow, spam prevention, secure access for moderators, deletion requests, and source update processes. Establish criteria for attributing and verifying accounts; consent does not itself verify residency. Separate test content from real submissions. Review accessibility with assistive technology. Decide how to collect feedback securely without unnecessary identifiers. Public launch requires an explicit audience change from this private deployment.

## Five-minute usability test
Facilitator: seek consent to take notes; record observations without unnecessary personal details. Say “We are testing the site, not you. Please think aloud.” Do not demonstrate the answer first.
- 0:00–0:30: Ask whether they are exploring housing, have lived off campus, or both.
- 0:30–1:30: “Find a property you would consider. Show how you would learn about it.” Observe search, filters, and navigation.
- 1:30–2:30: “Compare two of the five properties. What trade-offs do you see?” Observe selection and interpretation.
- 2:30–3:30: “What is missing? Find a question you would ask before signing.” Check whether they distinguish one account from a consensus and advertisements from verification.
- 3:30–4:30: “If you have a real experience, try submitting it. Otherwise inspect the form and tell us what you would need.” Allow optional fields to be skipped. Ask where they think the submission will appear.
- 4:30–5:00: “Leave usability feedback. What was most confusing? Where do you think this feedback went?” Export with consent if the team needs the file.
Record task completion, hesitation, misunderstanding, and suggested changes. Avoid coaching. Clear test data when finished if requested.

## Five neutral upperclassman survey questions
1. Where and during which term(s) did you live off campus, and was it a lease or sublease? You may skip identifying details.
2. What factors mattered most when choosing that housing?
3. How would you describe your experience? What worked well and what, if anything, was challenging?
4. How did your total housing costs compare with what you expected? Share a range only if comfortable.
5. What information would have helped before deciding, and where did you look for it?

Research findings placeholder: add dates, recruitment method, sample size, consent-approved quotations, themes, and limitations only after collecting evidence. Never invent results.

## Deployment and photo sources
Download chapel-home-source.zip from Our project and follow DEPLOYMENT.md for local preview, Netlify, or GitHub Pages. data.js contains original image URLs and source pages for every photo. Public research summaries are separate from team-provided reviews, never counted as new student submissions. They include dates and uncertainty.
