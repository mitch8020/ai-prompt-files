## FOR DEBUGGING

[ONE REPO ISSUE] I am experiencing an error during [STEPS] | a bug in the taliho-v3-[frontend/backend] repository where [ISSUE DESCRIPTION].
Please perform the following:

1. Trace the Issue: Explore the repository to identify the specific files and functions likely responsible for this behavior.
2. Root Cause Analysis: Analyze the logic and state flow to determine the primary cause of the failure. Prompt me for any additional input, perceived app behaviors, or updated error logs to properly debug this problem
3. Documentation: Create a brief report (save to [ISSUE_NAME + “ANALYSIS”].md) explaining why the feature is failing.
4. Solution: Propose and implement a fix, ensuring it doesn't break existing functionality. Run relevant tests to verify the solution if possible.

---

[BOTH REPO ISSUE] I am experiencing an error during [STEPS] | a bug in the taliho-v3-[frontend/backend] repository where [ISSUE DESCRIPTION].

Please perform the following:

1. Cross-Repository Review: Before diving into fixes, review BOTH the frontend and backend repositories to understand the full data flow and identify where the issue originates. Determine whether the problem stems from the frontend, backend, or their interaction.
2. Trace the Issue: Explore both repositories to identify the specific files, API endpoints, and functions likely responsible for this behavior. Map out the complete request/response chain if applicable.
3. Root Cause Analysis: Analyze the logic and state flow across both layers to determine the primary cause of the failure. Confirm whether the issue is frontend-only, backend-only, or a mismatch between the two. Prompt me for any additional input, perceived app behaviors, or updated error logs to properly debug this problem
4. Documentation: Create a brief report (save to [ISSUE_NAME + "_ANALYSIS"].md) explaining:
   a. Where the issue originates (frontend/backend/both)
   b. Why the feature is failing
   c. The affected files in each repository
5. Solution: Propose and implement a fix in the appropriate repository (or both if needed), ensuring it doesn't break existing functionality. Verify the fix works end-to-end by testing the integration between frontend and backend. Run relevant tests to confirm the solution if possible.

---

[DEBUG] Can you write a follow up prompt to Claude Code to find a solution to the issue and implement the fix for it? Return this new prompt in markdown format.

```
[DEBUG FOLLOW UP] It is still not working after a solution has been implemented. Can you write a follow up prompt to Claude Code to try again and find other alternatives to fix the issue? Return this new prompt in markdown format.

Prompt me for any additional input, perceived app behaviors, or updated error logs to properly debug this problem
----------------------------------------------------------------------------------------------------------
FOR PLANNING WITH CLAUDE
----------------------------------------------------------------------------------------------------------
[PLAN] I need a new and improved prompt for Claude to create a plan for the following feature implementation to optimize effectiveness and clarity. Return this new prompt in markdown format. Here is the initial prompt:
[DESCRIBE WHAT YOU WANT TO DO IN MONKEY LANGUAGE]
```

[PLAN CREATION] Create a plan to accomplish the implementation plan described in the [INSERT PLAN FILE] file.

