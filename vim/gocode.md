1. **What's gocode**
    - An autocompletion daemon for the Go programming language.Gocode is a helper tool which is intended to be integrated with your source code editor, like vim and emacs. It provides several advanced capabilities, which currently includes:

2. **How it works**
    - It is called *daemon*, because it uses client/server architecture for caching purposes. In particular, it makes autocompletions very fast. Typical autocompletion time with warm cache is 30ms, which is barely noticeable.

3. **It works like**
    - You can watch the [demo screencast](http://nosmileface.ru/images/gocode-demo.swf).
    - ![Gocode in vim](http://nosmileface.ru/images/gocode-screenshot.png)

4. **Setup**
    - Intall go and set GOPATH & GOROOT, for example, my typcial seeting
        - GOPATH: /styx/home/hzdingkai2013/workspace/go_project
        - GOROOT: /styx/home/hzdingkai2013/workspace/go

    - Download and install godoc
        - go get -u github.com/nsf/gocode (-u flag for "update")
        - Install official Go vim scripts from **$GOROOT/misc/vim**. If you did that already, proceed to the step next
        - Install gocode vim scripts. Usually it's enough to do the following:
            - cd $GOPATH/src/github.com/nsf/gocode/vim
            - ./update.bash
            - gocode set propose-builtins true
            - gocode set lib-path "/home/border/gocode/pkg/linux_amd64"(optional)
    - Configure vimrc(~/.vimrc)
        - syntax on 
        - filetype plugin on
        - filetype plugin indent on
        - set ofu=syntaxcomplete#Complete
        - imap <silent> ` <C-X><C-O>

5. **Reference**
  - You can get more detailed info from below URL:
        - https://github.com/tracymacding/tools/blob/master/vim/gocode.md
        - http://blog.5d13.cn/resources/goweb/01.4.html
        - http://www.xiaozhou.net/setup-golang-environment-for-vim-2014-01-25.html
        - http://blog.hsatac.net/2013/08/my-vimrc-for-golang/
        - http://my.oschina.net/goskyblue/blog/192647
