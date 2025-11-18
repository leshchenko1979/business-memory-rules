# Business Memory Rules - Cursor IDE Integration

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A comprehensive memory management system designed specifically for Cursor IDE. This system enables Cursor to maintain structured, efficient business memory management across multiple projects while ensuring data integrity and preventing duplication.

**⚠️ Important**: Requires disabling Cursor's built-in memory system for optimal performance.

## 📋 Table of Contents

- [Overview](#overview)
- [Installation](#installation)
- [Setup](#setup)
- [Usage](#usage)
- [File Structure](#file-structure)
- [Core Principles](#core-principles)
- [Updates](#updates)
- [Contributing](#contributing)
- [License](#license)

## 🎯 Overview

Business Memory Rules provides Cursor IDE with intelligent memory management capabilities for business contexts. It establishes clear guidelines for organizing information, tracking progress, and ensuring data consistency across multiple projects and businesses.

## 🎯 Purpose

This system enables Cursor to:

- **Maintain Business Context**: Keep track of multiple business projects simultaneously
- **Ensure Data Integrity**: Prevent information duplication and maintain single sources of truth
- **Enable Efficient Memory**: Organize information for quick retrieval and optimal context usage
- **Support Business Operations**: Provide structured memory for planning, analysis, and problem-solving
- **Scale Across Projects**: Handle multiple business contexts without confusion

## ✨ Key Features

### 🏗️ Structured Memory Organization
- Hierarchical directory structure for businesses and projects
- Clear separation between factual data and planning information
- Systematic file organization with consistent naming conventions

### 📊 Progress Tracking
- Automated progress logging with accurate date tracking
- Chronological organization of completed actions and decisions
- Integration of key metrics and reference linking

### 🔄 Memory Optimization
- Proactive memory maintenance and reorganization
- Automatic detection of optimization opportunities
- Intelligent content consolidation and duplicate removal

### 🗣️ Dialog-Driven Rule Generation
- Learns actionable rules, procedures, workflows, preferences from conversations
- Dynamically creates `.mdc` rule files in `memory-bank/.cursor/rules/`
- Agent autonomously names and organizes rule files by domain/process
- Each rule file must include Cursor metadata:

```
---
description: "[Brief description of learned rules]"
alwaysApply: false
---
```

- Confirms significant additions/changes with the user before creating/updating
- Rules automatically apply via Cursor’s rule system once saved

### 🎯 Context Management
- Automatic context determination based on user interactions
- Seamless switching between different business/project contexts
- Clear indication of current active context

### ✅ Data Integrity Controls
- Single source of truth enforcement
- Reference-based information linking instead of duplication
- Confirmation protocols for significant changes

## 🚀 Installation & Setup

### Prerequisites

- **Cursor IDE** (latest version recommended)
- Git (for submodule management)
- Terminal/command line access

### ⚠️ Critical: Disable Cursor Memory First

**You MUST disable Cursor's built-in memory system before installation to prevent conflicts:**

1. Open Cursor Settings
2. Navigate to "Rules & Memories"
3. **Disable** "Memories"

**This is essential** - the Business Memory Rules system needs exclusive control over memory management. Running both systems simultaneously will cause conflicts and duplicate memory management.

### One-Command Cursor Setup

```bash
# Navigate to your Cursor workspace
cd /path/to/your/cursor/project

# Create Cursor rules directory
mkdir -p .cursor/rules

# Add Business Memory Rules as submodule
cd .cursor/rules
git submodule add https://github.com/leshchenko1979/business-memory-rules.git business-memory-rules
git submodule update --init --recursive
cd ../..
```

### What You Get After Setup

- ✅ **Automatic Cursor Integration** - Rules are applied automatically in Cursor
- ✅ **Memory Bank Created Automatically** - Cursor creates and manages the memory bank structure
- ✅ **Seamless Workflow** - Business memory management integrated into Cursor
- ✅ **Easy Updates** - Simple git commands to keep rules current
- ✅ **Complete Documentation** - All rules and guidelines included
- ✅ **Automatic Rule Loading** - Cursor automatically loads rules from .cursor/rules/
- ✅ **Dialog-Driven Rule Learning** - Learns from conversations and writes `.mdc` rules to `memory-bank/.cursor/rules/`

## 📁 Cursor Project Structure

After setup, your Cursor workspace will have this structure:

```
your-cursor-project/
├── .cursor/
│   └── rules/
│       └── business-memory-rules/    # Git submodule with core rules

├── memory-bank/                      # Your business memory
│   └── .cursor/
│       └── rules/                    # Dialog-driven learned rules (.mdc)
│   └── YourBusiness/
│       ├── business.md               # Business overview and goals
│       ├── progress-log.md          # Completed actions and decisions
│       └── project-artifacts/       # Factual documents and files
└── [your project files]
```

### File Purpose Guide

| File | Purpose | Content Type |
|------|---------|-------------|

| `business.md` | Business overview | Mission, goals, strategy, partnerships |
| `progress-log.md` | Activity tracking | Completed actions with dates |
| `project-artifacts/` | Document storage | Factual documents, completed work |

## 🏛️ Core Principles

### 1. Single Source of Truth
Each piece of information is stored in exactly one location to prevent inconsistencies and duplication.

### 2. Proactive Memory Management
The system actively maintains its own structure, relevance, and searchability rather than just passively recording information.

### 3. Reference-Based Linking
Instead of copying information, use references to link between related pieces of information.

### 4. Context Awareness
Automatically determine the appropriate business/project context based on user interactions and content analysis.

### 5. Date Accuracy
Always use the system `date` command for timestamps - never hallucinate or guess dates.

## 💡 Usage in Cursor

### How It Works in Cursor

Once set up, the Business Memory Rules are automatically applied by Cursor:

1. **Automatic Context Tracking**: Cursor maintains business/project context across your work
2. **Smart Memory Organization**: Information is automatically organized in the memory bank
3. **Progress Logging**: Completed actions are logged with accurate timestamps
4. **Seamless Integration**: Memory management happens transparently in your workflow

#### Dialog-Driven Rules in Practice
- Explain processes or preferences in chat to teach the system
- Significant new rules are confirmed with you before saving
- Confirmed rules are saved as `.mdc` files under `memory-bank/.cursor/rules/` with metadata:

```
---
description: "[Brief description of learned rules]"
alwaysApply: false
---
```

- Saved rules are automatically applied by Cursor

### Working with Business Memory

Cursor automatically handles business memory management:

- **Context Creation**: Cursor creates business/project contexts as needed
- **File Organization**: Documents and information are automatically organized
- **Progress Logging**: Actions are logged automatically with accurate timestamps
- **Memory Optimization**: Cursor maintains optimal memory structure

### Memory Bank Structure

Your business memory is organized as:

```
memory-bank/
└── YourBusiness/
    ├── business.md           # Business overview, goals, strategy
    ├── progress-log.md      # Chronological activity log
    └── project-artifacts/   # Documents, files, resources
```

### Cursor Integration Features

- **Automatic Rule Application**: Business memory rules are applied automatically
- **Context Awareness**: Cursor understands when you're working on different businesses
- **Progress Tracking**: Actions are logged automatically with accurate dates
- **File Organization**: Documents are stored in appropriate project locations

## 🤝 Contributing

Help improve Cursor's business memory management capabilities:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/cursor-enhancement`)
3. Commit your changes (`git commit -m 'Add Cursor enhancement'`)
4. Push to the branch (`git push origin feature/cursor-enhancement`)
5. Open a Pull Request

### Contribution Guidelines

- Focus on Cursor IDE integration improvements
- Test changes with real Cursor workflows
- Ensure compatibility with Cursor's rule system
- Update documentation for Cursor-specific features

## 🔄 Updating Business Memory Rules

Keep your Cursor business memory rules current with the latest features:

### Update Commands:
```bash
# Update the submodule to latest version
git submodule update --remote .cursor/rules/business-memory-rules

# Check what changed in the latest update
git log --oneline -5 .cursor/rules/business-memory-rules
```

### Checking for Updates:
```bash
# Check if updates are available
git submodule status

# View current version
cd .cursor/rules/business-memory-rules && git describe --tags --abbrev=0 && cd ../..
```

---

**Built for AI agents, by AI agents.** This system represents best practices for maintaining coherent, efficient memory management in complex business environments.
