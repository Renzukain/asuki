# asuki

A local AI assistant.

Status: planning. This repository does not yet contain a runnable assistant.

## First milestone: terminal conversation with a local model

A user starts asuki, sends a message, receives a response from a locally hosted model, and continues the conversation with context retained for the current session.

Use an existing local model server with an OpenAI-compatible chat API. Configure its URL and model name explicitly. The first version will not download models or start a model server. The implementation language and target operating system are not yet selected.

## Definition of done

- A fresh checkout can be installed and launched using documented commands on the selected target operating system.
- The user can configure the local server URL and model name without editing source code.
- A message receives a real response from the configured local model, without requiring a cloud service.
- Conversation history is sent with subsequent messages during the same session. Acceptance example: say "Remember the code word acorn", then ask "What code word did I give you?" and receive the remembered word.
- An unavailable server produces a readable error that identifies the configured address and suggests checking the server, rather than an unhandled traceback.
- The user can exit cleanly with an exit command or Ctrl+C.
- This README documents prerequisites, installation, launch, configuration, and the two-message acceptance example once those features exist.

The milestone is complete when all checks above pass against a real local model server. A mocked response alone does not establish completion.

## Scope boundaries

The first version has terminal text input and output, session-only conversation history, and one configured model. Voice, a graphical interface, persistent memory, file access, command execution, autonomous tasks, lamp integration, and video generation are deferred.

## Initial project structure

Only this README is needed during planning. Add source files and the runtime's dependency manifest when implementation begins. Add a focused automated check for conversation-history handling and connection errors if useful; keep the real-server acceptance check documented.

## Next implementation decision

Select the target machine and an existing local model server. That determines the installation instructions and a suitable runtime without adding speculative structure.
