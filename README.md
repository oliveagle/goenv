# goenv - Set up a Golang environment

I got tired of manually setting my GOPATH when I went from one project to another,
so I wrote a small utility to set up my environment for me. It is similar in spirit to Python's
`virtualenv`, though it does less, and does it a little differently.

The main difference is that instead of an 'activate' script that sets up your environment,
this opens up a new subshell for you to work in. It will also download
and install the version of Go that you want it to.

**NOTE**: I do not have a Mac to test this on. I know it works on Linux, and
I _think_ it will work on OSX, but I'm not sure. If you want to test it,
and maybe send me a pull request to fix any issues you find, I would
appreciated it.

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
