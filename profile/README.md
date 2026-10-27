# CoCreateJS

> **Build once. Scale anywhere.**
>
> **CoCreateJS** is an open-source ecosystem consisting of two independent but complementary technologies:
>
> - [**CoCreate Client**](#cocreate-client): A lightweight, declarative JavaScript framework that brings application logic directly into HTML attributes or a headless JavaScript API, allowing developers to focus on design and user experience rather than complex framework logic. Perfect for building websites, applications, CRMs, ERPs, website builders, e-commerce platforms, dashboards, CMSs, PWAs, and collaborative tools.
> - [**CoCreate Runtime**](#cocreate-runtime): A lightweight, distributed server runtime that connects to any third-party API (including AI models), writes to multiple databases in parallel, and automatically orchestrates, scales, heals, and synchronizes applications across any cloud with built-in authentication and authorization.
>
> Each can be used independently, or together to create fully distributed real-time systems.

---

## Quick Start

Get up and running in under 60 seconds with either the HTML Client or Distributed Server Runtime.

### 1. CoCreate Client (Browser)

Simply include the CDN script tag in your HTML file to enable instant real-time data attributes and reactivity:

```html
<!-- CDN Script -->
<script src="https://cdn.cocreate.app/latest/CoCreate.min.js"></script>

<!-- Collaborative real-time input bound directly to database -->
<input array="users" object="5f8d04f1" key="name" placeholder="Enter full name" save />
```

Explore the source code and core client repository on github: **[CoCreateJS Repository](https://github.com/CoCreateJS/CoCreateJS)**

### 2. CoCreate Runtime (Node.js)

Start a self-orchestrating server node:

```js
import server from '@cocreate/server';

async function boot() {
  try {
    // Initialize core server capabilities (database, IPC, sockets, TLS, state)
    await server.init();

    // 1. Master Role Execution (Loads storage engines & master orchestration modules)
    if (server.isMaster) {
      await import('@cocreate/cron-jobs');
      await import('@cocreate/server/storage/firestore');
      await import('@cocreate/server/storage/mongodb');
      await import('@cocreate/server/storage/mysql');
      await import('@cocreate/server/storage/postgresql');
      await import('@cocreate/server/storage/qdrant');
      await import('@cocreate/server/storage/sqlite');
    }

    // 2. Worker Role Execution (Loads application modules & handles worker logic)
    if (server.isWorker) {
      // Worker 1 specific module loading
      if (server.workerId === 1) {
        await import('@cocreate/notification');
      }

      // Modules loaded across all worker processes
      const { default: Usage } = await import('@cocreate/usage');
      await import('@cocreate/organizations');
      await import('@cocreate/unique');
      await import('@cocreate/users');
      await import('@cocreate/url-uploader');

      new Usage(server.organization_id || server.organizationID);

      // Custom route registration via Map (path -> handler)
      server.routes.set('/api/v1/health', async (req, res) => {
        res.writeHead(200, { 'Content-Type': 'application/json' });
        res.end(JSON.stringify({
          status: 'healthy',
          workerId: server.workerId,
          pid: process.pid
        }));
      });
    }
  } catch (error) {
    console.error('Critical error during server bootstrap:', error);
    process.exit(1);
  }
}

boot();
```

Explore the source code and distributed server runtime repository on github: **[CoCreate-server Repository](https://github.com/CoCreateJS/CoCreate-server)**

---

## Why CoCreateJS?

Modern software is often fragmented.

Frontend frameworks focus on rendering.

Backend frameworks focus on routing.

Infrastructure tools focus on deployment.

Orchestrators focus on containers.

Databases focus on storage.

Developers spend enormous amounts of time integrating dozens of technologies before writing the actual application.

CoCreateJS approaches the problem differently.

Instead of treating the browser, servers, databases, and infrastructure as isolated systems, CoCreateJS treats them as one distributed runtime where every component communicates through a unified object model.

The result is dramatically less infrastructure code, fewer moving pieces, and significantly faster development.

---

# Two Independent Projects

## CoCreate Client

The client framework focuses on user experience and interface design instead of writing repetitive JavaScript.

By leveraging an **HTML attribute API** and a complementary **headless JavaScript API**, CoCreate Client turns standard HTML into a dynamic, reactive interface. Instead of writing boilerplate state management, DOM manipulation, routing, data bindings, and synchronization code, developers add application behavior directly within HTML attributes.

This paradigm shifts the developer's priority to what matters most: **design, accessibility, and user experience**.

### Visual Comparison: Declarative HTML vs. Traditional Framework

| Concept | Traditional (React/Vue + State + Fetch) | CoCreate Client (Declarative HTML) |
| :--- | :--- | :--- |
| **Real-time Input Binding** | Needs `useState`, `onChange` handlers, debouncing, `fetch()` calls, error states, and WebSocket hooks. | `<input array="users" object="123" key="name" save />` |
| **Form Submission** | Event handlers, DOM serialization, API route mapping, response parsing, state reset. | `<form array="users" object><button type="submit">Save</button></form>` |
| **Real-time Live List** | Fetching data on mount, WebSocket subscriptions, list diffing, manual state merging. | `<div array="users" render><span key="name"></span></div>` |

### Features

- **[HTML Attribute API](#declarative-html):** Drive full application logic and state directly inside HTML tags.
- **[Headless JavaScript API](#headless-javascript-api):** Complete programmatic access whenever customized control is required.
- **Focus on UI/UX:** Spend time crafting visual experiences rather than wiring framework logic together.
- Declarative HTML
- Framework agnostic
- Progressive enhancement
- Real-time synchronization
- Offline-first architecture
- Service Worker integration
- IndexedDB synchronization
- Shared collaborative editing
- Lazy-loaded modules
- Small initial footprint (~70 KB)
- Complete ecosystem (~410 KB fully loaded)
- SEO friendly
- Mobile friendly
- PWA support

Applications include:

- Website builders
- CMS platforms
- CRM systems
- ERP systems
- Project management
- Chat systems
- AI applications
- Dashboards
- E-commerce
- Admin panels
- Internal tools
- Customer portals
- Mobile applications

---

## CoCreate Runtime

The runtime is completely independent from the client.

It has no dependency on the HTML framework.

You can use:

- React
- Vue
- Angular
- Svelte
- Solid
- Next.js
- Nuxt
- Express
- Native Node.js
- Mobile applications
- Desktop applications
- IoT devices

or no framework at all.

The runtime simply provides distributed infrastructure.

### Key Capabilities

- **[Universal API & AI Connectivity](#framework-agnostic--universal-integrations):** Connect seamlessly with any third-party REST, GraphQL, WebSocket API, or AI model (OpenAI, Anthropic, Gemini, local LLMs).
- **[Parallel Multi-Database Writes](#database-agnostic--parallel-storage):** Execute operations across multiple databases simultaneously (e.g., MongoDB, PostgreSQL, SQLite, Firestore) without changing business logic.
- **[Built-in Authentication & Authorization](#security--governance):** Enterprise-grade security, RBAC, and multi-tenant isolation built directly into the data path.
- **[Self-Orchestrating & Density-Based Auto-Scaling](#self-replicating--density-driven-auto-scaling):** Self-replicating runtime nodes that continuously monitor cluster density, shed load, and spin up new instances globally where traffic demands.

---

# Runtime Overview

The runtime is a lightweight Node.js execution environment designed specifically for distributed applications.

Unlike traditional servers that run independently, every CoCreate Runtime node participates in a synchronized cluster.

Each server understands:

- nearby servers
- organizations
- routing
- sockets
- databases
- replication
- synchronization
- scaling
- failover

without requiring Kubernetes or external orchestration.

It acts as a unified integration backbone that can seamlessly communicate with any third-party API (including modern AI platforms) while executing CRUD operations across multiple databases in parallel with enterprise-grade authentication and authorization built directly into the data path.

---

# Runtime Highlights

- Universal API & AI Integration
- Parallel Multi-Database Writes
- Built-in Authentication & Authorization
- Density-Driven Self-Replicating Auto-Scaling
- Multi-cloud & Cloud agnostic
- Self-healing & Automatic failover
- Distributed routing, sockets, & storage
- Real-time replication
- Horizontal and Vertical scaling
- Shared state & Live synchronization
- Cluster awareness & Health monitoring
- Worker and Master processes
- IPC & TLS security
- Built-in API & Static server
- Extensible routing & Plugin architecture

---

# Lightweight by Design

The entire architecture is engineered to stay minimal without sacrificing capability.

- **Runtime:** ~150 MB memory footprint
- **Client Bootstrap:** ~70 KB initial footprint
- **Complete Client Ecosystem:** ~410 KB fully loaded

### Complete System with Minimal Footprint

That **~410 KB maximum footprint** is all you will ever need.

Because CoCreate Client is built entirely on composable, reusable primitives, this single ~410 KB ecosystem contains the complete toolkit required to build, render, and bring to life *any* complex web application or enterprise platform, from website builders and CMSs to full-scale CRMs, ERPs, and AI tools.

No extra frameworks, bloated third-party dependencies, or massive bundles are required. The core primitives scale endlessly across all of your UI needs.

---

# Framework Agnostic & Universal Integrations

Nothing in the runtime assumes your application architecture or limits external connectivity.

Connect easily with:

- Any Third-Party REST or GraphQL APIs
- AI Services (OpenAI, Anthropic, Gemini, local LLMs)
- WebSockets & Message Queues
- Custom RPC protocols
- Any Database Engine

The runtime acts as a universal router and proxy for external services, standardizing payloads into a unified object model while handling authentication and session state automatically.

---

# Distributed by Default

Every runtime instance is designed to participate in a distributed system.

Nodes automatically share information regarding:

- load
- health
- bandwidth
- latency
- storage
- organizations
- replication
- synchronization

allowing applications to scale horizontally without changing application code.

---

# Self-Replicating & Density-Driven Auto-Scaling

Scaling in CoCreate Runtime goes far beyond simple server spinning. Nodes are **self-replicating** and intelligently manage the entire network topology.

### Density-Based Traffic Shedding
The runtime continuously evaluates localized node **density** (traffic volume, active socket connections, latency, memory utilization, and bandwidth limits). When a node or region approaches target threshold limits, it sheds traffic to nearby nodes or triggers the spawning of a new instance.

### Autonomous Mesh Orchestration
- **Self-Replication:** Nodes autonomously spawn clones of themselves vertically (allocating processes) and horizontally (instantiating new cloud or edge nodes) directly in geographic or cloud locations where demand surges.
- **Dynamic Cluster Management:** As localized traffic fluctuates, nodes automatically coordinate to form new clusters, balance load, shed connection bottlenecks, and collapse idle nodes back down.
- **Location-Aware Deployment:** When high density is detected in specific regions, new nodes are dynamically spawned closer to those users to minimize latency and optimize network bandwidth.

No Kubernetes, complex terraform scripts, or manual infrastructure orchestration required; the runtime network manages its own lifecycle.

---

# Self Healing

If a server disappears:

- workloads move
- sockets reconnect
- replicas continue serving
- synchronization resumes

No manual intervention required.

---

# Multi Cloud

Deploy simultaneously across:

- AWS
- Azure
- Google Cloud
- DigitalOcean
- Hetzner
- OVH
- Vultr
- Linode
- Oracle Cloud
- On-premise
- Raspberry Pi
- Bare metal

All nodes operate as one distributed runtime.

---

# Routing

Routing is intentionally simple.

```js
server.routes.set("/users", async (req, res) => {
	// your logic
});
```

Routes execute in installation order.

If a route finishes the request, execution stops.

Otherwise, execution continues.

If no routes match, the runtime automatically falls back to its built-in API and static file server.

---

# Extensibility

Everything is replaceable.

```js
server.api = myApi;

server.files = myStaticServer;
```

No special plugin APIs are required.

Everything is simply JavaScript.

---

# Boot Process

```js
import server from '@cocreate/server';

await server.init();

if (server.isMaster) {
	// master modules & storage engines
}

if (server.isWorker) {
	// worker modules & business logic
}

if (server.workerId === 1) {
	// worker 1 specific modules
}
```

Masters load orchestration modules.

Workers load worker-level modules.

Specific modules are loaded only in specified workers by checking worker ID (such as targeting `server.workerId === 1` for isolated task processing).

Applications load only what they need.

---

# Plugin Architecture

Modules extend the runtime simply by importing them.

```js
await import("@cocreate/users");
await import("@cocreate/organizations");
await import("@cocreate/socket");
await import("@cocreate/storage");
```

No registration boilerplate.

No configuration files.

Just JavaScript.

---

# Unified Object API

Every CoCreate module exposes a consistent event-driven API where actions are completely defined within a unified payload object using dot-notation methods (e.g., `object.create`, `object.update`, `array.read`, `array.delete`).

### Method Reference Matrix
<!-- ... existing code -->
```js
// CoCreate Unified Payload Pattern:
// 1. Creating an object
crud.send({
  method: "object.create",
  array: "users",
  object: { name: "John Doe", email: "john@example.com" },
  storage: ["mongodb", "sqlite"]
});

// 2. Updating objects (single object or array of objects)
crud.send({
  method: "object.update",
  array: "users",
  object: { _id: "12345", name: "Jane Doe" }
});

// 3. Updating an array collection definition / configuration
crud.send({
  method: "array.update",
  array: { name: "users", permissions: { read: "all" } }
});

// Unified execution pattern across all system handlers:
crud.send(payload);
server.send(payload);
socket.send(payload);
file.send(payload);
api.send(payload);
```

To listen for actions, modules register event listeners using `on`, passing the target dot-notation method name and a callback function:
<!-- ... existing code -->
#### Replication & Error Resilience
- **Dual Writes & Parallel Dispatch:** Operations are sent concurrently across all designated storage engines.
- **Failover & Rollback Handling:** If one database target encounters a network drop or write failure, the node logs the offset, triggers asynchronous reconciliation retry queues, and continues serving reads from responsive replicas.
<!-- ... existing code -->
# Headless JavaScript API

Everything available declaratively is also available programmatically using unified payload transmission with dot-notation methods.

```js
crud.send({
  method: "object.update",
  array: "users",
  object: {
    _id: "12345",
    name: "Jane Doe",
    role: "Admin"
  }
});
```

The HTML API and JavaScript API are equivalent.

Choose whichever fits your project.

---

# Collaboration

Real-time collaboration is built into the ecosystem.

Applications can synchronize:

- documents
- forms
- dashboards
- editors
- chats
- whiteboards
- design tools

without additional synchronization libraries.

---

# Offline First

Applications continue functioning without connectivity.

Changes synchronize automatically when connections return.

---

# Security & Governance

Designed with multi-tenant deployments and strict isolation in mind.

Features include:

- Organization and tenant isolation
- Granular permission & role-based access systems (RBAC)
- Seamless JWT authentication
- End-to-end TLS encryption
- Secure WebSockets
- Distributed multi-node authorization checks

---

# Ideal For

- SaaS
- CRM
- ERP
- CMS
- Website builders
- Application builders
- AI platforms
- Internal tools
- E-commerce
- Collaborative editors
- Business automation
- Distributed systems

---

# Philosophy

CoCreateJS favors primitives over magic.

Everything is built using familiar JavaScript concepts:

- Objects
- Arrays
- Maps
- Async functions
- Events
- Modules

Developers remain in control.

The framework stays out of the way.

---

# Documentation

Documentation is continuously expanding.

[https://github.com/CoCreateJS](https://github.com/CoCreateJS)

---

# Community

Contributions are welcome.

Whether improving documentation, fixing bugs, creating modules, or building applications, every contribution helps grow the ecosystem.

---

# License & Enterprise Support

Licensed under the **GNU Affero General Public License v3.0 (AGPL-3.0)**.

### Commercial Licensing & Enterprise Onboarding
For organizations requiring proprietary software embedding, private SLA guarantees, custom security audits, or enterprise deployment assistance, commercial licenses and dedicated support tiers are available:

- **Enterprise Inquiries:** [contact@cocreatejs.com](mailto:contact@cocreatejs.com)
- **Commercial Licensing Options:** [https://cocreatejs.com/pricing](https://cocreatejs.com/pricing)

---

## Links

- Organization github: [https://github.com/CoCreateJS](https://github.com/CoCreateJS)
- CoCreateJS Repository: [https://github.com/CoCreateJS/CoCreateJS](https://github.com/CoCreateJS/CoCreateJS)
- CoCreate-server Repository: [https://github.com/CoCreateJS/CoCreate-server](https://github.com/CoCreateJS/CoCreate-server)
- Website: [https://cocreatejs.com](https://cocreatejs.com)
- Documentation: [https://cocreatejs.com/docs](https://cocreatejs.com/docs)
- Issues: [https://github.com/CoCreateJS/issues](https://github.com/CoCreateJS/issues)
