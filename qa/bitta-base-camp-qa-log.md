# Bitta / Praxis Base Camp QA Log

## 2026-06-03 — Embedded Base Camp chat: Business Guide routing / Ryan test

### Transcript summary
Visitor wanted to “really dial in my systems.” Base Camp clarified whether this meant business systems or personal/family systems. Visitor answered: “Workflows and team roles, really.” Base Camp correctly routed to Business Guide. When visitor asked “All right. What do I need to do?”, Base Camp exposed a full handoff summary.

### What passed
- Correctly recognized “systems,” “workflows,” and “team roles” as business operations / growth-readiness pressure.
- Asked one useful clarifying question before routing.
- Correct route: `Business Guide`.
- Did not ask for duplicate contact info.
- Did not give regulated advice.

### Changes needed
1. **Remove visitor-facing internal handoff summary.**
   - Current output showed: Route, Confidence, Why this route, Visitor fields, Contact status, Boundary flags, Ryan activation, recommended next action.
   - These should be hidden/session-internal only, not shown to the visitor.

2. **Replace handoff with short visitor-facing next-step copy.**
   - Preferred visible pattern:
     > You’re in the right lane. This sounds like a Business Guide issue — workflows, team roles, and operating clarity. The next step is the Business Guide specialist, which can help organize where the system is unclear before a human follow-up.
     >
     > Session route label: Business Guide — Process / Systems Clarity

3. **Do not mention “handoff summary” to the visitor unless Bitta can hide it.**
   - If Bitta supports hidden/session notes, put the detailed handoff there.
   - If Bitta does not support hidden notes, use only the short route label above.

4. **Remove internal metadata from visible copy.**
   - Do not show: confidence, boundary flags, Ryan activation, reviewer notes, cross-lane context, “contact status,” or internal routing logic.

5. **Make the next action concrete once the specialist page is ready.**
   - Current line “continue into the Business Guide” is not enough if the rep cannot actually transfer or link.
   - When the Business Guide specialist embed exists, visible output should tell the visitor exactly how to continue.
   - Until then, Base Camp should not imply a seamless active transfer.

6. **Check duplicate/repeated opener behavior.**
   - The transcript showed two similar openers:
     - “I can help you get oriented...”
     - “I’m here with you...”
   - Ask Bitta whether this is platform greeting + rep greeting duplication, transcript artifact, or prompt behavior. The visitor should see only one clean opener.

### Bitta request / question
Please confirm whether Bitta supports hidden/session-internal handoff notes separate from visitor-visible chat text. If yes, we want the full handoff stored there and only a short visitor recap shown. If not, we want Base Camp to show only a short recap plus a backend-safe route label.

### Status
Needs Bitta prompt/platform revision before this behavior is considered ready for meaningful traffic.
