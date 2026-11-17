# Herdr config

Free, open-source plugins and settings for [Herdr](https://herdr.dev/).

| Folder | For | What's in it |
| --- | --- | --- |
| [`plugins/`](plugins/) | Herdr TUI (`herdr`) | Plugins, each installable on its own |
| [`app/`](app/) | Herdr app (`herdr-app`) | Settings files to link into `~/.config/herdr-app` |

## Plugins

These run in the Herdr TUI's plugin system. The Herdr app and herdr-core don't load them.

| Plugin | What it does | Install |
| --- | --- | --- |
| [Ambient Sound](plugins/herdr-sound/) | Quiet thinking pulse, tool-call tink, and completion chime for Claude Code and Codex on macOS | `herdr plugin install programmarchy/herdr-config/plugins/herdr-sound` |
| [Email Bridge](plugins/herdr-email/) | Forward authenticated AgentMail messages to a Herdr workspace/tab | `herdr plugin install programmarchy/herdr-config/plugins/herdr-email` |

After installing Ambient Sound, run `herdr plugin action invoke programmarchy.ambient-sound.configure` to add the agent tool hooks. See its [README](plugins/herdr-sound/README.md) for options and uninstall instructions.

Email Bridge also needs one AgentMail inbox and private setup before its listening pane starts. See its [README](plugins/herdr-email/README.md).

If you installed a plugin from the old `programmarchy/herdr-plugins/<plugin>` path, uninstall it and install it again from the path above. `herdr plugin update` can't follow the move.

## App settings

See [`app/README.md`](app/README.md).

## License

[MIT](LICENSE). The icons in `app/my-icons/` come from [LobeHub Icons](https://github.com/lobehub/lobe-icons) (MIT); see [`app/my-icons/LICENSE-LobeHub.txt`](app/my-icons/LICENSE-LobeHub.txt).
