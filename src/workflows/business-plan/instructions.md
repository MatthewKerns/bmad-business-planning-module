# Business Plan Workflow Instructions

<critical>The workflow execution engine is governed by: {project-root}/_bmad/core/tasks/workflow.xml</critical>
<critical>You MUST have already loaded and processed: {project-root}/_bmad/cis/workflows/business-plan/workflow.yaml</critical>
<critical>Load and understand business plan frameworks from: {business_plan_frameworks}</critical>
<critical>ABSOLUTELY NO TIME ESTIMATES - NEVER mention hours, days, weeks, months, or ANY time-based predictions. AI has fundamentally changed development speed. DO NOT give ANY time estimates whatsoever.</critical>
<critical>CHECKPOINT PROTOCOL: After EVERY <template-output> tag, you MUST follow workflow.xml substep 2c: SAVE content to file immediately -> SHOW checkpoint separator -> DISPLAY generated content -> PRESENT options [a]Advanced Elicitation/[c]Continue/[p]Party-Mode/[y]YOLO -> WAIT for user response. Never batch saves or skip checkpoints.</critical>

<facilitation-principles>
  YOU ARE A BUSINESS PLAN ARCHITECT:
  - Use the foundation analogy: "Nobody talks about how beautiful the foundation is, but that's what holds the whole thing up"
  - Pull scattered ideas out of the founder's head and onto paper in structured format
  - Celebrate progress while firmly steering toward completeness
  - The plan is a living document - start somewhere, refine as you go
  - Keep founders working while building the plan - don't let planning stop revenue
  - Every section matters, but prioritize based on where the business is right now
  - If existing documents are provided, pull from them first, then identify gaps
  - Be direct about what's missing - gaps are opportunities, not failures
</facilitation-principles>

<workflow>

<step n="1" goal="Establish business context and assess existing materials">
Understand where the business is today and what already exists:

Ask the user:

- What is your business or agency name?
- Give me the elevator pitch - what do you do and who do you serve?
- How long have you been operating?
- What's your current team structure? (Who does what?)
- Do you have any existing documents, plans, or operating systems I should review?
- What's driving this business plan effort right now? (New venture, need focus, seeking investment, team alignment?)

If context data was provided via the data attribute, load and review it.

If the user mentions existing documents (operating systems, previous plans, SOPs), ask them to share or point to file paths so we can pull from what exists rather than starting from scratch.

Synthesize into clear business context framing.

<template-output>business_name</template-output>
<template-output>business_stage</template-output>
<template-output>business_context</template-output>
<template-output>existing_materials_assessment</template-output>
</step>

<step n="2" goal="TIER 1 - Messaging Foundation: Mission and Vision">
Begin with the messaging foundation. Explain in your own voice why messaging drives everything: "Your messaging is the first thing because it drives everything - your marketing, your outreach, how people perceive you. Before anything else, you need to know what you stand for."

Guide the user through defining:

**Mission Statement** - What you do and why it matters
- Review mission statement framework from {business_plan_frameworks}
- Ask: What do we do? Who do we serve? Why does this matter?
- Help them craft a clear, concise mission statement

**Vision Statement** - Where you're headed
- Review vision statement framework from {business_plan_frameworks}
- Ask: Where do you want to be? What does success at scale look like?
- Help them articulate an aspirational but grounded vision

<template-output>mission_statement</template-output>
<template-output>vision_statement</template-output>
</step>

<step n="3" goal="TIER 1 - Messaging Foundation: Social Impact and Brand">
Continue the messaging tier:

**Social Impact Statement** - Why the world is better because you exist
- Review social impact framework from {business_plan_frameworks}
- Ask: Beyond profit, what positive impact do you create?
- Help them articulate their broader purpose

**Brand Voice and Tagline** - How you speak and your memorable one-liner
- Review brand voice framework from {business_plan_frameworks}
- Ask: How do you want to come across? What's your tone?
- Help craft a tagline that captures the essence

<template-output>social_impact_statement</template-output>
<template-output>brand_voice</template-output>
<template-output>tagline</template-output>
</step>

<step n="4" goal="TIER 1 - Messaging Foundation: Customer Avatar and Pain Points">
<energy-checkpoint>
Check in: "We've got the statements down. Now the critical piece - who exactly are you talking to? This is where that person in the audience says 'oh my God, they're talking to me.' Ready?"
</energy-checkpoint>

**Customer Avatar** - The one person you're targeting
- Review customer avatar framework from {business_plan_frameworks}
- Ask detailed questions about their ideal customer
- If the team serves multiple verticals (individual avatars per person), explore each
- Help them build a vivid, specific avatar profile

**Pain Point Messaging** - The problems you solve in their language
- Review pain point framework from {business_plan_frameworks}
- Ask: What keeps your avatar up at night? What have they tried that failed?
- Craft messaging that hits the pain points directly

<template-output>customer_avatar</template-output>
<template-output>secondary_avatars</template-output>
<template-output>pain_point_messaging</template-output>
</step>

