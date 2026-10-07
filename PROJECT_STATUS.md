# Playwright QA Automation Project

## Current Status

Day: 2
Step: 30
Overall Progress: In Progress



## Completed

### Day 1
- Step 1 — Environment Assessment ✅
- Step 2 — GitHub Repository Setup ✅
- Step 3 — Target Application Verification ✅
- Step 4 — Project Scope Definition ✅
- Steps 5–10 — Completed and verified ✅

### Day 2
- Step 11 — Created PROJECT_STATUS.md ✅
- Step 12 — Committed project status baseline ✅
- Step 13 — Pushed commit to GitHub ✅
- Step 14 — Verified GitHub repository state ✅


## Current Step

Day 2 — Step 30

Status:
IN PROGRESS

## Files Created/Modified

- PROJECT_STATUS.md

## Commands Completed

- Environment verification
- Git repository setup
- Repository configuration

## Technical Concepts Learned

- Project environment validation
- Git repository management
- Target application assessment
- Project scope definition

## Interview Questions Covered

- Why use Playwright for UI automation?
- Why combine UI and API automation?
- How should an automation framework be designed around the target application's capabilities?

## Problems Encountered

None currently recorded.

## Solutions

None currently recorded.

## Pending

- Verify PROJECT_STATUS.md
- Continue framework implementation
- Build UI automation layer
- Build API automation layer
- Build UI/API integration layer
- Configure CI/CD
- Configure reporting
- Build interview examples

## Next Step

Day 2 — Step 31

## Resume Instruction

Continue from:
Day 2 — Step 30


## Target Application

Application:
Automation in Testing — Restful Booker Platform

Primary Base URL:
https://automationintesting.online

Decision:
SELECT

Architecture:
One application / one primary environment with UI and API capabilities.

Verified Capabilities:
- UI available ✅
- REST API available ✅
- Authentication available ✅
- Booking CRUD operations available ✅
- Room API available ✅
- UI/API relationship verified ✅
- API health endpoint verified ✅

Important Environment Limitation:
The deployed environment resets its seeded data approximately every 10 minutes.

Automation Strategy Implication:
Test data must be isolated and controlled. API-based setup and cleanup will be preferred where appropriate rather than relying on persistent shared state.

Architectural Note:
The platform exposes multiple service/API paths, but they belong to the same Restful Booker application and deployed environment. No unrelated external application or mock API will be introduced.
