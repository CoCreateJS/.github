# CoCreateJS

> **Build once. Scale anywhere.**
>
> **CoCreateJS** is CoCreate's JavaScript project for building applications across the browser and distributed server environments. It brings together two complementary parts:
>
> - **[CoCreate Client](https://github.com/CoCreateJS/CoCreateJS)** — a lightweight client-side JavaScript framework with a declarative HTML attribute API and a headless JavaScript API. Use it to build websites, applications, CRMs, ERPs, website builders, e-commerce platforms, dashboards, CMSs, PWAs, and collaborative tools.
> - **[CoCreate Server](https://github.com/CoCreateJS/CoCreate-server)** — a distributed server runtime for connecting application logic to APIs, databases, and other services. It provides the foundation for clustered, real-time applications that can run across cloud environments.
>
> CoCreate Client and CoCreate Server can be used independently or together. CoCreateJS also includes modules and plugins that extend client and server capabilities.

## Quick Start

Get started with CoCreate Client in the browser or initialize CoCreate Server in a Node.js application.

### CoCreate Client (Browser)

Include the client script in an HTML page to enable CoCreate's declarative attributes and reactivity:

```html
<script src="https://cdn.cocreate.app/latest/CoCreate.min.js"></script>

<!-- A collaborative input bound to a database record -->
<input array="users" object="5f8d04f1" key="name" placeholder="Enter full name" save />
```

Explore the [CoCreate Client repository](https://github.com/CoCreateJS/CoCreateJS).

### CoCreate Server (Node.js)

Initialize the server runtime and load the modules needed by each process role:

```js
import server from '@cocreate/server';

async function boot() {
  try {
    // Initialize core server capabilities: database, IPC, sockets, TLS, and state.
    await server.init();

    // The primary server loads storage engines and orchestration modules.
    if (server.isPrimary) {
      await import('@cocreate/cron-jobs');
      await import('@cocreate/server/storage/firestore');
      await import('@cocreate/server/storage/mongodb');
      await import('@cocreate/server/storage/mysql');
      await import('@cocreate/server/storage/postgresql');
      await import('@cocreate/server/storage/qdrant');
      await import('@cocreate/server/storage/sqlite');
    }

    // Worker processes load application modules and route handlers.
    if (server.isWorker) {
      if (server.workerId === 1) {
        await import('@cocreate/notification');
      }

      const { default: Usage } = await import('@cocreate/usage');
      await import('@cocreate/organizations');
      await import('@cocreate/users');

      new Usage(server.organization_id || server.organizationID);

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

Explore the [CoCreate Server repository](https://github.com/CoCreateJS/CoCreate-server).

## Why CoCreateJS?

Application development often spans separate frontend frameworks, backend services, databases, and infrastructure tools. Developers spend time connecting these systems before they can focus on the application itself.

CoCreateJS brings client and server capabilities together as one JavaScript project. CoCreate Client helps define interface behavior in HTML or JavaScript. CoCreate Server provides distributed runtime capabilities for application services, data, and real-time communication.

Use the parts you need, independently or together, and extend them with CoCreate modules and plugins.

## CoCreateJS Project Structure

CoCreateJS includes two core parts:

| Part | Purpose | Package |
| :--- | :--- | :--- |
| **CoCreate Client** | Browser-side interface, data binding, and reactivity | `@cocreate/client` |
| **CoCreate Server** | Distributed server runtime, cluster services, and integrations | `@cocreate/server` |

CoCreate modules and plugins extend the client, the server, or both. Applications can use the CoCreateJS project as a whole or select the pieces that fit their architecture.

## CoCreate Client

CoCreate Client focuses on interface behavior and user experience. Its HTML attribute API turns standard markup into a declarative interface. A complementary headless JavaScript API provides programmatic control when an application needs it.

Instead of writing repetitive state management, DOM manipulation, routing, data binding, and synchronization code, developers can express common behaviors directly in HTML attributes and use JavaScript where custom logic is needed.

### Declarative HTML and JavaScript

| Concept | Typical implementation | CoCreate Client example |
| :--- | :--- | :--- |
| **Real-time input binding** | State management, change handlers, network requests, error states, and socket subscriptions | `<input array="users" object="123" key="name" save />` |
| **Form submission** | Event handlers, serialization, API mapping, response handling, and form reset | `<form array="users" object><button type="submit">Save</button></form>` |
| **Live list** | Initial fetch, subscriptions, list updates, and manual state merging | `<div array="users" render><span key="name"></span></div>` |

### Client Features

- HTML attribute API for declarative application behavior
- Headless JavaScript API for programmatic control
- Framework agnostic and progressively enhanced
- Real-time synchronization and shared collaborative editing
- Offline-first architecture with IndexedDB synchronization
- Service Worker integration and PWA support
- Lazy-loaded modules
- SEO and mobile friendly
- Small initial footprint (approximately 70 KB)
- Complete client ecosystem (approximately 410 KB fully loaded)

CoCreate Client can be used to build:

- Websites and website builders
- CMS platforms
- CRM and ERP systems
- Project management tools
- Chat and AI applications
- Dashboards and admin panels
- E-commerce experiences
- Internal tools and customer portals
- Collaborative editors and mobile web applications

## CoCreate Server

CoCreate Server is the server-side part of the CoCreateJS project. It is a distributed JavaScript runtime for application services, integrations, data operations, and real-time systems.

The server runtime is independent of CoCreate Client. It can support applications built with React, Vue, Angular, Svelte, Solid, Next.js, Nuxt, Express, native Node.js, mobile or desktop clients, IoT devices, or no client framework at all.

### Server Runtime Capabilities

- **API and AI connectivity:** Integrate with REST, GraphQL, WebSocket APIs, AI services, and custom protocols.
- **Multi-database operations:** Run operations across supported storage engines, including MongoDB, PostgreSQL, SQLite, and Firestore.
- **Cluster coordination:** Run primary and worker processes with shared state, health monitoring, routing, and synchronization.
- **Multi-cloud deployment:** Deploy nodes across cloud providers, on-premise systems, edge locations, and bare-metal servers.
- **Authentication and authorization:** Apply authentication, permissions, and tenant isolation across application data paths.
- **Real-time services:** Coordinate sockets, messaging, and data synchronization across nodes.
- **Extensible modules:** Add server capabilities by importing the CoCreate modules an application uses.

## Server Runtime Overview

Each CoCreate Server node can participate in a distributed cluster. Nodes coordinate application workloads and share information used for routing, real-time communication, storage, synchronization, and cluster health.

The runtime provides a foundation for distributed applications without requiring every project to assemble its own server, database, socket, and orchestration layers from scratch.

## Cluster and Distributed Runtime

CoCreate Server is designed for clustered deployments. Its runtime can coordinate:

- Primary and worker processes
- Cluster membership and health
- Application routes and services
- Socket connections and events
- Shared state and synchronization
- Storage connections and data operations
- Replication and failover behavior

Scale the runtime horizontally or vertically according to the deployment and workload. Cluster and scaling behavior depends on the configured infrastructure and modules.

## Multi-Cloud and Deployment

CoCreate Server can be deployed across cloud providers and self-managed environments, including:

- AWS
- Microsoft Azure
- Google Cloud
- DigitalOcean
- Hetzner
- OVH
- Vultr
- Linode
- Oracle Cloud
- On-premise environments
- Raspberry Pi and other supported devices
- Bare-metal servers

Nodes can operate as parts of the same distributed application, subject to the network and deployment configuration.

## API and AI Integrations

CoCreate Server can connect application services to external systems, including:

- REST and GraphQL APIs
- AI services such as OpenAI, Anthropic, Gemini, and local models
- WebSocket services and message queues
- Custom RPC protocols
- Supported database engines

The runtime provides a place to coordinate integrations and application data operations. Specific providers and capabilities depend on the modules and configuration used by the application.

## Routing

Register custom routes on the server:

```js
server.routes.set('/users', async (req, res) => {
  // Add application logic here.
});
```

Routes execute in installation order. If a route completes the request, execution stops. Otherwise, request handling continues. If no custom route handles a request, the runtime can fall back to its configured API and static file server.

## Extensibility

CoCreate Server is extended through JavaScript modules. Import the capabilities an application needs:

```js
await import('@cocreate/users');
await import('@cocreate/organizations');
await import('@cocreate/socket');
```

Runtime components such as the API and static file server can also be assigned directly when an application needs custom behavior:

```js
server.api = myApi;
server.files = myStaticServer;
```

## Boot Process

Initialize the server before loading modules. Load primary-level, worker-level, and worker-specific modules in the appropriate process roles:

```js
import server from '@cocreate/server';

await server.init();

if (server.isPrimary) {
  // Load primary server modules and storage engines.
}

if (server.isWorker) {
  // Load modules used by worker processes.
}

if (server.workerId === 1) {
  // Load modules for a specific worker.
}
```

Applications can load modules only in the process roles that need them.

## Unified Object API

CoCreate modules use a unified payload pattern with dot-notation methods such as `object.create`, `object.update`, `array.read`, and `array.delete`.

```js
// Create an object.
crud.send({
  method: 'object.create',
  array: 'users',
  object: { name: 'John Doe', email: 'john@example.com' },
  storage: ['mongodb', 'sqlite']
});

// Update an object.
crud.send({
  method: 'object.update',
  array: 'users',
  object: { _id: '12345', name: 'Jane Doe' }
});

// Update an array definition or configuration.
crud.send({
  method: 'array.update',
  array: { name: 'users', permissions: { read: 'all' } }
});
```

Modules can expose matching operations through their own handlers. The exact available methods depend on the module in use.

### Replication and Error Handling

When an operation targets multiple storage engines, the configured storage modules can dispatch the operation to those targets. Applications should define how to handle partial failures, retries, reconciliation, and reads from available replicas for their deployment requirements.

## Headless JavaScript API

CoCreate Client and CoCreate modules can be used programmatically with JavaScript APIs. For example:

```js
crud.send({
  method: 'object.update',
  array: 'users',
  object: {
    _id: '12345',
    name: 'Jane Doe',
    role: 'Admin'
  }
});
```

Use declarative HTML or JavaScript according to the needs of the application.

## Collaboration and Real-Time Synchronization

CoCreate modules can support real-time collaboration and synchronization for documents, forms, dashboards, editors, chats, and other shared experiences. The specific behavior depends on the modules and services configured in the application.

## Offline-First Client Applications

CoCreate Client can use browser storage such as IndexedDB to support offline workflows. Changes can synchronize with configured server and storage services when connectivity is available.

## Security and Governance

CoCreateJS supports application patterns for multi-tenant deployments and access control, including:

- Organization and tenant isolation
- Granular permissions and role-based access control (RBAC)
- JWT authentication integrations
- TLS and secure WebSocket deployment
- Authorization checks across distributed services

Applications should configure and review security controls for their own deployment, data, and threat model.

## Lightweight by Design

CoCreateJS is built from composable modules so applications can load the capabilities they need.

- **Server runtime:** approximately 150 MB memory footprint, depending on workload and configuration
- **Client bootstrap:** approximately 70 KB initial footprint
- **Complete client ecosystem:** approximately 410 KB fully loaded

Client sizes and server resource use vary with the modules, configuration, and workload. The modular design lets applications avoid loading client features they do not use.

## Ideal For

- SaaS platforms
- CRM, ERP, and CMS applications
- Website and application builders
- AI platforms and integrations
- Internal tools and customer portals
- E-commerce applications
- Collaborative editors
- Business automation
- Distributed and real-time systems

## Philosophy

CoCreateJS favors familiar JavaScript primitives over hidden behavior. Developers work with objects, arrays, maps, asynchronous functions, events, and modules while choosing how much of the CoCreate ecosystem to use.

## Documentation

Documentation and project information are available at:

- [CoCreateJS on GitHub](https://github.com/CoCreateJS)
- [CoCreateJS documentation](https://cocreatejs.com/docs)

## Community

Contributions are welcome across CoCreateJS. Help improve documentation, fix bugs, create modules, or build applications with the project.

- [GitHub organization](https://github.com/CoCreateJS)
- [Issues](https://github.com/CoCreateJS/issues)

## License and Enterprise Support

CoCreateJS is licensed under the **GNU Affero General Public License v3.0 (AGPL-3.0)**. Check the license file in each repository for the terms that apply to that component.

### Commercial Licensing and Enterprise Onboarding

Commercial licensing and dedicated support may be available for organizations that need proprietary software embedding, service-level agreements, security reviews, or deployment assistance.

- **Enterprise inquiries:** [contact@cocreatejs.com](mailto:contact@cocreatejs.com)
- **Commercial licensing:** [cocreatejs.com/pricing](https://cocreatejs.com/pricing)

## Links

- **Company:** [CoCreate](https://cocreatejs.com)
- **Project:** [CoCreateJS organization on GitHub](https://github.com/CoCreateJS)
- **Client:** [CoCreate Client repository](https://github.com/CoCreateJS/CoCreateJS)
- **Server:** [CoCreate Server repository](https://github.com/CoCreateJS/CoCreate-server)
- **Website:** [cocreatejs.com](https://cocreatejs.com)
- **Documentation:** [cocreatejs.com/docs](https://cocreatejs.com/docs)
- **Issues:** [GitHub issues](https://github.com/CoCreateJS/issues)
