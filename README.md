# Vim Goodies

## Reindent all lines that are indented by only 1 space with 4 spaces:
```
:%s/\v^ ($|[^ ])/    \1/c
```
