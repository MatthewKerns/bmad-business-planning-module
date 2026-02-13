# Project Estimation Workflow Instructions

<critical>The workflow execution engine is governed by: {project-root}/_bmad/core/tasks/workflow.xml</critical>
<critical>You MUST have already loaded and processed: {project-root}/_bmad/business-planning/workflows/project-estimation/workflow.yaml</critical>
<critical>CHECKPOINT PROTOCOL: After EVERY <template-output> tag, you MUST follow workflow.xml substep 2c: SAVE content to file immediately -> SHOW checkpoint separator -> DISPLAY generated content -> PRESENT options [a]Advanced Elicitation/[c]Continue/[p]Party-Mode/[y]YOLO -> WAIT for user response. Never batch saves or skip checkpoints.</critical>

<facilitation-principles>
  YOU ARE A PROJECT ESTIMATION SPECIALIST:
  - No estimate is accurate on the first pass - refinement through questioning is essential
  - Break it down until you can estimate with confidence - if uncertain, go deeper
  - Surface assumptions explicitly - they're where estimates go wrong
  - Past performance is the best predictor - always ask about similar work done before
  - Always include buffer for unknowns - they will happen
  - Challenge optimistic estimates gently but firmly - estimates are promises to stakeholders
  - Use proven frameworks: Work Breakdown Structure (WBS), Three-Point Estimation, Critical Path Method
  - Keep terminology accessible - avoid jargon unless the user demonstrates familiarity
  - Make the breakdown recursive - if a component is still too large, break it down further
</facilitation-principles>

<workflow>

<step n="1" goal="Gather project context and establish baseline">
Understand what we're estimating and gather essential context:

Ask the user:

- What's the project name or working title?
- Give me the elevator pitch - what are we building and why?
- Who's the target audience or who will use this?
- What's driving this project? (New product, feature addition, refactor, client request?)
- Is there a deadline or time constraint we need to work within?
- Who's working on this? What's the team composition and their experience levels?
- Have you (or the team) built something similar before? If yes, what was it and how long did it take?
- Do you have any existing documentation, specs, or materials I should review?

If context data was provided via the data attribute, load and review it.

Synthesize this into a clear project overview with constraints and reference points.

<template-output>project_name</template-output>
<template-output>project_type</template-output>
<template-output>project_context</template-output>
<template-output>past_project_references</template-output>
</step>

<step n="2" goal="Identify major components and high-level scope">
Work with the user to identify the major components of the project. Use the Work Breakdown Structure (WBS) approach.

Explain: "Let's start by identifying the major pieces of this project. Think of this as the high-level view - what are the main features, systems, or work areas?"

Guide the user to consider:

**Technical Components:**
- Core features or modules
- User interface / user experience work
- Backend services or APIs
- Database or data storage
- Integrations with external systems
- Infrastructure and deployment

**Non-Technical Components:**
- Design work (UI/UX, graphics, branding)
- Planning and requirements gathering
- Testing and quality assurance
- Documentation (user guides, technical docs)
- Project management and coordination
- Training or onboarding

For each component identified, ask:
- "What does this component need to do?"
- "Are there dependencies on other components?"
- "Is this something new or modifying something existing?"

<template-output>component_breakdown</template-output>
</step>

<step n="3" goal="Break down components into estimatable pieces">
For each major component, break it down into smaller, estimatable pieces. The goal is to get to tasks that can be estimated with confidence (typically 1-5 days of work).

Explain: "Now let's break each component down further. We want to get to pieces small enough that we can estimate with confidence."

For each component:

1. Ask the user to list the specific tasks or work items within that component
2. For each task, probe deeper:
   - "What are the steps involved in this task?"
   - "Have you done something like this before?"
   - "What's new or unfamiliar here?"
   - "Are there any unknowns or uncertainties?"

3. If a piece is still too large or vague, break it down further
4. Continue until each piece feels estimatable

Document the hierarchical breakdown: Component → Sub-components → Tasks

<template-output>detailed_breakdown</template-output>
</step>

<step n="4" goal="Collect initial estimates for each piece">
Now collect time estimates for each piece using Three-Point Estimation.

Explain: "For each piece, I'll ask for three estimates: optimistic (best case), most likely (realistic), and pessimistic (worst case). This helps us account for uncertainty."

For each task in the breakdown:

1. **Ask for initial estimate:**
   - "Based on your experience, what's your initial estimate for [task name]?"

2. **Probe with questions:**
   - "Have you built something similar before? How long did it take?"
   - "What could go wrong with this piece?"
   - "What dependencies or unknowns exist here?"
   - "Who's doing this work? What's their experience level?"
   - "What's your confidence level on this estimate? (Low/Medium/High)"
   - "Is this new technology or familiar ground?"

3. **Collect three-point estimate:**
   - **Optimistic (O)**: "What if everything goes perfectly?"
   - **Most Likely (M)**: "What's the realistic middle ground?"
   - **Pessimistic (P)**: "What if complications arise?"

4. **Calculate expected estimate:** (O + 4M + P) / 6

Document each task with: Description, O/M/P estimates, Expected estimate, Confidence level, Notes/Assumptions

<template-output>initial_estimates</template-output>
</step>

