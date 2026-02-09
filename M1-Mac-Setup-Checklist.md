# M1 MacBook Development Environment Setup

**Purpose**: Complete migration from Intel Mac to M1 Mac with full development toolchain<br>
**Started**: [Add date]<br>
**Completed**: [Add date]

---

## Phase 1: Foundation ✓

### 1.1 Homebrew (ARM-native)
- [ ] Install Homebrew for ARM (`/opt/homebrew`)
  ```bash
  /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
  ```
- [ ] Add Homebrew to PATH
  ```bash
  echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile
  eval "$(/opt/homebrew/bin/brew shellenv)"
  ```
- [ ] Verify installation: `brew --version`
- [ ] Notes: _______________________________________________

### 1.2 Fish Shell
- [ ] Install Fish via Homebrew: `brew install fish`
- [ ] Add Fish to available shells: `echo /opt/homebrew/bin/fish | sudo tee -a /etc/shells`
- [ ] Set Fish as default shell: `chsh -s /opt/homebrew/bin/fish`
- [ ] Restart terminal and verify: `echo $SHELL`
- [ ] Configure Fish preferences (if needed)
- [ ] Notes: _______________________________________________

### 1.3 Git
- [ ] Install Git via Homebrew: `brew install git`
- [ ] Configure user name: `git config --global user.name "Your Name"`
- [ ] Configure user email: `git config --global user.email "your@email.com"`
- [ ] Generate SSH key: `ssh-keygen -t ed25519 -C "your@email.com"`
- [ ] Add SSH key to ssh-agent
- [ ] Add SSH key to GitHub/GitLab/Bitbucket
- [ ] Test SSH connection: `ssh -T git@github.com`
- [ ] Notes: _______________________________________________

### 1.4 iTerm2 with AI Plugin
- [ ] Download iTerm2 from https://iterm2.com/
- [ ] Install iTerm2
- [ ] Open iTerm2 and complete initial setup
- [ ] Go to https://console.anthropic.com/ and sign in
- [ ] Navigate to API Keys section
- [ ] Create new API key (name: "iTerm2 AI Plugin")
- [ ] Copy API key (store securely)
- [ ] Open iTerm2 → Settings → AI
- [ ] Enable AI Plugin
- [ ] Paste Anthropic API key
- [ ] Select model (recommend: Claude Sonnet 4.5)
- [ ] Test AI functionality
- [ ] Notes: _______________________________________________

### 1.5 Claude Desktop
- [ ] Download Claude Desktop from https://claude.ai/download
- [ ] Install Claude Desktop app
- [ ] Launch Claude Desktop
- [ ] Sign in with Claude account credentials
- [ ] Verify Max subscription is active
- [ ] Configure preferences (appearance, notifications)
- [ ] Test basic functionality
- [ ] Notes: _______________________________________________

### 1.6 fnm + Node.js 20
- [ ] Install fnm: `brew install fnm`
- [ ] Add fnm to Fish config:
  ```fish
  echo 'fnm env --use-on-cd | source' >> ~/.config/fish/config.fish
  ```
- [ ] Restart Fish shell
- [ ] Install Node 20: `fnm install 20`
- [ ] Set as default: `fnm default 20`
- [ ] Verify: `node --version` (should show v20.x.x)
- [ ] Verify: `npm --version`
- [ ] Notes: _______________________________________________

### 1.7 Docker Desktop (ARM-native)
- [ ] Download Docker Desktop for Apple Silicon from https://www.docker.com/products/docker-desktop
- [ ] Install Docker Desktop
- [ ] Launch Docker Desktop
- [ ] Complete initial setup and sign in (if applicable)
- [ ] Enable Kubernetes (optional)
- [ ] Configure resource limits (CPU, Memory)
- [ ] Verify: `docker --version`
- [ ] Verify: `docker ps`
- [ ] Test with hello-world: `docker run hello-world`
- [ ] Notes: _______________________________________________

---

## Phase 2: Dev Tools ✓

### 2.1 VS Code (Apple Silicon)
- [ ] Download VS Code for Apple Silicon from https://code.visualstudio.com/
- [ ] Install VS Code
- [ ] Launch VS Code
- [ ] Sign in with GitHub/Microsoft account (for Settings Sync)
- [ ] Enable Settings Sync (if desired)
- [ ] Configure basic preferences
- [ ] Notes: _______________________________________________

### 2.2 Claude Code CLI
- [ ] Install globally: `npm install -g @anthropic-ai/claude-code`
- [ ] Verify installation: `claude-code --version`
- [ ] Run initial setup: `claude-code`
- [ ] Authenticate with Anthropic account
- [ ] Test basic functionality
- [ ] Notes: _______________________________________________

