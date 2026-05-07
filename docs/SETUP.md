# Setup Guide

## Quick Start

### Prerequisites
- OpenClaw installed and configured
- Git installed
- GitHub account

### Initial Setup

1. **Clone the repo:**
   ```bash
   git clone https://github.com/Cbks77/OpenClaw.git
   cd OpenClaw
   ```

2. **Link to your OpenClaw workspace:**
   ```bash
   # Symlink or copy configs as needed
   cp configs/* ~/.openclaw/workspace/
   ```

3. **Customize:**
   - Edit configuration files in `configs/`
   - Add your assets to `assets/`
   - Create automation scripts in `scripts/`

## What to Store Here

✅ **Safe to commit:**
- Public configuration templates
- Documentation
- Scripts (without secrets)
- Public assets

❌ **Never commit:**
- API keys or tokens
- Personal memory files (MEMORY.md, USER.md)
- Sensitive user data
- Private credentials

## Contributing

Feel free to add useful configs, scripts, or documentation!

---

Questions? Open an issue or reach out! 🔥