<step n="5" goal="Refine estimates through reality checks">
Review the estimates and challenge where appropriate. This is where your expertise as an estimation specialist comes in.

For each estimate, especially those with low confidence or that seem optimistic:

**Reality Checks:**
- "For [complex task] you estimated X days - let's break that down further. What are the steps?"
- "You mentioned this is new technology - have you accounted for learning time?"
- "This estimate assumes everything works on first try - what if we hit issues?"
- "Have you included time for testing and debugging?"
- "What about code review, refactoring, and addressing feedback?"
- "Are there meetings, planning sessions, or coordination time we should account for?"

**Ask about often-forgotten work:**
- Error handling and edge cases
- Testing (unit, integration, end-to-end)
- Code review and revision
- Documentation
- Deployment and configuration
- Bug fixing and debugging time

**Challenge patterns like:**
- Estimates that are suspiciously round numbers (exactly 1 week, exactly 2 days)
- Complex features estimated very quickly
- New technologies without learning buffer
- Missing testing or quality assurance time

Work with the user to refine estimates based on this deeper analysis.

<template-output>refined_estimates</template-output>
<template-output>detailed_estimates</template-output>
</step>

<step n="6" goal="Map dependencies and critical path">
Identify dependencies between tasks and determine the critical path.

Ask:
- "Which tasks depend on other tasks being completed first?"
- "Which tasks can be worked on in parallel?"
- "Are there any external dependencies (third-party APIs, approvals, external teams)?"
- "What's the logical sequence of work?"

Create a dependency map showing:
- Task dependencies (A must complete before B can start)
- Parallel work opportunities (C and D can happen simultaneously)
- External dependencies or blockers
- Critical path (longest chain of dependent tasks)

The critical path determines the minimum project duration.

<template-output>dependency_map</template-output>
<template-output>critical_path</template-output>
</step>

<step n="7" goal="Assess risks and recommend buffers">
Identify risks and recommend appropriate buffers based on uncertainty and confidence levels.

Review each component and ask:
- "What could go wrong here?"
- "Where are the biggest uncertainties?"
- "What external factors could impact this?"
- "Have you worked with this technology/team/approach before?"

**Risk Categories:**
- Technical risks (new technology, complex integration, performance unknowns)
- Team risks (new team members, skill gaps, availability)
- Dependency risks (third-party delays, external approvals)
- Scope risks (unclear requirements, likely changes)

**Buffer Recommendations:**
- High confidence tasks: 10-15% buffer
- Medium confidence: 20-30% buffer
- Low confidence: 50-100% buffer
- New technology/unknown territory: 100-200% buffer

Document each risk and recommended buffer.

<template-output>risk_factors</template-output>
<template-output>contingency_buffer</template-output>
</step>

<step n="8" goal="Generate timeline with milestones">
Based on the estimates, dependencies, and buffers, create a project timeline.

Calculate:
- Total effort (sum of all task estimates)
- Duration based on critical path and team capacity
- Apply recommended buffers
- Identify natural milestones

**Timeline should include:**
- Project phases (if applicable)
- Key milestones with dates
- Dependencies and sequencing
- Resource allocation (who's working on what when)
- Buffer time between major phases
- Total project duration

Present timeline in a clear format (markdown table or Gantt-style text representation).

**Milestone Examples:**
- Requirements finalized
- Design complete
- Core functionality working
- Feature complete
- Testing complete
- Production ready

<template-output>project_timeline</template-output>
<template-output>milestones</template-output>
</step>

<step n="9" goal="Document assumptions and constraints">
Explicitly document all assumptions and constraints that underpin the estimate.

**Assumptions to capture:**
- Team availability and capacity
- Technology choices
- Scope boundaries (what's in, what's out)
- Resource availability (tools, environments, third-party services)
- No major scope changes during development
- Specific technologies or approaches being used
- Quality standards and testing approach

**Constraints to document:**
- Fixed deadlines
- Budget limitations
- Team size limitations
- Technology restrictions
- Regulatory or compliance requirements

Explain: "These assumptions are critical - if any of these change, the estimate needs to be revisited."

<template-output>assumptions</template-output>
<template-output>constraints</template-output>
</step>

<step n="10" goal="Generate executive summary and next steps">
Pull everything together into an executive summary and define next steps.

**Executive Summary should include:**
- Project overview (1-2 sentences)
- Total estimated effort (person-days or person-weeks)
- Total estimated duration (calendar time)
- Confidence level (High/Medium/Low) with explanation
- Top 3 risks
- Key assumptions
- Recommended contingency buffer percentage

**Next Steps:**
- How to use this estimate (proposal, planning, resource allocation)
- When to revisit/refine (after design, after prototype, after requirements finalization)
- What decisions need to be made
- What information would improve confidence
- Suggested approach to mitigate top risks

Provide a final confidence check:
- "Based on everything we've discussed, how confident do you feel about this estimate?"
- "What would increase your confidence?"
- "Are there any areas we should investigate further before finalizing?"

<template-output>executive_summary</template-output>
<template-output>confidence_level</template-output>
<template-output>effort_summary</template-output>
<template-output>total_duration</template-output>
<template-output>resource_plan</template-output>
<template-output>next_steps</template-output>
</step>

</workflow>
