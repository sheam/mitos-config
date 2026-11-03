# mitos-config

My configuration for the [Mitos](https://mitos.computer) editor: keybindings, editor settings, language servers, snippets and a custom theme.

## Install Mitos

Follow the install guide first: <https://mitos.computer/docs/install>

## Using this config

Mitos reads its configuration from `~/.config/mitos`. Clone this repo there:

```sh
# back up any existing config first
[ -d ~/.config/mitos ] && mv ~/.config/mitos ~/.config/mitos.bak

git clone https://github.com/sheam/mitos-config.git ~/.config/mitos
```

Restart Mitos (or open a new session) to pick up the changes.

## Contents

| Path | Purpose |
|------|---------|
| `config.toml` | Editor settings, keybindings, statusline, theme selection |
| `languages.toml` | Language server and per-language settings (Go, TypeScript/TSX) |
| `snippets/` | Native snippets for Go, TypeScript and TSX |
| `themes/focus_nova.toml` | The `focus_nova` theme, enabled in `config.toml` |

## Customizing

- **Theme:** change `theme = "focus_nova"` in `config.toml`.
- **Keybindings:** edit the `[keys.normal]` section. Defaults here: `C-h`/`C-left` previous buffer, `C-l`/`C-right` next buffer, `C-q` close buffer.
- **Language servers:** install the servers referenced in `languages.toml` (e.g. `go install golang.org/x/tools/gopls@latest` for Go) and make sure they are on your `PATH`.
