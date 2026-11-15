# CoCreateJS

### One build. Connects anything. Deploys everywhere.

**An AI-native JavaScript ecosystem for building, connecting, deploying, and operating applications.**

From declarative interfaces to distributed infrastructure, CoCreateJS unifies application development, real-time communication, databases, security, AI-powered automation, and cloud orchestration in one extensible JavaScript ecosystem.

Build applications with JavaScript. Connect AI through MCP. Give authorized agents the tools to understand, build, and operate your applications.

CoCreateJS brings together three complementary pillars—**CoCreateClient, CoCreateServer, and CoCreateAI**—supported by a growing ecosystem of reusable modules, database engines, integrations, and infrastructure services.

Together, they provide a connected foundation for creating applications, running them across environments, and turning business objectives into executable workflows.

**One ecosystem. Three pillars. Unlimited possibilities.**

---

## The Three Pillars

### [CoCreateClient](https://github.com/CoCreateJS/Client)

**One code. Build anything. Run anywhere.**

Build interactive, connected, and offline-capable applications with declarative HTML and JavaScript.

CoCreateClient provides a dual API: developers can express application behavior through HTML attributes, programmatic JavaScript, or a combination of both.

Create websites, dashboards, business applications, collaborative experiences, Progressive Web Apps, and cross-platform interfaces without being locked into a traditional frontend framework.

**Build and interact.**

**Package:** `@cocreate/client`

### [CoCreateServer](https://github.com/CoCreateJS/Server)

**One runtime. Any app. Every cloud.**

Run applications, APIs, databases, workflows, and distributed infrastructure through one extensible JavaScript runtime.

CoCreateServer connects application services, storage systems, security, networking, workers, and cloud infrastructure through consistent programmatic interfaces.

Deploy independently, extend existing applications, or coordinate distributed workloads across servers, regions, and providers.

**Execute and operate.**

**Package:** `@cocreate/server`

### CoCreateAI

**One intelligence. Any role. Every task.**

Connect intelligent agents to your applications, business data, APIs, workflows, and distributed infrastructure.

CoCreateAI enables AI-powered experiences that go beyond conversation and code generation. Through authorized tools and runtime capabilities, agents can assist with customer relationships, communications, marketing, finance, software development, analytics, deployments, and infrastructure operations.

From understanding an objective to planning, executing, verifying, and completing work, CoCreateAI brings intelligence into the entire application and business lifecycle.

**Understand and orchestrate.**

**Package:** `@cocreate/ai`

---

## Table of Contents

