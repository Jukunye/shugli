# Shugli

Unified Internal Operations Platform (Backoffice + HRIS)

> **Project status:** Early development. Nothing here is stable yet —
> schema, APIs, and UI are all subject to change. Not accepting external
> contributions or deployments at this time.

## Executive Summary

### The problem

Growing companies drown in two parrallel messes.

1. Backoffice chaos
   - Non-technical staff writting SQL
   - Scattered admin tools
   - No unified audit trail
2. HR sprawl
   - Employee data in spreadsheets
   - Leave tracked in email
   - Payroll reconciled manually

Off-the-shelf solutions (Retool, BambooHR, Workday, Salesforce) are rigid, expensive, siloed and force the company to adapt to their workflow instead of the reverse.

## MVP - Foundation & First Value

Goal: ship a working, secure internal platform that replaces at least one painful manual process.

| Domain                  | Added                                                                                                                      |
| :---------------------- | :------------------------------------------------------------------------------------------------------------------------- |
| **Auth & RBAC**         | Login/logout, session management, forgot-password, roles, permissions, permissions middleware on every request.            |
| **Admin shell**         | Main layout with sidebar/header, dynamic navigation driven by the user's permissions.                                      |
| **Universal Data Grid** | Reusable, config-driven grid: server-side pagination, sorting, filtering, inline edit, bulk actions                        |
| **Entity CRUD**         | Dynamic forms (create/edit/delete) with client + server validation, applied to 3 entities only: users, employee, customer. |
| **Audit log**           | Automatic interception of all mutations. who/what/when/before/after.                                                       |
| **Employee Directory**  | Profiles, departments, positions, manager hierarchy, profile photo upload.                                                 |
| **Document Management** | Upload, version, expiry tracking for contracts, IDs, certifications.                                                       |

**Out of scope for MVP:** Payroll, leave, org chart visualization, workflows, dashboards.

**Definition of Done:** A non-technical user can log in, add an employee, edit a customer, upload a contract and an admin can see change in the audit log - all without a developer touching SQL.
