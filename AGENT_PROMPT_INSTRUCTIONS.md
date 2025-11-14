# Agent Prompt Instructions

Copy and paste these instructions into your prompt when starting a new coding agent session.

---

## 📋 Instructions for AI Agent

You are working in a **multi-agent repository** where multiple AI coding agents may be working simultaneously. You **MUST** follow the coordination protocol to avoid conflicts.

### 🚨 CRITICAL: Read AGENT.md First

**Before doing ANY work**, you must:
1. Read the `/home/user/psych-shelf-exam/AGENT.md` file completely
2. Follow all coordination protocols described in that file
3. Update the file as you work

### 🆔 Your Agent Identity

When you start working:
1. Generate your unique Agent ID using format: `AGENT-YYYYMMDD-HHMM-XXX`
   - Example: `AGENT-20251114-1330-ABC`
   - Use current UTC date/time and random 3-letter suffix
2. Use this ID consistently in all AGENT.md updates

### ✅ Startup Checklist (DO THIS FIRST!)

Execute these steps **in order** before starting your actual task:

1. **Read AGENT.md**
   ```
   Read /home/user/psych-shelf-exam/AGENT.md completely
   ```

2. **Register Yourself**
   - Add entry to "Active Agents Registry" table
   - Set status to 🟢 ACTIVE
   - Include your current task description

3. **Check for Conflicts**
   - Review "File/Directory Locks" section
   - Check if any files you need are locked
   - If locked, coordinate in "Communication Board"

4. **Lock Your Files**
   - Add entries to "File/Directory Locks" for all files you'll modify
   - Use appropriate lock type (READ/WRITE/MODIFY)
   - Be specific about which files

5. **Create Task Entry**
   - Add detailed entry in "Current Tasks In Progress"
   - Include estimated completion time
   - List all files you'll affect

6. **Check Messages**
   - Review "Communication Board" for relevant messages
   - Check "Alerts & Warnings" for critical info

### 🔄 While Working

Every 15-30 minutes:
1. **Update your task status** in "Current Tasks In Progress"
2. **Check Communication Board** for new messages
3. **Watch for alerts** that might affect your work
4. **Verify your locks** are still appropriate

If you encounter issues:
1. **Post in Communication Board** with appropriate priority
2. **Add alert** if it affects other agents
3. **Don't proceed** if you might conflict with another agent

### ✅ Completion Checklist (DO THIS WHEN DONE!)

When you finish your task:

1. **Remove File Locks**
   - Delete all your entries from "File/Directory Locks"

2. **Log Completion**
   - Move task details to "Completed Tasks Log"
   - Include all files modified
   - Add commit hash if you committed

3. **Update Registry**
   - Change status to 🔴 COMPLETED in "Active Agents Registry"

4. **Notify Others**
   - Post completion message in "Communication Board"
   - Alert any agents waiting on your work

5. **Update Stats**
   - Increment "Tasks Completed Today" in "Repository Status"
   - Update "Total Active Agents" count

### 🚫 What NOT to Do

- ❌ Don't modify files locked by other agents
- ❌ Don't skip updating AGENT.md (even if it seems tedious)
- ❌ Don't commit without removing your locks first
- ❌ Don't ignore messages in Communication Board
- ❌ Don't work on same files as another active agent without coordinating

### 🆘 Conflict Resolution

If you encounter a conflict:

1. **Stop work immediately** on the conflicting item
2. **Check AGENT.md** for the other agent's status
3. **Post in Communication Board** to coordinate
4. **Wait for response** or work on non-conflicting items
5. **Coordinate timing** - maybe you work sequentially
6. **Document resolution** in Communication Board

Priority rules:
- 🔴 CRITICAL alerts = everyone stops and reviews
- Earlier timestamp = higher priority for same-file conflicts
- Explicit coordination overrides timestamp priority

### 📝 Update Template Examples

**Adding yourself to Active Agents Registry:**
```
| AGENT-20251114-1330-ABC | 🟢 ACTIVE | Creating mood disorders content | 2025-11-14 13:30 | 01-Mood-Disorders/*.md |
```

**Locking files:**
```
| 01-Mood-Disorders/major-depressive-disorder.md | AGENT-20251114-1330-ABC | WRITE | Creating MDD content | 2025-11-14 13:30 |
```

**Task in progress:**
```
### AGENT-20251114-1330-ABC - Create Mood Disorders Content
- **Started:** 2025-11-14 13:30 UTC
- **Estimated Completion:** 2025-11-14 15:00 UTC
- **Description:** Creating comprehensive content for all mood disorders including MDD, bipolar, dysthymia
- **Files Affected:**
  - 01-Mood-Disorders/major-depressive-disorder.md (new)
  - 01-Mood-Disorders/bipolar-disorder.md (new)
  - 01-Mood-Disorders/README.md (update)
- **Dependencies:** None
- **Blockers:** None
- **Status Updates:**
  - [13:30] Started work on MDD content
  - [14:00] Completed MDD, starting bipolar disorder
```

**Communication Board message:**
```
### [2025-11-14 13:45] From: AGENT-20251114-1330-ABC | To: ALL | Priority: MED
**Subject:** Completing mood disorders section
**Message:** I'm working on the mood disorders content and will be done by 15:00 UTC. If anyone needs to work in this directory, please coordinate with me first.
**Action Required:** None unless you need mood disorders files
**Response:** (Leave blank for others to respond)
```

### 🎯 Your Actual Task

[This is where you describe the specific task for this agent]

**Remember:**
1. Follow the coordination protocol in AGENT.md
2. Update AGENT.md frequently
3. Communicate with other agents
4. Clean up when done

Good luck!
