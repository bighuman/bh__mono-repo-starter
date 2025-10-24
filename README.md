# Mono Repo Starter

A TypeScript monorepo with three workspaces using Yarn workspaces.

## Workspaces

- **shared**: Common TypeScript interfaces and types
- **server**: Express.js API server
- **client**: Next.js web application

## Getting Started

### Prerequisites

- Node.js 18+
- Yarn

### Installation

```bash
yarn install
```

### Development

Start all workspaces in development mode:

```bash
yarn dev
```

Or start individual workspaces:

```bash
# Start server only
yarn workspace @server/api dev

# Start client only
yarn workspace @client/web dev
```

### Building

Build all workspaces:

```bash
yarn build
```

### Linting and Formatting

```bash
# Lint all workspaces
yarn lint

# Format all files
yarn format

# Type check all workspaces
yarn type-check
```

## API Endpoints

The server provides the following endpoints:

- `GET /health` - Health check endpoint

## Architecture

- **Shared types**: Defined in `packages/shared/src/types.ts`
- **Server**: Express.js app with TypeScript, imports shared types
- **Client**: Next.js app with TypeScript, imports shared types and fetches from server
