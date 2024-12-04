# 🌩️ Shiden - Simplify Command-Line Magic!

**Shiden** (_紫電_, meaning "Purple Lightning") is a sleek abstraction over the [Commander.js](https://github.com/tj/commander.js) library, designed to make building and managing CLI tools delightful, dynamic, and lightning-fast ⚡.

<p align="center">
  <img src="https://raw.githubusercontent.com/AdiPat/shiden/refs/heads/main/assets/shiden_logo.png" />
</p>

Whether you're writing your first CLI or looking to level up your command-line workflows, **Shiden** brings simplicity, power, and innovation to the table.

---

## ✨ Features

- 🔥 **Starter Code Generator**: Bootstrap your CLI project with starter code and tests from a config file.
- 🚀 **Dynamic Updates**: Update your config file, re-run the tool, and watch your code evolve in real-time.
- 📦 **Abstractions Made Simple**: Expose clean APIs for common Commander.js functionality, making your code more intuitive.
- 🤖 **AI-Generated Help**: Automatically generate beautiful, human-friendly help sections with AI.
- 🛠️ **Extend with Ease**: Add arguments, options, and commands dynamically with minimal boilerplate.
- 📈 **Powerful Yet Simple**: Build scalable CLI tools without getting lost in complexity.

---

## 📄 Installation

Install Shiden via npm:

```bash
npm install --save shiden
```

---

## 🚀 Getting Started

### Example Config File (`shiden.config.json`)

Define your CLI using a simple JSON configuration:

```json
{
  "name": "mycli",
  "version": "1.0.0",
  "description": "My Awesome CLI Tool",
  "commands": [
    {
      "name": "greet",
      "description": "Greet someone with a friendly message",
      "options": [
        {
          "flag": "-n, --name <name>",
          "description": "The name of the person to greet"
        }
      ]
    }
  ]
}
```

### Generate Starter Code

Run the CLI generator:

```bash
npx shiden init
```

This creates your CLI project structure:

```
.
├── src/
│   ├── index.js
│   ├── commands/
│   │   └── greet.js
├── test/
│   └── greet.test.js
├── package.json
└── shiden.config.json
```

### Dynamic Updates

Update `shiden.config.json` and re-run:

```bash
npx shiden update
```

Shiden dynamically updates your CLI codebase, adding new commands, options, or arguments.

---

## 🔧 Usage

After generating your CLI, you can run it directly:

```bash
node src/index.js greet -n "Aditya"
```

Output:

```
Hello, Aditya! 👋
```

---

## 🛠️ API

### `shiden.init()`

Generates starter code from a config file.

- **Usage**:
  ```bash
  npx shiden init
  ```

### `shiden.update()`

Dynamically updates the CLI project based on the updated config file.

- **Usage**:
  ```bash
  npx shiden update
  ```

### `shiden.addAIHelp()`

Adds an AI-generated help section to your CLI commands.

- **Usage**:
  ```javascript
  const { addAIHelp } = require("shiden");
  addAIHelp(command, {
    aiKey: "your-ai-api-key",
    context: "Generate a friendly description for a command.",
  });
  ```

### `shiden.exposeCommonAPIs()`

Simplifies common Commander.js functionality like adding commands, options, and arguments.

- **Usage**:

  ```javascript
  const { exposeCommonAPIs } = require("shiden");
  const cli = exposeCommonAPIs();

  cli
    .command("sayhello")
    .description("Print a hello message")
    .action(() => console.log("Hello from Shiden!"));
  ```

---

## 🎯 Why Shiden?

Shiden isn't just a wrapper over Commander.js — it's a complete toolkit for developers who value simplicity, productivity, and creativity. Build smarter, better, and faster CLI tools.

---

## 🏗️ Contributing

We love contributions! Open issues, suggest features, or submit PRs to make Shiden even better.

---

## 💖 Thanks to Commander.js

A huge shoutout to [Commander.js](https://github.com/tj/commander.js), the backbone of Shiden. 🚀

---

## 📜 License

Licensed under the [MIT License](./LICENSE).

---

> 🌩️ **Shiden** – Lightning-fast CLI development, reimagined.
