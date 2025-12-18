## Top Gists

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

## Memo

Delete all containers including its volumes and images
```sh
docker rm -vf $(docker ps -aq)
docker rmi -f $(docker images -aq)
```

Delete Claude Code Symbols that cause Tofu on macOS
```sh
sudo sed -i '' -e $'s/\u23F8//g' -e $'s/\u23F5\u23F5//g' -e $'s/\u21E2//g' /path/to/lib/node_modules/@anthropic-ai/claude-code/cli.js
```

Delete all UI indicators in Claude Code
```sh
sudo sed -i '' -e $'s/\u23FA//g' -e $'s/\u23F8//g' -e $'s/\u23F5//g' -e $'s/\u21E2//g' -e $'s/\u2705//g' -e $'s/\u274C//g' -e $'s/\u26A0//g' /usr/local/node/lib/node_modules/@anthropic-ai/claude-code/cli.js
```
