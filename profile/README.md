# CoCreateJS

### One build. Connects anything. Deploys everywhere.

**An AI-native JavaScript ecosystem for building, connecting, deploying, and operating applications.**

From declarative interfaces to distributed infrastructure, CoCreateJS unifies application development, real-time communication, databases, security, AI-powered automation, and cloud orchestration in one extensible JavaScript ecosystem.

Build applications with JavaScript. Connect AI through MCP. Give authorized agents the tools to understand, build, and operate your applications.

CoCreateJS brings together two independent but complementary runtimes, a growing collection of reusable modules, and integrated services designed to support the complete application lifecycle.

### [CoCreateClient](https://github.com/CoCreateJS/CoCreateJS)

**One code. Build anything. Run anywhere.**

A lightweight, declarative and programmatic JavaScript runtime for building reactive, connected, collaborative, and offline-capable applications.

Create websites, dashboards, business applications, Progressive Web Apps, and cross-platform experiences using familiar HTML and JavaScript.

Use declarative HTML attributes, headless JavaScript APIs, or both.

**Package:** `@cocreate/client`

### [CoCreateServer](https://github.com/CoCreateJS/CoCreate-server)

**One runtime. Any app. Every cloud.**

A distributed JavaScript runtime for hosting applications, exposing APIs, managing data, coordinating services, and operating infrastructure across cloud environments.

Run standalone applications, extend existing systems, or build distributed platforms with integrated networking, storage, security, automation, and AI-accessible capabilities.

**Package:** `@cocreate/server`

CoCreateClient and CoCreateServer can operate independently or together.

Through CoCreateDB, CoCreateAI, CoCreateMCP, structured workflows, and infrastructure services, the ecosystem extends beyond application development into the systems that run and manage applications.

**One JavaScript ecosystem. From interface to infrastructure.**

---

## Table of Contents

