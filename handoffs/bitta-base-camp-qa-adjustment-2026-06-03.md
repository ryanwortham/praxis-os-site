# Message to Bitta — Base Camp embedded chat QA adjustment

Hey Bitta team — we tested the embedded Praxis Base Camp rep with this path:

Visitor: “Really dial in my systems.”
Rep: asked whether this meant business systems or personal/family.
Visitor: “Workflows and team roles, really.”
Rep: correctly routed to Business Guide.
Visitor: “All right. What do I need to do?”
Rep: displayed the full handoff summary to the visitor.

The route was correct, but the visitor-facing output needs to change.

Requested changes:

1. Please do **not** show the full handoff summary to the visitor.
   - Hide/remove visible fields like route confidence, boundary flags, Ryan activation, contact status, reviewer/internal notes, and detailed routing logic.

2. If the platform supports hidden/session-internal notes, put the full handoff summary there instead.

3. If hidden notes are not available, show only a short visitor recap and one backend-safe route label.

Preferred visible copy pattern:

> You’re in the right lane. This sounds like a Business Guide issue — workflows, team roles, and operating clarity. The next step is the Business Guide specialist, which can help organize where the system is unclear before a human follow-up.
>
> Session route label: Business Guide — Process / Systems Clarity

4. Please avoid saying “handoff summary” in visible visitor copy unless that handoff is hidden from the visitor.

5. Please check the opener behavior. The transcript showed two similar opening lines, which may be a platform greeting + rep greeting duplication or a prompt issue. We want one clean opener only.

6. Until the Business Guide specialist embed is actually installed/connected, Base Camp should not imply a seamless active transfer. Once the specialist embed exists, the visible next step should give the visitor a clear “continue here” action.

Overall: routing logic passed; handoff visibility and next-step wording need revision.
