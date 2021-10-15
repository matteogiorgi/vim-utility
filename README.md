# vim-utility

A usefull collection of my vim utility functions.

Remember to add the following autogroup somewhere in your Vim configs (preferably inside `~/.vim/plugin/`) in order to make Vim run `launch()` function every time it tries to open a directory.

> FZF should be installed in oyur system for a optimal workflow.
> (check out my FZF config inside my [.dotfiles](https://github.com/matteogiorgi/.dotfiles/tree/master/fzf/.config/fzf) repo)

```
augroup shutuponopen
    autocmd!
    autocmd VimEnter * silent! autocmd! FileExplorer *
    autocmd BufEnter * call onopen#launch()
augroup END
```
