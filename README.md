# Kifer Admin Framework

Kifer is a lightweight, fast, and customizable admin system framework for Roblox developers who want full control without unnecessary bloat. Instead of forcing you into a pre-built UI or a specific command setup, Kifer lets you build your own admin experience exactly how you want it.

> [!NOTE]
> Kifer is a framework, not a finished admin panel. You choose the UI, layout, and workflow.

## Features
- **Modular Command System** – Easily add, remove, or modify commands.
- **Flexible Permissions** – Supports player-based, group-rank-based, or custom logic.
- **UI-Agnostic** – Works with any UI framework or custom interface.
- **Secure and Server-Sided** – Designed to prevent exploit misuse.
- **Lightweight** – Minimal overhead and optimized execution path.

> [!TIP]
> If you already use a custom UI library or toolkit, Kifer integrates without forcing design changes.

## Purpose
Many admin systems are bulky, locked down, or visually opinionated.  
Kifer focuses on the core engine:

- Permission tiering
- Command registration and execution
- Networking and event flow

You create the admin system that fits your game's style and needs.

> [!IMPORTANT]
> Kifer is intended for developers who want customization and control. This is not a drag-and-drop admin panel.

## Installation

Place Kifer in `ServerScriptService` or another secure server container:

```lua
local Kifer = require(path.to.Kifer)

Kifer.RegisterCommand("kick", function(sender, target, reason)
    target:Kick(reason or "Removed from the server.")
end, {
    Permission = "Moderator"
})
