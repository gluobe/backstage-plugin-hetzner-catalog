# Hetzner Cloud Catalog Backend Module

Welcome to the Hetzner Cloud Catalog Backend Module!  
This module integrates Hetzner Cloud resources into Backstage.

## Table of Contents

- [Hetzner Cloud Catalog Backend Module](#hetzner-cloud-catalog-backend-module)
  - [Table of Contents](#table-of-contents)
  - [Introduction](#introduction)
  - [Functionalities](#functionalities)
  - [Dependencies](#dependencies)
    - [1. Hetzner Backend Plugin](#1-hetzner-backend-plugin)
    - [2. Frontend Plugin (Optional)](#2-frontend-plugin-optional)
  - [Quick Start](#quick-start)
    - [Installation](#installation)
    - [Development](#development)
  - [Contributing](#contributing)
  - [License](#license)
    - [Attribution](#attribution)

---

## Introduction

The Hetzner Cloud Catalog Backend Module is a Backstage backend catalog module that automatically discovers and imports Hetzner Cloud resources into the Backstage catalog.  
It connects to your Hetzner Cloud environment, fetches resources such as servers (VMs), volumes, and primary IPs, and creates corresponding entities in Backstage.  
This enables you to visualize, manage, and relate your Hetzner infrastructure directly from the Backstage catalog, providing a unified view of your cloud assets and their dependencies.

---

## Functionalities

This backend catalog module provides the following key functionalities for Backstage:

- **Entity Creation for Backstage Catalog**: Automatically discovers and creates entities for Hetzner Cloud resources (such as servers, volumes, and primary IPs) in the Backstage catalog.
- **Resource Synchronization**: Periodically fetches the latest state of Hetzner Cloud resources and keeps the Backstage catalog up to date.
- **Relationship Mapping**: Establishes relationships between resources (e.g., linking volumes to their attached servers) using Backstage's entity relations.
- **Custom Metadata and Annotations**: Enriches catalog entities with Hetzner-specific metadata and annotations for better traceability and management.
- **Extensible Resource Support**: Easily extendable to support additional Hetzner Cloud resource types as needed.

---

## Dependencies

### 1. Hetzner Backend Plugin

The main Hetzner backend plugin provides the API endpoints and backend logic for Hetzner Cloud integration.  
Repository:  
[https://github.com/gluobe/backstage-plugin-hetzner-backend](https://github.com/gluobe/backstage-plugin-hetzner-backend)

### 2. Frontend Plugin (Optional)

An optional frontend plugin is available for integrating with the backend plugin. The frontend plugin provides a user interface in Backstage to visualize Hetzner Cloud resources. It includes:

- **Hetzner Cloud Page**: An overview of the Hetzner Cloud platform.
- **Hetzner Resource Card**: A card component that displays detailed information about a specific Hetzner Cloud resource directly within the entity page in the Backstage catalog.

The frontend plugin can be found at:

[https://github.com/gluobe/backstage-plugin-hetzner](https://github.com/gluobe/backstage-plugin-hetzner)

Alternatively, you can create your own frontend plugin to suit your specific needs. The backend plugin is designed to support custom frontend implementations, so installing this provided frontend plugin is not mandatory.

However, it is strongly recommended to either install the provided frontend plugin or create your own. Without a frontend plugin, you will not have a user interface in Backstage to visualize Hetzner Cloud resources, which significantly limits the usability of this backend plugin. A frontend plugin is essential for providing insights into your Hetzner Cloud infrastructure and enabling effective management of your resources.

---

## Quick Start

The following sections will help you get the module setup and running.

### Installation

1. Install the backend catalog module:

   ```bash
   yarn --cwd packages/backend add @gluo-nv/backstage-plugin-catalog-backend-module-hetzner
   ```

### Development

For local development, you can run the backend module in isolation:

```bash
# Navigate to the backend module directory
cd packages/backend

# Run the backend module
yarn start
```

The backend module should now be running locally. You can test the API endpoints using a tool like Postman or curl.

For development with the frontend plugin, refer to the frontend plugin's documentation for setup and development instructions.

---

## Contributing

We welcome contributions to improve this module! If you’d like to contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bugfix.
3. Submit a pull request with a clear description of your changes.

For major changes, please open an issue first to discuss your ideas.

---

## License

This plugin is licensed under the GNU Affero General Public License v3.0 (AGPL-3.0).

### Attribution

This plugin was created by [Gluo NV](https://gluo.be).  
Any use or distribution must include proper attribution to the original author.
