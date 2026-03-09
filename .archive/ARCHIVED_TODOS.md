ARCHIVED COMPLETED JP TODOS:

- Completed Zoho Data Migration Sync ✅
- Try writing a prompt to do end to end mobile test ✅ [COMPLETE - PERFORMANT]
- Cleanup Backend Branches ✅
- Settings Page Overhaul ✅ [COMPLETE – PENDING FINAL FULL SWEEP]
  o Need to fix Integrations and Subscriptions Sections [COMPLETE]
  o Bug fix for Storage & Usage section [COMPLETE]
- Update sub description on each table page (one line each) ✅
- Complete and Thorough Review of Procore Fetch Page and Uncovering Underlying Errors ✅ [COMPLETE – NEEDS MANUAL VISUAL TESTING]
  o During validation, make sure to add the PROMPT VALIDATION ON PROCORE FETCH FIXES at the bottom of this file
- Delete Project Needs to Delete All Underlying Groups, QR Codes, Documents, Procore Items ✅ [COMPLETE – NEEDS MANUAL BACKEND VERIFICATION TESTING]
- Negative Numbers being set for company projectsCount, documentsCount, qrgroupsCount, and qrcodesCount (company id: 6642c200e731021be4bce527) ✅ [COMPLETE – FIX IMPLEMENTED]
- Breadcrumbs on Documents in Fetch Procore Items Page not working ✅ [COMPLETE]
- Missing Self Healing Functions for projectsCount, documentsCount, documentStorageUsed, qrCodeStorageUsed, qrCodesCount, qrGroupsCount ✅ [COMPLETE]
- Create legacy QR codes from V2 local and see what they look like on V3 ✅ [COMPLETE]
- FETCH PROCORE ITEMS PAGE STATES ✅ [COMPLETE – NEEDS MANUAL TESTING]
  o For the Fetch Procore Items page, add and standardize all of the different conditions a user would see as empty states, free trial states, procore integration connection status states, pricing tier states, group fetch vs single fetch (with regards to project reference pills similar to , connected project does not have a procore project, qr code is not assigned to a project, etc.
- LEGACY SELF HEALING GROUPS & QR CODES ✅ [COMPLETE]
- My QR Codes page & projects page not showing correct qr code type for legacy qr codes ✅ [COMPLETE]
- Update all arrangement and equipment data references in the frontend to make use of groups ✅ [COMPLETE]
- Create Taliho DB Backfill Admin Page ✅ [COMPLETE]
- CACHING CHECK (Data caching optimization for taliho frontend tables – Claude) ✅ [COMPLETE]
- TABLE SKELETON OPTIMIZATIONS & STANDARDIZATION ✅ [COMPLETE]
  o I need a review of the implementation of table skeletons and see if there are any improvements we can make globally. We don’t need to keep showing the skeleton loaders if we’re not fetching new data from caching that data on first load. We want to make sure we prep as much as possible for stale data.
- Legacy arrangements and equipment not showing up in groups and projects ✅ [COMPLETE]
- Add a subtle animation when closing the trial banner ✅ [COMPLETE]
- Add subtle animation when procore tool tables close, when items are selected in the fetch procore items page ✅ [COMPLETE]
- Add move to project action and bulk action on my qr codes page ✅ [COMPLETE]
- Add CSV Upload for Company Categories in Settings ✅ [COMPLETE]
- BUG: Z index of filters showing behind bulk actions bar✅ [COMPLETE]
- Folder Validation Missing folder.controller.ts:105 Cross-company folder access possible ✅ [COMPLETE]
- Make sure there is consistent date formatting across pages (1/1/2026 vs Jan 1, 2026) ✅ [COMPLETE]
- Double Check Printouts for Layout consistency and branding ✅ [COMPLETE]
- Update Zebra template to 69mm x 48mm and make sure it is an exact replica from v2 ✅ [COMPLETE]
- Add set password to qr code row level actions and bulk action to my qr codes page ✅ [COMPLETE]
- Create QR Prefix + Quantity not following the start and end as well as the exclude numbers inputs ✅ [COMPLETE]
- Projects in the projects and dashboard page needs a small procore icon to indicate that project has a connected procore project ✅ [COMPLETE]
- Print by group on bulk action print for groups page; Separate printouts by group ✅ [COMPLETE]
- My QR Codes need to filter qr codes belonging to archived projects by default; search needs to support archived qr codes ✅ [COMPLETE]
- Groups need to filter groups belonging to archived projects by default; search needs to support archived groups ✅ [COMPLETE]
- Search Project needs to include archived projects ✅ [COMPLETE]
- My QR Codes type filter not working [LOCAL PROD TEST DEPLOYMENT] ✅ [COMPLETE]
- Procore \* mobile pages missing handling if project is archived where the qr code belongs; Make sure the error doesn’t keep going to rollbar if the project is archived. ✅ [COMPLETE]
- Debug db backfill ✅ [COMPLETE]
- There is a timing issue for the @qrcode.$qrcodeId.tsx page where when accessing a procore tool, the first state that we see is that “No data available” and then the table skeleton shows up and then the data. ✅ [COMPLETE]
- No 20 qr code limit for assorted group option in create qr page ✅ [COMPLETE]
- Merge main back to hotfix branch to catchup ✅ [COMPLETE]
- Complete fixes for SYSTEMATIC-LINT-ISSUES-REPORT.md ✅ [COMPLETE]
- Run npm run test:cov for backend and npm run test:coverage for frontend and create tests for all uncovered files and lines ✅ [COMPLETE]
- Group detail page needs to sort the list alphabetically by default ✅ [COMPLETE]
- Clear filter missing from group detail page ✅ [COMPLETE]
- Disable QR Code creation for archived projects in project detail page and group detail page ✅ [COMPLETE]

- JP TODOS [PRE LAUNCH]: ✅ [COMPLETE]
- Step 1: Run DB Backfill functions (/admin/db-backfill)
- Step 2: Run Data Aggregations for data fixes
- Step 3: Push V3 Frontend & Backend
- Step 4: Update v2 repo to redirect to https://appv3.taliho.com
- Step 5: Run DB Backfill functions (/admin/db-backfill)
- Step 6: Run Data Aggregations for data fixes
- FULL PAGE REVIEWS [PRE LAUNCH]:
- PROJECTS PAGE ✅ [COMPLETE]
- MY QR CODES PAGE ✅ [COMPLETE]
- GROUPS PAGE ✅ [COMPLETE]
- CREATE QR ✅ [COMPLETE]
- Fetch Procore Items ✅ [COMPLETE]
- Full Project Detail Page Review ✅ [COMPLETE]
- Full Group Detail Page Review ✅ [COMPLETE]
- Full QR Code Detail Page Review ⭕
- Complete Full Mobile Manual Visual Review 🔄️ [IN PROGRESS]
- Patch all missing functionality and gaps in UI ✅ [COMPLETE]
- Make sure all error logging is done through Rollbar ✅ [COMPLETE]
- ⭕ Add Fetch by CSV from Procore [KEVIN – JP CULLEN REQUEST]
- 🔄️ Implement NFC Compatibility again with V2 links (NFC Embedded on Concrete Wall Idea) [3B NICHOLAS REQUEST – JUST NEEDS DEBUGGING – FOCUS ON CREATING NEW NFC CARDS ONLY]
- 🔄️ MANUAL MOBILE TESTS!!! [FOR KEVIN – JP CULLEN]
- ⭕ `/redirect/qrcodes/:id` NEEDS TO REDIRECT DIRECTLY TO `/scannedQR`; THEN WE’RE LETTING `/scannedQR` MAKE THE DECISION ON WHERE TO TAKE THE USER FROM THERE; !!! DEPRECATE CREATING NEW QR CODES WITH `/redirect/qrcodes /:id` EMBEDDED IN THE URL !!!
- 🔄️ Need to Update GHL Sync Function to include real time updates for Company Name, Number of QR Codes, Number of Scans, etc. [MICHAEL STANTON REQUEST – JUST NEEDS DEBUGGING OF MIGRATED FIELDS]
  o Add GHL Opportunity ID to Taliho Company Object Records
-

ARCHIVED MARIAM TODOS:

- Implement Documents Move to Folder Feature 🐬 [MARIAM WORKING ON]
- Implement QR Codes Move to Group, Groups Move to Project 🐬 [MARIAM WORKING ON]
- Clicking QR Code from Group Detail page not working (REFRESH TOKEN ISSUE) ⭕
- Add Company Categories Implementation in Settings 🐬 ✅ [MARIAM COMPLETED]
- Audit Set Password Heirarchy for QR Codes, Groups, Projects, Company 🐬 [MARIAM WORKING ON]

ARCHIVED CLAUDE COMPLETED:

- Add Groups Print
- Add Groups List Empty State
- Add Group Detail 404 Styling
- Add Group Detail Set Password Modal
- Add QR Detail 404 Handling
- Add QR Detail error toasts TODO
- Add My QR Codes empty State
- Add Project Groups tab Empty State
- Add Projects List Empty State
- Add Category Editor (Settings)
- Add Procore Connection Status
- Add Download QR Codes Backend
- Add Set Password Projects Backend
- Add Password Change Settings Backend
- ✅ APP EVALUATION [COMPLETE]
  o Pre-prompt:
  ▪ Refer to the @taliho-v3-frontend/EVALUATION-REPORT.md and the @taliho-v3-frontend/CLAUDE-PROMPTS.md files for full context on this prompt
- ✅ 7: PRICING PLAN [FULLY COMPLETE][COMPLETE – WORKING THROUGH VERIFICATION PLAN NOW]
  o Pre-prompt:
  ▪ Refer to the @taliho-v3-frontend/PRICING-PLAN-PROMPTS.md file for full context on this prompt
- ✅ Update Website [COMPLETE]