```
[QUICK PLAN IMPLEMENTATION] Complete the implementation for the plan described in the [INSERT PLAN FILE] file.
----------------------------------------------------------------------------------------------------------

[PLAN IMPLEMENTATION + PROMPTS CREATION]
[IMPLEMENTATION PLAN PROVIDED] Based on the proposed solution and implementation plan described at [INSERT IMPLEMENTATION PLAN FILE], create an Implementation Roadmap that decomposes the work into independent, decoupled tasks.
For each task, provide a targeted Claude Code prompt designed for a standalone instance. Ensure that:
1.	Isolation: Each prompt defines a strict scope to avoid file conflicts between instances.
2.	Context: Each prompt includes necessary background from the root cause analysis.
3.	Validation: Each prompt includes specific test commands to run to verify that specific sub-task.
Save this prompt plan to [ISSUE_NAME + “PROMPT_PLAN].md

----------------------------------------------------------------------------------------------------------
[PLAN IMPLEMENTATION + PROMPTS CREATION]
[PROPOSED SOLUTION - NO IMPLEMENTATION PLAN] Based on the proposed solution, create an implementation plan markdown file. Save this to a [ISSUE_NAME + “FIX_PLAN].md markdown file.

After creating the implementation plan markdown file, create an Implementation Roadmap that decomposes the work into independent, decoupled tasks. For each task, provide a targeted Claude Code prompt designed for a standalone instance. Ensure that:
1.	Isolation: Each prompt defines a strict scope to avoid file conflicts between instances.
2.	Context: Each prompt includes necessary background from the root cause analysis.
3.	Validation: Each prompt includes specific test commands to run to verify that specific sub-task.

Save this prompt plan to [ISSUE_NAME + “PROMPT_PLAN].md

----------------------------------------------------------------------------------------------------------

[PLAN IMPLEMENTATION + PROMPTS CREATION]
[REPORT PROVIDED – NO IMPLEMENTATION PLAN] Based on this report, create an implementation plan markdown file. Save this to a [ISSUE_NAME + “FIX_PLAN].md markdown file.

After creating the implementation plan markdown file, create an Implementation Roadmap that decomposes the work into independent, decoupled tasks. For each task, provide a targeted Claude Code prompt designed for a standalone instance. Ensure that:
1.	Isolation: Each prompt defines a strict scope to avoid file conflicts between instances.
2.	Context: Each prompt includes necessary background from the root cause analysis.
3.	Validation: Each prompt includes specific test commands to run to verify that specific sub-task.

Save this prompt plan to [ISSUE_NAME + “PROMPT_PLAN].md

----------------------------------------------------------------------------------------------------------
FOR CREATING ENHANCED PROMPTS WITH CLAUDE
----------------------------------------------------------------------------------------------------------
I need to create a new and improved prompt for Claude Code to optimize effectiveness and clarity. Return this new prompt in markdown format. Here is the initial prompt:

[OPTIONAL] It has completed my previous request, but the feature is still not functioning properly

[DESCRIBE WHAT YOU WANT TO DO IN MONKEY LANGUAGE]
----------------------------------------------------------------------------------------------------------
FOR SYSTEM EVALUATION PROMPTS
----------------------------------------------------------------------------------------------------------
[PLAN EVALUATION & VERIFICATION] Review the taliho-v3-frontend and taliho-v3-backend repositories to ensure all tasks outlined in [INSERT IMPLEMENTATION PLAN FILE] have been completed accurately. Conduct a comprehensive evaluation to identify any missing, incomplete, or partially implemented tasks. Provide a detailed report summarizing your findings.
```

## [POST EVALUATION & VERIFICATION - PENDING TASK PROMPTS] Based on the attached [INSERT EVALUATION REPORT FILE] file, create an execution plan to resolve all partially completed and incomplete tasks. To implement these solutions, generate a series of targeted, specific prompts that can be run across multiple parallel instances of Claude Code simultaneously.

[MASTER ARCHITECT REVIEW]

[ROLE] Act as a Senior Software Architect and Technical Auditor.
[CONTEXT] Multiple parallel Claude Code instances have completed their assigned tasks based on a modular Implementation Plan. All changes have been applied to the current working directory.
[REFERENCE MATERIAL] > \* Implementation Plan: [INSERT IMPLEMENTATION PLAN FILE]
[TASK] Your goal is to audit the current state of the repository to ensure that every phase of the Implementation Plan has been executed correctly, consistently, and without introducing new regressions.
[EXECUTION STEPS]

