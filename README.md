# awesome-cursor-rules
A curated list of awesome Cursor rules (.cursorrules) and MCP servers for AI-assisted development. maintained by AgentIndex.app
# Awesome Cursor Rules & MCP Servers

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)
[![Website](https://img.shields.io/website?url=https%3A%2F%2Fagentindex.app&label=AgentIndex.app)](https://agentindex.app)

> A curated list of best practices, `.cursorrules` files, and MCP servers to supercharge your AI coding experience with Cursor, Windsurf, and VSCode.

---

## 🚀 The Ultimate Collection (Better Experience)

**Searching for specific rules by language or framework?**

👉 **[Visit AgentIndex.app](https://agentindex.app)** for the full, searchable directory with one-click copy and compatibility checks.

*(We update the website daily with new agents and rules that aren't listed here yet!)*

---

## 📚 Contents

- [General Rules](#general-rules)
- [iOS & macOS](#ios--macos)
- [Web Development](#web-development)
- [Python & AI](#python--ai)
- [MCP Servers](#mcp-servers)
- [Contributing](#contributing)

## General Rules
*通用规则，适用于大多数项目*

- **Senior Developer Persona**: Forces the AI to think deeply before answering. [Source](https://agentindex.app)
- **Concise Coder**: No yapping, just code. Optimized for speed.

## iOS & macOS
*Focus on Swift, SwiftUI, Objective-C*

- **SwiftUI Expert & Clean Architecture**:
    * **Description**: Forces Cursor to use the latest Swift 5.9+ syntax, prioritize value types, and strictly follow MVVM pattern.
    * **Rule Content**: [Copy from AgentIndex.app](https://agentindex.app) (Or use the snippet below)
    * **.cursorrules Snippet**:
      ```markdown
      You are an expert iOS Developer proficient in Swift, SwiftUI, and Combine.
      
      - Always use `struct` over `class` unless you need reference semantics.
      - Use `some View` for body types.
      - Prefer `Async/Await` over completion handlers.
      - Strictly follow MVVM: Views should only talk to ViewModels.
      - For UI, always assume iOS 16+ unless specified otherwise.
      - When using SF Symbols, ensure availability check.
      ```

- **XCode Build Fixer**: Helps debug obscure derived data and signing issues. [Get Rule](https://agentindex.app)

## Web Development
*React, Vue, Next.js, Tailwind*

- **Next.js 14 App Router & SEO**:
    * **Description**: Enforces modern Next.js 14+ conventions (App Router, Server Components) and SEO best practices.
    * **.cursorrules Snippet**:
      ```markdown
      You are an expert in Next.js 14+, React, and TypeScript.
      
      - **App Router**: Always use the `app/` directory. Do not use the `pages/` directory.
      - **Server Components**: All components are Server Components by default. Use `'use client'` only when necessary (e.g., hooks, event listeners).
      - **Data Fetching**: Use standard `fetch` with async/await in Server Components. Avoid `useEffect` for data fetching.
      - **Images**: Always use `next/image` with proper sizing and format (WebP).
      - **Metadata**: Use the Metadata API for SEO tags, not `<head>`.
      - **Filenames**: Use `page.tsx`, `layout.tsx`, `loading.tsx` conventions.
      ```

- **Tailwind CSS Master**:
    * **Description**: Generates clean, responsive, and maintainable Tailwind utility classes.
    * **.cursorrules Snippet**:
      ```markdown
      You are a Tailwind CSS expert.
      
      - **Utility First**: Use utility classes over custom CSS. Avoid `@apply` unless absolutely necessary.
      - **Responsive Design**: Use mobile-first breakpoints (`sm:`, `md:`, `lg:`).
      - **Sorting**: Order classes logically (Layout -> Box Model -> Typography -> Visuals).
      - **Arbitrary Values**: Use `[]` for one-off values sparingly.
      - **Colors**: Use semantic color names (e.g., `text-primary`, `bg-surface`) if defined, otherwise standard palette.
      ```

## Python & AI
*FastAPI, PyTorch, Django*

- **Clean Python & PEP 8**:
    * **Description**: Writes Pythonic code focusing on type safety, readability, and standard formatting.
    * **.cursorrules Snippet**:
      ```markdown
      You are an expert Python developer.
      
      - **Style**: Strictly follow PEP 8 standards (indentation, snake_case for functions/vars).
      - **Type Hinting**: Always use the `typing` module. Function signatures must have type hints.
      - **Docstrings**: Use Google-style docstrings for all public functions and classes.
      - **Modern Python**: Use `f-strings` for formatting. Use `pathlib` instead of `os.path`.
      - **Error Handling**: Use specific exceptions (e.g., `ValueError`) instead of generic `Exception`.
      ```

## MCP Servers
*Model Context Protocol Integrations - Copy these configs to your `claude_desktop_config.json`*

- **PostgreSQL Inspector**:
    * **Description**: Give AI safe, read-only access to inspect your database schema and run queries to debug issues.
    * **Config (JSON)**:
      ```json
      "postgres": {
        "command": "npx",
        "args": [
          "-y",
          "@modelcontextprotocol/server-postgres",
          "postgresql://user:password@localhost:5432/your_db_name"
        ]
      }
      ```

- **Git Commit Assistant**:
    * **Description**: Allows AI to read your `git diff` and `git status` to automatically generate semantic commit messages.
    * **Config (JSON)**:
      ```json
      "git": {
        "command": "npx",
        "args": [
          "-y",
          "@modelcontextprotocol/server-git"
        ]
      }
      ```

---
- **Statsnet MCP**:
    * **Description**: Background check any company in the world: registration, executives, courts and finances.
    * **Repo**: [https://github.com/usenetstate/statsnet-mcp](https://github.com/usenetstate/statsnet-mcp)
    * **Remote**: `https://statsnet.co/mcp`
    * **Config (JSON)**:
      ```json
      "statsnet": {
        "url": "https://statsnet.co/mcp"
      }
      ```

## Contributing

We love contributions!
1. Fork this repo.
2. Create a branch (`git checkout -b add-new-rule`).
3. Commit your changes.
4. Push to the branch.
5. Create a **Pull Request**.

**Or simply submit your Agent/Rule directly at [AgentIndex.app](https://agentindex.app) for faster listing!**
