# Daily Task Plan Template

## Feature: [Your Feature Name]

### Agent: [agent-name-1]
1. [Specific task 1]
2. [Specific task 2]  
3. [Add tests and validation]
4. [Retry if tests fail]
5. [Submit PR]

### Agent: [agent-name-2]
1. [Specific task 1]
2. [Specific task 2]
3. [Add integration test]
4. [Log ❌/✅ in terminal output]
5. [Push PR]

## Example Feature: Authentication System

### Agent: auth-ui-agent
1. Create /auth/login React page
2. Add form validation with Zod
3. Implement dark mode UI with DaisyUI
4. Build 3 test cases: render, validation, submission
5. Retry if login.test.ts fails
6. Submit PR

### Agent: auth-api-agent  
1. Create /api/auth POST route
2. Add JWT token generation
3. Add integration test for login flow
4. Log ❌/✅ in terminal output
5. Push PR

## Daily Schedule Template

| Time | Action |
|------|--------|
| 08:30 | Write daily task prompts + goals |
| 09:00 | Spawn agents and queue tasks |
| 09:15–12:00 | Cursor builds, tests, retries |
| 12:00 | BugBot reviews PRs |
| 13:00 | Manual or agent PR review |
| 14:00–17:00 | Queue next feature set |
| 17:00–18:00 | PR merge, cleanup, planning for next day |

## Agent Prompt Templates

### Basic Agent Spawn:
```
Spawn agent `[agent-name]`:
1. [Task 1]
2. [Task 2] 
3. Add tests with ✅/❌ terminal output
4. Retry if tests fail
5. Submit PR with test coverage
```

### Self-Healing Agent:
```
1. Run tests via pnpm test
2. If output includes ❌, identify failed tests and regenerate
3. Retry tests once
4. If ✅ appears, continue to PR
5. Include test coverage in PR body
``` 