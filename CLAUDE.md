# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A single-page web application (小红书笔记生成器) for creating Xiaohongshu-style social media notes. Pure static HTML with embedded CSS/JS - no build process required. Open `index.html` directly in browser to run.

## Key Features

- **Markdown Editor** (left panel): Write content with image paste support (Ctrl+V)
- **Live Preview** (center): Real-time card preview with zoom and grid/list views
- **Style Config** (right panel): 4 themes (Minimal, Serif, Acid, Tech), cover settings, typography controls
- **Export**: Single JPG or bulk ZIP download via html-to-image + jszip

## File Structure

- `index.html` - Complete application (1400+ lines)
  - Inline Tailwind CSS via CDN
  - 4 theme definitions (`.theme-minimal`, `.theme-serif`, `.theme-acid`, `.theme-tech`)
  - Embedded JavaScript for editor, renderer, and export logic

## Important Implementation Details

- **Image handling**: Paste images as base64, stored in `state.bodyImages` object, referenced in markdown as `![截图](img:{id})`
- **Page splitting**: Use `@---` delimiter in markdown to create multiple cards
- **Row layout**: Use `::: row ... :::` syntax for multi-image rows
- **State management**: `state` object tracks style, sizes, and images
- **Themes**: `STYLES` array defines 4 built-in themes with CSS classes and config objects

## Common Tasks

- Add new theme: Define CSS class (`.theme-X`) and add entry to `STYLES` array + `themeStyles` object in `renderCoverHTML`
- Modify export quality: Adjust `pixelRatio` and `quality` in `htmlToImage.toJpeg()` calls
- Add new font: Add Google Fonts link in `<head>`, reference in CSS
