# px - Project Agent Hub

A CLI tool to quickly bootstrap multi-repo development environments for AI agents.

## Features

- **Project Isolation:** Keeps all your AI feature-work in one configurable location.
- **Git Validation:** Ensures only valid repositories are linked.
- **AI-Ready:** Automatically generates an `AGENTS.md` context file.
- **Clean Symlinking:** Directly links repos into the root for shallow file-path discovery.

## Installation

1. Clone the repo: `git clone https://github.com/your-username/px.git`
2. Run installation: `./px install`

## Usage

- `px init my-new-feature`
- `px add ~/path/to/repo`
- `px list`