### 2.3 Claude Code VS Code Extension
- [ ] Open VS Code
- [ ] Go to Extensions (⇧⌘X)
- [ ] Search for "Claude Code"
- [ ] Install the extension
- [ ] Open Claude Code sidebar
- [ ] Configure extension settings
- [ ] Connect to Claude Code CLI
- [ ] Test integration
- [ ] Notes: _______________________________________________

### 2.4 Other VS Code Extensions
- [ ] Docker extension
- [ ] ShellCheck extension
- [ ] YAML extension
- [ ] GitLens extension
- [ ] Python extension (if needed)
- [ ] Java Extension Pack (if needed)
- [ ] Any other project-specific extensions
- [ ] Notes: _______________________________________________

---

## Phase 3: Claude Desktop + Cowork ✓

### 3.1 Claude Desktop Configuration
- [ ] Claude Desktop is already installed (from Phase 1)
- [ ] Verify Claude Desktop is running
- [ ] Check for updates
- [ ] Notes: _______________________________________________

### 3.2 Cowork Setup
- [ ] Open Claude Desktop
- [ ] Navigate to Cowork settings/features
- [ ] Enable Cowork (requires M1 Mac)
- [ ] Configure Cowork preferences
- [ ] Grant necessary permissions
- [ ] Test file and task management features
- [ ] Notes: _______________________________________________

---

## Phase 4: Projects ✓

### 4.1 Clone Repositories
- [ ] Create workspace directory: `mkdir -p ~/workspace`
- [ ] List all repositories to clone: _______________________________________________
- [ ] Clone repo 1: _______________________________________________
- [ ] Clone repo 2: _______________________________________________
- [ ] Clone repo 3: _______________________________________________
- [ ] Clone repo 4: _______________________________________________
- [ ] Clone repo 5: _______________________________________________
- [ ] Notes: _______________________________________________

### 4.2 Install Project Dependencies
- [ ] Project 1: `cd [project1] && npm install` (or equivalent)
- [ ] Project 2: `cd [project2] && npm install` (or equivalent)
- [ ] Project 3: `cd [project3] && gradle build` (or equivalent)
- [ ] Project 4: _______________________________________________
- [ ] Project 5: _______________________________________________
- [ ] Notes: _______________________________________________

### 4.3 Verify Builds and Tests
- [ ] Project 1: Run build and verify success
- [ ] Project 1: Run tests and verify passing
- [ ] Project 2: Run build and verify success
- [ ] Project 2: Run tests and verify passing
- [ ] Project 3: Run build and verify success
- [ ] Project 3: Run tests and verify passing
- [ ] Address any ARM-specific compatibility issues
- [ ] Notes: _______________________________________________

---

## Phase 5: Decommission Intel Mac ✓

### 5.1 Audit
- [ ] Verify all critical tools are working on M1
- [ ] Verify all projects build successfully on M1
- [ ] Verify all tests pass on M1
- [ ] Check for any missing tools or configurations
- [ ] Notes: _______________________________________________

### 5.2 Transfer Files
- [ ] Transfer non-repo documents
- [ ] Transfer credentials and API keys
- [ ] Transfer configuration files (.bashrc, .gitconfig, etc.)
- [ ] Transfer SSH keys (if not regenerated)
- [ ] Transfer any other personal files
- [ ] Notes: _______________________________________________

### 5.3 Security Cleanup
- [ ] List all API keys on Intel Mac: _______________________________________________
- [ ] Revoke or rotate API keys tied to Intel Mac
- [ ] Remove credentials from Intel Mac
- [ ] Sign out of all accounts on Intel Mac
- [ ] Factory reset Intel Mac (optional)
- [ ] Notes: _______________________________________________

---

## Post-Migration ✓

### Additional Tools (as needed)
- [ ] Postman or Insomnia (API testing)
- [ ] Database tools (DBeaver, TablePlus, etc.)
- [ ] Java JDK (if needed): `brew install openjdk@17`
- [ ] Python (if needed): `brew install python@3.11`
- [ ] Android Studio (if needed)
- [ ] Xcode (if needed - download from App Store)
- [ ] Other tools: _______________________________________________

### Configuration Verification
- [ ] All environment variables set correctly
- [ ] All shell aliases and functions working
- [ ] All integrations (CI/CD, cloud services) configured
- [ ] Backup strategy in place
- [ ] Notes: _______________________________________________

---

## Troubleshooting Notes

**Date**: [Add date]<br>
**Issue**: _______________________________________________<br>
**Resolution**: _______________________________________________

**Date**: [Add date]<br>
**Issue**: _______________________________________________<br>
**Resolution**: _______________________________________________

**Date**: [Add date]<br>
**Issue**: _______________________________________________<br>
**Resolution**: _______________________________________________

---

## Completion Summary

**Total Time**: [Add duration]<br>
**Major Challenges**: _______________________________________________<br>
**Lessons Learned**: _______________________________________________<br>
**Next Steps**: _______________________________________________
