# Bastion - Real-Time Monitoring of Risks in Agents

Powered by takara.ai's ds-1, a high-performance low latency embedding model.
Forked original repo to train a transformer classifier for risk detection over actions rather than LLM for extra speed. 
Here was the first repo (made during the hack): https://github.com/cappuch/antislopfactory

## Features
- Tool-level Risk Classification
- Token-Level Risk classification
- Tool Usage Tracking 
- Human-in-the-loop Approval System
- Comprehensve logging/monitoring
- User-friendly Interface for Managing Tools and Approvals

![safety classifier](data/safety_classifier.png)

## Tool Classification Categories
- safe: tools that are sandboxed, read-only, or have limited capabilities (e.g., running Lua/Python in a sandbox, simple calculations)
- approval_required: tools that can modify the system but require human review (e.g., file operations that can delete/write files, modify configs)
- unsafe: tools that can execute arbitrary/untrusted code, access sensitive data, or perform operations that could compromise the system
