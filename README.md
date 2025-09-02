# libx-core# libx-core

**Modern Documentation Framework for Multi-Project Monorepos**

A powerful monorepo framework for creating and managing multiple documentation
sites with shared components, themes, and automated workflows. Perfect for
technical documentation, project portfolios, and multi-language content
management.

## ✨ Features

- **🏗️ Monorepo Architecture** - Efficient management of multiple documentation
projects
- **🎨 Shared Design System** - Reusable UI components and consistent theming
- **🌍 Multi-language Support** - Built-in internationalization (i18n) utilities
- **📚 Version Management** - Document versioning and content organization
- **🚀 Auto-generated Navigation** - Dynamic sidebar and navigation generation
- **⚡ Fast Development** - Hot reload and optimized build processes
- **📱 Modern Stack** - Built with Astro, TypeScript, and modern tooling

## 🚀 Quick Start

### Prerequisites

- Node.js 18+
- pnpm 8+

### Installation

```bash
# Clone the repository
git clone https://github.com/your-username/libx-core.git
cd libx-core

# Install dependencies
pnpm install

# Start development server
pnpm dev

Create Your First Project

# Create a new documentation project
pnpm create:project my-docs "My Documentation" "私のドキュメント"

# Start the development server
pnpm dev

Visit http://localhost:4321 to see your site!

📁 Project Structure

libx-core/
├── packages/          # Shared packages
│   ├── ui/           # UI components library
│   ├── theme/        # Theme system
│   ├── i18n/         # Internationalization utilities
│   └── versioning/   # Version management
├── apps/             # Documentation projects
│   ├── project-template/  # Template for new projects
│   └── top-page/     # Landing page
├── config/           # Shared configuration
└── scripts/          # Automation scripts

🛠️ Available Commands

Development

pnpm dev              # Start all development servers
pnpm dev:selective    # Start specific projects only

Building

pnpm build            # Build all projects
pnpm build:local      # Build for local preview
pnpm build:selective  # Build specific projects

Project Management

pnpm create:project   # Create new documentation project
pnpm add:language     # Add language to existing project
pnpm create:version   # Create new version for project

📖 Creating Documentation

1. Project Creation

Use the automated project creation script:

pnpm create:project api-docs "API Documentation" "API文書" \
  --description-en="Complete API reference" \
  --description-ja="完全なAPIリファレンス" \
  --icon="code"

2. Content Structure

Organize your content with version-first structure:

apps/your-project/src/content/docs/
├── v1/
│   ├── en/           # English content
│   └── ja/           # Japanese content
└── v2/
    ├── en/
    └── ja/

3. Adding Languages

Automatically add new languages to existing projects:

node scripts/add-language.js your-project ko --auto-template

🎨 Customization

Theme Configuration

Customize colors, typography, and spacing:

// packages/theme/src/colors.ts
export const colors = {
  primary: '#your-color',
  secondary: '#your-secondary',
  // ...
}

Component Library

Access shared components in your projects:

---
import { Button, Card, Navigation } from '@docs/ui';
---

<Card>
  <Button>Click me</Button>
</Card>

🌍 Multi-language Support

Built-in support for multiple languages with automatic:
- URL routing (/v1/en/guide → /v1/ja/guide)
- Language switching interface
- Content organization by language

Supported languages: English, Japanese, Chinese (Simplified/Traditional),
Spanish, Portuguese, Korean, German, French, Russian, Arabic, Indonesian,
Turkish, Hindi, Vietnamese

📚 Advanced Features

Automatic Sidebar Generation

pnpm build:sidebar    # Generate navigation for all projects

Selective Builds

pnpm build:selective  # Choose which projects to build

Version Management

# Create new version with content copying
node scripts/create-version.js my-docs v2.0 --interactive

📄 License

This project is licensed under the MIT License - see the LICENSE file for
details.
