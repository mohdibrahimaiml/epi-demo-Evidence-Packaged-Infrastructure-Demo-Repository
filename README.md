# EPI Demo Repository

Welcome! This repository contains example `.epi` recordings that demonstrate the Extended Prompt Interaction (EPI) format.

## What is EPI?

EPI (Evidence Packaged Infrastructure) is a universal recording layer for AI systems. It captures and packages every model interaction, code execution, and context snapshot into a single verifiable file — creating a permanent, auditable record of how any AI decision was made.

**Status:** Prototype/proof-of-concept. Not yet a standardized format.

## Quick Start

### Try the Demo
```bash
# Clone this repo
git clone https://github.com/mohdibrahimaiml/epi-demo-Evidence-Packaged-Infrastructure-Demo-Repository.git
cd epi-demo-Evidence-Packaged-Infrastructure-Demo-Repository

# Run the demo (no dependencies needed)
python demo/api_demo.py

# Inspect output
cat demo_output_basic/steps.jsonl
cat demo_output_basic/environment.json
```

### Full Implementation
For the complete recorder with OpenAI integration, signing, and packaging:
- See [README_DEMO.md](./README_DEMO.md)
- Contact afridiibrahim41@gmail.com for NDA access

## Demo Files

### 🎯 [basic-usage/](./basic-usage)
Simple chat completion demonstrating core recording capabilities.
- Single API call
- Request/response capture
- Model configuration

### 🌊 [openai-streaming/](./openai-streaming)
Streaming chat completion with real-time token delivery.
- SSE stream capture
- Token-by-token replay
- Latency measurement

### 💬 [multi-turn/](./multi-turn)
Complete conversation with context and follow-ups.
- Multiple API calls
- Message history
- Conversation flow

## File Format

Each `.epi` file is a signed ZIP archive containing:
- `manifest.json` — Metadata and step sequence
- `steps/` — Individual interaction steps (requests/responses)
- `context/` — Environment and configuration data
- `signature.json` — Cryptographic signature (optional)

## Use Cases

- **Debugging**: Capture and replay failing interactions
- **Testing**: Regression tests from real interactions
- **Documentation**: Executable API examples
- **Auditing**: Compliance and quality assurance
- **Research**: Dataset collection and analysis

## Toolchain

```bash
# View recording
epi view my-file.epi

# Validate format
epi check my-file.epi

# Replay interaction
epi replay my-file.epi

# Compare recordings
epi diff file1.epi file2.epi
```

## Learn More

This is a proof-of-concept demo. For the full implementation (available under NDA):
- Contact: afridiibrahim41@gmail.com
- See: [PRIVATE_COMPONENTS.md](./PRIVATE_COMPONENTS.md)
- Architecture: [ARCHITECTURE.md](./ARCHITECTURE.md)

## Contributing

Found an issue or want to add more demos? Pull requests welcome!

## License

Demo files are provided as examples under CC0 (public domain).
