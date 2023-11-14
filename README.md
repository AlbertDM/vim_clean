# vim_clean
`vim_clean` expects to be a VIM text editor configuration for environments where internet is not an option and plugins can't be installed.

## Options intended

```
vim --version
VIM - Vi IMproved 7.4 (2013 Aug 10, compiled Sep 30 2020 08:08:00)
Included patches: 1-207, 209-629
Modified by <bugzilla@redhat.com>
Compiled by <bugzilla@redhat.com>
Huge version without GUI.  Features included (+) or not (-):
+acl             +farsi           +mouse_netterm   +syntax
+arabic          +file_in_path    +mouse_sgr       +tag_binary
+autocmd         +find_in_path    -mouse_sysmouse  +tag_old_static
-balloon_eval    +float           +mouse_urxvt     -tag_any_white
-browse          +folding         +mouse_xterm     -tcl
++builtin_terms  -footer          +multi_byte      +terminfo
+byte_offset     +fork()          +multi_lang      +termresponse
+cindent         +gettext         -mzscheme        +textobjects
-clientserver    -hangul_input    +netbeans_intg   +title
-clipboard       +iconv           +path_extra      -toolbar
+cmdline_compl   +insert_expand   +perl            +user_commands
+cmdline_hist    +jumplist        +persistent_undo +vertsplit
+cmdline_info    +keymap          +postscript      +virtualedit
+comments        +langmap         +printer         +visual
+conceal         +libcall         +profile         +visualextra
+cryptv          +linebreak       +python/dyn      +viminfo
+cscope          +lispindent      -python3         +vreplace
+cursorbind      +listcmds        +quickfix        +wildignore
+cursorshape     +localmap        +reltime         +wildmenu
+dialog_con      -lua             +rightleft       +windows
+diff            +menu            +ruby/dyn        +writebackup
+digraphs        +mksession       +scrollbind      -X11
-dnd             +modify_fname    +signs           -xfontset
-ebcdic          +mouse           +smartindent     -xim
+emacs_tags      -mouseshape      -sniff           -xsmp
+eval            +mouse_dec       +startuptime     -xterm_clipboard
+ex_extra        +mouse_gpm       +statusline      -xterm_save
+extra_search    -mouse_jsbterm   -sun_workshop    -xpm
```

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
