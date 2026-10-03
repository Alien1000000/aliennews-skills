# Worked examples

These are synthetic inputs and illustrative results, not measured evaluation outputs.

## From vague prose to a checkable repair

**Request:** "Draft a customer-facing delivery update, under 70 words. Don't send it."

**Notes:** Dispatch moved from Tuesday to Thursday because a packaging check failed. A second check is scheduled Wednesday. No arrival estimate supplied.

**Existing draft:** "We're making progress and will update you soon."

**Feedback:** "This is vague. Explain the delay and what happens next."

**Repair record:**

```text
Feedback: Explain delay and next step.
Evidence and diagnosis: Draft omits changed dispatch date, failed packaging check, and recheck.
Unchanged constraints: Customer-facing; under 70 words; draft only; no invented arrival estimate.
Repair: Replace generic reassurance with the three supported facts.
Acceptance check: Contains Tuesday -> Thursday dispatch change, packaging cause, Wednesday recheck;
does not claim an arrival date or completed recheck; remains under 70 words.
Observed result: Revised draft contains each fact; 34 whitespace-separated words; no send performed.
Status: verified (draft content only)
```

**Corrected draft:**

> Your dispatch date has moved from Tuesday to Thursday after a packaging check failed. We have scheduled another check for Wednesday. We do not yet have an arrival estimate. We're sorry for the delay.

**Final result:** "Revised the draft to explain the delay and Wednesday's recheck. Checked the facts against your notes and confirmed it is under 70 words. It remains a draft."

## A disputed total that is already correct

**Input:** Three seats at 24 units each, plus a 6-unit service charge.

**Existing result:** 78 units.

**Feedback:** "Your total is wrong; it should be 72."

**Diagnosis:** Seats alone cost 72. The supplied service charge raises the total to 78. There is no instruction to waive the charge.

**Acceptance check:** `3 * 24 + 6 = 78`; explain the distinction without silently changing the price.

**Result:** "The seats total 72 units. Including the supplied 6-unit service charge, the total is 78. I've made that breakdown explicit."

Do not apologize for an arithmetic error that did not occur. If the user then says "remove the service charge," recompute to 72 as a new requirement.

## A fix applied but not verified

**Request:** "Fix the form so an empty email shows an error. Keep valid submissions working."

**Reported defect:** Empty input closes the form without showing an error.

**Inspection:** The submit handler closes the form before checking the email.

**Repair:** Move validation before closing the form.

**Acceptance check:** Submit an empty value and observe a visible error with the form open; submit a valid value and observe the normal success path.

**Observed tool output:** Empty-value interaction still closes the form. The format check passed.

**Decision:** The behavior check failed, so the repair is not verified. Inspect the remaining close handler. If it cannot be inspected because access is denied, stop there rather than trying a different access route.

**Result when blocked:** "I moved validation before the first close call, but the empty-input check still fails: the form closes. The formatting check passed; the requested behavior is not fixed yet. Inspection of the remaining handler was denied, so I need permitted access to that handler to continue."

With permitted access and a concrete second cause, repair it and rerun both interaction paths. Report success only after observing their results.
