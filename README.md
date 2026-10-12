# REAL Jellybeans

**English** | [한국어](README.ko.md)

A dark VS Code theme that stays as close as possible to the colors of [nanotech/jellybeans.vim](https://github.com/nanotech/jellybeans.vim).

## How it differs from the existing Jellybeans theme (DimitarNonov)

- **The 16 terminal colors are actually distinct.** The existing theme sets `ansiBlack` and `ansiWhite` to the same color (`#e8e8d3`), and every Bright color equals its normal counterpart, which breaks tmux status bars, htop, fzf, and similar tools.
- **Syntax colors follow the vim highlight groups.** Type `#ffb964`, Structure/PreProc `#8fbfdc`, StorageClass `#c59f6f`, Delimiter `#668799`, StringDelimiter `#556633`, Identifier `#c6b6ee`, Title `#70b950`, and so on.
- **UI color bugs are fixed.** Swapped info/warning notification icon colors, green warnings, a status bar that does not change while debugging, and nearly invisible selection and current-line highlights.

## Palette

| vim group | Color | Used for in VS Code |
| --- | --- | --- |
| Normal | `#e8e8d3` / bg `#151515` | Default text and background |
| Comment | `#888888` italic | Comments |
| Constant | `#cf6a4c` | Numbers, constants, booleans |
| String | `#99ad6a` | Strings |
| StringDelimiter | `#556633` | Quotes |
| Special | `#799d6a` | Escapes, entities |
| Identifier | `#c6b6ee` | self/this, string interpolation |
| Statement | `#8197bf` | Keywords, tags |
| Structure / Operator / PreProc | `#8fbfdc` | Operators, class/struct, imports, decorators |
| StorageClass | `#c59f6f` | Modifiers such as static/const, CSS properties |
| Type | `#ffb964` | Types, class names |
| Function | `#fad07a` | Functions |
| Delimiter | `#668799` | Brackets, separators |
| Title | `#70b950` bold | Markdown headings |

jellybeans.vim does not define a 16-color terminal palette. The 8 normal colors are taken from the palette above, and the 8 Bright colors are each normal color mixed 30% toward white. Black is `#3b3b3b` so it stays distinct from the background, and bright black is the comment color `#888888`.

## Installation

Download the `.vsix` from [Releases](https://github.com/Zachary-Lee-Jaeho/vscode-REAL-jellybeans-theme/releases), then:

```sh
code --install-extension real-jellybeans-theme-<version>.vsix
```

Or build it yourself:

```sh
npx @vscode/vsce package
code --install-extension real-jellybeans-theme-*.vsix
```

Then pick **REAL Jellybeans** from `Preferences: Color Theme`.

## License

MIT. The color palette comes from [jellybeans.vim](https://github.com/nanotech/jellybeans.vim) by NanoTech, also MIT licensed.