1. Plan Cross-Reference: Systematically review the modified files against each step of the Implementation Plan. Verify that no requirement was skipped or partially implemented.
2. Cross-Module Consistency: Check for logical "handshakes" between the tasks. (e.g., If 'Task A' updated a data structure, ensure 'Task B' consumes that structure using the new schema).
3. Code Quality & Redundancy: Identify any redundant code, debug statements, or "TODOs" left behind by the parallel instances. Ensure the code style is consistent across all modified files.
4. Functional Validation: Run the primary test suite (e.g., npm test or pytest) and any specific reproduction scripts created during the analysis phase.
5. Final Correction: If you find discrepancies between the implementation and the plan, fix them immediately to ensure 100% alignment with the roadmap.
   [OUTPUT #1] Provide a "Final Audit Report" [ISSUE_NAME + "AUDIT_REPORT"].md markdown file listing:
   ● Each item from the Implementation Plan and its status (Completed/Corrected).
   ● A summary of any logical inconsistencies you resolved.
   ● Final test results and confirmation of the fix for the original issues.
   [OUTPUT #2] Finally, if any updates need to be made, create a prompt plan [ISSUE_NAME + “PROMPT_PLAN].md to generate multiple targeted prompts for other Claude Code instances to execute these fixes through parallel instances simultaneously.

---

[FRONTEND + BACKEND EVAL]
I need a complete evaluation of the taliho-v3-frontend and taliho-v3-backend repositories to assess their readiness for our v3 desktop production deployment. I need to know which parts of the desktop version:

1. Lack basic functionality.
2. Lack empty states.
3. Lack error pages.
4. Have incomplete or mismatched API connections
5. Contain visually breaking components.
6. Have any other issues that could block our v3 production release.
   The goal of v3 is to release the simplest, most functional version of the app while maintaining high quality for the desktop experience. Conduct a comprehensive review of both repositories to identify areas needing updates.
   Create a report summarizing all areas missing functionality, containing non-working or breaking features, or having partial implementation. For example, consider non-functional buttons or "coming soon" placeholders as critical items for the v3 release.
   Finally, create a plan to generate multiple targeted prompts for other Claude Code instances to execute these fixes through parallel instances simultaneously.

---

## FOR BUILD & LINT PROMPTS (FRONTEND)

BUILD, LINT, TEST FRONTEND

Task: Frontend Audit (Build, Lint, & Test) and Resolution Plan
Repository: [ADD REPOSITORY NAME]

1. Diagnostics:
   o Run npm run build and npm run lint.
   o Run all unit tests (e.g., npm run test).
2. Analysis: Generate a categorized list of all build errors, lint warnings, and test failures.
   o For test failures, distinguish between broken features vs. outdated tests.
3. Unused Variable Protocol: Before deleting unused variables, components, or test helpers, investigate if they belong to an unfinished feature or specific UI implementation that was in progress.
4. Planning: Create a systematic plan to fix these issues.
   o Goal: Ensure the build passes, lint is clean, and all tests pass (green).
   o Constraint: Do not simply delete or "skip" failing tests. Fix the underlying code issue. If a test is truly obsolete, provide a justification for removing it.
5. Execution: Do not apply quick fixes. Ensure every change is context-aware and maintains the frontend architectural integrity.

## Action: Please present the summary of issues (including test failures) and your proposed plan before modifying any files.

## FOR BUILD & LINT PROMPTS (BACKEND)

BUILD, LINT, TEST BACKEND

Task: Backend Audit (Build, Lint, & Test) and Resolution Plan
Repository: [ADD REPOSITORY NAME]

1. Diagnostics:
   o Run npm run build and npm run lint.
   o Run all unit tests.
2. Analysis: Generate a categorized list of errors, warnings, and test failures.
   o For test failures, identify if the issue is a logic error, a schema mismatch, or a database state issue.
3. Unused Variable Protocol: For any unused variables, functions, or exports, investigate if they are placeholders for future API endpoints, database migrations, or unfinished business logic before removal.
4. Planning: Create a systematic plan to resolve these issues.
   o Goal: Achieve a clean build and a 100% passing test suite.
   o Constraint: Prioritize stability. Fix the root cause of test failures rather than lowering test strictness.
5. Execution: Do not apply "quick fixes." Ensure all changes align with the backend's data safety and performance standards.

## Action: Please present the diagnostic report (Build/Lint/Test) and your proposed plan before proceeding with edits.

## FOR BUILD & LINT PROMPTS (FULLSTACK)

BUILD & LINT SYSTEM

Task: Comprehensive Build & Lint Audit and Resolution Plan
Repository: [ADD REPOSITORY NAMES]

1. Diagnostics: Run npm run build and npm run lint for both the taliho-v3-frontend and taliho-v3-backend repositories.
2. Analysis: Generate a categorized list of all errors and warnings. For each category, identify the root cause (the "why") to prevent recurrence.
3. Planning: Create a systematic plan to resolve these issues. Prioritize stability and avoid breaking changes.
4. Unused Variable Protocol: Before suggesting the deletion of any unused variables, investigate the surrounding code. Determine if the variable belongs to an unfinished feature or a specific implementation detail that should be completed rather than removed.
5. Execution: Do not apply "quick fixes." Ensure every proposed change is context-aware and maintains the integrity of the application.

## Please present the List of Issues and the Action Plan before proceeding with any file edits.

## FOR E2E PROMPTS

E2E FRONTEND MISSING TESTS

Task: Identify Frontend Coverage Gaps and Generate Critical E2E Tests

Repository: taliho-v3-frontend

1. Discovery & Gap Analysis:
   o Scan the src/routes (or src/pages) and src/components directories to identify high-value user flows (e.g., Authentication, Checkout, User Onboarding, Complex Form Submissions).
   o Compare these flows against the existing E2E test files.
   o List the critical user journeys that currently have zero or insufficient test coverage.
2. Proposal:
   o Propose a list of new test scenarios to cover these gaps.
   o Prioritize "Happy Paths" (successful completion) and "Critical Error Paths" (e.g., payment failure handling).
3. Consistency Protocol: Analyze the existing E2E test setup (e.g., Cypress vs. Playwright patterns, custom commands, fixture usage). Ensure any new tests strictly adhere to these established patterns.
4. Implementation Plan:
   o Draft the code for these new tests.
   o Ensure robust element selection (prioritize data-testid or accessible roles over fragile CSS selectors).
5. Execution:
   o Write the tests.
   o Verify they pass locally (if possible) or provide instructions on how to seed the environment to make them pass.

## Action: Please list the Missing Critical Paths you identified and your Test Scenario Proposal before writing the code.

E2E BACKEND MISSING TESTS

Task: Identify Backend Coverage Gaps and Generate Critical API Tests

Repository: taliho-v3-backend

1. Discovery & Gap Analysis:
   o Scan src/controllers, src/routes, and src/services to identify high-risk API endpoints (e.g., endpoints that mutate data, handle payments, or manage authorization).
   o Compare these endpoints against the existing integration/E2E test suite.
   o Identify endpoints that lack "Happy Path" tests or security regression tests.
2. Proposal:
   o Propose a list of new integration test scenarios.
   o Focus on workflows (e.g., "Create User -> Login -> Update Profile") rather than just isolated unit tests.
3. Data Integrity Protocol: Ensure that the proposed tests include setup and teardown logic (seeding and cleaning) to prevent polluting the test database.
4. Implementation Plan:
   o Draft the test code using the project's existing testing framework (e.g., Jest + Supertest).
   o Define expected status codes and schema validation for the responses.
5. Execution:
   o Implement the tests.

## Action: Please present the List of Uncovered Endpoints and the Workflow Scenarios you plan to test before writing the code.

## FOR REVIEW

## Can you complete a comprehensive review of the taliho-v3-frontend and taliho-v3-backend repositories for any missing contract tests to validate that our frontend client's API usage aligns with the backend API's specification (contract) to catch mismatches in parameters or data structures early?

Can you complete a comprehensive review of the delete endpoints in the taliho-v3-backend-prod repository to make sure there aren't any bugs that would delete large sections of data unintentionally. Only include critical or high importance bugs in your report.

Also complete a comprehensive review of the taliho-v3-frontend-prod repository to make sure the frontend delete endpoints have been updated based on the recent changes made to the backend API endpoints about making sure there aren’t any bugs that would delete large sections of data unintentionally.

I don’t have a lot of time as we’re pushing this app to production this weekend, so I only need to know the bugs that should prevent us from pushing to production.

Ignore the following backend modules for your review: activity-log, arrangement, equipment, nfc, status-log

## Do NOT update the code yet. Only create the report of your findings and add proposals on how to implement a solution for each problem you identify.

## Can you complete a comprehensive review of the delete endpoints for the procore item module in the taliho-v3-backend-prod repository to make sure there aren't any bugs that would delete large sections of data unintentionally. Ignore the following backend modules for your review: activity-log, arrangement, equipment, nfc, status-log Do NOT update the code yet. Only create the report of your findings and add proposals on how to implement a solution for each problem you identify.

## Can you complete a comprehensive review of the taliho-v3-frontend-prod repository to make sure the frontend delete endpoints have been updated based on the recent changes made to the backend API endpoints for the procore item module about making sure there aren’t any bugs that would delete large sections of data unintentionally. Ignore the following backend modules for your review: activity-log, arrangement, equipment, nfc, status-log Do NOT update the code yet. Only create the report of your findings and add proposals on how to implement a solution for each problem you identify.

Can you complete a comprehensive review of the set password feature in the taliho-v3-frontend-prod and taliho-v3-backend-prod repositories to make sure we are setting the passwords correctly?

For context, when a qr code with a set password is scanned, we only need to be checking the password properties of that specific qr code. Thus, each qr code's password condition is independent of each other. When it comes to setting a group password, we are still recording those password properties within the group document itself, but also, we are individually setting those password properties to each qr code that belongs to that qr code. This means that setting a group password will overwrite any previously set qr code passwords for the qr codes in that group and setting a qr code password (for a qr code belonging to a group) after a group password has been set will overwrite the qr code's own password only for that qr code. When a new qr code is added (create or move) to a group with an active set password, the new qr code will need to copy the group's password properties.

We also need to make sure that we include any db backfill tasks regarding the set password feature (i.e. missing qr code password properties from only being set in the group level password) in the admin.db-backfill file.

## Do NOT update the code yet. Only create the report of your findings and add proposals on how to implement a solution for each problem you identify.

## FOR FEATURE PROMPTS

FOLDER ZIP DOWNLOAD

Feature: Folder ZIP Download Endpoint
Priority: LOW Type: Feature Enhancement Effort: ~4-6 hours
Current State
● Frontend shows message: "Folder download as ZIP is not yet supported. Please download individual files."
● Users can still download files individually (full functionality)
Implementation Required
Backend (taliho-v3-backend-prod)

1. Create new endpoint in src/modules/folder/folder.controller.ts:
2. @Get(':id/download')
3. async downloadFolderAsZip(
4. @Param('id') folderId: string,
5. @Query('companyId') companyId: string,
6. ): Promise<StreamableFile>
7. Implement ZIP generation in src/modules/folder/folder.service.ts:
   o Recursively collect all documents in folder and subfolders
   o Generate presigned URLs for each document
   o Stream documents into archiver/JSZip
   o Return StreamableFile with proper headers
8. Frontend changes:
   o Update qrcode-paginated-table.tsx line ~378 to call new endpoint
   o Handle download progress for large folders
   Acceptance Criteria
   ● Clicking "Download" on a folder downloads ZIP containing all nested files
   ● Progress indicator for large folders
   ● Error handling for empty folders

```
Instance 1 Prompt (Folder ZIP Download)
TASK: Implement folder ZIP download endpoint

WORKING DIRECTORY: c:\Projects\Taliho Web App\prod\taliho-v3-backend-prod

IMPLEMENTATION:
1. Add new route to folder.controller.ts:
   GET /folder/:id/download?companyId=xxx

2. Service implementation:
   - Recursively get all documents in folder tree
   - Validate user has access to folder
   - Generate presigned S3 URLs for each document
   - Create ZIP stream using archiver package
   - Return as StreamableFile

3. Error handling:
   - Empty folder: Return 204 No Content
   - Folder not found: Return 404
   - Documents inaccessible: Skip with warning

DEPENDENCIES:
- npm install archiver @types/archiver

ACCEPTANCE CRITERIA:
- Folder with nested subfolders downloads as single ZIP
- Folder structure preserved in ZIP
- Progress headers for large downloads
----------------------------------------------------------------------------------------------------------
CI/CD PIPELINES

Task: Create/Optimize CI/CD Pipeline for Automated Testing

Repositories: taliho-v3-frontend, taliho-v3-backend
1.	Configuration Audit: Review the current repository structure and identify the necessary environment variables, secrets, and database dependencies (e.g., Redis, PostgreSQL, or mock services) required to run the full test suite.
2.	Workflow Design: Draft a GitHub Actions workflow that triggers on pull_request and push to the main branch. The workflow should include:
o	Dependency Caching: Implement caching for node_modules to ensure fast execution times.
o	Parallel Jobs: Separate the workflow into parallel jobs for Linting, Unit Tests, and E2E Tests to reduce the total "time to feedback."
o	Environment Setup: Include steps to seed the test database and start the backend/frontend servers before E2E execution.
3.	Artifact Management: Configure the pipeline to save failure screenshots or video recordings (if using Cypress/Playwright) as artifacts so they can be reviewed when a test fails in the cloud.
4.	Stability Check: Ensure the pipeline includes a "Clean Up" phase to prevent resource leaks or hanging processes.
5.	Execution: Create or update the .yml file in the appropriate directory.

Action: Please present the Pipeline Architecture (the sequence of jobs and their dependencies) before creating the workflow file.
----------------------------------------------------------------------------------------------------------
```
