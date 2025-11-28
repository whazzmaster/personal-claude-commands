# Claude Commands

Reusable Claude Code slash commands and a justfile for Claude-powered git workflows.

## What's Included

### Slash Commands

- **`/commit`** - Generate Conventional Commits 1.0.0 compliant commit messages from staged changes
- **`/pr`** - Generate comprehensive pull request titles and descriptions
- **`/simple-pr`** - Generate concise PRs for minor changes

### Justfile Recipes

- `just commit` - Generate commit message with Claude, review in editor, then commit
- `just pr` - Choose between simple or full PR generation
- `just full-pr` - Generate detailed PR with Claude
- `just simple-pr` - Generate concise PR with Claude

## Setup

### 1. Clone the repo

```bash
git clone <repo-url> ~/.claude/commands
```

### 2. Copy the justfile

```bash
cp ~/.claude/commands/justfile ~/justfile
```

### 3. Install dependencies

Make sure `just` and `gum` are installed:

```bash
# macOS
brew install just gum

# Or see:
# https://github.com/casey/just
# https://github.com/charmbracelet/gum
```

### 4. Create a shell alias

To use the global justfile from anywhere, add this alias to your shell config (`.bashrc`, `.zshrc`, etc.):

```bash
alias j="just --justfile ~/justfile --working-directory ."
```

## Usage

Once configured, use the recipes from any git repository:

```bash
# Stage changes and generate a commit message
git add .
j commit

# Create a pull request
j pr
```

The slash commands are also available directly in Claude Code:

```
/commit
/pr
/simple-pr
```
