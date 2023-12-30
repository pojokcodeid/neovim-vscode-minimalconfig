# NEOVIM - VSCODE CONFIG GUIDE

## Installation

### Install Neovim Debian Based

1. Install Snap

- https://snapcraft.io/docs/installing-snap-on-debian

```bash
sudo apt update
sudo apt install snapd
sudo snap install core
snap --version
```

2. Install Neovim

- https://snapcraft.io/nvim

```bash
sudo snap install nvim --classic
snap list
nvim -v
```

### Install Visual Studio Code

Download and install Visual Studio Code

- https://code.visualstudio.com/docs/setup/linux <br>

```bash
sudo dpkg -i code_1.53.2-1584973000_amd64.deb
```

Other installation options:

```bash
sudo snap install --classic code
code --version
```

### Install Visual Studio Code Extensions

- https://marketplace.visualstudio.com/items?itemName=PojokCode.pcode-icon
- https://marketplace.visualstudio.com/items?itemName=PojokCode.pcode-theme
- https://marketplace.visualstudio.com/items?itemName=asvetliakov.vscode-neovim
- https://marketplace.visualstudio.com/items?itemName=VSpaceCode.whichkey

### Configuration

#### settings.json

```json
{
  "workbench.iconTheme": "pcode-icon-theme-dark-spesifik",
  "workbench.productIconTheme": "fluenticon",
  "workbench.colorTheme": "Jetbrains Dracula Theme",
  "window.titleBarStyle": "custom",
  "workbench.editor.enablePreview": false,
  "window.commandCenter": false,
  "editor.minimap.renderCharacters": false,
  "window.menuBarVisibility": "compact",
  "workbench.activityBar.location": "top",
  "extensions.experimental.affinity": {
    "asvetliakov.vscode-neovim": 1
  }
}
```

Complete configuration check the file `settings.json`

#### keybindings.json

```json
[
  {
    "key": "space",
    "command": "whichkey.show",
    "when": "!whichkeyActive && neovim.mode == 'normal'"
  },
  {
    "key": "space",
    "command": "whichkey.show",
    "when": "sideBarFocus && !inputFocus && !whichkeyActive"
  }
]
```

Complete configuration check the file `keybindings.json`
