# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This repository is for a Danish board advisory and presentation project focused on AI in the education sector. The goal is to establish expertise in board and leadership guidance about AI in educational institutions.

## Agent Architecture

This project uses specialized agents for board advisory work. Agents are defined in `.claude/agents/` and invoked using the Task tool.

### Available Specialized Agents:

#### Core Board Advisory Agents

1. **board-presentation-builder** (Red/Sonnet)
   - Creates timeplans, agendas, and presentation structures
   - Expert in Danish board governance and meeting facilitation
   - Use for: Building 60-90 minute board presentation plans

2. **decision-framework-specialist** (Blue/Sonnet)
   - Transforms topics into votable decision proposals
   - Expert in decision science and strategic framing
   - Use for: Defining what decisions boards need to make

3. **slide-design-architect** (Green/Sonnet)
   - Designs presentation deck structures and visual specifications
   - Expert in executive-level visual communication
   - Use for: Creating PowerPoint/Keynote deck structures

4. **board-communications-expert** (Yellow/Sonnet)
   - Creates pre-read materials, board packages, follow-up communications
   - Expert in executive communications (Danish)
   - Use for: Writing board packages, emails, summaries

5. **business-strategy-advisor** (Purple/Sonnet)
   - Evaluates materials and provides strategic business advice
   - Expert in consulting business models and market positioning
   - Use for: Strategic planning, quality assurance, business development

#### Business Development & Growth Agents

6. **marketing-thought-leadership** (Orange/Sonnet)
   - Creates marketing content, thought leadership, brand-building materials
   - Expert in content marketing and LinkedIn strategy for consultants
   - Use for: LinkedIn posts, case studies, blog content, website copy, conference proposals

7. **workshop-seminar-designer** (Cyan/Sonnet)
   - Designs interactive workshops, training programs, extended seminars
   - Expert in adult learning and facilitation design
   - Use for: Half-day/full-day workshops, training curricula, facilitation guides

8. **proposal-sales-specialist** (Magenta/Sonnet)
   - Creates client proposals, pitches, scopes of work, sales materials
   - Expert in consulting proposal writing and value-based pricing
   - Use for: Client proposals, pricing structures, engagement letters, pitch decks

9. **research-intelligence-analyst** (Teal/Sonnet)
   - Conducts research, gathers intelligence, synthesizes information
   - Expert in educational policy analysis and market intelligence (Danish focus)
   - Use for: Policy analysis, competitive intelligence, trend monitoring, research summaries

### How to Use Agents:

Invoke agents using the Task tool with the agent name as `subagent_type`:

```
Task(
  subagent_type="board-presentation-builder",  // Agent name
  description="Brief task summary",
  prompt="Specific work request for this agent..."
)
```

**The agent definition (identity, expertise, principles) comes from `.claude/agents/[name].md`**
**You only provide the SPECIFIC TASK in the prompt parameter**

### Orchestrator Mode:

Use the `orchestrator` skill to enter orchestrator mode where you delegate ALL work to specialized agents and only coordinate between them.

## Repository Purpose

This is a **documentation and content repository** for developing board seminar materials, presentations, and workshops. It currently contains three key documents in Danish:

- **Instruktion til projektet.txt**: Project goals and scope
- **Ramme for oplæg til bestyrelser.txt**: Framework for board presentations (structure, design, key decisions)
- **Rammer for visuals og præsentationer.txt**: Visual design guidelines and best practices for board presentations

## Key Content Principles

### Board Presentation Structure
1. Strategic agenda with decisions prioritized first
2. Professional presentation opening with vision/strategic goals
3. Early presentation of decision proposals with clear rationale
4. Visual elements (icons, timelines, graphics) for clarity
5. Clear documentation of decisions with responsibilities and deadlines
6. Appendix for detailed supporting materials

### Visual Design Guidelines
- **Leadership-driven narrative and storytelling**: Start with clear, bold goals
- **Executive summary slides**: Minimal details, scannable text, large fonts
- **Strategic visual hierarchy**: Guide attention with contrast and placement
- **Brand-aligned visuals**: Clean, simple, confident visual style
- **Clarity first - decisions upfront**: Place bottom-line/key decisions first
- **Action-oriented next steps**: End with powerful, concise recommendations
- **Smart data visualization**: Summarize insights, avoid data overload
- **Professional consistency**: Maintain visual identity throughout
- **Appendix for deep-dive**: Backup slides for detailed Q&A

## Language

All content is in **Danish**. Maintain Danish language when working with existing files or creating new content unless explicitly instructed otherwise.

## Future Development

This repository may expand to include:
- Presentation templates (PowerPoint/Google Slides)
- Workshop materials and exercises
- Case studies and examples
- Supporting research and references
- Marketing and outreach materials
