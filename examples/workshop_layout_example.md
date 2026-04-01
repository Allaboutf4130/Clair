Clair Example — Workshop Layout Planning
This example demonstrates how Clair processes a real‑world problem using its full cognitive pipeline.
The goal is not to produce the “perfect” workshop layout, but to show how Clair reasons, calibrates uncertainty, and verifies its own thinking.

🧩 Task
“How do I design a small workshop layout for woodworking?”

This is a practical, multi‑constraint problem involving safety, space optimization, and workflow.

🧠 1. Perception
Clair identifies the task type:

Category: spatial planning / workshop design

Constraints: limited space, tool placement, safety, workflow

Missing info: room dimensions, tool list, ventilation, power outlets

Required reasoning: multi‑step, constraint‑based

Output (example):

Code


Copy
TaskType: WorkshopLayout
KeyConstraints: Space, Safety, Workflow
MissingInfo: Dimensions, Tools, Ventilation
⚖️ 2. Affect
Clair evaluates risk and urgency:

Safety risk: medium

Complexity: moderate

Verification strictness: elevated

Reasoning depth: increased

Output (example):

Code


Copy
RiskLevel: Medium
VerificationRequired: True
ReasoningDepth: 2
🧩 3. Reasoning
Clair generates a provisional plan:

Place large stationary tools along walls

Keep central area open for assembly

Group dust‑producing tools near ventilation

Ensure 3–4 ft of clearance around table saw

Store hand tools near workbench

Keep lumber storage near entry

Provisional output:

Code


Copy
DraftLayout:
  - Table saw centered with clearance
  - Workbench near natural light
  - Dust tools near ventilation
  - Lumber storage by entry
  - Assembly area in center
🎚️ 4. Calibration
Clair checks for uncertainty:

Missing dimensions → high uncertainty

Unknown tool list → medium uncertainty

Safety constraints incomplete → verification required

Calibration output:

Code


Copy
Confidence: 0.42
UncertaintySources: MissingDimensions, MissingToolList
VerificationNeeded: True
🔍 5. Verification
Clair cross‑checks the plan:

Cross‑check against known workshop safety rules:
Table saw clearance: ✔

Dust collection: ✔

Tool grouping: ✔

Alternative reasoning path:
Try optimizing for minimal walking distance

Compare with original plan

No contradictions found

Verification output:

Code


Copy
Verified: Partially
Notes: Layout valid but incomplete without dimensions
🧠 6. Memory
Clair stores:

Verified workshop design heuristics

Confidence scores

Provenance (task → verification → outcome)

Memory entry example:

Code


Copy
Fact: "Table saw requires 3–4 ft clearance"
Confidence: High
Source: VerifiedSafetyRule
💬 7. Response
Clair produces a final answer with explicit uncertainty:

Final Output:

Here is a safe, efficient starting layout for a small woodworking workshop.
Some details remain uncertain because room dimensions and tool list were not provided.

Place the table saw in the center with 3–4 ft clearance

Put the workbench near natural light or a wall

Group dust‑producing tools near ventilation

Keep lumber storage near the entry

Leave the center open for assembly

Store hand tools near the workbench

If you provide room dimensions and your tool list, I can generate a precise layout.

⭐ What This Example Demonstrates
Clair’s structured pipeline

Honest uncertainty

Verification before output

Modular cognition

Real‑world reasoning

Safety‑aware planning

This example helps users understand how Clair thinks, not just what it outputs.

