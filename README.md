# Blow-Up

A dark color theme for VS Code / VSCodium, forked from
[Naysayer88](https://github.com/soulshined/Visual-Studio-Code-Naysayer88-Color-Theme)
by David Freer (MIT). Like the original, it is inspired by Jonathan Blow's EMACS UI.

## What this fork changes

- **Semantic highlighting is on** (`"semanticHighlighting": true`). The original
  ships without it, so LSP-provided types were dropped: `size_t` got colored by
  the TextMate grammar while your own `slot_handle` stayed plain. Custom types
  now match built-in ones.
- Types (`class`, `struct`, `enum`, `typeParameter`, `concept`) → `#9DE3C0`.
- Variables, parameters and fields pinned to `editor.foreground` (`#bdb395`) so
  enabling semantics doesn't recolor them.
- Control-flow keywords (`if`, `else`, `for`, `return`, ...) → `#cee5ed`,
  split out from the operator keywords, which stay `#CCC`.
- Strings → `#2c9e93`.
- Numeric literals → `#7edccd` (the original left them at the default foreground).
- Dropped the original's `contributes.configuration` block. It was malformed for
  current VS Code and never applied — see the settings recommendation below.

## Recommended settings

To get the original's intended feel, in your `settings.json`:

```json
{
    "editor.lineNumbers": "off",
    "editor.cursorStyle": "block"
}
```

## Download

Grab .vsix from the [**latest release**](https://github.com/Kecksohn/blow-up/releases/latest)


## Installation

### UI:
`Extensions` -> `...` -> `Install from VSIX` -> (Downloaded File)

### CLI:
```
codium --install-extension blow-up-*.vsix
```

Then pick **Blow-Up** via `Ctrl+K Ctrl+T`.

## Building

```
npx @vscode/vsce package
```

## Note

This is a UI color theme, not a complete syntax highlighter. It does not cover
every language's grammar.

## License

MIT. See [LICENSE](LICENSE) — copyright retained from the upstream project.
