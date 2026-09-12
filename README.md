# Container Yard Management System

A web-based platform developed during my software development internship at **Hovmark Data ApS in Esbjerg, Denmark**, supporting container yard operations through dedicated workflows for clients, drivers, and administrators.

The system covers container visits from order creation and arrival through yard placement, operational tasks, departure, and billing.

> This repository is a portfolio case study containing project documentation and screenshots. The company’s source code is private and is not included.

## Project Context

| Detail | Description |
| --- | --- |
| Company | Hovmark Data ApS |
| Location | Esbjerg, Denmark |
| Role | Lead Developer |
| Project type | Internship and final examination project for the AP Degree in Computer Science |
| Project period | October 2025 – January 2026 |
| Full internship period | August 2025 – January 2026 |

## My Contribution

I led the development of the platform and implemented core functionality across the frontend, backend, database, and deployment.

My work included:

- Designing and implementing workflows for clients, drivers, and administrators.
- Building API endpoints and business logic for orders, container visits, operational tasks, yard placement, and billing.
- Modelling the yard structure and capacity constraints, including sectors, rows, slots, and stacking rules.
- Generating more than **3,000 yard positions** to support assignment logic and workflow testing.
- Developing a two-stage slot assignment algorithm combining constraint filtering and scoring.
- Supporting manual slot selection with recommendations and human-readable explanations.
- Implementing JWT authentication, role-based access control, and consistent state transitions.
- Validating API behaviour through Swagger and checking end-to-end workflows with the company stakeholder.
- Deploying the application to the company’s server environment using Webmin.

## Project Overview

The platform brings together the main functions required to manage a container yard:

- Container order and visit registration.
- Planned and actual arrival and departure tracking.
- Yard slot assignment.
- Operational task management.
- Customer access to container status.
- Billing and tariff management.
- User and client administration.

## Role-Based Workflows

### Client Portal

- Create and manage container orders.
- View planned and actual container visits.
- Check order and container status.
- Access billing records and invoices.

### Driver Portal

- View planned arrivals.
- Register container arrivals.
- Assign yard slots manually or automatically.
- Execute operational tasks.
- Manage container movements within the yard.

### Administrator Portal

- Manage users and clients.
- Create and manage orders and operational tasks.
- Configure the yard structure.
- Manage tariffs and billing.
- Monitor active and completed operations.

## Yard Management and Slot Assignment

The yard is represented through **sectors, rows, and slots**, with capacity and stacking constraints used to determine valid container positions.

Slot assignment uses two stages:

1. **Constraint filtering:** identify positions that satisfy the applicable placement rules.
2. **Scoring:** rank valid positions to support operationally suitable placement.

The assignment functionality supports:

- Automatic slot allocation.
- Manual placement with recommendations.
- Power-enabled container positions.
- Capacity and stacking constraints.
- Operational efficiency scoring.
- Human-readable explanations for recommendations.

More than **3,000 yard positions** were generated and used to support assignment logic and test operational workflows.

## Technology Stack

| Area | Technologies |
| --- | --- |
| Frontend | Blazor WebAssembly |
| Backend | C#, ASP.NET Core Minimal APIs |
| Data storage | SQL database |
| Authentication and access | JWT, role-based authorisation |
| API validation | Swagger |
| Deployment | Webmin-managed Linux server environment |

## Architecture

The application separates responsibilities across three layers:

- **Presentation:** the Blazor WebAssembly frontend provides interfaces for clients, drivers, and administrators.
- **Application:** the ASP.NET Core API handles requests, business rules, workflow transitions, and access control.
- **Data:** the SQL database stores application records and relationships.

The frontend communicates with the API, which applies the relevant business rules and accesses the database. JWT authentication and role-based authorisation control access to protected functionality.

## Validation and Deployment

Validation included API checks through Swagger and end-to-end workflow checks with the company stakeholder.

These checks covered the interaction between user roles, order and visit states, slot assignment, and operational tasks.

The application was deployed to the company’s server environment using Webmin.

## Business Purpose

The platform was designed to support daily container yard operations through a shared system with structured workflows and role-specific interfaces.

Its intended benefits include:

- Clearer visibility into container status and ongoing operations.
- Consistent handling of workflow states.
- Less reliance on manual coordination.
- Structured yard allocation.
- Centralised tariff and billing management.
- Controlled access for clients, drivers, and administrators.

## Screenshots

The screenshots in this repository demonstrate the application’s client, driver, and administrator interfaces, including examples of container workflows and yard management functionality.

They provide a visual overview of the project while keeping the company’s source code private.
