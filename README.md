# ez-chat

## Overview
A modular chat interface that supports both Claude and Ollama models, allowing seamless switching between the two based on configuration.

## Module Inputs
- **claude**: Boolean input to toggle between Claude (true) and Ollama (false) models
- **claude_api**: API key for Claude integration
- **prompt**: The text message/prompt to send to the AI model
- **system**: System prompt to set context for the AI conversation
- **chatlog**: JSON array containing the conversation history
- **temp**: Temperature parameter for controlling randomness in responses (default: 0.8)
- **tokens**: Maximum number of tokens for the response (default: 100)
- **model**: Model name for Ollama (default: "openhermes")

## Module Outputs
- **response**: The AI model's text response to the prompt
- **chatlog_**: Updated conversation history as a JSON array

## Notes
- If claude_api is not provided in the input, it will attempt to read from "data/CLAUDE_API" file
- The module automatically handles conversation state management and model switching
- When using Claude mode, requires a valid Claude API key
- When using Ollama mode, requires a local Ollama installation with the specified model
