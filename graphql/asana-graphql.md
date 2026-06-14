# Asana GraphQL

## Overview

**Provider:** Asana  
**Native GraphQL:** No  
**Schema Type:** Conceptual data model derived from the Asana REST API  
**Docs:** https://developers.asana.com/reference/rest-api-reference  
**GitHub:** https://github.com/Asana

## Description

Asana does not offer a public native GraphQL endpoint. The Asana platform exposes its capabilities exclusively through a REST API available at `https://app.asana.com/api/1.0`. The schema in `asana-schema.graphql` is a comprehensive conceptual GraphQL SDL derived from the Asana REST API surface, covering all documented resource types. It is intended for tooling, catalog enrichment, code generation, and interoperability use cases — not for execution against a live GraphQL endpoint.

## Core Resource Types

The conceptual schema covers the following resource types drawn from the Asana REST API:

- **Task** — the primary unit of work; supports subtasks, dependencies, followers, tags, custom fields
- **Project** — a collection of tasks; has sections, members, status updates, briefs, and custom fields
- **Portfolio** — a collection of projects; supports memberships and status updates
- **Workspace** — top-level organizational container; contains teams, users, and projects
- **Team** — a group of users within a workspace or organization; has projects and memberships
- **User** — a person with access to Asana; belongs to workspaces and teams
- **Section** — an ordered grouping of tasks within a project
- **Tag** — a label applied to tasks for categorization
- **CustomField** — a user-defined field with types: text, number, enum, multi_enum, date, people
- **CustomFieldSetting** — the association between a custom field and a project/portfolio/team/goal
- **Story** — an activity record (comment or system event) on a task or project
- **Attachment** — a file or URL linked to a task or project
- **Event** — a change event on a resource, used with the Events API
- **Webhook** — a subscription to resource changes delivered via HTTP POST
- **ProjectStatus** — (deprecated) a color-coded progress update on a project
- **StatusUpdate** — the successor to ProjectStatus; supports goals and portfolios
- **ProjectMembership** — the relationship between a user and a project
- **TeamMembership** — the relationship between a user and a team
- **WorkspaceMembership** — the relationship between a user and a workspace
- **PortfolioMembership** — the relationship between a user and a portfolio
- **Goal** — an organizational objective with metric tracking
- **GoalRelationship** — a connection between goals (supporting vs. subgoal)
- **TimePeriod** — a named time range used with goals
- **Job** — an async operation (e.g., project duplication)
- **OrganizationExport** — a bulk export of workspace data
- **UserTaskList** — a user's personal task inbox
- **TaskTemplate** — a reusable template for creating tasks
- **ProjectTemplate** — a reusable template for creating projects
- **ProjectBrief** — a rich text document describing a project
- **Allocation** — a resource allocation record linking users to projects
- **Budget** — a budget (time or cost) for a project
- **Rate** — a monetary rate for a user on a project
- **Reaction** — an emoji reaction on a story or task
- **AuditLogEvent** — an immutable security/compliance event record
- **Role** — an RBAC role definition (Enterprise+)
- **EnumOption** — a value within an enum custom field
- **Like** — a like on a story or task (legacy)
- **TaskCounts** — aggregated task count metrics for a project
