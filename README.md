## Top Gists

#### Grill Me Skill Improved
https://gist.github.com/kuangyujing/117a84d60d1b70acc15bc0eaccb507d0

#### How to start tmux with attach if a session exists
https://gist.github.com/kuangyujing/5b0e16fb341ab4aaef2c4afeb287bf29

#### Create Service Principal for Dataverse
https://gist.github.com/kuangyujing/e63b18370a27bfad072e69244753f4f2

## Top Repos

#### [xfce4-terminal](https://github.com/dracula/xfce4-terminal)

Dark theme for xfce4-terminal

#### [html5.vim](https://github.com/kuangyujing/html5.vim)

Vim plugin for modern HTML5 syntax hightlight and indentation

#### [minimap.vim](https://github.com/kuangyujing/minimap.vim)

Blazing fast minimap / scrollbar for vim, powered by code-minimap written in Rust.

#### [power-platform-sdd](https://github.com/kuangyujing/power-plstform-sdd)

Spec-driven Development Kit for Power Platform

## CLAUDE.md Tips

Suppress emoji and ambiguous-width symbols
```
## Emoji/symbols
Scope: terminal chat, commit messages, PR titles/bodies. Exempt: emoji/symbols as data in code (regex/string literals).
- No emoji: U+231A-U+231B, U+2328, U+23CF, U+23E9-U+23F3, U+23F8-U+23FA, U+2600-U+27BF, U+2B00-U+2BFF, U+1F000-U+1FAFF; modifiers/joiners U+200D, U+FE0F, U+1F3FB-U+1F3FF, U+20E3. Status: [x] [ ] OK NG DONE.
- No ambiguous-width symbols (EAW=A): arrows U+2190-U+21FF, enclosed alphanumerics U+2460-U+24FF, geometric shapes U+25A0-U+25FF. Use ASCII.
- (1)(2)(3) or 1. 2. 3. for ① ② ③; * - + for ★ ☆ ● ○ ◆ ■ ▲.
- Box Drawing U+2500-U+257F: allowed.

```

## Memo

Delete all containers including its volumes and images
```sh
docker rm -vf $(docker ps -aq)
docker rmi -f $(docker images -aq)
```

Remove Claude Code Symbols that cause Tofu on macOS
```sh
sudo sed -i '' -e $'s/\u23F8//g' -e $'s/\u23F5\u23F5//g' -e $'s/\u21E2//g' /path/to/lib/node_modules/@anthropic-ai/claude-code/cli.js
```

Remove all UI indicators in Claude Code
```sh
# Replace /path/to/lib/node_modules with the actual path to your global node_modules directory
sudo sed -i '' -e $'s/\u23FA//g' -e $'s/\u23F8//g' -e $'s/\u23F5//g' -e $'s/\u21E2//g' -e $'s/\u2705//g' -e $'s/\u274C//g' -e $'s/\u26A0//g' /path/to/lib/node_modules/@anthropic-ai/claude-code/cli.js
```
