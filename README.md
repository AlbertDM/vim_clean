# vim_clean
`vim_clean` expects to be a VIM text editor configuration for environments where internet is not an option and plugins can't be installed.

## Ctags
 
`~/workspace/: ctags -R`

* Specific location:
```
vim .vimrc
+++ set tags=~/workspace/tags
```
* General ctags:
```
vim .vimrc
:set tags=tags
```

`vim -t <tag name>` to open vim straight on the tag
`Ctrl+]` to jump to tag when over a word
`Ctrl+T` to pop back
`:tselect` or `:stselect` to open
`:tnext`, `:tprev` to go to next/prev tag finding
`:help tags` for more 🙂
 
podeis usar ctags -R desde distintas carpetas. Entonces, si en vimrc teneis :set tags=tags siempre buscara el archivo tags de la misma carpeta des de donde se ejecuta vim. El fichero tags es lo que genera ctags -R, logicamente se le puede cambiar el nombre y entonces seria :set tags=mytags
