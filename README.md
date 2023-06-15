# Vim Goodies

## Diff the current tab with the next one:
```
:execute 'vertical diffsplit ' . fnameescape(bufname(tabpagebuflist(tabpagenr()+1)[0]))
```
Slightly simpler, but leaves a global variable around:
```
let x = expand('%') | tabprev | execute 'vertical diffsplit ' . fnameescape(x)
```
In both versions, just to ":q" on the left window to exit the diff.

## Reindent all lines that are indented by only 1 space with 4 spaces:
```
:%s/\v^ ($|[^ ])/    \1/c
```
