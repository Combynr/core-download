# combynr:core

combynr:core is a small, free app for running AI models on your own computer. It runs
GGUF models with llama.cpp, gives you a chat window in your browser, and lets the model use
a few basic tools. There is no online account and nothing to sign up for: you sign in with a
local password that never leaves your computer, and the app listens on `127.0.0.1` only.

It is also a quick way to find out what your hardware can run before you commit to anything
bigger.

## Download

Get the file for your computer from the [latest release](../../releases/latest):

| Your computer | File |
|---|---|
| Windows 10 or 11 (64-bit) | `combynr-core-<version>-windows-x64.zip` |
| Mac with Apple silicon (M1 or newer) | `combynr-core-<version>-macos-arm64.tar.gz` |
| Linux (64-bit) | `combynr-core-<version>-linux-x64.tar.gz` |

Each file has a `.sha256` file beside it, so you can check the download is intact.

## Run it

### Windows

1. Right-click the zip and choose **Extract All**.
2. Open the extracted folder and double-click **combynr-core.exe**.
3. If Windows shows "Windows protected your PC", click **More info**, then **Run anyway**.
   The app is not yet code-signed.
4. Your browser opens on combynr:core. Keep the black window open while you use it;
   close it to stop the app.

If the app reports a missing DLL when it starts a model, install the Microsoft Visual C++
Redistributable (x64) from Microsoft.

### macOS

1. Double-click the `.tar.gz` file to unpack it.
2. Open the folder, right-click **combynr-core** and choose **Open**, then **Open** again.
   macOS asks this once because the app is not yet notarised.
3. A Terminal window opens and your browser opens on combynr:core. Close the Terminal
   window to stop the app.

If macOS still refuses, open Terminal in that folder and run
`xattr -dr com.apple.quarantine .` once.

### Linux

```bash
tar -xzf combynr-core-*-linux-x64.tar.gz
cd combynr-core-*/
./combynr-core
```

Your browser opens on <http://127.0.0.1:8765/>. Press Ctrl+C in the terminal to stop.

## First run

1. Create your local account. It exists only on this computer.
2. Open **System check** to see what the app found: CPU, memory, GPU, disk and runtime.
3. Open **Models**. Import a `.gguf` file you already have, or paste a direct `https://`
   link to a `.gguf` file to download it. A small instruction-tuned model with tool support
   in a Q4 quantisation is a good first choice.
4. Start the model, then open **Chat**.
5. Open **Files** to see the working folder the model's file tools are limited to. Pick a
   folder made for this: the model can read and change any file in it without asking.

## What it does

- **Local models.** Import or download `.gguf` models, start and stop them, pick the context size.
- **Chat.** Streaming replies, saved chats, markdown.
- **Basic tools.** The model can list, read and write files in one working folder, and run
  Python in a restricted worker.
- **MCP servers.** Add Model Context Protocol servers. Their tools are checked with
  [mcp_auditor](https://github.com/Combynr/mcp_auditor) and you approve or deny them before
  the model can call anything. If a server changes its tools, it must be approved again.
- **Voice input.** Speech to text with whisper.cpp (included on Windows).
- **System check.** One page that shows what the app found.

The Upgrades page lists what the paid Combynr products add.

## Where your data is

Everything is kept in `~/.combynr-core` (`%USERPROFILE%\.combynr-core` on Windows): the
database, models and logs. To remove the app, delete its folder and that data folder.

## Security, plainly

- The app listens on `127.0.0.1` only and sends nothing to Combynr.
- File tools are confined to the one working folder you choose.
- Python that the model writes runs in a separate process with limits: a time limit, its
  own run folder, no network sockets, a cleared environment. **These are limits, not
  isolation and not a security boundary.** The code runs as your user.
- MCP servers are programs on your computer or services you connect to. The check is a
  heuristic and cannot prove a server is safe. Only add servers you trust.

Report a security problem privately: see [SECURITY.md](SECURITY.md).

## Known limits

- Model downloads inside the app do not use an HTTP proxy. Behind a proxy, download the
  `.gguf` file yourself and import it.
- On macOS the memory cap for sandboxed Python is not applied, because the system refuses
  it. The time limit and the other checks still apply.
- Voice input is included on Windows only; on macOS and Linux, install `whisper-cli`
  yourself and set its path in Settings.
- Builds are not yet code-signed.

## Licence

combynr:core is free to use, including at work. It is proprietary freeware: you may not
modify, resell, redistribute or reverse engineer it. See [LICENSE](LICENSE).
Third-party components keep their own open-source licences, see
[THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).

Questions and bug reports: [open an issue](../../issues).
