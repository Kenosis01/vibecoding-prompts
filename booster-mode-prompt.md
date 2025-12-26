# Booster Mode

## Core Rule
**Frontend first, then backend. Every step. Always.**

Frontend requirements drive backend design. User needs come first.

## Todo.md Format

```markdown
# Todo List

## Next 10 Steps
1. [ ] **Frontend**: [Specific action]
2. [ ] **Frontend**: [Specific action]
3. [ ] **Frontend**: [Specific action]
4. [ ] **Frontend**: [Specific action]
5. [ ] **Backend**: [Specific action]
6. [ ] **Backend**: [Specific action]
7. [ ] **Backend**: [Specific action]
8. [ ] **Backend**: [Specific action]
9. [ ] **Frontend**: [Specific action]
10. [ ] **Frontend**: [Specific action]
```

## Step Rules

- **Specific**: "Create Button.tsx with primary/secondary variants" not "Build UI"
- **Atomic**: One action per step, no combining
- **Frontend before backend**: Always, without exception
- **10 steps max**: Only see 10 at a time, generate more after completing
- **Verifiable**: You know it's done when you see it

## Step Generation Order

For each new step, ask:

1. What UI element does the user need next?
2. What component must exist before that?
3. What backend support is required for that component?
4. What data model enables that backend support?
5. Repeat

## Good Step Examples

**Frontend:**
- [ ] Create Button.tsx with primary/secondary/danger variants
- [ ] Add loading spinner to Button when isLoading prop is true
- [ ] Create Card.tsx with header, content, footer sections
- [ ] Implement responsive grid layout for product listing
- [ ] Create login page with email and password inputs
- [ ] Connect login form to authentication API

**Backend:**
- [ ] Create User model with email, password_hash, name fields
- [ ] Write migration for users table with proper indexes
- [ ] Implement POST /api/users endpoint with validation
- [ ] Add JWT authentication middleware
- [ ] Create GET /api/products endpoint with pagination
- [ ] Implement search functionality for products endpoint

## Bad Step Examples

**Avoid:**
- [ ] Build the UI # Too vague
- [ ] Set up the API # Unclear
- [ ] Do the buttons # Incomplete
- [ ] Make it work # What does this mean?

## Thinking Before Each Step

### Frontend
- What user problem does this solve?
- What existing components can I reuse?
- Is this component accessible?
- Does it handle error and loading states?
- Is it responsive?

### Backend
- What data does the frontend need?
- Is this endpoint secure?
- Does it validate inputs?
- How will this scale?
- Is it properly logged?

## Update Cycle

1. Complete step → mark `[x]` in todo.md
2. Verify the work is complete and correct
3. Move to next step

After completing 10 steps:
1. Mark all completed steps as `[x]`
2. Remove all `[x]` steps from the list
3. Generate 10 new specific steps
4. Continue with new steps

## Anti-Patterns to Avoid

1. **Big Steps**: Break into smallest possible actions
2. **Backend Only**: Frontend always comes first
3. **Vague Descriptions**: Be specific about what to create
4. **Skipping Todo.md**: Update after every single step
5. **Jumping Ahead**: Only generate 10 steps, not the whole project

## Checklist

- [ ] Todo.md created at project start
- [ ] First 10 steps written
- [ ] Each step is specific and atomic
- [ ] Frontend before backend for every step
- [ ] Steps marked [x] when complete
- [ ] New 10 steps generated after completing 10
- [ ] Process repeated until done

## Remember

```
Frontend → Backend → Frontend → Backend
One step at a time
10 steps visible max
Complete → Mark [x] → Generate next 10
```
