# ELP — Per-Screen Descriptions (for Figma)

A description block for every frame in the export, to place under each screen in Figma. Each block: **Purpose · Design decision · States · MVP.** Mapped one-to-one to the 69 frames, in the export's order and grouping.

> **Note — income/business screens:** this export is the **Practitioner** view, so the principal-only money screens (Add income or expense, Who's paid, Set fees, Month summary) are **not** in this frame set. Capture a **Principal-role export** to add them; descriptions for those are at the end so they're ready to drop in.

---

## Onboarding & authentication

**1. Loading**
Purpose: session gate on launch — decides where the user lands. Decision: routes to Home (valid session), unlock (PIN set), or sign-in (none); works offline. States: checking, → routed. MVP: offline-first, long-lived auth.

**2. Enter phone number**
Purpose: the single entry point (serves sign-in *and* sign-up). Decision: one field the user knows — no username/password to invent. Prefilled +27. States: empty, typing, invalid. MVP: phone-based minimal entry.

**3. Enter the code (OTP)**
Purpose: verify the number. Decision: 6-digit auto-advancing code; wrong code is retriable, nothing locks; resend timer. States: empty, entered, wrong code, resend, change number. MVP: OTP-verified sign-in, no lockouts.

**4. Terms & consent**
Purpose: evidenced agreement to terms & privacy. Decision: three plain points + links to full docs (replacing the old legal walls); one checkbox. States: default, not-agreed (checkbox flags). MVP: consolidated consent, POPIA.

**5. WhatsApp consent**
Purpose: explicit opt-in for WhatsApp Business messaging. Decision: a *separate, skippable* step — declining blocks nothing, withdrawable later. States: agree, skip. MVP: explicit evidenced WhatsApp/Meta consent.

**6. Create a PIN**
Purpose: optional quick-unlock. Decision: skippable (an offer, not a wall); confirm step so it can't be set by mistake; works offline. States: create, confirm, mismatch (reset, no lockout), skipped. MVP: PIN unlock, offline.

**7. Checking your details**
Purpose: brief interstitial while the account resolves. Decision: routes to *You've been invited* (WL) or *Your name* (self-declare). States: checking → routed. MVP: two entry paths.

**8. You've been invited**
Purpose: confirm a pre-loaded record (invited/WL). Decision: "Is this you?" against name/role/site; "This isn't me" branches to self-declare. States: confirm, reject. MVP: invited path.

**9. Number not recognised**
Purpose: handle a number with no pre-loaded record. Decision: informational, routes to self-declare or help — never a dead end. States: not-found. MVP: inform-don't-block; shared-number handling.

**10. Your name**
Purpose: self-declare identity (OA). Decision: minimal — first/last name only. States: empty, entered. MVP: self-declare path, minimal entry.

**11. Your role**
Purpose: set Practitioner or Principal. Decision: **two cards, teaching derived** — recognition over branching questions; classification data (owner/teaches) written behind the choice; no Assistant. States: practitioner, principal. MVP: role classification.

**12. Your preschool**
Purpose: minimal site creation (principal). Decision: one field — "What's your preschool called?" — changeable later; fuller details scaffolded. States: empty, entered. MVP: stripped-down onboarding (name + one class).

**13. Preschool code**
Purpose: join an existing site (practitioner). Decision: join by QR/code — no long setup. States: empty, invalid code, joined. MVP: join by tenant link/QR.

**14. Add your ID document — onboarding**
Purpose: identity capture for safeguarding tenants. Decision: document-type selector + SA-ID checksum (derives DOB); **non-blocking, deferrable** ("do this later"); only hard gate is closed-tenant mismatch. States: valid, invalid (inline), passport/other, closed-tenant mismatch, offline, deferred. MVP: identity document, required for SmartStart, optional/config for OA.

**15. All set**
Purpose: confirm completion, route to Home. Decision: surfaces deferred items as "complete your profile." States: done. MVP: scaffold-over-time.

**16. Unlock with PIN**
Purpose: fast re-entry for returning users. Decision: PIN unlock works offline; Forgot-PIN recovers by OTP. States: enter, wrong PIN (retriable), forgot. MVP: PIN unlock, no lockouts.

**17. Reset your PIN**
Purpose: recover a forgotten PIN. Decision: re-verify by OTP, then set a new PIN — no lockout. States: verify, set new. MVP: forgiving recovery.

**18. Opening**
Purpose: straight-to-Home path (valid session, no PIN). Decision: no friction when none is needed. States: opening. MVP: returning-user routing.

**19. Returning user flow** *(annotation frame)*
Purpose: documents the three returning-user outcomes (unlock / straight-to-home / sign-in). Not an app screen — a decision-flow note. Keep as reference.

**20. The full flow** *(annotation frame)*
Purpose: the end-to-end onboarding map. Reference annotation, not an app screen.

---

## Home

**36. Home — register due (default)**
Purpose: tell the practitioner the single most important thing now. Decision: one context-aware **Today card** (overline + one-line + primary button) + a quiet "a few things need a look" line; **no category tiles**. Priority ladder picks the card. States: this is the default (register). MVP: daily loop, one primary action.

**37. Home — consent imminent**
Purpose: same home, re-prioritised. Decision: a consent deadline outranks the register, so consent becomes the hero — demonstrates context-awareness. States: consent-urgent. MVP: time-critical consent surfaced.

**38. Home — all clear**
Purpose: reassurance when nothing needs doing. Decision: a calm "you're all caught up" — calm is the reward, not a blank screen. States: all-clear. MVP: low cognitive load.

**39. Home — month start**
Purpose: principal/oversight prompt at month start (e.g. "who's paid?"). Decision: surfaces the month's money task when relevant. States: month-start. MVP: fee tracking prompt.

**40. Menu**
Purpose: the long-tail navigation (☰). Decision: everything rarer than the bottom-bar destinations lives here — keeps Home focused. States: open. MVP: hybrid hub + bar.

**43. Needs a look — all** *(list)*
Purpose: the full "things that need attention" list behind the Home line. Decision: aggregates incomplete registrations, approaching consent deadlines, cover needs. States: has-items, empty. MVP: proactive flagging of incomplete records.

---

## Classes & children

**44. Classes**
Purpose: see and open classes. Decision: classes live in the classroom section, not profile; counts derived. States: list, empty. MVP: class management.

**45. Class detail**
Purpose: a class roster + launch attendance. Decision: opens the register; shows the children in the class. States: roster, empty. MVP: per-class attendance.

**46. Add a class**
Purpose: create/edit a class. Decision: name (free text, no age bands), active days + times (filter attendance), assign practitioner; empty class allowed; no ratios. States: create, edit. MVP: class creation rules.

**47. Child profile**
Purpose: the record for one child. Decision: minimum shown, rest scaffolded; consent status; mark-as-left. States: complete, incomplete (flagged), left. MVP: child registration + management.

**48. Butterflies** *(class example)*
Purpose: an example class-detail frame (named class). Decision: same pattern as Class detail. States: roster. MVP: class management.

**49. Child — personal information**
Purpose: view/edit the child's details. Decision: minimum required; DOB drives age; child ID optional. States: view, edit. MVP: minimum registration fields.

**50. Child — your notes**
Purpose: free-text notes on a child. Decision: optional, practitioner's own notes. States: empty, has-notes. MVP: optional fields.

**51. Child — no longer attending (mark as left)**
Purpose: deactivate a child. Decision: easy and **reversible**; single free-text reason; no automated deactivation (operator owns the data). States: confirm, left. MVP: easy deactivation.

---

## Attendance

**52. Take attendance**
Purpose: the daily register. Decision: **all default present, tap to mark absent, submit** — fastest register for paper users; single owner per class; **incomplete registration and missing/overdue consent are flagged, never blocked**. States: all-present, some-absent, incomplete flag, consent flag (with "send consent request" alongside the mark), submitted. MVP: attendance always recordable (decision #2).

**53. Attendance saved**
Purpose: confirm the register is recorded. Decision: reassures, and confirms it will sync if offline. States: saved, saved-offline. MVP: offline-first.

**54. Register status**
Purpose: see which registers are done/incomplete per class. Decision: submitted and incomplete visible. States: complete, incomplete. MVP: submitted/incomplete visibility.

**55. Change a register**
Purpose: edit a past register. Decision: editable correction. States: editing. MVP: edit past attendance.

---

## Child registration & consent

**56. Share a registration link**
Purpose: send registration to a caregiver. Decision: practitioner shares a link (e.g. WhatsApp); caregiver completes the child's details on the web form. States: share, copied. MVP: caregiver self-registration.

**57. Registration links**
Purpose: track links shared and their status. Decision: shows pending/completed self-registrations. States: pending, completed. MVP: partial-registration visibility.

**58. Consent — class**
Purpose: consent status across a class. Decision: shows who has/needs consent. States: mixed, all-consented. MVP: consent gates the record.

**59. Send consent request**
Purpose: request consent from a caregiver. Decision: one-tap request; available alongside attendance (never blocks it). States: send, sent. MVP: consent request.

**60. Consent sent**
Purpose: confirm the request went out. States: sent. MVP: consent lifecycle.

**61. Consent deadline warning**
Purpose: warn that a consent deadline is approaching. Decision: informational escalation; after the deadline, unconsented data is deleted (records/backend). States: approaching, overdue. MVP: consent deadline + deletion.

**62. Consent received**
Purpose: confirm consent captured; the record becomes fully usable. States: received. MVP: consent gates usability.

**63. Messaging · consent (caregiver)**
Purpose: the caregiver's messaging opt-out. Decision: a caregiver can opt out of WhatsApp / withdraw consent at any time. States: on, withdrawn. MVP: withdrawable messaging consent.

---

## Resources

**21. Resources — categories**
Purpose: the info-corner entry, by category. Decision: categorised (Running your preschool, Early learning activities, Health & safety, Funding & subsidies). States: list. MVP: resources ('info corner').

**22. Resources — list**
Purpose: resources within a category. Decision: name, description, link, data-free flag; like + flag-broken. States: list, empty. MVP: resource attributes.

**23. Resource detail**
Purpose: a single resource. Decision: opens the link; if not data-free, warns first; like / report-broken. States: default, data-warning. MVP: data-free flag.

**64. Resources** *(hub/tab)*
Purpose: the Resources tab landing. Decision: same taxonomy as the categories screen. States: default. MVP: resources.

---

## Feedback & notifications

**24. Feedback — type**
Purpose: choose feedback kind. Decision: bug vs programme (idea). Routing differs. States: select. MVP: feedback loop.

**25. Feedback — write**
Purpose: write the feedback. Decision: title + body. States: empty, entered. MVP: feedback capture.

**26. Feedback sent**
Purpose: confirm submission (queues offline). States: sent, queued-offline. MVP: offline-first feedback.

**27. My feedback**
Purpose: list the user's feedback and its status. States: list, empty. MVP: full feedback visibility.

**28. Feedback thread**
Purpose: follow a feedback conversation. Decision: bug → admin; programme → coach + admin; replies appear here. States: open, replied. MVP: feedback routing.

**41. Notifications**
Purpose: reminders and coach-visit records. Decision: registers, consent deadlines, visits — nothing else; coach-visit record is WL-only. States: list, empty. MVP: nudges + coach visit record.

**42. Notification settings**
Purpose: control nudge volume. Decision: channel + volume — every nudge needs a purpose. States: default. MVP: tightly controlled nudges.

---

## Staff & site (principal)

**29. Staff list**
Purpose: see practitioners at the site. Decision: view + profiles; WL/OA distinction and practitioner states preserved. States: list, empty. MVP: staff management.

**30. Staff — mark on leave**
Purpose: mark a practitioner on leave. Decision: keeps the class covered by triggering reassignment. States: mark, on-leave. MVP: basic leave/absence.

**31. Reassign classes**
Purpose: move a class to another practitioner. Decision: so attendance continues. States: select, reassign. MVP: reassign so attendance can be taken.

**32. Classes reassigned**
Purpose: confirm reassignment. States: done. MVP: leave handling.

---

## Profile

**33. Profile — onboarding**
Purpose: the profile completeness prompt post-onboarding. Decision: a completeness card with one next action; scaffold, not nag. States: items-remaining, complete. MVP: scaffold-over-time.

**65. Profile — app**
Purpose: the profile home in daily use. Decision: sections (personal, contact, site, network, messaging), help, switch, sign out. States: default. MVP: profile management.

**66. Personal details**
Purpose: view/edit name (and role). Decision: editable, minimal. States: view, edit. MVP: profile fields.

**67. Contact**
Purpose: cell number + optional email. Decision: editable. States: view, edit. MVP: contact info.

**68. Network details**
Purpose: show club and coach/mentor. Decision: **read-only, tenant-set** ("set by [tenant]") — visible but not editable. States: populated, empty. MVP: network details visible-not-editable.

**69. Messaging & consent**
Purpose: the user's *own* messaging consent. Decision: see and **withdraw their own WhatsApp consent at any time** (blocks nothing); Terms/Privacy links. Distinct from the caregiver opt-out. States: on, withdrawn, offline. MVP: withdrawable messaging consent (POPIA).

---

## Leave programme

**34. Leave programme**
Purpose: a practitioner leaves a site. Decision: leaving lets them establish or join a new site. States: default. MVP: practitioner can leave.

**35. Leave — confirm**
Purpose: confirm leaving. Decision: clear consequence, reversible path to a new site. States: confirm. MVP: leave → new site.

---

## To add from a Principal-role export (income/business — not in this set)

**Income dashboard** — money in/out this month + route to summary; simple, not a budgeting tool. MVP: §3.5 income.
**Add income or expense** — unified: income/expense → type → amount → date; income types fees/subsidy/stipend/donation/other. MVP: unified capture (decision #3).
**Who's paid** — monthly checklist auto-populated from expected fees. MVP: 'which caregivers paid?'.
**Set fees** — per class (age group), adjustable per child, bulk-updatable. MVP: fees per class + per child.
**Month summary** — money in, out, what's left; no exports. MVP: simple summary.
**Site details (editable)** — programme/site name, optional location + 'same as home address' toggle; owned by principal here. MVP: site info.
