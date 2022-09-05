# vim-esc-to-eng for macOS

## install
  
1. get source from  [input-source-switcher](https://github.com/vovkasm/input-source-switcher.git)  
  and build, install binaries.
2. add copy the code below to vimrc 

## or

1. clone repo to any location
2. copy <downloaded_repo>/lib/libInputSourceSwitcher.dylib to /usr/local/lib
3. copy <downloaded_repo>/bin/issw to /usr/local/bin
4. add to vimrc
```vimscript
let g:XkbSwitchLib="/usr/local/lib/libInputSourceSwitcher.dylib"
let g:imeoff="/usr/local/bin/issw com.apple.keylayout.ABC"
augroup IMEDisableGroup
  autocmd!
  autocmd InsertLeave * :call system(g:imeoff)
augroup END
```
