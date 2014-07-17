1. **What's gotags**
    - An tool which can shows functions and structs in *.go file, with the help of tagbar

2. **How it works**
    - sorry, i don't know

3. **It works like**
    - ![Gotags in vim](https://github.com/tracymacding/tools/blob/master/pic/gotags.jpg)

4. **Setup**
    - Install tarr, using vundle
        - add "Bundle 'majutsushi/tagbar'" in vimrc(~/.vimrc)
        - open vim, run BundleInstall
    - Download and install gotags
        - go get github.com/jstemmer/gotags
    - Configure vimrc(~/.vimrc), like this  
    nmap <F8> :TagbarToggle<CR>  let g:tagbar_type_go = {   
    'ctagstype' : 'go',    
    'kinds'     : [  
    'p:package',  
    'i:imports:1',  
    'c:constants',  
    'v:variables',  
    't:types',  
    'n:interfaces',  
    'w:fields',  
    'e:embedded',  
    'm:methods',  
    'r:constructor',  
    'f:functions'  
    ],  
    'sro' : '.',  
    'kind2scope' : {  
    't' : 'ctype',  
    'n' : 'ntype'  
    },  
    'scope2kind' : {  
    'ctype' : 't',  
    'ntype' : 'n'  
    },  
    'ctagsbin'  : 'gotags',  
    'ctagsargs' : '-sort -silent'  
    }  

5. **Reference**
  - You can get more detailed info from below URL:
        - http://monnand.me/p/vim-golang-environment/zhCN/
