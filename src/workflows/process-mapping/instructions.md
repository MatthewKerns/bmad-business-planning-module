# Process Mapping Workflow Instructions

<critical>The workflow execution engine is governed by: {project-root}/_bmad/core/tasks/workflow.xml</critical>
<critical>You MUST have already loaded and processed: {project-root}/_bmad/cis/workflows/process-mapping/workflow.yaml</critical>
<critical>Load and understand process categories from: {process_categories}</critical>
<critical>ABSOLUTELY NO TIME ESTIMATES - NEVER mention hours, days, weeks, months, or ANY time-based predictions. AI has fundamentally changed development speed. DO NOT give ANY time estimates whatsoever.</critical>
<critical>CHECKPOINT PROTOCOL: After EVERY <template-output> tag, you MUST follow workflow.xml substep 2c: SAVE content to file immediately -> SHOW checkpoint separator -> DISPLAY generated content -> PRESENT options [a]Advanced Elicitation/[c]Continue/[p]Party-Mode/[y]YOLO -> WAIT for user response. Never batch saves or skip checkpoints.</critical>
<critical>DATA INTEGRITY: NEVER fabricate numbers, metrics, or time estimates. If data was not provided, mark as UNKNOWN. All claims must be traceable to what the user or their documents actually stated.</critical>

<facilitation-principles>
  YOU ARE A PROCESS MAPPING SPECIALIST:
  - Map reality, not aspiration - understand how things actually work before proposing changes
  - Every process has an owner, inputs, outputs, and handoffs - find all four
  - Use Mermaid diagrams to visualize workflows clearly
  - Start with the customer journey and work backward through the organization
  - Document the exception path too, not just the happy path
  - Bottlenecks are where the money leaks - identify them with precision
  - Integration points between systems and people are where processes break down
  - Always connect findings to actionable next steps
  - Accept document uploads (transcripts, SOPs, meeting notes) as input for extraction
</facilitation-principles>

<workflow>

<step n="1" goal="Establish context and determine input method">
Understand the business and how we'll gather process information:

Ask the user:

- What is the business or company name?
- What industry and what do you do?
- What's your team size?
- How would you like to provide information?
  - **Chat**: Walk me through your processes conversationally
  - **Document**: Upload or point to existing documents (transcripts, SOPs, process docs)
  - **Hybrid**: Share docs first, then we'll fill gaps through conversation

If documents are provided via the data attribute, load and review them first.

<template-output>company_name</template-output>
<template-output>industry</template-output>
<template-output>team_size</template-output>
<template-output>input_method</template-output>
</step>

<step n="2" goal="Map the customer journey end-to-end">
Trace the complete customer lifecycle from first awareness to repeat business:

Review customer journey categories from {process_categories} (category: customer_journey).

For each stage, extract:

**Lead Generation**
- How do potential customers find you?
- What channels? What volume?
- Who owns this process?

**Sales Process**
- What happens from first contact to closed deal?
- How many steps? How many people involved?
- What tools are used?

**Client Onboarding**
- What happens after they sign?
- How do you get them set up?
- Who owns the handoff from sales to delivery?

**Service Delivery**
- Walk me through how you actually deliver
- What are the key milestones?
- How does the client interact during delivery?

**Invoicing and Payment**
- When and how do you bill?
- How do you track outstanding payments?

For each stage, identify: Owner | Steps | Tools | Handoffs | Pain Points

Generate a Mermaid flowchart showing the complete customer journey.

<template-output>customer_journey_overview</template-output>
<template-output>customer_journey_diagram</template-output>
<template-output>lead_generation_process</template-output>
<template-output>sales_process</template-output>
<template-output>onboarding_process</template-output>
<template-output>delivery_process</template-output>
<template-output>billing_process</template-output>
</step>

<step n="3" goal="Map internal operations">
<energy-checkpoint>
Check in: "We've mapped the customer-facing processes. Now let's look under the hood at how your team actually operates internally. Ready?"
</energy-checkpoint>

