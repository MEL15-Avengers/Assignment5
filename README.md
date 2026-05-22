# Moonlight WMS — Report Task Allocation
### Assignment 5 — Final Report

> **Link 1 (Tuesday Morning):** Project Files submission
> **Link 2 (Tuesday Afternoon):** Final Report submission

---

## Team Members & Assigned Sections

| Section | Topic | Assigned To |
|---------|-------|-------------|
| Section 1 | Project Management | Anil Budthapa |
| Section 2.1 | Database Design | Diwas |
| Section 2.2 | System Frontend / UI | Thi Phuong |
| Section 2.3 | Modular Coding Standards + Integration Code | Anil K.C. |
| Section 3.1 + 3.2 + 3.3 | System Testing Overview | Ritesh + Ashima |
| Section 3.4 + 3.5 | OS & Browser Platform Testing | Marc Martin |
| Section 3.7 | Module Test Results | Anil Budthapa + Diwas |

---

## Section 1 — Project Management
**Owner:** Anil Budthapa

### What to include
- How the team was organised and managed throughout the project
- Each team member's role and responsibilities
- Resources used — tools, platforms, software (GitHub, VS Code, PostgreSQL, etc.)
- Project schedule/timeline — planned vs actual milestones
- How the software development process was managed (branching strategy, pull requests, task allocation)
- GitHub status — reference to Assignment 2, 3, 4 (repository links)

### Requirements
- Professional document style
- No AI-generated text
- Must reference actual dates, decisions, and events from the project

---

## Section 2.1 — Database Design
**Owner:** Diwas

### What to include
- ER diagram / database schema diagram
- Screenshots of the database structure (reuse existing screenshots if no changes have been made — note "no changes" if so)
- Table list with a brief description of each table and its purpose:

| Table | Description |
|-------|-------------|
| `app_users` | Stores user accounts, roles, and status |
| `products` | Product catalog with SKU, name, price, stock |
| `categories` | Product category groups |
| `stock_movements` | Records of all inbound/outbound/transfer stock changes |
| `alerts` | Low-stock and system alerts |
| `audit_logs` | System-wide audit trail of sensitive actions |
| `password_reset_codes` | One-time reset tokens with expiry |
| `registration_codes` | Codes used for new user self-registration |
| `pending_accounts` | Accounts awaiting admin approval |

- Key relationships between tables (foreign keys, joins)
- Any schema changes made since the previous submission

### Requirements
- Screenshots must be clear and readable
- Follow report template structure

---

## Section 2.2 — System Frontend / User Interfaces
**Owner:** Thi Phuong

### What to include
Screenshots of all major UI pages (use same screenshots if no changes, or updated ones if changed):

| Page | Description |
|------|-------------|
| Login | Email/password login form |
| Register | New user signup form |
| Reset Password | Forgot password flow |
| Staff Dashboard | KPI cards, charts, activity feed |
| Site Manager Dashboard | Zone utilisation, team activity |
| Admin Dashboard | System-wide metrics, security alerts |
| Products | Product listing, search, filters |
| Inventory | Stock per warehouse/zone, adjust stock |
| Stock Movements | Inbound/outbound/transfer records |
| Alerts | Low-stock notifications panel |
| Admin — User Management | User list, roles, status |
| Admin — Roles & Permissions | Permission matrix |
| Admin — Audit Log | System-wide audit trail |
| AI Chatbot | Floating chatbot panel with tool chips |

- Brief caption/description under each screenshot
- Show role-based differences where relevant (Admin vs Staff view)

### Requirements
- Actual app screenshots only — no mockups
- Follow report template format

---

## Section 2.3 — Modular Coding Standards + Integration Code
**Owner:** Anil K.C.

### What to include

#### Modular Coding Standards
- Show that the codebase is split into separate modules (one file/folder per feature)
- List all major modules with their file paths and responsibilities:

| Module | Key Files | Responsibility |
|--------|-----------|----------------|
| Authentication | `Login.jsx`, `Register.jsx`, `server.cjs` | JWT login, registration, password reset |
| Dashboard | `Dashboard.jsx`, `AdminDashboard.jsx` | Role-aware KPI display |
| Products | `Products.jsx`, `AddProduct.jsx` | Product CRUD, categories, suppliers |
| Inventory | `Inventory.jsx`, `WarehouseZones.jsx` | Stock levels, zones, adjustments |
| Admin | `UserManagement.jsx`, `AuditLog.jsx` | User/role/permission/audit management |
| AI Chatbot | `AIChatbot.jsx`, `aiTools.cjs` | AI tool use, role-based responses |

#### Integration Code (Essential)
- Raw source code connecting frontend to backend — paste actual code at 10pt coding font size
- Must include:
  - API call from React (fetch/axios) to Express route
  - JWT attachment in request headers (`Authorization: Bearer …`)
  - Backend route handler receiving and processing the request
  - Database query (parameterised SQL — no raw string injection)
  - Response returned to frontend

#### Example structure to document
```
Frontend (React)  →  api.js (Axios)  →  server.cjs (Express route)  →  PostgreSQL
                                              ↓
                                        aiTools.cjs (for AI module)
```

### Important
- **Remove ALL AI-generated code** before including in the report
- **Remove ALL AI-generated comments**
- Code must use a **coding font at 10pt size** in the document
- Raw code only — no syntax highlighting or styled blocks

---

## Section 3.1 + 3.2 + 3.3 — System Testing Overview
**Owners:** Ritesh + Ashima (shared)

### 3.1 — Objective of System Testing
**(Ritesh)**
- State the purpose and goals of system testing for Moonlight WMS
- What the tests aim to verify:
  - Functional correctness of each module
  - Integration between frontend and backend
  - Role-based access control (who can do what)
  - Responsiveness across devices and browsers
