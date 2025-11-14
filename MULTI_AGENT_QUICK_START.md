# Multi-Agent Coordination - Quick Start Guide

## 🎯 Purpose

This system allows multiple AI coding agents to work simultaneously in the same repository without conflicts.

## 📁 Files Created

1. **AGENT.md** - The coordination hub (agents read/write this constantly)
2. **AGENT_PROMPT_INSTRUCTIONS.md** - Copy-paste instructions for each agent prompt
3. **MULTI_AGENT_QUICK_START.md** - This file (for you, the human coordinator)

## 🚀 How to Use This System

### Starting a New Agent

1. **Open new agent session** (new terminal, new chat, etc.)

2. **Copy instructions from AGENT_PROMPT_INSTRUCTIONS.md** into your prompt:
   ```
   You are working in a multi-agent repository...
   [paste entire contents of AGENT_PROMPT_INSTRUCTIONS.md]

   Your Actual Task: [describe what you want this agent to do]
   ```

3. **The agent will automatically:**
   - Read AGENT.md
   - Register itself
   - Lock files it needs
   - Start working
   - Update status as it works
   - Clean up when done

### Running Multiple Agents

You can have 2, 3, 5, or more agents working simultaneously!

**Example Scenario:**

**Agent 1:**
```
[Paste AGENT_PROMPT_INSTRUCTIONS.md]

Your Actual Task: Create comprehensive content for all mood disorders in
the 01-Mood-Disorders directory.
```

**Agent 2:**
```
[Paste AGENT_PROMPT_INSTRUCTIONS.md]

Your Actual Task: Create comprehensive content for psychotic disorders in
the 02-Psychotic-Disorders directory.
```

**Agent 3:**
```
[Paste AGENT_PROMPT_INSTRUCTIONS.md]

Your Actual Task: Create comprehensive psychopharmacology content in the
13-Psychopharmacology directory.
```

All three agents will:
- Register themselves in AGENT.md
- Lock their respective directories
- Work independently without conflicts
- Update their status in real-time
- Communicate if needed

### Monitoring Progress

1. **Check AGENT.md regularly** to see:
   - Which agents are active
   - What they're working on
   - What's been completed
   - Any issues or alerts

2. **Look for:**
   - Status updates in each agent's task section
   - Completed tasks in the log
   - Messages in Communication Board
   - Alerts that need attention

### Handling Issues

**If agents conflict:**
- They will post in Communication Board
- Earlier agent usually has priority
- They'll coordinate timing or approach

**If an agent gets stuck:**
- It will post an alert
- Other agents can help in Communication Board
- You can intervene if needed

**If you need to intervene:**
- Read AGENT.md to understand current state
- Post in Communication Board as "HUMAN-COORDINATOR"
- Update locks or task assignments as needed

## 💡 Tips for Success

1. **Assign Independent Tasks** - Give agents work in different directories when possible
2. **Be Specific** - Clear task descriptions prevent confusion
3. **Check AGENT.md** - Review periodically to monitor progress
4. **Let Agents Coordinate** - They'll handle most conflicts automatically
5. **Task Granularity** - Break big tasks into smaller chunks for better coordination

## 📊 Example Workflow

### Hour 0: Start 3 agents
- Agent A: Mood disorders content
- Agent B: Psychotic disorders content
- Agent C: Pharmacology content

### Hour 1: Check progress
- All agents registered in AGENT.md
- Each locked their directories
- Status updates showing progress

### Hour 2: Agent A finishes
- Logs completion
- Removes locks
- Commits work
- Updates status to COMPLETED

### Hour 2.5: Start Agent D
- Agent D: Emergency psychiatry content
- Registers, locks files, starts work

### Hour 3: All agents complete
- Review AGENT.md for completion log
- Check all commits were made
- Verify no locks remaining

## 🔧 Customization

You can modify the system by editing AGENT.md:

- **Add custom sections** for your workflow
- **Add task templates** for common work
- **Create priority rules** specific to your project
- **Add checklists** for quality assurance

## ⚠️ Important Notes

1. **Agents must follow protocol** - Include AGENT_PROMPT_INSTRUCTIONS.md in every prompt
2. **AGENT.md is source of truth** - All coordination happens there
3. **Commit regularly** - Agents should commit when tasks complete
4. **One task at a time per agent** - Keeps coordination simple
5. **Clear on exit** - Agents must clean up locks and update status

## 🎓 Advanced Usage

### Dependent Tasks
If Agent B needs Agent A's work:
- Agent B checks Communication Board
- Agent B waits or works on other tasks
- Agent A notifies when complete
- Agent B proceeds

### Shared Files
If multiple agents need same file:
- First agent locks for WRITE
- Others post in Communication Board
- Coordinate sequential access
- Or refactor to eliminate dependency

### Quality Review Agent
Start an agent to review all completed work:
```
Your Actual Task: Review all content created by other agents for accuracy,
consistency, and completeness. Add notes in Communication Board for any
issues found.
```

## 📞 Getting Help

If agents aren't coordinating properly:
1. Check they have AGENT_PROMPT_INSTRUCTIONS.md in their prompt
2. Verify AGENT.md is being updated
3. Look for error messages in agent outputs
4. Manually coordinate by posting as HUMAN-COORDINATOR

---

**You're all set!** Start spawning agents and watch them coordinate automatically! 🚀