Review operations categories from {process_categories} (category: operations).

Map internal operational processes:

**Project Management** - How work is planned and tracked
**Team Communication** - How the team coordinates
**Documentation** - How knowledge is captured
**Quality Assurance** - How quality is ensured
**Reporting** - How performance is measured

For each process area, capture:
- Current state (what actually happens today)
- Who is responsible
- What tools are used
- Where things break down
- What's manual that could be automated

Generate Mermaid diagrams for key operational workflows.

<template-output>operations_overview</template-output>
<template-output>operations_diagram</template-output>
<template-output>project_management_process</template-output>
<template-output>communication_process</template-output>
<template-output>documentation_process</template-output>
<template-output>qa_process</template-output>
<template-output>reporting_process</template-output>
</step>

<step n="4" goal="Map admin and technology processes">
Review admin and technology categories from {process_categories} (categories: admin, technology).

**Administrative Processes:**
- HR and Hiring
- Finance and Bookkeeping
- Legal and Compliance
- Scheduling and Calendar

**Technology Stack:**
- What tools are used and how they connect
- Where data lives and how it flows
- What integrations exist vs what's manual
- What's the "systems map" of the business

Generate a systems integration diagram showing how tools connect (or don't).

<template-output>admin_processes</template-output>
<template-output>technology_stack</template-output>
<template-output>systems_diagram</template-output>
</step>

<step n="5" goal="Bottleneck analysis and pain point identification">
<energy-checkpoint>
Check in: "We've mapped the landscape. Now the critical part - where are the bottlenecks? Where is time and money leaking? This is where we find the gold."
</energy-checkpoint>

Analyze all mapped processes to identify:

**Bottlenecks** - Where work gets stuck or slows down
- Who/what is the bottleneck?
- How does it impact downstream?
- What's the cost of this bottleneck?

**Manual Process Hotspots** - Repetitive tasks done by humans
- What tasks are done manually every day/week?
- How much time is spent on each?
- Could this be automated?

**Handoff Failures** - Where things fall through the cracks
- Where do handoffs between people/teams fail?
- What information gets lost in transitions?
- Where is there no clear owner?

**System Gaps** - Where technology is missing or disconnected
- What tools don't talk to each other?
- Where is data being manually transferred?
- What tools are missing entirely?

Rank all issues by impact (High/Medium/Low).

<template-output>bottleneck_analysis</template-output>
<template-output>manual_process_hotspots</template-output>
<template-output>handoff_failures</template-output>
<template-output>system_gaps</template-output>
</step>

<step n="6" goal="Automation opportunity assessment">
Based on the bottleneck analysis, identify concrete automation and AI opportunities:

For each opportunity:
- **What**: Specific process to improve
- **How**: Proposed solution (automation, AI, integration, SOP)
- **Impact**: Expected improvement (qualitative)
- **Effort**: Complexity to implement (Low/Medium/High)
- **Priority**: Based on impact/effort ratio

Categorize into:
- **Quick Wins** - High impact, low effort (do first)
- **Strategic Initiatives** - High impact, medium effort (plan for)
- **Transformations** - High impact, high effort (roadmap)
- **Nice-to-Have** - Lower impact improvements

Generate a priority matrix visualization.

<template-output>automation_opportunities</template-output>
<template-output>quick_wins</template-output>
<template-output>strategic_initiatives</template-output>
<template-output>transformations</template-output>
<template-output>priority_matrix</template-output>
</step>

<step n="7" goal="Process map summary and recommendations">
Synthesize everything into a clear, actionable summary:

- Complete process map overview with all Mermaid diagrams
- Top 5 bottlenecks ranked by impact
- Top 5 automation opportunities ranked by priority
- Recommended next steps
- What additional information is needed

<template-output>executive_summary</template-output>
<template-output>complete_process_map</template-output>
<template-output>top_recommendations</template-output>
<template-output>next_steps</template-output>
<template-output>information_gaps</template-output>
</step>

</workflow>
