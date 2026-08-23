# automator-quick-actions

A collection of macOS Automator Quick Actions (Finder right-click actions) for common workflows.

## Prerequisites

- macOS (tested on 26.7 (25G220))
- [VSCodium](https://vscodium.com/) installed, with the `codium` CLI shim added to your PATH
  (in VSCodium: ⇧⌘P → **Shell Command: Install 'codium' command in PATH**)
- [LocalSend](https://localsend.org/) installed (Homebrew, App Store, or direct download)

## Installation

1. Download or clone this repo
2. Double-click the `.workflow` file(s) you want in Finder — macOS will prompt to install the Quick Action automatically
3. Alternatively, manually copy the `.workflow` folder(s) into `~/Library/Services/`
4. Right-click a file or folder in Finder → **Quick Actions** to find them

## Included Actions

### Open with VSCodium
Opens the selected folder in a new VSCodium window.

```bash
/opt/homebrew/bin/codium -n "$1"
```

### Share with LocalSend
Opens the selected file/folder with LocalSend, ready to send.

```bash
#!/bin/bash
open -a "LocalSend" "$1"
```

## Contributing

Pull requests welcome — add your own Quick Action alongside a short description and any prerequisites it needs.
