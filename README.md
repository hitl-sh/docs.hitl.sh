# HITL.sh Documentation

This repository contains the documentation for [HITL.sh](https://hitl.sh), a human-in-the-loop platform for AI agents. HITL.sh provides human supervision for AI workflows, ensuring quality, safety, and compliance in automated processes.

## What is HITL.sh?

HITL.sh (Human in the Loop) is a mobile-first platform that adds human oversight to AI workflows. It acts as a bridge between your AI systems and human reviewers, providing:

- **Review Templates**: Customizable interfaces for human review
- **Agent Inbox**: Centralized dashboard for managing review requests
- **Smart Notifications**: Email, Slack, and custom notification channels
- **Workflow Control**: Multi-step review processes and manual triggers
- **API Integration**: SDKs and REST API for seamless integration

## Documentation Structure

### Guides
- **Getting Started**: Quickstart guide and core concepts
- **Core Features**: Agent Inbox, review templates, workflows, notifications
- **Integrations**: Python SDK, TypeScript SDK, n8n, Make.com, LangGraph
- **Templates & UI**: Review template creation and customization

### API Reference
- **Core API**: Reviews, templates, teams, and authentication
- **Webhooks**: Real-time event notifications and payload handling

### Examples
- **Use Cases**: Content moderation, sales approval, AI training, workflow control
- **Code Samples**: Python, TypeScript, and webhook examples

## Getting Started

### Prerequisites
- Node.js 18+ and npm
- Mintlify CLI: `npm i -g mint`

### Local Development
1. Clone this repository
2. Install dependencies: `npm install`
3. Start development server: `mint dev`
4. Open `http://localhost:3000`

### Building
```bash
# Build for production
mint build

# Deploy to production
mint deploy
```

## Contributing

We welcome contributions to improve our documentation! Here's how you can help:

### Adding New Content
1. Create new `.mdx` files in appropriate directories
2. Update `docs.json` to include new pages in navigation
3. Follow our content style guide (see below)
4. Test locally with `mint dev`

### Content Guidelines
- **Clear and concise**: Write for developers and technical users
- **Practical examples**: Include code samples and real-world use cases
- **Consistent structure**: Follow existing page layouts and formatting
- **Mobile-first**: Consider mobile users in all content
- **Accessibility**: Use proper headings, alt text, and semantic markup

### Code Examples
- **Language-specific**: Use appropriate syntax highlighting
- **Complete examples**: Provide working, copy-pasteable code
- **Best practices**: Follow language conventions and security guidelines
- **Error handling**: Include proper error handling and edge cases

## Key Features

### Human-in-the-Loop Workflows
- **AI Generation**: AI creates content, decisions, or outputs
- **Human Review**: Human reviewers examine and approve/reject
- **Result Processing**: Workflows continue based on review outcomes
- **Iterative Improvement**: Support for feedback loops and revisions

### Integration Methods
- **SDKs**: Python and TypeScript SDKs for direct integration
- **Workflow Tools**: Native nodes for n8n, Make.com, and other platforms
- **HTTP API**: RESTful API for custom integrations
- **Webhooks**: Real-time notifications for review events

### Review Templates
- **Custom Fields**: Text, boolean, selection, file, and specialized field types
- **Validation Rules**: Required fields, data formats, and cross-field validation
- **Conditional Logic**: Show/hide fields based on user input
- **Branding**: Custom colors, logos, and styling options

## Use Cases

### Content Moderation
- Review AI-generated blog posts, social media content, and marketing copy
- Ensure compliance with brand guidelines and legal requirements
- Collect feedback for content improvement

### Sales Approval
- Automate sales processes while maintaining human oversight
- Review high-value transactions and complex deals
- Ensure compliance with sales policies and regulations

### AI Training
- Collect human feedback to improve AI model performance
- Create training datasets for model fine-tuning
- Evaluate AI outputs for bias and quality issues

### Workflow Control
- Add checkpoints to complex automated workflows
- Enable manual triggers for exceptional cases
- Coordinate multiple review steps across workflows

## Architecture

### Core Components
- **Review Engine**: Manages review lifecycle and state
- **Template System**: Defines review interfaces and validation
- **Assignment Engine**: Routes reviews to appropriate reviewers
- **Notification System**: Sends alerts and updates
- **Webhook Service**: Delivers real-time events

### Security Features
- **API Key Authentication**: Secure access to all endpoints
- **Webhook Signatures**: Verified payload delivery
- **Role-Based Access**: Granular permission control
- **Data Encryption**: All data encrypted in transit and at rest
- **Audit Logging**: Complete history of all actions

### Performance
- **Global Distribution**: Low-latency access worldwide
- **Auto-scaling**: Automatic scaling based on demand
- **Connection Pooling**: Efficient API connection management
- **Caching**: Intelligent caching for improved performance

## Support

### Getting Help
- **Documentation**: Browse our comprehensive guides
- **Community**: Join our [Discord community](https://discord.gg/hitlsh)
- **Support**: Email [support@hitl.sh](mailto:support@hitl.sh)
- **GitHub**: Check out our [open source examples](https://github.com/hitlsh)

### Resources
- **Quickstart Guide**: [docs.hitl.sh/quickstart](https://docs.hitl.sh/quickstart)
- **API Reference**: [docs.hitl.sh/api-reference](https://docs.hitl.sh/api-reference)
- **Examples**: [docs.hitl.sh/examples](https://docs.hitl.sh/examples)
- **Integrations**: [docs.hitl.sh/integrations](https://docs.hitl.sh/integrations)

## License

This documentation is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## About HITL.sh

HITL.sh is built by humans in Berlin who believe that AI should work with humans, not replace them. Our platform enables organizations to harness the power of AI while maintaining human oversight and control.

- **Website**: [hitl.sh](https://hitl.sh)
- **Twitter**: [@hitlsh](https://twitter.com/hitlsh)
- **LinkedIn**: [hitlsh](https://linkedin.com/company/hitlsh)
- **GitHub**: [hitlsh](https://github.com/hitlsh)
