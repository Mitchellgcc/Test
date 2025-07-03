# Autonomous Cursor Workflow Setup

🤖 **Fully automated development workflow with self-healing agents**

## Quick Start

1. **Install dependencies:**
   ```bash
   pnpm install && pnpm build
   ```

2. **Test the setup:**
   ```bash
   pnpm test
   ```

3. **Start development:**
   ```bash
   pnpm dev
   ```

## How It Works

### 🔧 Infrastructure (Already Set Up)
- `.cursor/environment.json` - Defines install commands and background terminals
- `.cursor/rules` - Architectural constraints injected into every agent session
- `package.json` - Basic project structure with parseable test output

### 🗂 Daily Workflow
1. **Plan your day** using `tasks-template.md`
2. **Spawn Background Agents** (Ctrl + E → New Background Agent)
3. **Queue tasks** with self-healing prompts
4. **Monitor progress** via Background Agent panel
5. **Review PRs** with BugBot integration

### 🤖 Agent Management

#### Spawn an Agent:
```
Press Ctrl + E → New Background Agent
Name: "feature-auth-agent"
```

#### Queue Self-Healing Tasks:
```
1. Create /auth/login React page with DaisyUI dark mode
2. Add form validation with Zod
3. Run tests via pnpm test
4. If output includes ❌, retry with improved error handling
5. If ✅ appears, submit PR with test coverage
```

### 🧪 Self-Monitoring

All test outputs include parseable status:
- `✅ TESTS PASSED` - Success
- `❌ TEST FAILURE` - Needs retry
- `✅ BUILD COMPLETED` - Ready for PR

### 📋 Agent Prompt Templates

Copy and paste these into your Background Agents:

**Basic Feature Agent:**
```
Spawn agent `ui-component-agent`:
1. Create /components/[ComponentName] with TypeScript
2. Add dark mode styling with DaisyUI + Tailwind
3. Build 3 test cases: render, props, interactions
4. Run pnpm test and ensure ✅ output
5. Retry if any ❌ failures occur
6. Submit PR with test coverage summary
```

**API Development Agent:**
```
Spawn agent `api-endpoint-agent`:
1. Create /api/[endpoint] route with async/await
2. Add input validation and error handling
3. Create integration test with ✅/❌ logging
4. Run pnpm test and verify all pass
5. If failures, add debugging and retry
6. Submit PR when all tests show ✅
```

## 🛰️ Remote Orchestration (Optional)

- **Slack Integration**: Invite @Cursor bot to channel
- **Web Dashboard**: Monitor agents via browser
- **Mobile Support**: Full workflow management on phone

## 🔁 Daily Schedule

| Time | Action |
|------|--------|
| 08:30 | Plan tasks using template |
| 09:00 | Spawn agents and queue work |
| 09:15–12:00 | Agents build, test, retry |
| 12:00 | BugBot reviews PRs |
| 13:00 | Manual PR review |
| 14:00–17:00 | Queue next features |
| 17:00–18:00 | Merge, cleanup, plan tomorrow |

## 🎯 Next Steps

1. Copy `tasks-template.md` to `tasks-today.md`
2. Fill in your specific features
3. Start spawning agents with the templates above
4. Watch the autonomous magic happen! ✨ 