# Bastion - Real-Time Monitoring of Risks in Agents

Powered by takara.ai's ds-1, a high-performance low latency embedding model.
Modified our repo slightly to train a transformer classifier for risk detection over actions rather than LLM. First repo made during the hack: https://github.com/cappuch/antislopfactory

## Features
- tool-level classification
- message-level safety classification
![safety classifier](data/safety_classifier.png)
- tool usage tracking
- human-in-the-loop approval system
- comprehensive logging and monitoring
- user-friendly interface for managing tools and approvals

## Tool Classification Categories
- safe: tools that are sandboxed, read-only, or have limited capabilities (e.g., running Lua/Python in a sandbox, simple calculations)
- approval_required: tools that can modify the system but require human review (e.g., file operations that can delete/write files, modify configs)
- unsafe: tools that can execute arbitrary/untrusted code, access sensitive data, or perform operations that could compromise the system