- [Why CoCreateJS?](#why-cocreatejs)
- [One Ecosystem, Three Pillars](#one-ecosystem-three-pillars)
- [Quick Start](#quick-start)
- [CoCreateClient — Build and Interact](#cocreateclient--build-and-interact)
- [CoCreateServer — Execute and Operate](#cocreateserver--execute-and-operate)
- [CoCreateAI — Understand and Orchestrate](#cocreateai--understand-and-orchestrate)
- [AI-Native Applications and Business Automation](#ai-native-applications-and-business-automation)
- [CoCreateMCP — Connecting Intelligence to Capabilities](#cocreatemcp--connecting-intelligence-to-capabilities)
- [Data and Storage — Freedom by Design](#data-and-storage--freedom-by-design)
- [CoCreateDB — Native Data and Indexing](#cocreatedb--native-data-and-indexing)
- [Security and Key Management](#security-and-key-management)
- [Real-Time and Offline Applications](#real-time-and-offline-applications)
- [Workflows and Structured Execution](#workflows-and-structured-execution)
- [Distributed Infrastructure and Multi-Cloud](#distributed-infrastructure-and-multi-cloud)
- [Modularity and Extensibility](#modularity-and-extensibility)
- [Architecture](#architecture)
- [Use Cases](#use-cases)
- [Design Philosophy](#design-philosophy)
- [Project Repositories](#project-repositories)
- [Contributing](#contributing)
- [License](#license)
- [Resources](#resources)

---

## Why CoCreateJS?

Modern applications rarely operate in isolation.

Building and running an application may require a frontend framework, backend runtime, database, authentication system, real-time communication service, storage provider, deployment pipeline, infrastructure automation, monitoring tools, and numerous third-party APIs.

Introducing AI often adds another layer of complexity.

Developers connect models to isolated tools, build custom integrations for individual services, and maintain separate workflows for development, business operations, and infrastructure management.

The result is a fragmented application environment.

**CoCreateJS takes a different approach.**

Instead of treating every capability as a separate technology stack, CoCreateJS provides a unified JavaScript ecosystem where applications, data, services, workflows, AI agents, and infrastructure can interact through shared interfaces.

### Build Without Unnecessary Complexity

Use declarative HTML and JavaScript to create application interfaces and behavior.

### Run Without Infrastructure Lock-In

Deploy applications using an extensible server runtime that supports multiple cloud providers, storage systems, and distributed execution environments.

### Automate Beyond Individual Tools

Connect intelligent agents to the applications, APIs, business data, and infrastructure already available through the runtime.

### Adopt What You Need

Use CoCreateClient, CoCreateServer, or CoCreateAI independently.

Integrate individual modules into existing applications without adopting the entire ecosystem.

### Keep Your Options Open

Choose your frontend architecture, database provider, cloud infrastructure, and AI models.

CoCreateJS provides integrated capabilities without making every integration mandatory.

**Build applications, not infrastructure.**

---

## One Ecosystem, Three Pillars

CoCreateJS is organized around three complementary capabilities.

| Pillar | Responsibility | Focus |
|---|---|---|
| **CoCreateClient** | Build and interact | Interfaces, application behavior, connectivity, offline experiences |
| **CoCreateServer** | Execute and operate | APIs, data, workflows, networking, distributed infrastructure |
| **CoCreateAI** | Understand and orchestrate | Intelligent agents, business automation, development, operations |

These pillars are supported by reusable technologies that extend their capabilities.

### Supporting Technologies

| Component | Purpose |
|---|---|
| **CoCreateDB** | Native document storage, indexing, querying, and synchronization |
| **CoCreateMCP** | Model Context Protocol interface for authorized runtime capabilities |
| **CoCreateAST** | Structured application logic and executable workflows |
| **CoCreateKMS** | Cryptographic keys, credentials, and secret management |
| **CoCreateCluster** | Worker coordination and distributed execution |
| **CoCreateCLI** | Development, installation, and operational commands |
| **CoCreateDevice** | Cross-platform application and device integration |
| **CoCreate Modules** | Reusable application and infrastructure functionality |

These technologies are independently valuable, but they do not need to become separate entry points into the main CoCreateJS story.

For example, CoCreateServer supports numerous database adapters. Developers can use MongoDB, PostgreSQL, MySQL, SQLite, and other compatible storage systems without adopting CoCreateDB.

Similarly, CoCreateAI can connect to existing business applications and external APIs without requiring those systems to be rebuilt.

**The pillars define how developers and users engage with CoCreateJS. The supporting technologies provide the capabilities behind them.**

---

## Quick Start

CoCreateJS supports incremental adoption.

Start with a browser interface, a server runtime, or an AI-powered application experience.

### CoCreateClient

Include the browser runtime:

```html
<script src="https://cdn.cocreate.app/latest/CoCreate.min.js"></script>
```

Use declarative HTML to connect interface elements to application data:

```html
<input
  array="users"
  object="5f8d04f1"
  key="name"
  placeholder="Enter your name"
  save
/>
```

The element identifies the array, object, and key associated with its value.

Configured CoCreate modules can provide persistence, data binding, events, and synchronization.

### CoCreateServer

Install the server runtime:

```bash
npm install @cocreate/server
```

Initialize it:

```javascript
import server from '@cocreate/server';

await server.init();

if (server.isPrimary) {
  // Primary-process responsibilities.
}

if (server.isWorker) {
  server.routes.set('/health', async (req, res) => {
    res.writeHead(200, {
      'Content-Type': 'application/json'
    });

    res.end(JSON.stringify({
      status: 'healthy'
    }));
  });
}
```

CoCreateServer provides an extensible execution environment for application routes, APIs, workers, networking, storage, and distributed services.

### Extend with Modules

Load capabilities according to the responsibilities of each process:

```javascript
if (server.isPrimary) {
  await import('@cocreate/cron-jobs');
}

if (server.isWorker) {
  await import('@cocreate/users');
  await import('@cocreate/organizations');
}
```

The runtime can be extended without requiring every module to be loaded in every process.

### Connect AI

CoCreateAI provides application-integrated AI experiences, while CoCreateMCP exposes authorized server capabilities to compatible AI clients.

AI clients can use configured tools to interact with application data, execute workflows, and perform supported operations through CoCreateServer.

See the CoCreateAI and CoCreateMCP sections for the architecture.

---

## CoCreateClient — Build and Interact

### One code. Build anything. Run anywhere.

CoCreateClient is a JavaScript runtime for building interactive, reactive, collaborative, and offline-capable applications.

Its core philosophy is to make application behavior accessible through two complementary interfaces:

**Declarative HTML and programmatic JavaScript.**

### A Dual API

Developers can define common application behavior directly through HTML attributes.

```html
<form array="users" object>
  <input key="name" placeholder="Full name" />
  <input key="email" type="email" placeholder="Email" />

  <button actions="save">
    Save User
  </button>
</form>
```

Or use JavaScript to execute application operations:

```javascript
crud.send({
  method: 'object.create',
  array: 'users',
  object: {
    name: 'Jane Doe',
    email: 'jane@example.com'
  }
});
```

Both approaches work with the same underlying application capabilities.

Developers can use declarative attributes for common behaviors and JavaScript for custom logic.

### Core Capabilities

- Declarative HTML attributes
- Headless JavaScript APIs
- Reactive data binding
- Application state management
- CRUD operations
- Real-time subscriptions
- WebSocket communication
- Collaborative editing
- IndexedDB persistence
- Offline data access
- Service Worker integration
- Progressive Web Apps
- Component composition
- Forms and validation
- File handling
- Modular functionality
- Framework interoperability

### Framework Agnostic

CoCreateClient can operate independently or alongside existing frontend technologies.

Developers can integrate compatible capabilities with React, Vue, Angular, Svelte, Web Components, or plain JavaScript.

Using CoCreateClient does not require replacing an existing frontend architecture.

### Applications Across Devices

CoCreateClient uses standard web technologies to support websites, dashboards, business applications, Progressive Web Apps, and cross-platform experiences.

Related modules such as CoCreateDevice extend this direction through device-specific integration and packaging.

**Repository:** [CoCreateJS/Client](https://github.com/CoCreateJS/Client)

**Package:** `@cocreate/client`

---

## CoCreateServer — Execute and Operate

### One runtime. Any app. Every cloud.

CoCreateServer is a distributed JavaScript runtime designed to execute applications and coordinate the services and infrastructure behind them.

It provides a common operational environment for networking, APIs, storage, security, workflows, workers, and distributed execution.

### One Runtime, Many Capabilities

CoCreateServer brings together functionality commonly distributed across independent services:

- HTTP and HTTPS
- TLS certificate management
- WebSockets
- Application routing
- REST and custom APIs
- Static asset delivery
- Primary and worker processes
- Inter-process communication
- Cluster coordination
- Distributed messaging
- Data operations
- Database adapters
- Authentication and authorization
- Background jobs
- Scheduled workflows
- Health monitoring
- Infrastructure orchestration
- Multi-cloud integration
- AI-accessible operations through CoCreateMCP

The runtime is modular.

Applications load the capabilities they need rather than requiring every feature in every process.

### Independent or Integrated

CoCreateServer can power applications built with CoCreateClient, but it does not depend on CoCreateClient.

It can also serve existing frontend applications, backend services, APIs, and distributed workloads.

### Primary and Worker Architecture

CoCreateServer distinguishes between local primary-process responsibilities and worker execution.

A node may manage its own primary process and workers while participating in a broader distributed mesh.

Distributed coordination does not require one permanent global primary for every node.

### Data Without Lock-In

CoCreateServer provides a consistent interface to supported storage systems.

Applications can use external databases through adapters or choose CoCreateDB for integrated native storage.

The database engine is a deployment choice rather than a requirement for using the runtime.

### Infrastructure as an Application Capability

CoCreateServer is designed to coordinate operations such as:

- Provisioning servers
- Configuring services
- Deploying applications
- Managing workers
- Monitoring runtime health
- Scaling workloads
- Coordinating clusters
- Managing storage
- Executing recovery workflows

Supported operations depend on the installed modules, infrastructure integrations, and runtime configuration.

### A Runtime Accessible to AI

Through CoCreateMCP, selected CoCreateServer capabilities can be exposed as tools for compatible AI clients.

This allows AI agents to interact with the running application environment rather than being limited to generating source code or recommending terminal commands.

An authorized agent may inspect application state, query data, execute workflows, or invoke infrastructure operations using the same underlying runtime capabilities available to application developers.

**Repository:** [CoCreateJS/Server](https://github.com/CoCreateJS/Server)

**Package:** `@cocreate/server`

---

## CoCreateAI — Understand and Orchestrate

### One intelligence. Any role. Every task.

CoCreateAI connects intelligent agents to the applications, business processes, data, APIs, workflows, and infrastructure available through CoCreateJS.

It is designed to move beyond isolated AI conversations and task-specific assistants.

**CoCreateAI brings intelligence into the operating environment of the application itself.**

### Intelligence Across the Entire Business

CoCreateAI is not limited to software development or infrastructure management.

Through connected application capabilities, it can support roles and workflows across an organization.

**Customer Relationships**

Work with customers, contacts, leads, organizations, and CRM records.

**Communications**

Review messages, draft responses, organize conversations, and coordinate email, SMS, and other communication workflows through configured integrations.

**Sales and Finance**

Work with invoices, payment records, transactions, reporting, and connected payment services.

**Marketing**

Research topics, prepare campaigns, create content, coordinate publishing workflows, and analyze results through supported integrations.

**Development**

Assist with application interfaces, code, features, configuration, testing, debugging, and deployment workflows.

**Data and Analytics**

Query application data, inspect records, analyze trends, and prepare reports.

**Infrastructure**

Inspect telemetry, evaluate capacity, manage configured deployments, and assist with distributed infrastructure operations.

### From Conversation to Execution

An AI assistant traditionally provides information, recommendations, or generated code.

CoCreateAI can connect those decisions to executable application capabilities.

Consider a request:

> Review today's customer messages, identify the most urgent conversations, draft responses, and let me approve them before sending.

A connected workflow could:

1. Retrieve new messages from the application database.
2. Identify the associated customers and relevant business records.
3. Prioritize messages based on configured criteria.
4. Generate suggested responses.
5. Present the responses through an application interface.
6. Wait for user approval.
7. Send approved messages through configured communication APIs.
8. Update conversation and customer records.
9. Record the execution results.

The AI can use the application's existing data and tools rather than relying on disconnected external systems.

### Business Automation

The same architecture can support scheduled and event-driven workflows.

Examples include:

- Reviewing new leads every morning
- Preparing customer follow-up messages
- Generating invoice reminders
- Summarizing daily sales
- Researching marketing topics
- Drafting social media campaigns
- Scheduling approved communications
- Monitoring incoming support requests
- Updating application records
- Producing operational reports

CoCreateServer can coordinate scheduled execution through supported jobs and workflows.

The database can preserve business context and workflow state.

CoCreateAI provides reasoning and content generation.

CoCreateMCP provides access to the authorized tools needed to execute operations.

### Development and Infrastructure

The same intelligence layer can participate in technical workflows.

For example:

> Review our traffic distribution, identify regions experiencing increased latency, and recommend whether we should expand an existing cluster or deploy additional nodes.

A connected workflow could examine telemetry, compare available capacity, evaluate deployment options, and present a plan.

With the appropriate permissions and tools, it could then execute approved provisioning and deployment operations, inspect the resulting infrastructure, and verify application health.

The AI does not need to implement every infrastructure operation itself.

It can use CoCreateServer's existing capabilities.

### Declarative AI Interfaces

CoCreateAI includes application-integrated AI chat functionality built around CoCreateJS's declarative development model.

Developers can create AI experiences that fit naturally into application interfaces, including dashboards, business tools, administrative systems, and application builders.

### Model-Agnostic Connectivity

CoCreateAI is designed to work with configurable AI providers and compatible models.

Its application capabilities and runtime tools are not intended to depend permanently on one AI provider.

### One Intelligence, Many Roles

A single connected AI experience can assist with different responsibilities across the same application environment.

It can reason about business data, work with application interfaces, invoke APIs, coordinate workflows, and interact with distributed infrastructure.

These capabilities remain subject to the tools available, the permissions granted, and the operational controls configured by the application.

**One intelligence. Any role. Every task.**

**Package:** `@cocreate/ai`

---

## AI-Native Applications and Business Automation

### From Intent to Outcome

CoCreateJS connects application development, business operations, and infrastructure through one runtime ecosystem.

CoCreateAI extends that environment by allowing intelligent agents to work with the same capabilities used by applications and developers.

```text
                     User or Team
                          |
                          v
                      CoCreateAI
                          |
                 Understand Objective
                          |
                          v
                    Plan Workflow
                          |
                          v
                     CoCreateMCP
                          |
                 Authorized Tools
                          |
                          v
                    CoCreateServer
                          |
        +-----------------+-----------------+
        |                 |                 |
        v                 v                 v
    Business Apps      Data & APIs       Infrastructure
        |                 |                 |
    CRM / Invoices     CRUD / Storage    Cloud / Clusters
    Contacts           External APIs     Workers / Deploy
    Communications     Analytics         Monitoring
        |                 |                 |
        +-----------------+-----------------+
                          |
                          v
                   Execute Workflow
                          |
                          v
                  Verify and Record
                          |
                          v
                       Outcome
```

### A Connected Application Environment

The value of CoCreateAI comes from the capabilities available through CoCreateServer.

Applications may already contain:

- Customers
- Contacts
- Organizations
- Products
- Invoices
- Payments
- Messages
- Files
- Events
- Scheduled jobs
- Application configurations
- API integrations
- Infrastructure definitions

This information can be stored in CoCreateDB or in supported external databases.

AI agents can work with that information through authorized application interfaces and tools.

### One Runtime, Multiple Workflows

An organization might use the same CoCreateJS environment to:

- Build its website
- Operate its CRM
- Manage customer communications
- Process payments
- Run marketing campaigns
- Analyze business performance
- Deploy new application features
- Scale infrastructure
- Execute scheduled automation

CoCreateAI can provide an intelligent interface across those capabilities.

Instead of requiring a different disconnected AI integration for every department, compatible tools can expose application operations through a shared architecture.

### Human Oversight Where It Matters

AI automation does not require removing human control.

Applications can define workflows where agents prepare recommendations, generate drafts, or propose operations before execution.

Examples include:

- Approving outbound customer messages
- Reviewing marketing campaigns
- Confirming payment-related operations
- Approving infrastructure changes
- Reviewing generated code
- Validating deployment plans

The appropriate approval requirements depend on the action, its risk, and the organization's policies.

### Durable Automation

Scheduled jobs and structured workflows create opportunities for automation that continues beyond a single chat session.

An application can store workflow definitions, execution state, results, and business context.

CoCreateServer can coordinate supported scheduled operations, while AI participates when reasoning or content generation is required.

Reliable long-running automation also requires appropriate retry handling, authorization, idempotency, observability, and recovery mechanisms.

---

## CoCreateMCP — Connecting Intelligence to Capabilities

CoCreateMCP provides a Model Context Protocol interface to authorized CoCreateServer capabilities.

It allows compatible AI clients to discover available tools and execute supported operations.

### One Tool Interface

CoCreateServer already exposes application functionality through JavaScript APIs and modules.

CoCreateMCP provides a standardized way to make selected capabilities accessible to AI clients.

These capabilities may include:

- Application APIs
- CRUD operations
- Database queries
- Customer and contact management
- Business workflows
- File operations
- Runtime configuration
- Scheduled jobs
- Infrastructure operations
- Deployment workflows

### External AI Clients

Compatible external AI clients can connect to CoCreateMCP and interact with the capabilities exposed by CoCreateServer.

This allows developers and organizations to use AI tools they already prefer.

### CoCreateAI Integration

CoCreateAI can use the same MCP-based capability model to interact with application and server operations.

A shared tool interface allows AI models and application capabilities to evolve independently.

### Authorization by Design

MCP access should be controlled through explicit tool definitions and application permissions.

Sensitive capabilities require appropriate authentication, authorization, validation, auditing, and execution safeguards.

An AI client should not receive unrestricted access to every internal server method merely because it can connect to CoCreateMCP.

**CoCreateMCP connects intelligence to capabilities. CoCreateServer executes those capabilities.**

---

## Data and Storage — Freedom by Design

CoCreateJS treats data access as a core application capability without requiring one specific database engine.

CoCreateServer supports a broad collection of storage adapters, including integrations for relational, document, embedded, cloud-hosted, and other database systems.

Supported technologies and compatibility layers include database families such as:

- MongoDB
- PostgreSQL
- MySQL
- SQLite
- MariaDB
- CockroachDB
- Amazon DynamoDB
- Google Firestore
- Microsoft Azure Cosmos DB
- Other supported storage providers

Some integrations use compatible drivers or adapter layers rather than independent implementations.

### A Consistent Data Model

CoCreateJS uses shared concepts such as:

- `array`
- `object`
- `key`
- `filter`
- `sort`
- `limit`

These concepts allow applications to work with data through consistent APIs while adapters translate operations for their respective storage systems.

### One Application, Multiple Storage Options

Applications can select storage according to their requirements.

A deployment might use MongoDB for application documents, PostgreSQL for relational workloads, SQLite for embedded persistence, or CoCreateDB for native document storage.

CoCreateJS aims to reduce the amount of application code that must change when storage choices evolve.

Adapter compatibility and supported query semantics can differ between engines.

### AI and Data

Because data operations are exposed through the runtime, authorized AI tools can work with application information without requiring a separate custom integration for every database provider.

The AI interacts with supported application and database capabilities through CoCreateServer.

**Database freedom remains a core architectural principle.**

---

## CoCreateDB — Native Data and Indexing

CoCreateDB is a storage-agnostic JavaScript database engine built around first-class indexing.

It provides a native persistence option for CoCreateJS applications while remaining an independently useful database project.

### Documents and Storage

CoCreateDB is designed to persist JSON documents using configurable storage backends, including local filesystems and cloud object storage.

Collections can be represented through storage directories or equivalent namespaces.

### First-Class Indexing

Its indexing architecture organizes data by database, array, and key.

Indexes are segmented and maintain metadata that can support efficient lookup, filtering, and ordering.

The architecture emphasizes minimizing unnecessary document reads and making indexing primitives independently accessible.

### Runtime Integration

CoCreateDB integrates with CoCreateServer, allowing application operations and authorized tools to interact with data through the runtime.

This also creates opportunities for AI-assisted database exploration, index inspection, and query analysis.

### Distributed Data

CoCreateDB's architecture includes work toward distributed synchronization, on-demand caching, patch-based updates, and replica coordination.

The supported consistency and recovery guarantees depend on the implementation and deployment configuration.

### Optional by Design

CoCreateDB is not required to use CoCreateServer.

Developers can choose native storage or continue using their preferred supported database provider.

**Repository:** [CoCreateJS/db](https://github.com/CoCreateJS/db)

**Package:** `@cocreate/db`

---

## Security and Key Management

CoCreateJS is designed to integrate security throughout the application lifecycle.

Security capabilities include authentication, authorization, permissions, encryption-related services, and credential management.

### Application Security

Supported application patterns include:

- User authentication
- Organization and tenant isolation
- Role-based permissions
- Object-level access control
- Field-level access control
- API authorization
- Secure network communication

### CoCreateKMS

CoCreateKMS provides the architectural foundation for key and secret management.

Its responsibilities include managing access to cryptographic material, service credentials, and sensitive configuration according to the implementation and deployment environment.

### AI and Operational Security

AI-accessible tools introduce additional security requirements.

Applications should control:

- Which tools an agent can discover
- Which operations it can execute
- Which data it can access
- Which credentials are available
- Which actions require approval
- How execution is recorded
- How failures and unauthorized requests are handled

The objective is to enable useful automation without granting unnecessary privileges.

---

## Real-Time and Offline Applications

CoCreateJS combines browser-side persistence, real-time networking, and server-side data operations.

### Real-Time Capabilities

Applications can use supported modules for:

- WebSocket communication
- Data subscriptions
- Live updates
- Collaborative editing
- Shared application state
- Messaging
- Presence
- Distributed events

### Offline Capabilities

CoCreateClient can use IndexedDB and Service Workers to support local data access and offline application behavior.

```text
Application Interface
        |
        v
CoCreateClient
        |
        v
Local Storage / IndexedDB
        |
        v
Synchronization
        |
        v
CoCreateServer
        |
        v
Configured Database
```

Synchronization strategies and conflict handling depend on the application and configured modules.

### Progressive Web Apps

CoCreateClient supports applications built with standard web technologies that can be enhanced with offline resources, local persistence, and installable experiences.

---

## Workflows and Structured Execution

CoCreateJS uses structured operations to coordinate application behavior.

CoCreateAST provides a foundation for expressing executable logic and workflows as data.

### Applications as Structured Systems

Application definitions can include:

- Interfaces
- Components
- Data models
- Permissions
- Events
- API operations
- Workflows
- Runtime configuration
- Infrastructure definitions

### Workflow Execution

A workflow may coordinate multiple operations:

```text
Receive Event
      |
      v
Validate Permissions
      |
      v
Read Application Data
      |
      v
Evaluate Conditions
      |
      v
Execute Operations
      |
      v
Update State
      |
      v
Emit Results
```

### Workflows and AI

Structured workflows are particularly valuable for AI integration.

An agent can invoke an authorized workflow rather than attempting to execute arbitrary code.

The workflow can provide defined inputs, controlled operations, and structured results.

This allows application automation and AI-driven execution to share underlying capabilities.

### Scheduled Automation

CoCreateServer can coordinate supported cron jobs, scheduled tasks, and event-driven workflows.

Combined with application data and AI tools, these capabilities provide a foundation for recurring business and operational automation.

---

## Distributed Infrastructure and Multi-Cloud

CoCreateServer is designed for distributed execution across multiple infrastructure environments.

Supported and targeted environments include public cloud providers, self-managed servers, and compatible edge infrastructure.

### Distributed Runtime

```text
                    Global Routing
                          |
           +--------------+--------------+
           |              |              |
           v              v              v
        Region A        Region B        Region C
           |              |              |
      CoCreateServer CoCreateServer CoCreateServer
           |              |              |
        Workers         Workers         Workers
           |              |              |
           +--------------+--------------+
                          |
                    Runtime Mesh
                          |
                   Data & Services
```

### Infrastructure Capabilities

The architecture supports workflows for:

- Server provisioning
- Worker management
- Cluster coordination
- Application deployment
- Health monitoring
- Workload distribution
- Geographic placement
- Autoscaling
- Recovery
- Service configuration

Availability depends on the installed modules and provider integrations.

### AI-Assisted Operations

CoCreateAI can interact with exposed runtime tools to help analyze infrastructure and coordinate authorized operations.

For example, an agent could compare traffic density, regional latency, and existing server capacity before proposing a deployment.

With suitable tools and permissions, it could execute an approved workflow and inspect the resulting deployment.

### One Runtime Across Environments

CoCreateServer aims to provide consistent application behavior across compatible infrastructure environments.

Developers can use one runtime model while choosing where and how workloads execute.

---

## Modularity and Extensibility

CoCreateJS is a modular ecosystem.

Applications can use individual components without adopting the complete platform.

### Reusable Modules

Modules provide functionality for:

- Data operations
- Authentication
- Organizations
- Permissions
- Notifications
- File handling
- Messaging
- Integrations
- Background jobs
- Workflows
- AI
- Infrastructure operations

### Dynamic Loading

Modules can be imported when needed:

```javascript
await import('@cocreate/users');
await import('@cocreate/organizations');
await import('@cocreate/notification');
```

### Extensible Runtime

CoCreateServer allows developers to add custom routes, operations, services, and integrations.

```javascript
server.routes.set('/api/custom', async (req, res) => {
  res.writeHead(200, {
    'Content-Type': 'application/json'
  });

  res.end(JSON.stringify({
    message: 'Hello from CoCreateServer'
  }));
});
```

### Extensible AI Tools

Application capabilities can be exposed through structured MCP tools where supported.

This allows developers to extend the AI-accessible functionality of an application without duplicating its underlying business logic.

**Build the capability once. Expose it through the interfaces that need it.**

---

## Architecture

### Three Pillars. One Connected Ecosystem.

```text
                           CoCreateJS
                               |
             +-----------------+-----------------+
             |                 |                 |
             v                 v                 v
       CoCreateClient    CoCreateServer      CoCreateAI
             |                 |                 |
        Build & UI        Execute & Run     Understand & Act
             |                 |                 |
        Declarative       APIs / Routing     AI Models
        JavaScript        Networking         Agentic Workflows
        Real-Time         Workers            Business Automation
        Offline           Infrastructure     Intelligent Tools
             |                 |                 |
             +-----------------+-----------------+
                               |
                               v
                    Shared Capabilities
                               |
             +-----------------+-----------------+
             |                 |                 |
             v                 v                 v
         CoCreateDB       CoCreateMCP       CoCreateAST
             |                 |                 |
        Data / Indexes    AI Tool Access    Workflows
        Persistence       Tool Discovery    Automation
             |                 |                 |
             +-----------------+-----------------+
                               |
                               v
                     Supporting Services
                               |
                    Security / KMS / Cluster
                               |
                      Storage / APIs / Cloud
```

This diagram represents the conceptual product architecture rather than a strict runtime dependency graph.

CoCreateAI and external AI clients can access authorized runtime capabilities through CoCreateMCP.

CoCreateServer provides execution and infrastructure capabilities.

CoCreateClient provides application interfaces and user experiences.

Supporting modules extend the ecosystem without requiring every application to use every component.

### From Application to Business Operations

```text
User / Developer / Team
          |
          v
     CoCreateJS
          |
          +-- Build Interfaces
          |
          +-- Execute Applications
          |
          +-- Connect Data & APIs
          |
          +-- Automate Business Workflows
          |
          +-- Operate Infrastructure
          |
          +-- Enable AI Agents
          |
          v
    Connected Application
          |
          v
    Measurable Outcomes
```

The ecosystem connects the interface, execution environment, business operations, and intelligent automation.

---

## Use Cases

### Websites and Application Builders

Build interfaces, reusable components, and application experiences using declarative HTML and JavaScript.

### SaaS Platforms

Develop multi-tenant applications with shared data, permissions, APIs, and distributed infrastructure.

### CRM and Business Management

Manage customers, contacts, organizations, leads, activities, and operational records.

### Sales and Finance

Build workflows around invoices, payments, transactions, customer records, and reporting.

### Customer Communications

Coordinate email, SMS, messaging, customer support, and approval-driven response workflows through connected services.

### Marketing Automation

Research topics, generate content, prepare campaigns, schedule communications, and analyze performance through supported integrations.

### AI-Powered Business Operations

Connect intelligent agents to business data and application tools to assist with daily operations and recurring workflows.

### AI-Assisted Software Development

Use connected AI capabilities to assist with application creation, code changes, testing, debugging, and deployment.

### Real-Time Collaboration

Build collaborative applications, shared workspaces, dashboards, messaging systems, and live data experiences.

### Offline and Mobile Applications

Develop applications with local persistence, synchronization, and cross-platform deployment options.

### API and Workflow Automation

Connect external services and coordinate application operations through structured workflows.

### Distributed Infrastructure

Deploy and operate applications across servers, regions, and cloud providers.

### AI-Assisted Infrastructure Management

Use authorized runtime tools to analyze telemetry, recommend infrastructure changes, execute approved workflows, and inspect results.

### Existing Application Modernization

Add data services, real-time connectivity, automation, AI tools, or distributed capabilities to existing applications.

---

## Design Philosophy

### 1. JavaScript First

Use familiar JavaScript primitives and APIs across client, server, and application services.

### 2. Dual API

Support both declarative HTML and programmatic JavaScript where appropriate.

Developers should be able to choose the interface that best fits the task.

### 3. Primitives Over Unnecessary Abstractions

Expose useful capabilities directly without introducing avoidable complexity.

### 4. Modularity Without Fragmentation

Keep components independently useful while maintaining consistent conventions across the ecosystem.

### 5. Database Freedom

Support multiple storage providers through compatible adapters.

Native storage should expand options, not eliminate them.

### 6. Infrastructure Independence

Allow applications to operate across supported cloud providers and deployment environments.

### 7. Real-Time and Offline by Design

Treat connectivity, synchronization, and local operation as core application capabilities.

### 8. AI-Native, Not AI-Dependent

Make application capabilities accessible to intelligent agents without requiring AI for ordinary application execution.

### 9. From Intent to Execution

Connect reasoning and decision-making to structured application operations and workflows.

### 10. Security Throughout the Lifecycle

Apply authentication, authorization, permissions, and operational safeguards across applications, tools, data, and infrastructure.

### 11. Progressive Adoption

Use the capabilities you need and extend the ecosystem as your requirements grow.

### 12. Build Applications, Not Infrastructure

Reduce the operational complexity required to create and run useful applications.

---

## Project Repositories

CoCreateJS is developed by **CoCreate** and organized under the [CoCreateJS GitHub organization](https://github.com/CoCreateJS).

### Main Project

**[CoCreateJS](https://github.com/CoCreateJS/CoCreateJS)**

The main project repository and global documentation for the CoCreateJS ecosystem.

### Primary Pillars

| Project | Repository | Package |
|---|---|---|
| **CoCreateClient** | [CoCreateJS/Client](https://github.com/CoCreateJS/Client) | `@cocreate/client` |
| **CoCreateServer** | [CoCreateJS/Server](https://github.com/CoCreateJS/Server) | `@cocreate/server` |
| **CoCreateAI** | CoCreateJS organization | `@cocreate/ai` |

### Supporting Technologies

| Project | Description |
|---|---|
| **[CoCreateDB](https://github.com/CoCreateJS/db)** | Native database engine and first-class indexing |
| **CoCreateMCP** | MCP-compatible access to authorized runtime capabilities |
| **CoCreateAST** | Structured workflow execution |
| **CoCreateKMS** | Key and secret management |
| **CoCreateCluster** | Distributed execution and coordination |
| **CoCreateCLI** | Development and operational commands |
| **CoCreateDevice** | Cross-platform and device integrations |

Additional modules and integrations are available through the organization and their respective packages.

---

## Contributing

CoCreateJS is an open-source ecosystem, and contributions are welcome.

Contributions may include:

- Bug fixes
- Documentation improvements
- New modules
- Storage adapters
- API integrations
- Client enhancements
- Server runtime improvements
- AI integrations
- MCP tools
- Workflow capabilities
- Security improvements
- Performance optimizations
- Tests and examples

Before contributing, review the relevant repository's existing issues, documentation, and contribution guidelines.

We encourage implementations that preserve the project's core principles: JavaScript-first development, consistent APIs, modularity, interoperability, and infrastructure independence.

---

## License

CoCreateJS is distributed under the **GNU Affero General Public License v3.0 (AGPL-3.0)**.

Individual repositories may contain their own license files or additional notices. Review the relevant repository before using or distributing a component.

### Commercial Licensing and Enterprise Support

For commercial licensing, enterprise support, integrations, or deployment inquiries:

**Email:** [info@cocreatejs.com](mailto:info@cocreatejs.com)

**Website:** https://cocreatejs.com

---

## Resources

- **Website:** https://cocreatejs.com
- **Documentation:** https://cocreatejs.com/docs
- **Main GitHub Repository:** https://github.com/CoCreateJS/CoCreateJS
- **GitHub Organization:** https://github.com/CoCreateJS
- **CoCreateClient:** https://github.com/CoCreateJS/Client
- **CoCreateServer:** https://github.com/CoCreateJS/Server
- **CoCreateDB:** https://github.com/CoCreateJS/db
- **Contact:** [info@cocreatejs.com](mailto:info@cocreatejs.com)

---

## CoCreateJS

### One build. Connects anything. Deploys everywhere.

From the first line of HTML to distributed infrastructure, CoCreateJS brings application development, connectivity, data, security, AI, and deployment together in one JavaScript ecosystem.

**CoCreateClient** builds the experience.

**CoCreateServer** executes and operates the application.

**CoCreateAI** connects intelligence to the people, processes, and capabilities behind it.

Together, they enable developers, teams, and intelligent agents to build applications, automate business operations, and manage infrastructure through one connected ecosystem.

**Build applications, not infrastructure.**

Developed by **CoCreate**.
