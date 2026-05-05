# Go Runner — Downloads

A fast, native desktop app for running Go code snippets instantly — no project setup, no terminal.

This repository hosts the official downloadable installers for **Go Runner**. The source code lives elsewhere; this page exists so you can grab the app for your OS in one click.

---

## Download

**[→ Get the latest release](https://github.com/MrJSdev/go-runner-releases/releases/latest)**

Pick the file that matches your operating system and architecture:

| OS | Architecture | File |
|---|---|---|
| macOS | Apple Silicon (M1/M2/M3/M4) | `Go-Runner_<version>_aarch64.dmg` |
| macOS | Intel | `Go-Runner_<version>_x64.dmg` |
| macOS | Universal (both) | `Go-Runner_<version>_universal.dmg` |
| Windows | x86_64 | `Go-Runner_<version>_x64-setup.exe` or `.msi` |
| Linux | x86_64 (Debian/Ubuntu) | `go-runner_<version>_amd64.deb` |
| Linux | x86_64 (portable) | `go-runner_<version>_amd64.AppImage` |

---

## Requirements

Go Runner needs the **Go toolchain** installed on your machine to compile and run your code. If you don't have Go yet, install it from [go.dev/dl](https://go.dev/dl/) (version 1.21 or later).

The app auto-detects Go in these locations, so it works whether you launch from Finder, Spotlight, or the terminal:

```
/opt/homebrew/bin        Homebrew — Apple Silicon
/usr/local/bin           Homebrew — Intel
/usr/local/go/bin        Official Go installer
/opt/local/bin           MacPorts
~/go/bin                 GOPATH bin
~/.local/bin             User-local installs
```

---

## Install

### macOS

1. Download the `.dmg` for your chip (Apple Silicon or Intel — pick Universal if unsure).
2. Open the `.dmg` and drag **Go Runner** to your Applications folder.
3. **First launch:** because the app is not yet notarized by Apple, macOS may show *"Go Runner cannot be opened because the developer cannot be verified."* To bypass this:
   - **Right-click** the app in Applications → **Open** → **Open** in the dialog. *(Only needed on first launch.)*
   - Or run in Terminal: `xattr -d com.apple.quarantine "/Applications/Go Runner.app"`

### Windows

1. Download the `.exe` setup or `.msi` installer.
2. Run it. SmartScreen may show *"Windows protected your PC"* — click **More info** → **Run anyway**.
3. Follow the installer prompts.

### Linux

**Debian / Ubuntu (`.deb`):**
```bash
sudo dpkg -i go-runner_<version>_amd64.deb
```

**Portable (`.AppImage`):**
```bash
chmod +x go-runner_<version>_amd64.AppImage
./go-runner_<version>_amd64.AppImage
```

---

## What is Go Runner?

A notebook-style Go playground for your desktop:

- **Snippet mode** — write bare Go statements without `package main` or `func main()`. Auto-wrapped and compiled for you.
- **Inline output** — every `fmt.Print*` call shows its output as ghost text next to the line that produced it.
- **Third-party packages** — use any Go module; first-use prompts to `go get`, then caches.
- **Monaco editor** — VS Code-grade editor with Go autocomplete, snippets, and themes.
- **Resilient execution** — clean kill of infinite loops, panic stack traces, configurable timeouts, output limits.

---

## Issues & feedback

Found a bug or want to request a feature? Open an issue in this repo's [Issues tab](https://github.com/MrJSdev/go-runner-releases/issues).

---

## License

MIT
