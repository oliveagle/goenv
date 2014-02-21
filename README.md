# goenv - Set up a Golang environment

I got tired of manually setting my GOPATH when I went from one project to another,
so I wrote a small utility to set up my environment for me. It is similar in spirit to Python's
`virtualenv`, though it does less, and does it a little differently.

The main difference is that instead of an 'activate' script that sets up your environment,
this opens up a new subshell for you to work in. It will also download
and install the version of Go that you want it to.


## Installation

It is a single Python script, so you can just make it executable and put
it somewhere in your path.

    # you might need to add --no-check-certificate to the wget command...
    $ wget -O ~/bin/goenv https://raw.github.com/pwoolcoc/goenv/master/goenv
    # for the love of pete, don't just run scripts you get from the internet, check them first!
    $ $EDITOR ~/bin/goenv
    $ chmod +x ~/bin/goenv

## Usage

    $ cd /path/to/project
    $ echo $GOPATH

    # simplest usage
    $ goenv
    (golang-1.2) $ echo $GOPATH
    /path/to/project:/path/to/project/pkg/somepkg

    # specify Golang version
    $ goenv --version 1.1
    (golang-1.1) $

## Contact

pwoolcoc@gmail.com
