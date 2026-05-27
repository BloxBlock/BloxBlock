# BloxBlock

**Visual scripting tool for Roblox that generates real Lua code**

BloxBlock is a browser-based visual scripting platform that helps users build Roblox game logic using blocks (similar to Scratch), while generating real Lua code that can be used directly in Roblox Studio.

👉 https://bloxblock-app.web.app

---

## 🎯 Purpose

Many beginners struggle with learning Roblox scripting due to:

- Lua syntax complexity
- Lack of understanding of game logic structure
- Over-reliance on copy-pasted scripts

BloxBlock aims to solve this by making logic visual, while still exposing the real Lua code behind it.

---

## 🚀 Key Features

- 🧩 Visual scripting system powered by Blockly
- ⚡ Real-time Lua code generation
- 🔁 Bidirectional highlight (blocks ↔ generated code)
- 🎮 Pre-built game templates (Obby, Tycoon, Combat, Clicker)
- 💾 Cloud saving with Firebase
- 👤 User authentication system
- 🧩 Custom block creation system
- 🌐 Multi-language support (English / Spanish)

---

## 🎬 How it works

1. Open the editor
2. Drag and connect logic blocks
3. See Lua code generated in real time
4. Copy the code into Roblox Studio
5. Run your game instantly

Example flow:


Player joins → Give coins → Show message → Update stats


---

## 🧠 Core idea

BloxBlock is not meant to replace coding.

It is designed to:

> Help users understand how visual logic maps to real Lua scripting, making the transition to code easier and more intuitive.

---

## 🛠 Tech Stack

- Frontend: HTML, CSS, JavaScript (Vanilla)
- Block engine: Blockly 10.4.3
- Code generation: Lua generator system
- Backend: Firebase Authentication
- Database: Firestore
- Hosting: Firebase Hosting
- Internationalization: Custom i18n system

---

## 🧱 System Overview

### Block System
- Event-based logic (PlayerAdded, Touched, ClickDetector, etc.)
- Variables with optional global scope (_G support for cross-event logic)
- Game mechanics modules (combat, economy, UI, world manipulation)

### Templates
Includes working pre-built systems:

- 🎯 Obby (checkpoints, lava, platforms)
- 💰 Clicker (currency + multipliers)
- ⚔️ Combat Arena (weapons, damage zones, respawn system)
- 🏭 Tycoon (income, upgrades, rebirth system, saving/loading)

### Data System
- Persistent saving using Firestore
- Auto-save on change, tab close, and intervals
- Project sharing with public links

---

## 🧪 Example

lua
-- Generated Lua example

game.Players.PlayerAdded:Connect(function(player)
    local coins = Instance.new("IntValue")
    coins.Name = "Coins"
    coins.Value = 0
    coins.Parent = player
    coins.Value = coins.Value + 10
end)
📦 Project Structure
/editor        → Blockly editor logic
/blocks        → Custom block definitions
/generator     → Lua code generator
/templates     → Prebuilt game templates
/firebase      → Auth + database logic
/public        → Web frontend
📈 Roadmap
Better Lua debugging tools
AI-assisted block suggestions
Multiplayer collaborative editing
Mobile optimization
More advanced Roblox systems templates
💬 Feedback

This project is still evolving, and feedback is highly appreciated.

If you're a developer or Roblox creator:

What would make this useful in your workflow?
What is missing for you to actually use this in real projects?
🔗 Links
Live app: https://bloxblock-app.web.app
GitHub: (add repo link here)