- Scope — list which modules are included in testing

### 3.2 — Test Summary
**(Ritesh)**

#### Types of tests used:
| Test Type | Description |
|-----------|-------------|
| Functional Testing | Verify each feature works as specified |
| Integration Testing | Verify frontend ↔ backend communication |
| UI / Frontend Testing | Verify visual layout and user flows |
| Browser Compatibility | Verify app works across major browsers |
| Responsiveness Testing | Verify layout on Desktop, Tablet, Mobile |
| Security Testing | Verify role-based access gates |

#### Tools used:
| Tool | Purpose |
|------|---------|
| Selenium (open source) | Automated frontend testing |
| Browser DevTools | Manual responsiveness checks |
| Postman / curl | API endpoint testing |
| Manual testing | Exploratory and UI testing |

### 3.3 — Rationale for Test Results
**(Ashima)**

Explain what each result status means and the conditions that determine it:

| Status | Meaning | Condition |
|--------|---------|-----------|
| **Pass** | Feature works as expected | All acceptance criteria met |
| **Failed** | Feature does not work | One or more criteria not met, bug found |
| **Blocked** | Test could not be run | Depends on another feature not yet complete or environment issue |
| **Partial Pass** | Feature partially works | Some criteria met, minor issues found |

- Include the specific conditions that determine Pass vs Fail for this project
- Reference the FRs (Functional Requirements) where applicable

### Requirements
- Professional document style — no booklet/informal language
- No AI-generated text
- Follow report template

---

## Section 3.4 + 3.5 — OS & Browser Platform Testing
**Owner:** Marc Martin

### 3.4 — Operating System Platform Testing

Test the full application on each OS and record results in a table:

| Who | Operating System | Test Objective | Steps Taken | Expected Result | Actual Result | Pass / Fail |
|-----|-----------------|----------------|-------------|-----------------|---------------|-------------|
| | Windows | Login and navigate | Open browser → login → navigate | Dashboard loads | | |
| | macOS | Login and navigate | Open browser → login → navigate | Dashboard loads | | |
| | Linux | Login and navigate | Open browser → login → navigate | Dashboard loads | | |

- At minimum test: Login, Dashboard, Products, Inventory, Alerts on each OS
- Include browser used for each OS test
- Screenshots to support results encouraged

### 3.5 — Web Browser Platform Testing

Test on each major browser and record results:

| Who | Browser & Version | Test Objective | Steps Taken | Result | Pass / Fail |
|-----|------------------|----------------|-------------|--------|-------------|
| | Chrome | Full app navigation | Login → all pages | | |
| | Firefox | Full app navigation | Login → all pages | | |
| | Microsoft Edge | Full app navigation | Login → all pages | | |
| | Safari | Full app navigation | Login → all pages | | |

- Provide focus information about what was specifically tested (forms, charts, navigation, modals)
- Note any browser-specific issues found

### Requirements
- All tests must be real — actually run the app on each platform
- Professional document style
- Screenshots must accompany any failed tests

---

## Section 3.7 — Module Test Results
**Owners:** Anil Budthapa + Diwas (shared)

### What to include
Every module must be tested individually. For each module provide:
1. Screenshot of the module during testing
2. A row in the master testing result table

### Master Testing Result Table

| Module | Who Tested | How Tested | What Was Tested | Where (URL / Page) | Result |
|--------|-----------|-----------|-----------------|-------------------|--------|
| Authentication | | Manual + Selenium | Login, Register, Reset Password | `/login`, `/register` | |
| Dashboard | | Manual | KPI cards, charts, role views | `/dashboard` | |
| Products | | Manual + Selenium | List, Add, Edit, Delete, Search | `/products` | |
| Inventory | | Manual | Stock view, Adjust, Zones | `/inventory` | |
| Stock Movements | | Manual | Inbound, Outbound, Transfer | `/movements` | |
| Alerts | | Manual | Low stock trigger, dismiss | `/alerts` | |
| Admin — Users | | Manual | Create, Edit, Disable user | `/admin/users` | |
| Admin — Roles | | Manual | Role assignment, permission matrix | `/admin/roles` | |
| Admin — Audit Log | | Manual | View, filter audit entries | `/admin/audit` | |
| AI Chatbot | | Manual + Selenium | Tool calls, role gates, confirm flow | `/` (floating panel) | |

### Testing tools
- **Selenium** (open source) — for automated frontend tests
- **Manual testing** — for UI flows and exploratory testing
- **Integration testing** — verify API calls return correct data
- **Code-level testing** — backend route responses and DB writes

### Screenshot requirements
- One screenshot per module minimum
- Screenshot must show the test being run (not just the page open)
- For failed tests: screenshot showing the error or unexpected result

### Division of work
| Sub-task | Owner |
|----------|-------|
| Authentication, Dashboard, Products testing | Diwas |
| Inventory, Movements, Alerts, Admin, AI Chatbot testing | Anil Budthapa |
| Compile master result table | Both |

### Requirements
- Every row in the result table must be completed
- Both front-end and integration testing evidence required
- Follow report template format

---

## General Requirements for All Sections

- Report must be compared to and follow the **provided template**
- **No AI-generated text or code** in the report
- All code blocks must use a **coding font at 10pt size**
- Screenshots must be actual screenshots of the running application
- Professional document language throughout
- Remove any placeholder or draft text before final submission

---

## Submission Deadlines

| Deliverable | Deadline | Link |
|------------|----------|------|
| Assignment 5 — Project Files | Tuesday Morning | Link 1 |
| Final Report | Tuesday Afternoon | Link 2 |