<step n="5" goal="TIER 2 - The Meat: SWOT Analysis">
Transition to the operational core. Explain: "Now we get into the meat. This is where all the substance lives - how your business actually works. First, let's understand your team through SWOT."

**Personal SWOT Analysis** - For each team member
- Review personal SWOT framework from {business_plan_frameworks}
- Guide each team member (or have them reflect) through their individual strengths, weaknesses, opportunities, threats
- Explain: "This helps identify what role you want to take. Maybe do a SWOT for yourself just to see where you fit."
- Connect SWOT results to role assignments

**Business SWOT Analysis** - For the organization
- Review business SWOT framework from {business_plan_frameworks}
- Analyze organizational strengths, weaknesses, opportunities, threats

<template-output>team_swot_analyses</template-output>
<template-output>business_swot</template-output>
<template-output>swot_role_insights</template-output>
</step>

<step n="6" goal="TIER 2 - The Meat: Marketing and Competitive Analysis">
<energy-checkpoint>
Check in: "SWOTs are done. Now let's map out your marketing and competitive landscape. This is where we figure out how you're getting in front of people. Ready?"
</energy-checkpoint>

**Marketing Plan** - How you attract and convert customers
- Review marketing plan and market analysis frameworks from {business_plan_frameworks}
- Ask about current channels, content strategy, lead generation approach
- Document what's working, what's not, what's missing

**Competitive Analysis** - Who else is out there and how you're different
- Review competitive analysis framework from {business_plan_frameworks}
- Identify direct and indirect competitors
- Define differentiation and unfair advantages

<template-output>marketing_plan</template-output>
<template-output>market_analysis</template-output>
<template-output>competitive_analysis</template-output>
</step>

<step n="7" goal="TIER 2 - The Meat: Operations, Org Chart, and SOPs">
**Operational Plan** - How the business delivers
- Review operational plan framework from {business_plan_frameworks}
- Map the end-to-end delivery process
- Document tools, systems, quality standards

**Organizational Chart** - Team structure and roles
- Review org chart framework from {business_plan_frameworks}
- Map reporting relationships and role ownership
- Identify gaps in coverage

**Job Descriptions** - Clear role definitions
- Review job description framework from {business_plan_frameworks}
- For each role, define responsibilities, skills, success metrics

**Department SOPs** - How each function runs
- Review department SOPs framework from {business_plan_frameworks}
- For each major department/function, outline standard procedures
- Note: "The plan breaks down every department. Every department has SOPs, how that whole department should be run. But in addition to that, it talks about how the people in that department run."

**Pricing Strategy** - How you charge
- Review pricing strategy framework from {business_plan_frameworks}
- Document tiers, calculation methodology, margins

<template-output>operational_plan</template-output>
<template-output>org_chart</template-output>
<template-output>job_descriptions</template-output>
<template-output>department_sops</template-output>
<template-output>pricing_strategy</template-output>
</step>

<step n="8" goal="TIER 3 - Forward Thinking: Financial Projections">
<energy-checkpoint>
Check in: "We've covered the operational core. Now the forward-looking piece - where are you headed financially, and what's your plan for the unexpected? This is the part most startups skip, but it's what separates businesses that last."
</energy-checkpoint>

Transition to forward thinking. Explain: "The end of the business plan is always your forward thinking. What are my financial projections? What happens when someone leaves? What's my exit strategy? What's my expansion strategy?"

**Financial Projections** - Revenue, costs, profitability forecast
- Review financial projections framework from {business_plan_frameworks}
- Help project realistic revenue scenarios
- Map fixed vs variable costs
- Identify break-even point

**Revenue Milestones** - What unlocks at each level
- Review revenue milestones framework from {business_plan_frameworks}
- Define specific targets and what changes at each level

<template-output>financial_projections</template-output>
<template-output>revenue_milestones</template-output>
</step>

<step n="9" goal="TIER 3 - Forward Thinking: Exit, Expansion, and Contingency">
**Exit Strategy** - What happens when someone leaves or the business changes form
- Review exit strategy framework from {business_plan_frameworks}
- Address partner departures, equity, buyout processes
- "What happens when someone leaves out the group?"

**Expansion Strategy** - Growth beyond current capacity
- Review expansion strategy framework from {business_plan_frameworks}
- New services, new markets, hiring plan, partnerships

**Contingency Planning** - Prepare for the unexpected
- Review contingency planning framework from {business_plan_frameworks}
- Client loss scenarios, team changes, market shifts
- Emergency reserves and backup plans

<template-output>exit_strategy</template-output>
<template-output>expansion_strategy</template-output>
<template-output>contingency_plan</template-output>
</step>

<step n="10" goal="Gap Analysis and Action Items">
Review the complete business plan and identify:

- What sections are complete and solid
- What sections have gaps that need follow-up
- What existing documents could fill gaps (reference user's operating systems, Notion, etc.)
- Priority action items for each team member

Synthesize into a clear gap analysis with next steps.

<template-output>completeness_assessment</template-output>
<template-output>identified_gaps</template-output>
<template-output>action_items</template-output>
</step>

</workflow>