- [Why CoCreateJS?](#why-cocreatejs)
- [The CoCreateJS Ecosystem](#the-cocreatejs-ecosystem)
- [AI-Native Applications and Infrastructure](#ai-native-applications-and-infrastructure)
- [Quick Start](#quick-start)
- [CoCreateClient](#cocreateclient)
- [CoCreateServer](#cocreateserver)
- [CoCreateDB](#cocreatedb)
- [CoCreateAI](#cocreateai)
- [CoCreateMCP](#cocreatemcp)
- [Security and Key Management](#security-and-key-management)
- [Self-Contained Infrastructure](#self-contained-infrastructure)
- [Unified APIs and Connectivity](#unified-apis-and-connectivity)
- [Real-Time Collaboration and Offline Applications](#real-time-collaboration-and-offline-applications)
- [Distributed Infrastructure and Multi-Cloud](#distributed-infrastructure-and-multi-cloud)
- [Application Definitions and AST Workflows](#application-definitions-and-ast-workflows)
- [AI-Driven Development and Operations](#ai-driven-development-and-operations)
- [Build Once, Run Across Devices](#build-once-run-across-devices)
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

Modern application development often requires assembling and maintaining numerous independent technologies.

A typical application may depend on:

- A frontend framework
- A backend runtime
- REST and WebSocket services
- A database and caching layer
- Authentication and authorization services
- Secret and key management
- File and object storage
- Background jobs and workers
- API integrations
- Deployment pipelines
- Load balancing and service discovery
- Monitoring and autoscaling
- Cloud infrastructure and DNS management
- AI models, agents, and tool integrations

Each introduces dependencies, configuration, security considerations, and operational complexity.

**CoCreateJS takes a different approach.**

Instead of treating every application capability as a separate infrastructure problem, CoCreateJS provides a consistent set of JavaScript primitives, APIs, modules, and services that work together across client, server, data, AI, and infrastructure environments.

The ecosystem is designed around several principles.

**Less boilerplate.** Common application behaviors can be expressed through declarative HTML, JavaScript APIs, and reusable modules.

**Fewer dependencies.** Integrated services can reduce reliance on external infrastructure without preventing applications from using it.

**One development model.** Shared concepts such as arrays, objects, keys, events, and structured operations carry across browser, server, and database environments.

**Real-time by design.** WebSockets, subscriptions, collaboration, and synchronization are foundational application capabilities.

**Infrastructure independence.** Applications can operate across cloud providers, storage systems, and deployment environments.

**AI-native capabilities.** AI clients and agents can interact with exposed application and infrastructure tools through CoCreateMCP.

**Incremental adoption.** Use CoCreateClient, CoCreateServer, CoCreateDB, or individual modules independently.

**A complete application lifecycle.** Build, connect, secure, deploy, operate, scale, and evolve applications through a unified ecosystem.

CoCreateJS is not intended to replace every technology developers already use.

**It is designed to make fewer technologies mandatory.**

---

## The CoCreateJS Ecosystem

CoCreateJS is the overarching JavaScript project developed by **CoCreate**.

Its components are designed to operate independently while sharing compatible APIs, conventions, and integration patterns.

| Component | Purpose |
|---|---|
| **CoCreateClient** | Declarative interfaces, application behavior, reactivity, and offline capabilities |
| **CoCreateServer** | Distributed runtime, application hosting, networking, and infrastructure coordination |
| **CoCreateDB** | Storage-agnostic JavaScript database engine with first-class indexing |
| **CoCreateAI** | Declarative AI interfaces, model connectivity, and agentic application experiences |
| **CoCreateMCP** | AI-accessible tool interface for exposed server capabilities |
| **CoCreateKMS** | Key and secret management for application and infrastructure security |
| **CoCreateCluster** | Distributed execution, worker management, and mesh coordination |
| **CoCreateDevice** | Cross-platform application packaging and device integration |
| **CoCreateCLI** | Development, installation, deployment, and environment workflows |
| **CoCreateAST** | Structured application logic, workflows, and automation |
| **CoCreate Modules** | Reusable capabilities across the ecosystem |

Components and integrations evolve independently. Availability and supported operations depend on the corresponding package, runtime version, and deployment configuration.

### Independent by Design

Developers can use:

- CoCreateClient with an existing backend.
- CoCreateServer with an existing frontend.
- CoCreateDB independently of the complete runtime.
- CoCreateAI inside custom application interfaces.
- CoCreateMCP with compatible external AI clients.
- Individual modules inside existing applications.
- The complete ecosystem for integrated application and infrastructure development.

**Adopt what you need. Extend what you want.**

---

## AI-Native Applications and Infrastructure

### Build with AI. Connect through MCP. Operate through One Runtime.

CoCreateJS integrates artificial intelligence into the same architecture responsible for building, connecting, deploying, and operating applications.

Through **CoCreateMCP**, compatible AI clients can discover and execute authorized CoCreateServer capabilities, connecting AI agents to application data, APIs, workflows, runtime configuration, and infrastructure operations.

Through **CoCreateAI**, developers can build AI-powered application experiences declaratively, using the same HTML and JavaScript foundation that powers the rest of CoCreateJS.

The result is an architecture where AI can do more than generate code.

**AI can interact with the application and the infrastructure that runs it.**

### One Runtime, Shared Capabilities

CoCreateServer provides the operational foundation for application execution.

It coordinates networking, routing, workers, storage, data operations, security, workflows, and distributed infrastructure.

CoCreateMCP provides a standard interface through which authorized AI clients can discover and invoke exposed runtime capabilities.

CoCreateAI provides the application-facing AI experience, including declarative chat interfaces and agentic workflows.

CoCreateDB provides integrated data access and indexing, allowing authorized tools to query application data and inspect database structure.

Together, these components establish a shared operational environment for developers, applications, and AI agents.

```text
                    CoCreateJS
                         |
          +--------------+--------------+
          |                             |
          v                             v
    CoCreateClient                 CoCreateAI
    Applications                   AI Interfaces
    Declarative UI                 Agentic Workflows
          |                             |
          |                       AI Models
          |                             |
          +--------------+--------------+
                         |
                         v
                    CoCreateMCP
                         |
              Discoverable Tools
                         |
                         v
                   CoCreateServer
                         |
             Runtime & Authorization
                         |
       +-----------------+-----------------+
       |                 |                 |
       v                 v                 v
   CoCreateDB        CoCreateAST       Infrastructure
   Data & Indexes    Workflows         Cloud & Mesh
       |                 |                 |
       +-----------------+-----------------+
                         |
                         v
                  Applications
                  Data & Services
                  Infrastructure
```

External MCP-compatible AI clients can also connect through CoCreateMCP without requiring CoCreateAI as their interface.

### More Than Code Generation

Traditional AI-assisted development often ends when source code has been generated.

CoCreateJS extends the opportunity into the running application environment.

Authorized AI agents can interact with capabilities such as:

**Applications**

- Create and modify application resources
- Work with interfaces and components
- Inspect application configuration
- Execute application operations

**Data**

- Query CoCreateDB
- Discover available arrays and keys
- Inspect index definitions and metadata
- Perform authorized data operations
- Analyze query and storage behavior

**Workflows**

- Discover available AST workflows
- Execute structured operations
- Coordinate application and external APIs
- Automate repeatable processes

**Infrastructure**

- Inspect runtime configuration
- Work with deployment definitions
- Execute authorized provisioning workflows
- Monitor application and server state
- Assist with scaling, diagnostics, and recovery

The available capabilities are determined by the tools exposed through CoCreateMCP and the permissions granted to the requesting identity.

### AI as a Native Participant

CoCreateJS is designed so that application capabilities do not need to be implemented separately for developers, visual interfaces, and AI agents.

The same underlying operations can be exposed through:

- Declarative HTML
- JavaScript APIs
- Structured workflows
- Application interfaces
- MCP tools
- AI-driven automation

This creates a foundation for applications that are both programmable and agent-accessible.

**Build the capability once. Make it available wherever it belongs.**

---

## Quick Start

CoCreateClient and CoCreateServer can be used independently.

### CoCreateClient

Include the browser runtime:

```html
<script src="https://cdn.cocreate.app/latest/CoCreate.min.js"></script>
```

Add application behavior directly to HTML:

```html
<input
  array="users"
  object="5f8d04f1"
  key="name"
  placeholder="Enter your name"
  save
/>
```

The element is associated with an application object and key.

Configured CoCreate modules can provide data binding, persistence, reactivity, and synchronization.

No separate frontend framework is required.

For developers who prefer JavaScript, the same ecosystem exposes programmatic APIs.

### CoCreateServer

Install the server runtime:

```bash
npm install @cocreate/server
```

Initialize the runtime:

```javascript
import server from '@cocreate/server';

await server.init();

if (server.isPrimary) {
  // Initialize primary-process capabilities.
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

CoCreateServer provides an extensible environment for application routes, APIs, sockets, storage, and distributed coordination.

### Extend the Runtime

Modules can be loaded according to the responsibilities of each process.

```javascript
if (server.isPrimary) {
  await import('@cocreate/cron-jobs');
}

if (server.isWorker) {
  await import('@cocreate/users');
  await import('@cocreate/organizations');
}
```

Applications control which capabilities are loaded and where they execute.

---

## CoCreateClient

### One code. Build anything. Run anywhere.

CoCreateClient is a lightweight JavaScript runtime for building interactive, connected, and offline-capable applications.

It combines declarative HTML with headless JavaScript APIs, allowing developers to choose how application behavior is expressed.

The objective is simple:

**Spend less time implementing repetitive functionality and more time creating the application experience.**

### Declarative HTML

CoCreateClient extends standard HTML through attributes that describe application behavior.

```html
<form array="users" object>
  <input key="name" placeholder="Full name" />
  <input key="email" type="email" placeholder="Email" />

  <button actions="save">
    Save User
  </button>
</form>
```

Application behavior can be expressed without manually implementing every event listener, state update, network request, or serialization step.

### Headless JavaScript

The declarative layer is optional.

Developers can use JavaScript directly for data operations, application events, sockets, and custom logic.

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

The same underlying capabilities can be exposed through HTML attributes, JavaScript APIs, and reusable modules.

### Client Capabilities

- Declarative HTML attributes
- Headless JavaScript APIs
- Reactive data binding
- Application state management
- CRUD operations
- WebSocket connectivity
- Real-time subscriptions
- Collaborative editing
- IndexedDB integration
- Offline data handling
- Service Worker integration
- Progressive Web Apps
- Component composition
- Form management
- File uploads
- Lazy-loaded modules
- Framework interoperability
- Responsive and device-friendly applications

### Framework Agnostic

CoCreateClient can operate independently or alongside other frontend technologies.

Applications can integrate with React, Vue, Angular, Svelte, Web Components, plain JavaScript, and custom rendering systems.

Developers can adopt individual capabilities without replacing their existing frontend architecture.

### Lightweight by Design

CoCreateClient favors modular, lazy-loaded capabilities.

Earlier reference configurations targeted approximately 70 KB for the initial client runtime and approximately 410 KB for the complete loaded ecosystem.

These are reference measurements rather than universal bundle sizes. Actual sizes depend on the build, enabled modules, and compression method.

**Repository:** [CoCreateClient](https://github.com/CoCreateJS/CoCreateJS)

**Package:** `@cocreate/client`

---

## CoCreateServer

### One runtime. Any app. Every cloud.

CoCreateServer is a distributed JavaScript runtime designed to run applications, expose services, coordinate infrastructure, and connect systems across environments.

It can operate as an application server, extend an existing application, or provide the foundation for a distributed application platform.

CoCreateServer does not require CoCreateClient.

It can support applications built with other frontend and backend technologies through compatible networking and API interfaces.

### One Runtime, Multiple Responsibilities

CoCreateServer brings together capabilities traditionally distributed across multiple services:

- HTTP and HTTPS
- TLS certificate management
- WebSockets
- Application routing
- API execution
- Static file delivery
- Primary and worker processes
- Inter-process communication
- Cluster coordination
- Distributed messaging
- Data operations
- Storage integrations
- Authentication and authorization
- Background jobs
- Telemetry and health monitoring
- Autoscaling and lifecycle management
- Multi-cloud coordination
- AI-accessible tools through CoCreateMCP

The runtime is modular, allowing capabilities to be loaded only where they are needed.

### An AI-Accessible Runtime

CoCreateServer is more than an execution environment for application code.

Its runtime object provides access to application and infrastructure capabilities through programmatic interfaces.

CoCreateMCP makes selected capabilities accessible to compatible AI clients through structured tools.

This allows authorized agents to interact with the running environment rather than relying exclusively on source-code generation or external automation scripts.

An agent may be able to:

- Inspect runtime state
- Discover available operations
- Query application data
- Execute structured workflows
- Manage configured services
- Interact with infrastructure integrations

Access must remain controlled through tool definitions, authorization, and operational safeguards.

### Primary and Worker Architecture

Each runtime node can manage its own primary process and workers.

The primary process coordinates local runtime responsibilities, while workers execute assigned application capabilities.

Nodes can communicate across a distributed mesh without depending on a permanent global primary.

### One Configuration Model

CoCreateServer uses JavaScript, JSON, and structured application definitions to express runtime behavior.

Configuration can be targeted to individual clusters, servers, workers, organizations, or services.

A unified configuration model does not require every node to share an identical configuration.

Each deployment can define its own responsibilities while participating in the broader ecosystem.

### Run Any Application

CoCreateServer supports several adoption patterns.

**Build directly on the runtime.** Use its networking, routing, data, and orchestration capabilities as the application foundation.

**Extend an existing application.** Integrate CoCreate services with an established frontend or backend.

**Run distributed services.** Deploy coordinated nodes across regions and providers.

**Build an application platform.** Operate multiple applications, organizations, and environments.

**Enable agentic operations.** Expose authorized runtime capabilities to compatible AI clients through CoCreateMCP.

**Repository:** [CoCreateServer](https://github.com/CoCreateJS/CoCreate-server)

**Package:** `@cocreate/server`

---

## CoCreateDB

### Storage-Agnostic Data. First-Class Indexing.

CoCreateDB is a JavaScript database engine designed to make structured data accessible without requiring a traditional standalone database service for every deployment.

Its architecture centers on an independently accessible indexing primitive and a storage-agnostic document model.

Rather than requiring all data to live inside a single proprietary storage engine, CoCreateDB is designed to work with storage backends such as:

- Local filesystems
- Attached storage volumes
- Cloud object storage
- S3-compatible storage
- Distributed storage environments

### Documents as Data

CoCreateDB uses a document-oriented model.

Collections can map to storage directories or equivalent namespaces, while documents are serialized as JSON.

The engine manages indexing, retrieval, updates, and data access above the storage layer.

### Indexing as a First-Class Primitive

Indexing is central to CoCreateDB's design.

Indexes are organized by database, array, and key, including nested keys expressed through dot notation.

The segmented index architecture is designed to:

- Minimize unnecessary document reads
- Support ordered lookups
- Narrow query candidates efficiently
- Support filtering and sorting
- Scale index metadata incrementally
- Operate across different storage backends

Indexing primitives are intended to remain independently accessible rather than hidden inside the database engine.

### Data on Disk. Data Through the Runtime.

CoCreateDB provides two complementary ways to work with application data.

**Persistent storage** keeps documents and indexes in configured filesystem or object-storage backends.

**Runtime access** exposes database operations and structural information through JavaScript APIs.

This separation is particularly useful for automation and AI.

Authorized tools can query the database through CoCreateServer while also accessing supported metadata about indexes, storage organization, and data structures.

The database can expose information such as:

- Available databases
- Arrays and objects
- Indexed keys
- Index metadata
- Storage adapters
- Data partitions
- Query operations
- Runtime storage state

This provides the foundation for AI-assisted database exploration, query analysis, and operational diagnostics.

Direct filesystem inspection depends on the storage format, encryption configuration, and access permissions. Encrypted files are not assumed to be readable by CLI tools without authorized decryption.

### Designed for Distributed Applications

CoCreateDB's evolving architecture includes:

- On-demand data access
- Configurable caching
- Document-oriented CRUD
- Field-level patch operations
- Index-driven query planning
- Pub/sub-based synchronization
- Replica bootstrap between nodes
- Eventual consistency models
- Integration with the CoCreateServer mesh

Distributed behaviors require appropriate conflict handling, persistence guarantees, and recovery strategies for each deployment.

### Database Freedom

CoCreateDB expands the ecosystem's ability to operate without an external database service.

It does not remove support for existing databases.

CoCreateServer can continue to integrate with storage engines such as MongoDB, PostgreSQL, MySQL, SQLite, Firestore, and other supported providers.

Applications can choose between CoCreateDB, existing database systems, or a combination of storage services.

**The application API should not have to change simply because the storage backend changes.**

**Repository:** [CoCreateDB](https://github.com/CoCreateJS/db)

**Package:** `@cocreate/db`

---

## CoCreateAI

### Declarative AI. Connected Intelligence. Agentic Execution.

CoCreateAI brings artificial intelligence directly into the CoCreateJS application experience.

Developers can create AI-powered interfaces using declarative HTML and existing CoCreateClient capabilities.

This makes AI a natural extension of application development rather than a separate interface framework.

### Declarative AI Interfaces

CoCreateAI supports building application-integrated chat experiences using familiar HTML and JavaScript.

These interfaces can incorporate application styling, components, controls, and structured interactions.

Developers can create AI experiences that fit naturally within websites, dashboards, administrative systems, and application builders.

### Model-Agnostic Architecture

CoCreateAI is designed around configurable AI connectivity rather than a permanent dependency on one model provider.

The architecture aims to support compatible AI models and services while maintaining consistent application-facing interfaces.

This allows the AI experience to evolve independently of the underlying model implementation.

### Agentic Application Experiences

CoCreateAI can serve as an entry point for AI-driven application operations.

Through connected tools and workflows, authorized agents can assist with:

- Building application interfaces
- Creating application resources
- Working with data
- Executing structured workflows
- Connecting external services
- Managing configured application operations
- Initiating deployment and infrastructure workflows

The long-term architecture uses CoCreateMCP as the common tool interface for CoCreateAI and external AI clients.

This allows the application-facing AI experience to reuse capabilities already exposed by CoCreateServer.

### AI Without a Separate Application Stack

CoCreateAI follows the same development philosophy as the rest of CoCreateJS.

Developers can build the interface declaratively, connect it to application capabilities, and extend behavior through JavaScript.

**AI becomes another native application capability.**

**Package:** `@cocreate/ai`

---

## CoCreateMCP

### One Interface to Application and Infrastructure Capabilities.

CoCreateMCP exposes CoCreateServer capabilities through the Model Context Protocol.

It enables compatible AI clients to discover available tools and invoke authorized operations.

Because CoCreateServer already coordinates application services, data, workflows, and infrastructure, CoCreateMCP can provide access to those capabilities without requiring a separate integration for every AI provider.

### Discoverable Tools

CoCreateMCP provides a standardized way for AI clients to interact with exposed runtime operations.

Depending on configuration and permissions, these tools may provide access to:

- Application APIs
- Data operations
- CoCreateDB queries
- Database metadata
- AST workflows
- Runtime configuration
- Server operations
- External service integrations
- Deployment workflows
- Infrastructure management

### External and Internal AI

CoCreateMCP supports two complementary integration patterns.

**External AI clients** connect to exposed MCP tools and interact with authorized CoCreateServer capabilities.

**CoCreateAI** can use the same tool interface to execute agentic workflows within CoCreateJS applications.

This shared approach separates the AI model from the tools it can use.

Applications can change AI providers without needing to reimplement every underlying server operation.

### The Server as a Capability Platform

CoCreateServer provides the underlying application and infrastructure functionality.

CoCreateMCP exposes selected functionality through structured tool definitions.

AI clients discover and invoke those tools according to their permissions.

```text
AI Client
    |
    v
CoCreateMCP
    |
    v
Tool Discovery & Authorization
    |
    v
CoCreateServer
    |
    +-- Application APIs
    |
    +-- CoCreateDB
    |
    +-- CoCreateAST
    |
    +-- Runtime Configuration
    |
    +-- Infrastructure Services
```

CoCreateMCP is not intended to provide unrestricted access to every server method or internal object.

Sensitive operations should be exposed through controlled capabilities with authentication, authorization, validation, auditing, and appropriate approval requirements.

### Build Once. Expose as a Tool.

When application capabilities are structured and reusable, they can be made accessible through multiple interfaces.

A capability may be invoked by:

- A declarative HTML action
- A JavaScript function
- An application API
- An AST workflow
- An MCP-compatible AI client

**One capability. Multiple ways to interact with it.**

---

## Security and Key Management

Security is a foundational part of the CoCreateJS architecture.

The ecosystem is designed to coordinate application identity, permissions, credentials, and infrastructure access through reusable security capabilities.

### Authentication and Authorization

CoCreate modules support application patterns including:

- User authentication
- Organization and tenant isolation
- Role-based access control
- Object-level permissions
- Field-level permissions
- API authorization
- Workflow authorization
- Secure communication over TLS

### CoCreateKMS

CoCreateKMS is the ecosystem's key-management component, intended to centralize cryptographic key and secret-management responsibilities.

Its architectural role includes supporting:

- Application secrets
- Encryption key management
- Key lifecycle and rotation
- Service credentials
- Infrastructure credentials
- Controlled access to sensitive configuration
- Integration with authentication and authorization workflows

The exact security guarantees depend on the KMS implementation, configured key protection, access policies, and deployment environment.

Centralizing key management simplifies integration but does not eliminate the need for secure key storage, auditing, recovery, and operational controls.

### Security for AI-Accessible Infrastructure

When AI agents can interact with application and infrastructure capabilities, authorization becomes especially important.

CoCreateMCP should expose operations through defined tools rather than unrestricted runtime access.

Sensitive operations may require:

- Authenticated identities
- Scoped permissions
- Tool-level authorization
- Input validation
- Execution limits
- Audit logging
- Human approval for consequential actions
- Restricted access to secrets and credentials

The objective is to make infrastructure accessible to authorized automation without removing operational control.

### Security Across the Lifecycle

```text
Application Identity
        |
        v
Authentication & Permissions
        |
        v
Key & Secret Management
        |
        v
Authorized APIs & MCP Tools
        |
        v
Structured Workflows
        |
        v
Protected Data & Infrastructure
```

Security is not an optional layer added after deployment.

It is part of how applications, agents, services, data, and infrastructure interact.

---

## Self-Contained Infrastructure

### From Application to Infrastructure

One of the central architectural goals of CoCreateJS is to reduce dependence on separately operated infrastructure services.

A complete application environment may require:

- A runtime
- A database
- Key management
- Networking
- TLS
- Authentication
- Storage
- Background execution
- Monitoring
- Deployment automation
- Scaling
- Recovery
- AI-accessible operations

CoCreateJS is evolving toward an integrated model in which these responsibilities can be coordinated within the ecosystem.

### A Closed Infrastructure Lifecycle

The intended lifecycle connects the stages of application operation:

```text
Define Application
        |
        v
Build & Configure
        |
        v
Provision Infrastructure
        |
        v
Deploy Runtime
        |
        v
Initialize Storage & Security
        |
        v
Connect Services & AI Tools
        |
        v
Monitor & Scale
        |
        v
Recover, Update & Optimize
        |
        +------> Continuous Lifecycle
```

This model aims to make infrastructure reproducible, replaceable, and manageable through application-level workflows.

### AI Across the Lifecycle

Because CoCreateServer provides operational capabilities and CoCreateMCP can expose them as tools, authorized AI agents can participate in different stages of the lifecycle.

An agent might help configure an application, inspect its data, execute a deployment workflow, diagnose runtime behavior, or recommend infrastructure changes.

The same underlying services remain available to developers and conventional application automation.

AI is an additional interface to the system, not a replacement for its underlying capabilities.

### Self-Contained Does Not Mean Isolated

Applications can still connect to:

- External databases
- Third-party APIs
- Cloud services
- Existing authentication providers
- External key-management services
- Object storage
- Content delivery networks
- AI providers
- Custom infrastructure

The distinction is that CoCreateJS aims to make many common dependencies optional rather than mandatory.

**Own the application lifecycle without giving up integration freedom.**

---

## Unified APIs and Connectivity

### Connect Anything

CoCreateJS uses a consistent set of concepts to connect applications, data, services, AI agents, and infrastructure.

Its APIs are designed around familiar JavaScript structures and operations.

### A Shared Vocabulary

Common concepts include:

- `array` — a collection or group of objects
- `object` — a structured record or application entity
- `key` — an object property, including nested dot-notation paths
- `filter` — criteria for selecting and organizing data
- `on` — event or subscription handling
- `emit` — event or operation dispatch

These concepts can appear across client interfaces, server modules, database engines, and structured workflows.

### Unified Object Operations

```javascript
crud.send({
  method: 'object.read',
  array: 'users',
  filter: {
    query: {
      active: true
    },
    sort: {
      created: -1
    },
    limit: 25
  }
});
```

The same object-oriented operation model can be routed through supported modules and storage adapters.

### Multiple Communication Paths

CoCreateJS supports architectures using:

- HTTP and HTTPS
- WebSockets
- JavaScript events
- Inter-process communication
- Server-to-server messaging
- Distributed mesh communication
- REST APIs
- GraphQL integrations
- Model Context Protocol
- Provider-specific APIs
- Custom protocols

The goal is not to force every connection through one transport.

It is to make application capabilities accessible through consistent interfaces while preserving the requirements of each protocol.

### Connect Existing Systems

CoCreateJS is designed to integrate with existing infrastructure and applications.

Adopting CoCreateServer does not require replacing an existing frontend.

Adopting CoCreateClient does not require replacing an existing backend.

Using CoCreateDB does not require abandoning other supported storage engines.

Connecting an AI client does not require rebuilding the application around that model.

**Integration is a capability, not a migration requirement.**

---

## Real-Time Collaboration and Offline Applications

CoCreateJS combines client-side persistence, real-time communication, and server-side data operations to support connected applications that can continue functioning through intermittent connectivity.

### Real-Time Capabilities

Applications can use configured modules for:

- Live data binding
- Real-time subscriptions
- Collaborative editing
- Shared application state
- Event broadcasting
- Presence and messaging
- Distributed synchronization

### Offline-First Development

CoCreateClient can use browser capabilities such as IndexedDB and Service Workers to support offline workflows.

```text
Application Interface
        |
        v
CoCreateClient
        |
        v
Local IndexedDB
        |
        v
Synchronization Layer
        |
        v
CoCreateServer
        |
        v
CoCreateDB / Storage Adapters
```

Applications can read and update locally available data and synchronize changes when connectivity returns.

Conflict resolution and consistency guarantees depend on the configured synchronization strategy.

### Progressive Web Apps

CoCreateClient supports Progressive Web Application development through standard web technologies and compatible modules.

Applications can combine:

- Offline resources
- Installable web experiences
- Local persistence
- Background synchronization patterns
- Responsive interfaces
- Real-time updates when connected

---

## Distributed Infrastructure and Multi-Cloud

### Every Cloud

CoCreateServer is designed to operate across multiple infrastructure providers and deployment environments.

Potential targets include:

- Amazon Web Services
- Google Cloud
- Microsoft Azure
- Oracle Cloud Infrastructure
- DigitalOcean
- Other supported cloud providers
- Bare-metal servers
- Self-managed infrastructure
- Edge environments

Provider support and automated provisioning capabilities depend on configured integrations.

### Distributed Runtime Nodes

Each node can provide application and networking capabilities while participating in a larger cluster or mesh.

```text
                  Global Routing
                        |
           +------------+------------+
           |            |            |
           v            v            v
       Region A      Region B      Region C
           |            |            |
      CoCreateServer CoCreateServer CoCreateServer
           |            |            |
        Workers        Workers      Workers
           |            |            |
           +------------+------------+
                        |
                Distributed Mesh
                        |
              Shared Data & State
```

Nodes can coordinate routing, messaging, health, and application workloads according to deployment configuration.

### Autoscaling and Recovery

The runtime architecture supports workflows for:

- Node provisioning
- Worker allocation
- Health monitoring
- Horizontal scaling
- Vertical scaling
- Geographic placement
- Node draining
- Workload migration
- Replacement of unhealthy nodes
- Scale-to-zero strategies
- Rejoining and synchronization

The goal is to make application infrastructure responsive to actual demand.

### Geographic Routing

CoCreateJS's infrastructure roadmap includes geographically aware routing through DNS and edge-provider integrations.

Applications can use location and latency information to select appropriate runtime regions, with the goal of bringing application execution and data closer to users.

### No Permanent Global Primary

Individual runtime nodes can manage local primary and worker processes.

Distributed coordination does not require treating one permanent global server as the owner of every application operation.

This architecture supports independently operating nodes that participate in shared services and configured synchronization mechanisms.

### AI-Assisted Infrastructure Operations

CoCreateMCP creates a standardized way for authorized AI agents to interact with exposed infrastructure tools.

Agents can assist with inspecting configuration, initiating workflows, diagnosing failures, and coordinating operational tasks.

The runtime remains responsible for executing operations and enforcing configured permissions.

---

## Application Definitions and AST Workflows

CoCreateJS is designed to represent more than application data.

Application behavior, configuration, and workflows can also be expressed as structured information.

### Applications as Data

Application definitions may include:

- HTML
- CSS
- JavaScript
- Components
- Configuration
- Permissions
- Data models
- API definitions
- AST workflows
- Infrastructure definitions

This allows compatible application behavior to be stored, inspected, versioned, synchronized, and executed through reusable mechanisms.

### Structured Execution

CoCreateAST provides a model for expressing operations and workflows as structured data.

A workflow may coordinate:

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
Call External Services
      |
      v
Update State
      |
      v
Emit Results
```

Structured execution creates opportunities for:

- Reusable workflows
- Declarative automation
- Permission-controlled operations
- Visual workflow builders
- AI-assisted application behavior
- Auditable execution paths

AST execution must enforce appropriate validation, authorization, and resource limits.

### Workflows as AI Tools

Structured workflows are particularly useful for AI integration.

Instead of giving an agent unrestricted access to arbitrary code execution, applications can expose defined operations through CoCreateMCP.

An agent can discover a tool, provide structured inputs, and receive results from the workflow.

This approach connects AI-driven automation to the same operations used by the application itself.

---

## AI-Driven Development and Operations

### From Intent to Execution

CoCreateJS is designed to make application capabilities accessible to developers, applications, and authorized AI-driven workflows.

Rather than treating AI as a separate chatbot disconnected from application infrastructure, the ecosystem exposes structured operations that compatible AI tools can invoke.

```text
Developer / User / AI
          |
          v
Structured Request
          |
          v
Authentication & Authorization
          |
          v
CoCreateMCP / Application API
          |
          v
CoCreateAST / Workflow
          |
          v
CoCreateServer
          |
          +-- CoCreateDB
          |
          +-- Application Services
          |
          +-- Infrastructure
          |
          v
Result & State Update
```

### AI Across the Application Lifecycle

CoCreateJS aims to support AI-assisted workflows throughout development and operation.

**Build**

Generate interfaces, components, application logic, and structured workflows.

**Connect**

Integrate APIs, services, AI providers, and data sources.

**Configure**

Manage application settings, environments, and authorized infrastructure definitions.

**Deploy**

Execute deployment and provisioning workflows.

**Operate**

Inspect runtime state, application data, and system health.

**Optimize**

Analyze queries, indexes, workloads, and infrastructure utilization.

**Maintain**

Assist with diagnostics, updates, and recovery procedures.

### Human and AI Workflows

The same application primitives can support:

- Manual development
- Declarative interfaces
- Visual builders
- Programmatic automation
- AI-assisted creation
- Agentic workflows

Developers retain control over application logic, permissions, and infrastructure policies.

**AI does not replace the runtime. It uses the runtime.**

---

## Build Once, Run Across Devices

CoCreateJS aims to make application development portable across web, mobile, desktop, and other environments.

The shared JavaScript foundation helps developers reuse application logic, interfaces, data operations, and integrations.

### CoCreateDevice

CoCreateDevice extends this direction through device-specific packaging and integration.

The ecosystem targets environments including:

- Web browsers
- Progressive Web Apps
- Android
- iOS
- Windows
- Additional desktop and device platforms

Platform-specific capabilities and packaging may require corresponding tooling, wrappers, and configuration.

The objective is not necessarily to produce one identical binary for every platform.

It is to maximize reuse of application code and behavior while allowing the deployment output to match its target environment.

---

## Modularity and Extensibility

CoCreateJS is designed as a composable ecosystem.

Applications can use the complete project or select individual capabilities.

### Reusable Modules

Modules can provide functionality such as:

- CRUD
- Sockets
- Authentication
- Organizations
- Permissions
- Notifications
- File handling
- Data synchronization
- Background jobs
- API integrations
- AI integrations
- MCP tools
- Application workflows
- Infrastructure operations

### Load Only What You Need

Modules can be imported dynamically:

```javascript
await import('@cocreate/users');
await import('@cocreate/organizations');
await import('@cocreate/notification');
```

Runtime responsibilities can be separated across primary processes, workers, and deployment environments.

### Extend Existing Capabilities

CoCreateServer exposes extensible runtime interfaces.

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

Applications can provide custom implementations for compatible runtime services.

### Extend AI Capabilities

CoCreateMCP allows supported server operations to be exposed as tools for compatible AI clients.

This enables developers to extend the AI-accessible surface of an application without building a separate AI-specific implementation of every operation.

The goal is to expose useful primitives without requiring unnecessary wrapper layers.

---

## Architecture

CoCreateJS combines independent runtimes, shared APIs, modular services, AI-accessible tools, and distributed infrastructure.

```text
                         CoCreateJS
                             |
          +------------------+------------------+
          |                                     |
          v                                     v
    CoCreateClient                        CoCreateServer
          |                                     |
    Declarative HTML                       HTTP / HTTPS
    JavaScript APIs                        WebSockets
    Reactive Interfaces                    APIs & Routing
    IndexedDB                              Primary / Workers
    Offline / PWA                          Distributed Mesh
          |                                     |
          +------------------+------------------+
                             |
                             v
                   Shared Application APIs
                             |
          +------------------+------------------+
          |                                     |
          v                                     v
     CoCreateAI                           CoCreateMCP
          |                                     |
    Declarative Chat                      Tool Discovery
    AI Connectivity                       Tool Execution
    Agentic Workflows                     AI Client Access
          |                                     |
          +------------------+------------------+
                             |
                             v
                    CoCreateServer APIs
                             |
          +------------------+------------------+
          |                  |                  |
          v                  v                  v
      CoCreateDB        CoCreateAST        CoCreateKMS
          |                  |                  |
      Indexing           Workflows          Keys / Secrets
      Documents          Automation         Credentials
      Storage            Execution          Security
          |                  |                  |
          +------------------+------------------+
                             |
                             v
                   CoCreate Infrastructure
                             |
                    Cluster / Deployment
                             |
                    Cloud / Edge / Devices
```

This is a conceptual architecture. Components may be deployed independently, integrated selectively, or distributed across different infrastructure environments.

### One Ecosystem, Multiple Entry Points

CoCreateJS does not require developers to adopt every component.

Start with an HTML interface, a JavaScript API, a server, a database, an AI client, or an existing application.

Expand into additional capabilities as needed.

---

## Use Cases

### SaaS Platforms

Build multi-tenant applications with shared data, permissions, real-time communication, and distributed infrastructure.

### CRM and ERP Systems

Create data-driven applications using declarative interfaces, unified CRUD operations, and reusable workflows.

### Website and Application Builders

Compose applications from HTML, components, structured data, and configurable behaviors.

### AI-Powered Application Builders

Use declarative AI interfaces and authorized runtime tools to assist with creating, configuring, and deploying applications.

### Agentic Infrastructure Operations

Connect compatible AI clients through CoCreateMCP to inspect runtime state, execute workflows, and interact with authorized infrastructure capabilities.

### Content Management Systems

Manage content, assets, permissions, and publishing workflows through shared application APIs.

### E-Commerce

Build storefronts, administrative systems, product catalogs, and transactional workflows.

### Real-Time Collaboration

Develop collaborative editors, dashboards, chats, shared documents, and interactive workspaces.

### Offline and Mobile Applications

Build applications that use local storage and synchronize with configured backend services.

### AI-Powered Applications

Connect AI models to application data, APIs, tools, and authorized workflows.

### API and Workflow Automation

Integrate external services and coordinate structured operations across application systems.

### Distributed Infrastructure

Deploy and coordinate applications across cloud providers and geographic regions.

### Self-Hosted Platforms

Operate applications using integrated runtime, storage, and security components where supported.

### Existing Application Modernization

Add real-time communication, data services, automation, AI-accessible tools, or distributed capabilities without rewriting an entire application.

---

## Design Philosophy

### 1. JavaScript First

Use the language and platform primitives developers already know.

CoCreateJS favors JavaScript objects, arrays, maps, events, promises, and modules over introducing an entirely separate programming model.

### 2. Declarative Where Useful

Common application behavior should be expressible through configuration and HTML attributes.

Complex behavior should remain accessible through JavaScript.

Neither approach should prevent the other.

### 3. Primitives Over Abstractions

Expose useful capabilities directly.

Avoid adding unnecessary layers when existing JavaScript primitives already provide the required behavior.

### 4. Modularity Without Fragmentation

Components should remain independently useful while sharing compatible conventions.

A modular ecosystem should not require developers to relearn the same concepts for every module.

### 5. Storage Independence

Applications should not be permanently coupled to one database provider.

Data access should be adaptable to the storage systems that best fit the deployment.

### 6. Infrastructure Independence

Applications should be able to move between compatible providers and environments without rebuilding their architecture around each cloud.

### 7. Real-Time and Offline by Design

Connectivity and local operation should be application capabilities rather than unrelated afterthoughts.

### 8. AI-Native, Not AI-Dependent

AI should be able to interact with applications through structured, authorized tools.

Applications should remain functional without requiring an AI model to execute ordinary operations.

### 9. Security Throughout the Lifecycle

Authentication, permissions, keys, and infrastructure access should be considered at every layer.

### 10. Progressive Adoption

Start small.

Use the capabilities you need.

Extend the system as your application grows.

### 11. Build Applications, Not Infrastructure

Infrastructure should support the application, not consume the majority of development effort.

---

## Project Repositories

CoCreateJS is organized into focused repositories and packages.

| Project | Description |
|---|---|
| [CoCreateJS](https://github.com/CoCreateJS) | GitHub organization and ecosystem |
| [CoCreateClient](https://github.com/CoCreateJS/CoCreateJS) | Client-side JavaScript runtime |
| [CoCreateServer](https://github.com/CoCreateJS/CoCreate-server) | Distributed server runtime |
| [CoCreateDB](https://github.com/CoCreateJS/db) | Storage-agnostic JavaScript database engine |

Additional components, modules, and services are maintained within the CoCreateJS organization.

Package naming follows the CoCreate npm scope where applicable.

```text
@cocreate/client
@cocreate/server
@cocreate/db
@cocreate/ai
```

See individual repositories for installation requirements, supported versions, and available capabilities.

---

## Contributing

CoCreateJS is an open-source project, and contributions are welcome.

Contributions may include:

- Bug fixes
- Documentation improvements
- New modules
- Storage adapters
- API integrations
- MCP tools
- Client enhancements
- Runtime improvements
- AI integration improvements
- Security improvements
- Performance optimizations
- Tests and examples

Before submitting changes, review the relevant repository's contribution guidelines and existing issues.

We encourage implementations that preserve the project's core principles: composability, consistent APIs, JavaScript-first development, and infrastructure independence.

---

## License

CoCreateJS is distributed under the **GNU Affero General Public License v3.0 (AGPL-3.0)**.

Individual repositories may contain their own licensing terms or additional notices. Review the license file in the relevant repository before using or distributing a component.

### Commercial Licensing and Enterprise Support

Commercial licensing and enterprise support may be available for organizations requiring proprietary integration, dedicated deployment assistance, or additional operational support.

For inquiries:

**Email:** [info@cocreatejs.com](mailto:info@cocreatejs.com)

**Website:** https://cocreatejs.com

---

## Resources

- **Website:** https://cocreatejs.com
- **Documentation:** https://cocreatejs.com/docs
- **GitHub:** https://github.com/CoCreateJS
- **CoCreateClient:** https://github.com/CoCreateJS/CoCreateJS
- **CoCreateServer:** https://github.com/CoCreateJS/CoCreate-server
- **CoCreateDB:** https://github.com/CoCreateJS/db
- **Contact:** [info@cocreatejs.com](mailto:info@cocreatejs.com)

---

## CoCreateJS

From the first line of HTML to distributed infrastructure, CoCreateJS brings application development, connectivity, data, security, AI, and deployment together in one JavaScript ecosystem.

Developers build applications. AI agents interact with authorized capabilities. CoCreateJS provides the runtime, data, workflows, and infrastructure that connect them.

**Build applications, not infrastructure.**

Developed by **CoCreate**.
