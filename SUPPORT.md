# Support

Welcome to Calliope AI support! We're here to help you get the most out of our desktop applications.

## Getting Help

### Quick Links

- **Discord Community**: [Join our Discord](https://discord.gg/Z9bbbE6hJv) - The fastest way to get help!
- **Documentation**: [docs.calliope.ai](https://docs.calliope.ai) - Comprehensive guides and tutorials
- **GitHub Issues**: [Report bugs or request features](../../issues)
- **Email Support**: support@calliope.ai

## Before Asking for Help

Please try these steps first:

1. **Check the Documentation**
   - Review the [README.md](README.md) for installation and configuration instructions
   - Check the [CHANGELOG.md](CHANGELOG.md) for known issues and recent changes

2. **Search Existing Issues**
   - Someone may have already reported your issue or asked your question
   - Search [GitHub issues](../../issues) for similar problems

3. **Try Basic Troubleshooting**
   - Restart the application
   - Check that you're using the latest version
   - Verify your system meets the minimum requirements
   - Check your internet connection (for AI features)

## How to Get Help

### Discord Community (Recommended)

Our Discord server is the **best place** to get quick help from both the community and the Calliope team.

**Join here**: https://discord.gg/Z9bbbE6hJv

**Channels:**
- `#general` - General discussion and questions
- `#calliope-ide` - IDE-specific questions and issues
- `#calliope-lab` - Lab-specific questions and issues
- `#installation-help` - Help with installation and setup
- `#ai-providers` - Questions about AI provider configuration
- `#show-and-tell` - Share your projects and workflows
- `#feature-requests` - Discuss potential new features
- `#security` - Security-related discussions

**Tips for getting good help on Discord:**
- Use the appropriate channel
- Provide clear details about your issue
- Include your OS, version, and error messages
- Be patient - community members respond when they can

### GitHub Issues

For **bugs, feature requests, or documentation issues**, please open a GitHub issue:

**[Create a new issue](../../issues/new/choose)**

We have templates for:
- 🐛 [Bug Reports](../../issues/new?template=bug_report.yml)
- 💡 [Feature Requests](../../issues/new?template=feature_request.yml)
- 📦 [Installation Issues](../../issues/new?template=installation_issue.yml)
- 📚 [Documentation Issues](../../issues/new?template=documentation.yml)

**When opening an issue, please include:**
- Application name and version
- Operating system and version
- Package format (zip, deb, exe, etc.)
- Clear description of the problem
- Steps to reproduce
- Error messages or logs
- Screenshots (if applicable)

### Email Support

For issues that require private communication, you can email:

**support@calliope.ai**

**Use email for:**
- Account or billing questions
- Private security concerns (use security@calliope.ai for vulnerabilities)
- Questions that contain sensitive information

**Response time:** We typically respond within 24-48 hours during business days.

## Common Issues

### Installation Problems

#### macOS: "Application cannot be opened"

**Problem**: macOS Gatekeeper blocks unsigned applications

**Solution**:
1. Right-click (or Control+click) the application
2. Select "Open" from the menu
3. Click "Open" in the dialog that appears

**Why**: Our applications are currently unsigned. This is not a security risk - it's a limitation we're working to resolve.

#### Windows: SmartScreen Warning

**Problem**: Windows SmartScreen shows "Windows protected your PC"

**Solution**:
1. Click "More info"
2. Click "Run anyway"

**Why**: Similar to macOS, our applications are currently unsigned.

#### Linux: Permission Errors

**Problem**: Cannot execute the application

**Solution**:
```bash
# For AppImage
chmod +x Calliope-*.AppImage

# For extracted binaries
chmod +x calliope-ide  # or calliope-lab
```

### Application Won't Launch

**Problem**: Application crashes or won't start

**Troubleshooting steps:**

1. **Check system requirements**
   - macOS 10.15+ (Catalina or later)
   - Windows 10 or later
   - Linux with glibc 2.28+ (Ubuntu 20.04+, Fedora 29+)

2. **Verify architecture match**
   - Apple Silicon Mac? Download ARM64 version
   - Intel Mac? Download x64 version
   - Check with: `uname -m` (macOS/Linux) or System Information (Windows)

3. **Check logs**
   - **macOS**: `~/Library/Logs/Calliope*/`
   - **Windows**: `%APPDATA%\Calliope*\logs\`
   - **Linux**: `~/.config/Calliope*/logs/`

4. **Free up disk space**
   - Ensure at least 2GB free space

5. **Try fresh install**
   - Uninstall completely
   - Remove configuration directory
   - Reinstall from latest download

### AI Features Not Working

#### API Key Issues

**Problem**: "API key invalid" or "Authentication failed"

**Solution**:
1. Verify your API key is correct
2. Check you have credits/quota with the provider
3. Ensure the API key has proper permissions
4. Try regenerating the API key

#### Connection Timeouts

**Problem**: "Request timeout" or "Connection failed"

**Solution**:
1. Check your internet connection
2. Verify firewall isn't blocking requests
3. Try a different AI provider
4. For Ollama: Ensure Ollama is running (`ollama serve`)

#### Rate Limiting

**Problem**: "Too many requests" or "Rate limit exceeded"

**Solution**:
- Wait a few minutes before trying again
- Check your provider's rate limits
- Consider upgrading your API plan
- Use a local model (Ollama) for unlimited requests

### Calliope AI Lab Specific

#### First Launch Takes Forever

**Problem**: Lab initialization takes several minutes on first launch

**Solution**: This is **normal**! The first launch initializes:
- Python environment
- PostgreSQL database
- Jupyter server

**Typical first-launch time**: 2-5 minutes

#### Database Connection Errors

**Problem**: "Cannot connect to database"

**Solution**:
1. Ensure PostgreSQL isn't already running on port 5432
2. Check `~/.calliope-lab/postgres/` permissions
3. Try resetting the database (will lose data):
   ```bash
   rm -rf ~/.calliope-lab/postgres/
   ```
4. Restart the application

#### Notebook Won't Run

**Problem**: Cells won't execute or kernel keeps restarting

**Solution**:
1. Check the kernel is running (top-right corner)
2. Try restarting the kernel
3. Check Python packages are installed
4. Look for error messages in the notebook output

## System Requirements Reminder

### Minimum Requirements

- **RAM**: 4GB (8GB recommended)
- **Storage**: 2GB free space
- **OS**:
  - macOS 10.15 (Catalina) or later
  - Windows 10 or later
  - Linux with glibc 2.28+ (Ubuntu 20.04+, Fedora 29+, Debian 10+)

### Recommended Requirements

- **RAM**: 16GB or more
- **Storage**: 10GB+ free space (especially for Lab)
- **Internet**: For AI provider API calls and extension downloads
- **Display**: 1920x1080 or higher resolution

## AI Provider Setup Help

### Getting API Keys

**OpenAI**
- Sign up: https://platform.openai.com/signup
- Get key: https://platform.openai.com/api-keys
- Pricing: Pay-as-you-go

**Anthropic (Claude)**
- Sign up: https://console.anthropic.com/
- Get key: Console → API Keys
- Pricing: Pay-as-you-go

**Google (Gemini)**
- Get key: https://aistudio.google.com/app/apikey
- Pricing: Free tier available

**Ollama (Local)**
- Install: https://ollama.ai/
- Free and runs locally
- Pull models: `ollama pull llama3.1`

### Configuring API Keys

**In Calliope AI IDE:**
1. Open the Calliope chat panel
2. Click the gear icon (⚙️)
3. Select your provider
4. Enter your API key
5. Select models

**In Calliope AI Lab:**
1. Open Chat Studio
2. Click Settings
3. Select provider and enter key
4. Choose your model

## Still Need Help?

If you've tried everything and still need help:

1. **Join Discord**: https://discord.gg/Z9bbbE6hJv
2. **Open an issue**: Include all troubleshooting steps you've tried
3. **Email us**: support@calliope.ai with detailed information

## Community Support

Remember, our community is here to help! Don't hesitate to:

- Ask questions on Discord
- Share your solutions to help others
- Contribute to documentation
- Report bugs you encounter

## Feedback

We're always looking to improve! If you have feedback about:

- Documentation
- Support resources
- Feature requests
- User experience

Please let us know via:
- Discord: https://discord.gg/Z9bbbE6hJv
- GitHub Issues: [Submit feedback](../../issues/new/choose)
- Email: support@calliope.ai

---

**Last Updated**: January 14, 2025

Thank you for being part of the Calliope AI community!
