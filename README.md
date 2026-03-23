# zellij-zsh-completion

ZSH tab-completion for [zellij](https://zellij.dev) terminal workspace. Inspired by [conda-zsh-completion](https://github.com/conda-incubator/conda-zsh-completion).

**Note**: Mainly works for [oh-my-zsh](https://github.com/ohmyzsh/ohmyzsh/) as a custom plugin.

Features:

- Tab-completion for all zellij commands, subcommands, and options
- **Dynamic session completion**: `zellij attach [TAB]` lists active sessions for selection
- Also works with `kill-session` and `delete-session`
- Grouped command display (session / pane / config / misc)

## Installation

### Oh-My-Zsh

```zsh
git clone https://github.com/AlfredMoore/zellij-zsh-completion ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zellij-zsh-completion
```

Add it to your plugins in `~/.zshrc`:

```zsh
plugins=(... zellij-zsh-completion)
```

### Manual

Clone this repository:

```zsh
git clone https://github.com/AlfredMoore/zellij-zsh-completion ~/.zellij-zsh-completion
```

Add the following to your `~/.zshrc` **before** `compinit`:

```zsh
fpath+=~/.zellij-zsh-completion
autoload -Uz compinit && compinit
```


### Zim

Add the following to `~/.zimrc` **before** `zmodule completion`:

```zsh
zmodule AlfredMoore/zellij-zsh-completion
zmodule completion
```

Then run:

```zsh
zimfw install -v && exec zsh
```

## License

BSD-3-Clause
