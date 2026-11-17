# Herdr app settings

Files for the Herdr app's settings folder, `~/.config/herdr-app`. The app reloads them while it runs.

| File | What it does |
| --- | --- |
| `programs.json` | Shows Claude Code with the orange Claude starburst and Codex with the green OpenAI logo, in the agents list, tabs and pane headers |
| `my-icons/` | The icons `programs.json` points to, from [LobeHub Icons](https://github.com/lobehub/lobe-icons) (MIT) |

## Install

Link the files into the app's folder:

```sh
ln -s "$PWD/app/programs.json" ~/.config/herdr-app/programs.json
ln -s "$PWD/app/my-icons" ~/.config/herdr-app/my-icons
```

Run these from the repository root. Move any existing `programs.json` or `my-icons` aside first.

## After editing

The app watches its own folder, so it doesn't see edits made here through the link. Touch the link to reload, or restart the app:

```sh
touch -h ~/.config/herdr-app/programs.json
```

## Undo

Delete the two links. The app goes back to its built-in icons.
