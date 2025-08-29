# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is the documentation repository for HITL.sh (Human-in-the-Loop), a mobile-first platform that adds human oversight to AI workflows. The project uses Mintlify for documentation hosting and is built with MDX files for content.

## Development Commands

### Local Development
```bash
# Install Mintlify CLI globally
npm i -g mint

# Install dependencies
npm install

# Start development server
mint dev
# Opens at http://localhost:3000
```

### Building and Deployment
```bash
# Build for production
mint build

# Deploy to production
mint deploy
```

## Architecture

### Documentation Structure
- **MDX Files**: Content files written in MDX (Markdown + JSX) format
- **Configuration**: `docs.json` contains site structure, navigation, and theming
- **Navigation**: Organized into tabs (Guides, API Reference, Examples) with hierarchical groups
- **Assets**: Logos in `/logo/`, favicon as `/favicon.svg`

### Content Organization
- **Guides Tab**: Getting started, core concepts, mobile app, integrations, webhooks
- **API Reference Tab**: OpenAPI-based API documentation
- **Examples Tab**: Real-world use cases and implementations

### Key Files
- `docs.json`: Mintlify configuration and navigation structure
- `README.md`: Project overview and contribution guidelines
- `concepts.mdx`: Core platform concepts and architecture
- `api-reference/openapi.json`: API specification (currently placeholder content)

## Content Guidelines

### MDX Format
- Files use `.mdx` extension for Markdown with JSX components
- Mintlify-specific components available (Card, Columns, etc.)
- Front matter with title and description

### Navigation Updates
When adding new pages:
1. Create the `.mdx` file in appropriate directory
2. Update `docs.json` navigation structure
3. Test locally with `mint dev`

## Platform Features

### Core Components
- **Review Templates**: Customizable human review interfaces
- **Agent Inbox**: Centralized review management dashboard
- **Integration Methods**: SDKs (Python/TypeScript), workflow tools, HTTP API, webhooks
- **Mobile-First Design**: Optimized for mobile review workflows

### Security & Performance
- API key authentication
- Webhook signature verification
- Global distribution with low latency
- Auto-scaling based on demand

## Contribution Workflow

1. Create/edit `.mdx` files in appropriate directories
2. Update `docs.json` if adding new pages
3. Test locally with `mint dev`
4. Follow mobile-first content design principles
5. Include practical code examples and real-world use cases