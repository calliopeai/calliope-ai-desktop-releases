# Changelog

All notable changes to Calliope AI desktop applications will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [1.0.0] - 2025-01-14

### Calliope AI IDE

**Initial Release - Professional AI-Enhanced Development Environment**

#### Added
- **Core IDE Functionality**
  - Full-featured code editor with IntelliSense, syntax highlighting, and debugging
  - Integrated terminal with shell support
  - Built-in Git source control integration
  - Extension marketplace compatibility for thousands of extensions

- **Calliope AI Agent**
  - Rich chat interface with AI-powered coding assistance
  - Multi-provider LLM support (OpenAI, Anthropic, Google, Ollama)
  - Feature-specific model configuration (separate models for chat vs autocomplete)
  - Inline code completions with GitHub Copilot-style suggestions
  - AI-powered code editing and refactoring
  - Native chat participant integration (`@calliope`)
  - Secure API key management via SecretStorage API

- **Custom Branding & Themes**
  - Calliope custom theme with professional color schemes
  - Branded welcome screen and UI elements
  - Custom application icons and logos

- **Pre-installed Extensions**
  - Calliope AI Agent - Multi-provider AI coding assistant
  - Pergamon Theme - Custom Calliope branding
  - Claude Code Launcher - Quick launch for Claude Code
  - Amplifier - AI development environment enhancements

- **Platform Support**
  - macOS (Intel x64, Apple Silicon ARM64, Universal)
  - Windows (x64, ARM64)
  - Linux (x64, ARM64) with multiple package formats

#### Technical Highlights
- Web-first architecture for universal compatibility
- Dual-bundle system for optimal performance
- Secure configuration management
- Offline-capable with optional AI features

---

### Calliope AI Lab

**Initial Release - Advanced AI-Powered Data Analysis Environment**

#### Added
- **Notebook Environment**
  - Interactive notebook interface for data analysis
  - Full Python data science stack included
  - Support for multiple kernel types
  - Rich output rendering (tables, charts, images)
  - Markdown and code cell support

- **Chat Studio (Data Agent)**
  - AI-powered data analysis with natural language queries
  - Intelligent data exploration and insights
  - Automated visualization generation
  - Context-aware data manipulation suggestions

- **Multi-LLM Integration**
  - Support for Claude (Anthropic)
  - Support for GPT models (OpenAI)
  - Support for Gemini (Google)
  - Support for Ollama (local models)
  - Easy provider switching and configuration

- **Bundled Python Environment**
  - Complete data science stack via micromamba
  - Pre-installed packages: pandas, numpy, matplotlib, scikit-learn, and more
  - Jupyter notebook support
  - PostgreSQL database integration

- **Custom Extensions**
  - Pergamon Theme - Custom UI theming
  - Pergamon Server - Enhanced server capabilities
  - Jupyter AI v2 - Advanced AI features for notebooks
  - Custom data agent extensions

- **Data Persistence**
  - Local PostgreSQL database for data storage
  - Automatic workspace management
  - Session persistence across restarts
  - Configurable data directories

- **Platform Support**
  - macOS (Intel x64, Apple Silicon ARM64, Universal)
  - Windows (x64)
  - Linux (x64, ARM64)
  - Multiple package formats (DMG, DEB, RPM, AppImage, TAR.GZ)

#### Technical Highlights
- Electron-based desktop application
- Bundled Python environment (no separate installation required)
- Built-in PostgreSQL database
- Auto-update mechanism
- Completely offline-capable operation

---

## Build System Updates

### Desktop Build Infrastructure (v1.0.0)

#### Added
- Multi-platform CI/CD pipeline via GitHub Actions
- Automated builds for 6 platform/architecture combinations
- Parallel build execution for faster release cycles
- Artifact caching and optimization
- Tag-based release automation
- Manual workflow dispatch option

#### Platform Build Support
- macOS builds on macOS-14 runners
- Linux builds on Ubuntu runners
- Windows builds on Windows runners
- Cross-architecture compilation support

#### Build Optimizations
- Node.js heap size optimization for large builds
- Rollup binary management for webview compilation
- WebView asset bundling improvements
- Increased build timeouts for complex compilation (up to 4 hours)
- Memory allocation tuning (up to 16GB heap for webview bundles)

---

## Known Issues

### Calliope AI IDE
- **macOS Security**: Unsigned builds require right-click → "Open" on first launch
- **Windows SmartScreen**: May show warning; click "More info" → "Run anyway"
- **Linux**: Some distributions may require additional dependencies

### Calliope AI Lab
- **First Launch**: Initial Python environment setup may take 2-3 minutes
- **macOS Security**: Unsigned builds require right-click → "Open" on first launch
- **Windows SmartScreen**: May show warning; click "More info" → "Run anyway"

---

## Upgrade Notes

This is the initial v1.0.0 release. No upgrade path from previous versions is required.

Future releases will include upgrade instructions and migration guides as needed.

---

## What's Next?

### Planned for v1.1.0
- Code signing for macOS and Windows
- Additional AI provider integrations
- Enhanced offline capabilities
- Performance optimizations
- Extended documentation and tutorials

---

**Note**: For detailed release artifacts and downloads, check the [Releases](../../releases) page.

---

_Generated for the initial v1.0.0 public release of Calliope AI desktop applications._
