# Multi-Language OCR Form Processor

A Next.js application that processes multi-language forms and documents through GPT-4o-mini vision API to extract structured data into CSV files. Built with TypeScript, Next.js 14, and shadcn/ui.

## 🎯 Spec-Kit Workflow

This project was built using [spec-kit](https://github.com/github/spec-kit) with Claude Code for Spec-Driven Development. Follow these steps to recreate or extend this project:

### 1. Install Specify CLI

Choose your preferred installation method:

**Option 1: Persistent Installation (Recommended)**

Install once and use everywhere:

```bash
uv tool install specify-cli \
  --from git+https://github.com/github/spec-kit.git
```

Then use the tool directly:

```bash
specify init <PROJECT_NAME>
specify check
```

To upgrade specify run:

```bash
uv tool install specify-cli --force \
  --from git+https://github.com/github/spec-kit.git
```

**Option 2: One-time Usage**

Run directly without installing:

```bash
uvx --from git+https://github.com/github/spec-kit.git \
  specify init <PROJECT_NAME>
```

**Benefits of persistent installation:**
- Tool stays installed and available in PATH
- No need to create shell aliases
- Better tool management with `uv tool list`, `uv tool upgrade`, `uv tool uninstall`
- Cleaner shell configuration

### 2. Establish project principles

Launch your AI assistant in the project directory. The `/speckit.*` commands are available in the assistant.

Use the `/speckit.constitution` command to create your project's governing principles and development guidelines that will guide all subsequent development.

```
/speckit.constitution Create principles focused on multi-language OCR accuracy, \
form structure detection, user privacy, reliable CSV export quality, and \
accessibility standards
```

### 3. Create the spec

Use the `/speckit.specify` command to describe what you want to build. Focus on the **what** and **why**, not the tech stack.

```
/speckit.specify Build an application that processes multi-language forms and \
documents through OCR to extract structured data into CSV files. Users upload \
images or PDFs containing text in various languages (forms, handwritten notes, \
business documents), the app detects text regions and form fields, performs \
accurate multi-language OCR, and exports organized data as CSV with customizable \
column mappings. Support batch processing and ensure privacy by not storing files \
on the server.
```

### 4. Create a technical implementation plan

Use the `/speckit.plan` command to provide your tech stack and architecture choices.

```
/speckit.plan Use Next.js 14 with App Router and TypeScript for the web application. \
Use shadcn/ui for modern UI components and Tailwind CSS for styling. Implement OCR \
functionality using OpenAI GPT-4o-mini vision API through Vercel AI SDK. Use React \
Hook Form with Zod for form validation, Papa Parse for CSV generation, and p-queue \
for batch processing queue management. Include comprehensive testing with Vitest for \
unit tests and Playwright for E2E tests. Ensure ≥80% code coverage and WCAG 2.1 AA \
accessibility compliance.
```

### 5. Break down into tasks

Use `/speckit.tasks` to create an actionable task list from your implementation plan.

```
/speckit.tasks
```

### 6. Execute implementation

Use `/speckit.implement` to execute all tasks and build your feature according to the plan.

```
/speckit.implement
```

## ✨ Features

- 📄 **Multi-Language OCR**: Extract text from images and PDFs in 10+ languages
- 🎯 **Form Field Detection**: Automatically detect labels, fields, checkboxes, and tables
- 📊 **CSV Export**: Export structured data with custom column mappings
- 🚀 **Batch Processing**: Process up to 50 documents simultaneously
- 🔒 **Privacy-First**: No server-side storage, immediate deletion after export
- ♿ **Accessible**: WCAG 2.1 AA compliant with full keyboard navigation
- 📱 **Responsive**: Works on mobile, tablet, and desktop

## 🚀 Quick Start

### Prerequisites

- Node.js 18.17+ or 20.3+
- npm, pnpm, or yarn
- OpenAI API key ([Get one here](https://platform.openai.com/))

### Installation

```bash
# Clone the repository
git clone <repository-url>
cd live-claude-code

# Install dependencies
npm install

# Copy environment variables
cp .env.example .env.local

# Add your OpenAI API key to .env.local
# OPENAI_API_KEY=sk-proj-...
```

### Development

```bash
# Start development server
npm run dev

# Open http://localhost:3000
```

## 🙏 Credits

Built with [spec-kit](https://github.com/github/spec-kit) workflow and Claude Code.
