# dsh-emoji-picker

DeepSeek Harness plugin: adds an emoji quick-button to the chat input toolbar (the row with the model selector). Click **😊** to pick from 8 categories (~1870 base emoji); a click inserts the emoji at the end of your draft. Click anywhere outside the panel to dismiss it.

Data source: [`@emoji-mart/data`](https://github.com/missive/emoji-mart) (MIT, full Unicode set), embedded into the plugin itself by official category — no disk files or network requests at runtime.

## Features

- A 😊 button appears at the **left end** of the input bar (next to the attachment control)
- The panel switches between **text category tabs**: Smileys & People / Animals & Nature / Food & Drinks / Activities & Events / Travel & Places / Objects / Symbols / Flags
- Click a category and the grid below shows all emoji in that category; click one to insert it at the end of your draft
- **Clicking anywhere outside the panel** closes it automatically (you can also click × or press the button again)

## Install

```bash
dsh plugin --profile web add github:Arthu77/dsh-emoji-picker
```

Takes effect after restarting `dsh web`. If your profile name isn't `web`, replace `--profile web` with your profile name.

> ⚠️ On this machine (Windows), if `pnpm` reports `EPERM` when installing from a git repo, install manually: extract the repo's `tar.gz`, copy the whole folder to `<profile>/node_modules/dsh-emoji-picker`, then add `- insert: { - id: emoji-quick, name: 'dsh-emoji-picker' }` to `<profile>/cordis.patch.yml`, and restart.

## Screenshot

![Panel Demo](ScreenShot.png)

## License

MIT
