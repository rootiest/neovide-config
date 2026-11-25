# neovide-config

My [Neovide](https://neovide.dev) configuration, the GUI front end I use for
[my Neovim config](https://git.rootiest.dev/rootiest/neovim-config).

## Setup

```sh
git clone https://git.rootiest.dev/rootiest/neovide-config ~/.config/neovide
```

Needs Neovide 0.17+. Neovide reads `config.toml` at startup; restart it after
changes.

## Settings

| Key | Value | Why |
| --- | --- | --- |
| `startup-message-capture` | `false` | Neovide 0.17 attaches with `ext_messages` and `ext_cmdline` until it draws the first grid so it can capture startup messages. [noice.nvim](https://github.com/folke/noice.nvim) sets up during that window, sees the extensions enabled and refuses to load. Turning the capture off lets noice handle messages and the cmdline as usual. |

Settings that only apply inside Neovim (fonts, animations, `vim.g.neovide_*`)
live in the Neovim config instead.

## License

Released under the AGPL-3.0-or-later license. See [LICENSE](LICENSE).
