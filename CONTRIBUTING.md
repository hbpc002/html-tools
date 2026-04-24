# Contributing Guide

## How to Add a New Tool

### Method 1: Using the Web Interface (Recommended)

1. Open the deployed site (GitHub Pages URL)
2. Click "Add Tool" in the navigation
3. Fill in the tool details:
   - **Slug**: Unique identifier (e.g., `my-new-tool`)
   - **Name (English)**: Tool name in English
   - **Name (中文)**: Tool name in Chinese
   - **Description**: Brief description in both languages
   - **Tags**: Comma-separated tags
   - **Version**: Semantic version (default: 1.0.0)
   - **Author**: Your name
   - **HTML Content**: Your complete HTML tool code
4. Click "Generate Patch"
5. Copy the patch output
6. Create a Pull Request with the patch

### Method 2: Manual Contribution

1. Fork the repository
2. Add your tool file to `tools/{your-tool-slug}/index.html`
3. Update `tools.json` with the tool entry
4. Create a Pull Request

## Tool Requirements

- Single HTML file (inline CSS/JS allowed)
- No external dependencies (or use CDN)
- Responsive design
- Works in modern browsers

## Tool Manifest Schema

```json
{
  "slug": "tool-slug",
  "name_en": "Tool Name",
  "name_zh": "工具名称",
  "description_en": "Description",
  "description_zh": "描述",
  "path": "tools/tool-slug/index.html",
  "tags": ["tag1", "tag2"],
  "version": "1.0.0",
  "author": "Your Name",
  "homepage": "",
  "last_updated": "2026-04-24"
}
```

## CI/CD

The repository uses GitHub Actions to:
- Validate `tools.json` on each push
- Check for duplicate slugs
- Verify tool paths exist

## Language

This project supports bilingual (English/Chinese). Please provide names and descriptions in both languages when possible.