# px 🤖

**Context-aware project management for multi-repo AI development.**

`px` (Project X) is a lightweight CLI tool designed to bridge the gap between fragmented codebases and AI context windows. It allows you to create a unified "Project Hub" where multiple repositories are linked side-by-side, governed by a single `AGENTS.md` file.

---

## 📑 Table of Contents

- [Features](#-features)
- [Installation](#-installation)
- [Quick Start](#-quick-start)
- [The AI Advantage](#-the-ai-advantage)
- [Project Structure](#-project-structure)
- [Commands Summary](#-commands-summary)
- [License](#-license)

---

## ✨ Features

- **Sudo-Free Install:** Installs to `$HOME/.local/bin` for security and portability.
- **Git Validation:** Automatically verifies that linked folders are valid Git repositories before linking.
- **Flat Workspaces:** Links repos directly to the project root for shallow file-path discovery (optimized for LLMs).
- **Context First:** Generates an `AGENTS.md` template and opens it in your `$EDITOR` instantly.

---

## 📦 Installation

Clone the repository and run the install command. No root/sudo required.

```bash
git clone [https://github.com/your-username/px.git](https://github.com/your-username/px.git)
cd px
chmod +x px
./px install
```

> **Note:** Ensure `$HOME/.local/bin` is in your `PATH`.

If it's not, add the following line to your `.zshrc` or `.bashrc`:

```bash
export PATH="$HOME/.local/bin:$PATH"
```

---

## 🚀 Quick Start

### 1. Initialize a Project

Create a new feature hub. This will create the folder in your `$PX_ROOT` (default: `~/my-projects`) and open `AGENTS.md` in your preferred editor.

```bash
px init new-payment-flow
```

### 2. Link Repositories

Link as many repositories as you need for the feature.

```bash
px add ~/code/api-service
px add ~/code/web-frontend

```

### 3. Start Developing

Launch your AI agent of choice (e.g., Crush, Aider, Claude Engineer, or Cursor) in the project root.

```bash
# Example with Crush
crush
```

---

## 🤖 The AI Advantage

When working with LLMs, **structure is context**. `px` optimizes your workflow for modern AI agents:

- **Shallow Path Discovery:** By flattening the directory structure, agents spend fewer tokens "navigating" subdirectories and more tokens "coding."
- **Unified Intent:** The `AGENTS.md` serves as a cross-repo manifest. When an agent starts, simply say: _"Read AGENTS.md for the mission parameters."_
- **Full Git Power:** Because `px` uses symbolic links, agents maintain full access to the Git history, branches, and metadata of the original repositories.

---

## 📂 Project Structure

A typical `px` project looks like this:

```text
~/my-projects/new-payment-flow/
├── AGENTS.md            # Your primary AI mission & instructions
├── api-service/         # Symlink to ~/code/api-service
└── web-frontend/        # Symlink to ~/code/web-frontend
```

---

## 🛠 Commands Summary

| Command            | Description                                      |
| ------------------ | ------------------------------------------------ |
| `px init <name>`   | Bootstraps a project and opens the editor.       |
| `px add <path>`    | Links an existing Git repo into the project.     |
| `px list`          | Shows all projects and their linked repo counts. |
| `px remove <link>` | Safely removes a link and cleans `AGENTS.md`.    |
| `px install`       | Symlinks the script to your local bin folder.    |

---

## ⚙️ Configuration

You can customize the project location by setting the `PX_ROOT` variable in your shell profile:

```bash
export PX_ROOT="$HOME/work/ai-features"
```

---

## 📜 License

This project is licensed under the [MIT License](LICENSE).
