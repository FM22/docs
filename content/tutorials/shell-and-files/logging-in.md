---
title: "Using SSH to log in"
date: 2021-04-21T16:44:58+01:00
group: shell-and-files
layout: docs
toc: true
highlight: true
---

## Overview

Just as a butterfly emerges from its coccoon to explore the great
wonders of the world, you, too, will also uncover the great wonders of
Linux with the SRCF by your side. In this tutorial, we'll show you how
to log in to a UNIX-like shell and use the basics of the command line.

## Background

Much of the functionality offered by the SRCF is accessible via a
text-mode 'shell' interface on our server --- using this interface you
can manipulate files on your website directly, as well as running other
programs such as email software. When you get an SRCF account, you can
connect to the server and issue commands by typing them. If you're not
used to this, don't worry --- it's much less primitive than it sounds
and very powerful!

Because you are remotely accessing our servers, as opposed to your own computer, we will need a communication protocol. The most widely used one is called SSH, [secure shell protocol](https://en.wikipedia.org/wiki/Secure_Shell_Protocol).

## Logging in

### Linux or macOS

If you're running a Unix-based computer (including macOS) then logging
in is easy as it's built into the system:

1. Start your terminal
2. Type in `ssh <username>@shell.srcf.net`
3. Enter your password when prompted

{{< alert type="warning" >}}
You will not see your password as you type it. This is intentional!
{{<  /alert >}}

### Windows

If you're running a system without a native console, such as MS
Windows, then things are *slightly* trickier. Not much though, you just
have to go and get a console program. We recommend the PuTTY
application, downloadable for free
[here](https://www.chiark.greenend.org.uk/~sgtatham/putty/).

Once downloaded,

1. Run PuTTY
2. Enter the server name as `shell.srcf.net`, the protocol as SSH
    (port 22) and click to connect
3. Enter your username and SRCF password when prompted

{{< alert type="warning" >}}
Note that for obvious reasons your password will not be printed on the
screen. The password is case-sensitive, so make sure that caps lock is
not on if you are having problems.{{<  /alert >}}

## First steps

Now you're in! Let's see what this terminal is capable of!

Try running `ls`. You should see a bunch of text printed in the
terminal. These are your directories and files. By default, you start
out in your home directory once you log in. The absolute path is
`/home/CRSid`. You should, at minimum, see a `public_html` folder. As
you may have already discovered `ls` stands for list! You can pass in
additional flags to change its output: `ls -la`.

Now, try runnng `pwd`. This stands for *print working directory*. Think
of this as a street sign. Right now, you're somewhere in the middle of
complex and multi-layered file system on our shell server, which happens
to be your home directory. `pwd` tells you where you are in this
organized mess!

The last command we'll try is `cd public_html`. This **changes your
directory** to `public_html`. You're now on a different street!

The `public_html` directory is special. Any content placed here will be
served by our web server, Apache. Check out the tutorials to learn what
to do

{{< alert type="info" >}}
You can use `cd` with either absolute or relative paths.

`.` represents your current directory. So `cd .` should not do anything,
you can verify with `ls` or `pwd` to see if you're in the same
directory. If you want to move up a directory you can use `cd ..`.

If you want to go to your home directory you can use `cd ~`.

`~` has a special meaning like `..` does, it points to your home
directory. Can you guess what `cd ~/public_html` does? Try it out and
see if you were right!
{{<  /alert >}}

If you're interested in what else you can do with the shell, check out [our more advanced tutorial]({{< relref "/tutorials/shell-and-files/terminal-guide" >}}).

## Closing remarks

Did you like this or find this cool? We invite you to check out
[more tutorials]({{< relref "/tutorials" >}})
or [get in touch]({{< relref "/#help-and-support" >}}) to tell us what you thought!

If you have any suggestions for how we could improve this documentation
please send us an email at `support@srcf.net` or submit a Pull Request
on [GitHub](https://github.com/SRCF/docs)!
