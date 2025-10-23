# Multi-Language OCR Form Processor

A Next.js application that processes multi-language forms and documents through GPT-4o-mini vision API to extract structured data into CSV files. Built with TypeScript, Next.js 14, and shadcn/ui.

## 🎯 Spec-Kit Workflow

This project was built using [spec-kit](https://github.com/github/spec-kit) for Spec-Driven Development. Follow these steps to recreate or extend this project:

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

### Build & Deploy

```bash
# Build for production
npm run build

# Start production server
npm start

# Deploy to Vercel
vercel
```

## 📚 Documentation

- [Feature Specification](./specs/001-multilang-ocr-processor/spec.md) - Product requirements
- [Implementation Plan](./specs/001-multilang-ocr-processor/plan.md) - Technical architecture
- [Data Model](./specs/001-multilang-ocr-processor/data-model.md) - Entity definitions
- [Quickstart Guide](./specs/001-multilang-ocr-processor/quickstart.md) - Detailed setup
- [Tasks](./specs/001-multilang-ocr-processor/tasks.md) - Implementation breakdown

## 🧪 Testing

```bash
# Run all tests
npm test

# Unit tests with coverage
npm run test:unit

# Integration tests
npm run test:integration

# E2E tests (Playwright)
npm run test:e2e

# Coverage report
npm run test:coverage
```

## 🛠️ Tech Stack

- **Framework**: Next.js 14 (App Router)
- **Language**: TypeScript 5.x
- **UI**: shadcn/ui + Tailwind CSS
- **AI**: Vercel AI SDK + OpenAI GPT-4o-mini
- **Forms**: React Hook Form + Zod
- **Testing**: Vitest + Playwright + MSW
- **Image Processing**: OpenCV.js
- **CSV**: Papa Parse
- **Queue**: p-queue
- **Rate Limiting**: Upstash Redis (optional)

## 📁 Project Structure

```
app/
├── (main)/           # Main application routes
│   ├── layout.tsx   # App layout with navigation
│   └── page.tsx     # Home page with upload interface
├── api/             # API routes
│   └── ocr/         # OCR processing endpoint
└── globals.css      # Global styles

components/
├── ui/              # shadcn/ui primitives
├── upload/          # File upload components
├── ocr/             # OCR results display
├── export/          # CSV export components
└── batch/           # Batch processing

lib/
├── api/             # API client functions
├── ocr/             # OCR processing logic
├── export/          # CSV generation
├── validation/      # Zod schemas
└── utils/           # Utility functions

types/               # TypeScript definitions
hooks/               # Custom React hooks
tests/               # Test files
```

## 🔐 Environment Variables

```env
# Required
OPENAI_API_KEY=sk-proj-...

# Optional: Rate Limiting (Upstash)
UPSTASH_REDIS_REST_URL=https://...
UPSTASH_REDIS_REST_TOKEN=...

# Optional: Development
NEXT_PUBLIC_ENABLE_DEBUG=true
NEXT_PUBLIC_MAX_FILE_SIZE_MB=50
NEXT_PUBLIC_MAX_PDF_SIZE_MB=100
```

## 📋 Supported File Types

- **Images**: JPEG, PNG, TIFF, BMP, WebP (up to 50MB)
- **Documents**: PDF (up to 100MB)

## 🌍 Supported Languages

English, Spanish, French, German, Italian, Portuguese, Chinese, Japanese, Korean, Arabic, Russian, and more via GPT-4o-mini's vision capabilities.

## 🤝 Contributing

This project follows Test-Driven Development (TDD) with ≥80% code coverage required.

1. Write tests first (Red)
2. Implement minimal code (Green)
3. Refactor for quality (Refactor)
4. Ensure tests pass: `npm test`

## 📄 License

MIT

## 🙏 Credits

Built with [spec-kit](https://github.com/github/spec-kit) workflow and Claude Code.

---

**Need help?** Check the [Quickstart Guide](./specs/001-multilang-ocr-processor/quickstart.md) for detailed setup instructions.
