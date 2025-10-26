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

### 2. Run Spec-Kit Workflow

```
/speckit.constitution Build with Next.js + Tailwind CSS + shadcn/ui. Prioritise clean, simple, beautiful, and accessible UI/UX. Fully responsive across devices. Keep code minimal, readable, and idiomatic. No tests of any kind (no unit, integration, or end-to-end tests).

/speckit.specify Build a simple web app that allows users to upload image files (documents in various languages) and perform OCR using the OpenAI API.
Use `OPENAI_API_KEY` and model name from `.env.local`.
The API response must be returned in JSON format following `@output_schema.json`.
Display results in a two-column layout: left column shows the uploaded image, right column renders the parsed JSON as formatted HTML.
Provide a button for users to download the JSON output.

/speckit.clarify

/speckit.plan Build with Next.js, Tailwind CSS, and shadcn/ui. Use the OpenAI API to perform OCR parsing on document images. No tests of any kind.

/speckit.tasks

/speckit.implement
```
