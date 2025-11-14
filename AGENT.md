# Multi-Agent Coordination Document

**Last Updated:** 2025-11-14 01:32 UTC
**Repository:** psych-shelf-exam
**Purpose:** Coordinate multiple AI coding agents working simultaneously

---

## 🤖 Active Agents Registry

Update your entry when you start/stop working. Use format: `[Agent-ID] | Status | Current Task | Started | Files Locked`

| Agent ID | Status | Current Task | Started (UTC) | Files Locked |
|----------|--------|--------------|---------------|--------------|
| | | | | |

**Status Codes:**
- 🟢 ACTIVE - Currently working
- 🟡 PAUSED - Temporarily paused, will resume
- ⚪ IDLE - Available for new tasks
- 🔴 COMPLETED - Finished and exiting

---

## 🔒 File/Directory Locks

**CRITICAL:** Before modifying any file or directory, check this section and add your lock!

| Path | Locked By | Lock Type | Purpose | Locked Since |
|------|-----------|-----------|---------|--------------|
| | | | | |

**Lock Types:**
- READ - Reading only, others can read but not write
- WRITE - Exclusive write access, others should not touch
- MODIFY - Editing existing content, coordinate before making conflicting changes

**Rules:**
- Always check for locks before modifying files
- Add your lock BEFORE starting work
- Remove your lock when done
- If you need a locked file, add a message in Communication Board

---

## 📋 Current Tasks In Progress

Detail what you're actively working on. Update status frequently.

### [Agent-ID] - Task Title
- **Started:** YYYY-MM-DD HH:MM UTC
- **Estimated Completion:** YYYY-MM-DD HH:MM UTC
- **Description:** Brief description of what you're doing
- **Files Affected:** List of files being modified
- **Dependencies:** Any tasks that must complete first
- **Blockers:** Any issues preventing progress
- **Status Updates:**
  - `[HH:MM]` Update message
  - `[HH:MM]` Update message

---

## ✅ Completed Tasks Log

Record completed work for other agents to reference.

### [YYYY-MM-DD HH:MM] - Task Title (Agent-ID)
- **Description:** What was accomplished
- **Files Modified:** List of changed files
- **Commit Hash:** `abc123...` (if committed)
- **Notes:** Important information for other agents
- **Related Tasks:** Links to dependent tasks

---

## 💬 Communication Board

Leave messages for other agents. Check this regularly!

### [YYYY-MM-DD HH:MM] From: [Agent-ID] | To: [Agent-ID or ALL] | Priority: [LOW/MED/HIGH/URGENT]
**Subject:** Message subject
**Message:** Your message here
**Action Required:** What the recipient should do
**Response:** (Recipient fills this in)

---

## 🚨 Alerts & Warnings

Critical information all agents must see immediately.

| Timestamp | Severity | Alert | Agent ID | Status |
|-----------|----------|-------|----------|--------|
| | | | | |

**Severity Levels:**
- 🔴 CRITICAL - Stop all work, review immediately
- 🟡 WARNING - Be aware before proceeding
- 🔵 INFO - Useful information
- 🟢 RESOLVED - Previously critical, now resolved

---

## 📊 Repository Status

Overall status of the repository and coordination.

- **Total Active Agents:** 0
- **Tasks In Progress:** 0
- **Tasks Completed Today:** 0
- **Known Issues:** None
- **Next Available Task IDs:** T001, T002, T003...

---

## 🎯 Task Queue

Prioritized list of tasks waiting to be picked up. Claim a task by moving it to "Current Tasks In Progress"

### High Priority
- [ ] **T###**: Task description (Estimated effort: X hours)

### Medium Priority
- [ ] **T###**: Task description (Estimated effort: X hours)

### Low Priority
- [ ] **T###**: Task description (Estimated effort: X hours)

---

## 🔄 Coordination Protocol

### When You Start Working
1. Generate unique Agent ID (format: `AGENT-YYYYMMDD-HHMM-XXX`)
2. Register in Active Agents Registry with status 🟢 ACTIVE
3. Check File/Directory Locks for conflicts
4. Lock files you'll be modifying
5. Create entry in Current Tasks In Progress
6. Check Communication Board for relevant messages

### While Working
1. Update your task status every 15-30 minutes
2. Check Communication Board every 30 minutes
3. Watch for new locks on files you need
4. Post alerts if you encounter issues
5. Coordinate with other agents if conflicts arise

### When You Finish
1. Move task to Completed Tasks Log
2. Remove all your file locks
3. Update Active Agents Registry (status → 🔴 COMPLETED)
4. Commit changes with clear message referencing task ID
5. Alert dependent tasks in Communication Board
6. Update Repository Status counters

### Conflict Resolution
1. **Same File Needed:** Post in Communication Board, coordinate timing
2. **Merge Conflicts:** Senior agent (earliest timestamp) has priority
3. **Blocking Issues:** Post 🟡 WARNING alert, discuss in Communication Board
4. **Critical Problems:** Post 🔴 CRITICAL alert, all agents pause for review

---

## 📝 Naming Conventions

- **Agent IDs:** `AGENT-YYYYMMDD-HHMM-XXX` (e.g., AGENT-20251114-0132-ABC)
- **Task IDs:** `T###` (e.g., T001, T042)
- **Branches:** `agent/[task-id]-brief-description` (e.g., agent/T001-mood-disorders)
- **Commits:** `[Task-ID] Brief description` (e.g., "[T001] Add MDD diagnostic criteria")

---

## 🛠️ Best Practices

1. **Communicate Early and Often** - Don't surprise other agents
2. **Lock Granularly** - Lock specific files, not entire directories when possible
3. **Update Status Frequently** - Keep others informed of your progress
4. **Check Before Acting** - Always review locks and active tasks first
5. **Clean Up** - Remove locks and update status when done
6. **Be Specific** - Clear descriptions help everyone coordinate
7. **Time-box Tasks** - If blocked >30min, post alert and switch tasks
8. **Verify Before Commit** - Check your changes don't conflict with recent commits

---

## 📖 Quick Reference

**Before starting any work:**
```
1. Read entire AGENT.md
2. Check Active Agents Registry
3. Check File/Directory Locks
4. Check Communication Board
5. Add yourself to registry
6. Lock your files
7. Create task entry
```

**Before committing:**
```
1. Remove your file locks
2. Update completed tasks
3. Update agent status
4. Post completion message
5. Pull latest changes
6. Verify no conflicts
7. Commit and push
```

**If you need help:**
```
1. Post in Communication Board
2. Tag specific agent or use "ALL"
3. Set appropriate priority
4. Describe issue clearly
5. Check back every 15min for responses
```

---

**Remember:** This document is the single source of truth for multi-agent coordination. Keep it updated and check it frequently!
