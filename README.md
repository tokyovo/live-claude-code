# Multi-Language OCR Form Processor

A Next.js application that processes multi-language forms and documents through GPT-4o-mini vision API to extract structured data into CSV files. Built with TypeScript, Next.js 14, and shadcn/ui.

## 🎯 Spec-Kit Setup

This project uses [spec-kit](https://github.com/github/spec-kit) for Spec-Driven Development. To initialize spec-kit in your project:

### Prerequisites

- Python 3.8+ with `uv` or `uvx` installed
- AI coding assistant (Claude Code, GitHub Copilot, etc.)

### Initialize Spec-Kit

```bash
# Initialize in current directory
uvx --from git+https://github.com/github/spec-kit.git \
  specify init . \
  --ai claude \
  --ignore-agent-tools

# Or create a new project
uvx --from git+https://github.com/github/spec-kit.git \
  specify init <project_name> \
  --ai claude \
  --ignore-agent-tools
```

### Available Commands

After initialization, you can use these commands in your AI agent:

- `/speckit.specify` - Create or update feature specifications
- `/speckit.plan` - Generate implementation plans
- `/speckit.tasks` - Break down features into actionable tasks
- `/speckit.implement` - Execute implementation plan
- `/speckit.clarify` - Identify underspecified areas
- `/speckit.analyze` - Perform consistency analysis
- `/speckit.constitution` - Create/update project principles
- `/speckit.checklist` - Generate custom checklists

### Learn More

Visit the [spec-kit documentation](https://github.com/github/spec-kit) for detailed guides on Spec-Driven Development.

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
