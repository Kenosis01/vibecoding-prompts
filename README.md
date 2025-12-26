# AI Agent Prompts Collection

A curated collection of specialized AI agent prompts for frontend design, backend development, and systematic project execution. These prompts are designed to be used with vibecoding agents, AI coding assistants, and development workflows.

## Table of Contents

- [Overview](#overview)
- [Prompt Descriptions](#prompt-descriptions)
  - [Frontend Designer Agent](#frontend-designer-agent)
  - [Backend Developer Agent](#backend-developer-agent)
  - [Booster Mode](#booster-mode)
- [Usage Guide](#usage-guide)
  - [For Vibecoding Agents](#for-vibecoding-agents)
  - [Combining Prompts](#combining-prompts)
  - [Workflow Integration](#workflow-integration)
- [Best Practices](#best-practices)
- [File Structure](#file-structure)
- [Tips and Tricks](#tips-and-tricks)

## Overview

This collection contains three specialized prompts designed to work together or independently:

1. **Frontend Designer Agent** - Creates clean, modern, accessible frontend interfaces using shadcn/ui
2. **Backend Developer Agent** - Designs and implements robust, scalable backend systems
3. **Booster Mode** - Enhances any task with systematic step-by-step execution and todo.md management

Each prompt is self-contained and can be used individually, but they are most powerful when combined for full-stack development.

## Prompt Descriptions

### Frontend Designer Agent

**File:** `frontend-designer-agent-prompt.md`

**Name:** MinimalistUI Architect

**Purpose:** Create clean, modern, accessible frontend interfaces using shadcn/ui components.

**Key Features:**

- Minimalist design principles inspired by Apple's Human Interface Guidelines
- 8 design principles: Clarity, Consistency, Visual Hierarchy, Typography, Color Theory, Whitespace, Responsiveness, Accessibility
- 3-step formula: Color/Typography → Component Strategy → Creative Implementation
- Strict shadcn/ui integration (never recreate library components)
- Clean, maintainable code standards
- Applicable across any website type with only color/typography customization

**Best For:**

- Landing pages and marketing sites
- SaaS dashboards and admin panels
- E-commerce interfaces
- Content-heavy applications
- Any frontend requiring modern, minimalist aesthetics

### Backend Developer Agent

**File:** `backend-developer-agent-prompt.md`

**Name:** Backend Architect

**Purpose:** Design and implement robust, scalable backend systems with methodical precision.

**Key Features:**

- Comprehensive pre-development questionnaire for beginners
- 15+ questions covering authentication, databases, AI, payments, deployment
- 10-step implementation process with detailed guidance
- Third-party service integration (Clerk, Supabase, Firebase, etc.)
- Anti-hardcoding enforcement
- AI application special requirements (never hardcode model names)

**Best For:**

- SaaS application backends
- API development and integration
- Database design and optimization
- Authentication and authorization systems
- Payment processing integration

### Booster Mode

**File:** `booster-mode-prompt.md`

**Purpose:** Enhance any development task with systematic step-by-step execution and frontend-first workflow.

**Key Features:**

- Rolling 10-step todo.md window
- Frontend before backend for every single step
- Specific, atomic step generation
- Thinking prompts before each step
- Anti-pattern detection and avoidance

**Best For:**

- Any project requiring structured progress tracking
- Teams needing visibility into development steps
- Complex multi-phase projects
- Maintaining focus on one task at a time

## Usage Guide

### For Vibecoding Agents

Vibecoding agents are AI-powered development tools that can execute prompts and generate code. To use these prompts:

1. **Load the Prompt First:** Copy the entire prompt content into your agent's context or system prompt area.

2. **Start Fresh Projects:**
   ```
   1. Load Booster Mode as your primary execution framework
   2. Load Frontend Designer Agent for frontend tasks
   3. Load Backend Developer Agent for backend tasks
   ```

3. **For Modifications:**
   ```
   1. Load only the relevant prompt (frontend or backend)
   2. Reference existing code patterns
   3. Follow the prompt's established conventions
   ```

### Combining Prompts

For maximum effectiveness, combine all three prompts:

#### Option 1: Sequential Use

1. Start with Booster Mode to establish the todo.md workflow
2. Use Frontend Designer Agent to create frontend components
3. Use Backend Developer Agent to build supporting APIs
4. Continue cycling through until complete

#### Option 2: Parallel Teams

If your agent supports multiple instances:

- Agent 1: Frontend Designer Agent (frontend-only tasks)
- Agent 2: Backend Developer Agent (backend-only tasks)
- Agent 3: Booster Mode (project management and coordination)

#### Option 3: Integrated Workflow

Use Booster Mode as the outer framework, with frontend/backend prompts as sub-agents:

```
Booster Mode
├── Frontend Designer Agent (for frontend steps)
└── Backend Developer Agent (for backend steps)
```

### Workflow Integration

#### New Project Setup

1. **Initialize Booster Mode**
   - Create todo.md with first 10 steps
   - Generate frontend-first steps

2. **Apply Frontend Designer**
   - Use for UI/UX decisions
   - Follow design principles
   - Create shadcn/ui components

3. **Apply Backend Developer**
   - Answer pre-development questionnaire
   - Follow 10-step implementation
   - Integrate third-party services

4. **Iterate with Booster Mode**
   - Complete steps in todo.md
   - Generate next 10 steps
   - Continue until done

#### Existing Project Enhancement

1. **Load Relevant Prompt**
   - Frontend improvements → Frontend Designer Agent
   - Backend improvements → Backend Developer Agent
   - Process improvements → Booster Mode

2. **Analyze Current State**
   - Review existing code
   - Identify gaps
   - Plan improvements

3. **Execute Changes**
   - Follow prompt guidelines
   - Maintain consistency
   - Document changes

## Best Practices

### Prompt Loading

- **Always load the full prompt** - Partial prompts lead to incomplete results
- **Keep prompts in context** - Reference them throughout the session
- **Update as needed** - Customize for your specific requirements

### Frontend Development

- **Start with the design system** - Establish colors and typography first
- **Use shadcn/ui components** - Never recreate what the library provides
- **Think mobile-first** - Design for mobile, enhance for desktop
- **Test accessibility** - Verify WCAG compliance at each step

### Backend Development

- **Answer all questionnaire questions** - Incomplete answers lead to gaps
- **Plan database schema first** - Design before implementation
- **Never hardcode** - Use environment variables for everything
- **Integrate third-party services** - Use Clerk, Supabase, Firebase when appropriate

### Booster Mode Execution

- **Generate specific steps** - "Create Button.tsx" not "Build UI"
- **Mark steps complete immediately** - Keep todo.md accurate
- **Generate next 10 promptly** - Don't work without a visible next step
- **Maintain frontend-first** - Never break this rule

### Common Mistakes to Avoid

1. **Skipping the Questionnaire** - Backend Developer Agent needs all questions answered
2. **Creating Custom Components** - shadcn/ui provides everything needed
3. **Hardcoding Values** - Use environment variables and configuration
4. **Ignoring todo.md** - The todo list is your roadmap
5. **Backend-First Development** - Always frontend before backend

## File Structure

```
project-root/
├── README.md                           # This file
├── frontend-designer-agent-prompt.md   # Frontend prompt
├── backend-developer-agent-prompt.md   # Backend prompt
├── booster-mode-prompt.md              # Booster mode
└── [project files]/
    ├── todo.md                         # Managed by Booster Mode
    ├── src/
    │   ├── components/                 # Created by Frontend Agent
    │   └── pages/
    └── backend/                        # Created by Backend Agent
```

## Tips and Tricks

### Maximizing Prompt Effectiveness

1. **Provide Clear Requirements** - More context leads to better results
2. **Iterate Refinements** - Ask for improvements after initial generations
3. **Use Examples** - Show the prompt what you want
4. **Request Explanations** - Ask the agent to explain decisions

### Handling Complex Features

For features requiring both frontend and backend:

1. Use Booster Mode to create the step
2. Mark it as requiring both frontend and backend
3. Frontend Designer Agent creates the UI
4. Backend Developer Agent creates the API
5. Test integration together

### Customization Guide

**Frontend Designer Agent Customization:**
- Change color palette in design tokens
- Adjust typography scale
- Modify spacing system
- Update component variants

**Backend Developer Agent Customization:**
- Select different tech stack options
- Choose alternative third-party services
- Adjust database choices
- Modify authentication approach

**Booster Mode Customization:**
- Adjust step granularity (more or less specific)
- Change the 10-step window size
- Modify step generation order
- Add project-specific questions

### Troubleshooting

**Prompt Not Working:**
- Ensure full prompt is loaded
- Check context length limits
- Verify no conflicting prompts

**Inconsistent Results:**
- Repeat the prompt instruction
- Provide more specific requirements
- Ask for clarification

**Step Generation Issues:**
- Ensure previous steps are marked complete
- Check that requirements are clear
- Verify no missing context

## Quick Start

### 1. New Full-Stack Project

```markdown
1. Load all three prompts
2. Start with Booster Mode
3. Create todo.md with first 10 steps
4. Execute steps using Frontend/Backend agents
5. Complete 10 steps, generate next 10
6. Repeat until project is done
```

### 2. Frontend-Only Feature

```markdown
1. Load Frontend Designer Agent
2. Load Booster Mode
3. Generate specific frontend steps
4. Create components following design principles
5. Complete and iterate
```

### 3. Backend-Only Feature

```markdown
1. Load Backend Developer Agent
2. Load Booster Mode
3. Answer the questionnaire
4. Follow 10-step implementation
5. Complete and iterate
```

## Support and Updates

These prompts are designed to be living documents. Customize them for your specific needs and workflow. The core principles remain constant:

- Frontend first, always
- Clean, maintainable code
- Systematic step-by-step execution
- Never hardcode configurations
- Use established libraries and services

---

**Remember:** Good prompts lead to good code. Take time to understand each prompt's philosophy, and the results will reflect that understanding.
