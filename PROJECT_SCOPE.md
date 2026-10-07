DAY 1 — CONTINUING
Overall Progress: ~12%

Completed:

Day 1 — Step 1: Environment Assessment ✅
Day 1 — Step 2: GitHub Repository ✅
Day 1 — Step 3: Target Application Verification ✅
Current:

Day 1 — Step 4: Project Scope
Next:

Define the actual UI, API, integration, test-data, and CI scope based on the verified application.
STEP 4 — Project Scope
Objective
Define what this project will actually automate before we start building the framework.

The scope must be based on the capabilities we verified in Step 3—not on hypothetical features.

Why
A senior QA automation project should demonstrate risk-based coverage, not simply contain a large number of tests.

We need to be able to explain:

What we automate
Why we automate it
What we deliberately don't automate
Which tests belong to UI
Which belong to API
Which are hybrid
How test data is created and cleaned
What runs in smoke vs regression
What CI will validate
Prerequisites
Step 3 is verified:

Selected application: Restful-Booker-Platform Environment: https://automationintesting.online

Action
For this step, create a file in your repository:

PROJECT_SCOPE.md
Put the following initial scope into it.

:::writing{variant="document" id="58321" title="PROJECT_SCOPE.md"}

Playwright QA Automation Project — Scope
1. Project Purpose
Build an interview-ready Playwright automation framework demonstrating UI automation, API automation, UI/API integration, test-data management, debugging, reporting, CI/CD, and QA release validation against one real application.

2. Application Under Test
Application: Restful-Booker-Platform / Automation in Testing

Primary Environment:

https://automationintesting.online

The project will use this application as the single target for UI, API, and integration testing.

3. UI Automation Scope
The UI automation scope will focus on verified customer-facing hotel-booking workflows.

Planned areas include:

Application availability
Navigation
Room/booking-related workflows exposed by the UI
Booking form interaction
Required-field validation
Valid booking submission
Booking confirmation/result validation
Appropriate negative scenarios
Critical-path regression coverage
The exact scenarios will be finalized after direct UI exploration.

4. API Automation Scope
The API automation scope will focus on the application's supported APIs.

Planned areas include:

API availability/health validation where supported
Authentication
Booking retrieval
Booking creation
Booking update
Booking deletion
Request validation
Response validation
HTTP status-code validation
Headers where relevant
Negative API scenarios
Authentication/authorization failures where supported
Only API operations actually supported by the application will be automated.

5. UI/API Integration Scope
The project will demonstrate hybrid testing using the same application.

UI → API
Perform an operation through the UI and validate the resulting backend state through the API.

API → UI
Create or prepare appropriate backend data through the API and verify the corresponding state through the UI.

API → UI → API
Prepare required data through the API, perform a customer workflow through the UI, and validate the resulting backend state through the API.

These flows will only be implemented where the application's actual behavior supports reliable validation.

6. Test Data Scope
The project will use a combination of:

Deterministic static data
Dynamic test data where useful
API-generated test data
Environment-specific configuration
Test data will be designed to support:

Test isolation
Repeatability
Parallel execution considerations
Duplicate-data avoidance
API cleanup
7. Cleanup Scope
Where supported, API operations will be used to clean up test-created data.

The project will investigate:

Cleanup after successful tests
Cleanup after failed tests
Cleanup failure handling
Test-data isolation
Shared-environment risks
8. Authentication Scope
The application's own authentication mechanism will be used.

The project will investigate:

API authentication
Authentication token handling
Authenticated API requests
Reusable authentication setup
Authentication fixtures where justified
UI authentication will only be automated if the application's actual UI provides a meaningful authentication workflow.

No unrelated authentication system will be introduced.

9. Framework Scope
The framework will use:

Playwright Test
JavaScript
Page Object Model where appropriate
Playwright APIRequestContext
Custom fixtures where justified
Reusable API clients/services where justified
Test-data utilities where justified
Environment configuration
Playwright reporting
Trace/screenshots for debugging
GitHub Actions for CI
The framework will avoid unnecessary abstraction and empty architectural layers.

10. Test Organization
The project will eventually organize tests according to purpose, such as:

Smoke
Regression
UI
API
Integration
Critical-path scenarios
Exact tagging and organization will be finalized after the test inventory is established.

11. CI/CD Scope
GitHub Actions will eventually execute:

Appropriate smoke tests
Regression tests
API tests
UI tests
Integration tests as appropriate
CI will also provide useful failure artifacts such as:

Playwright reports
Screenshots
Traces
Execution strategy will account for the limitations of the shared deployed environment.

12. Release Validation Scope
The project will define QA quality gates around:

Smoke failures
Critical-path failures
Regression failures
Confirmed defects
Flaky tests
Environmental failures
Known accepted defects
Possible release outcomes:

Go
Conditional Go
No-Go
13. Explicit Non-Scope
The project will not:

Introduce a second application
Introduce an unrelated mock server
Use DummyJSON
Invent unsupported API endpoints
Force unsupported HTTP methods
Add unnecessary framework abstractions
Automate every UI element simply to increase test count
Treat test count as the primary measure of quality
Claim functionality that has not been verified
14. Known Environment Risks
The target is a publicly deployed application.

Known risks include:

Shared environment
Periodic environment/data reset
Authentication-token lifecycle
Potential transient failures
Data collisions
Parallel-execution considerations
These risks will be considered when designing test data, cleanup, retries, and CI execution.

15. Scope Principle
The implementation must always reflect the application's actual verified behavior.

If a planned scenario is unsupported or unreliable, it will be removed or redesigned rather than artificially implemented through an unrelated system. :::