seq2gif
=======
[![Build Status](https://travis-ci.org/saitoha/seq2gif.svg?branch=master)](https://travis-ci.org/saitoha/seq2gif)


Description
------------

This software converts a sequences record file generated by [ttyrec](https://github.com/mjording/ttyrec)
into a gif animation directly using portable built-in terminal emulation engine originated
from [yaft](https://github.com/uobikiemukot/yaft).
[yaft](https://github.com/uobikiemukot/yaft) provides rare terminal emulation
features such as SIXEL/DRCS.


Demo
----

This demo plays [sl](https://github.com/mtoyoda/sl) and records it with [ttyrec](https://github.com/mjording/ttyrec), and
converts that record into a GIF animation using seq2gif,
and converts that GIF into a SIXEL animation and plays it with [img2sixel](https://github.com/saitoha/libsixel#img2sixel).
Furthermore, generates the log record of above experience using [ttyrec](https://github.com/mjording/ttyrec), and
converts that log into the following GIF animation.

![ttyrec](https://raw.githubusercontent.com/saitoha/seq2gif/master/images/ttyrec.gif)


Build and Install
-----------------

```
  $ ./configure
  $ make
  # make install
```


Usage
-----

```
Usage: seq2gif [Options] < ttyrecord > record.gif

Options:
-w WIDTH, --width=WIDTH               specify terminal width in cell size
                                      (default: 80)
-h HEIGHT, --height=HEIGHT            specify terminal height in cell size
                                      (default: 24)
-l DELAY, --last-frame-delay=DELAY    specify delay in msec which is added
                                      to the last frame(default: 300)
-f COLORNO --foreground-color COLORNO specify foreground color palette
                                      number
-b COLORNO --background-color COLORNO specify background color palette
                                      number
-c COLORNO --cursor-color COLORNO     specify cursor color palette
                                      number
-t TABSTOP --tabstop TABSTOP          specify hardware tabstop(default: 8)
-H, --help                            show help
-V, --version                         show version and license information
```


Acknowledgements
----------------

### recterm

This program is derived from [recterm](https://github.com/uobikiemukot/recterm)
written by haru <uobikiemukot at gmail dot com> (@uobikiemukot)

### gifsave89

GIF encoder (gifsave89.c) is imported from [gifsave89](http://www.forkosh.com/gifsave90.html)
distributed under GPLv3+ by [John Forkosh Associates, Inc.](http://www.forkosh.com)(john@forkosh.com)

### milkjf
This package includes a C header file derived from milkjf font(gryph/milkjf.h).
Original milkjf font was designed by japanfarm (Nihon-Nouen) and used on Sharp X68000 series.
Chisato Yamauchi converted milkjf font to bdf for X Window System.
haru(@uobikiemukot) converted it to a C-styled header file.

### M+ BITMAP FONTS
This package includes a C header file derived from M+ font(gryph/mplus.h).

Original License:

```
M+ BITMAP FONTS            Copyright 2002-2005  COZ <coz@users.sourceforge.jp>

LICENSE

These fonts are free softwares.
Unlimited permission is granted to use, copy, and distribute it, with
or without modification, either commercially and noncommercially.
THESE FONTS ARE PROVIDED "AS IS" WITHOUT WARRANTY.
```

### Markus Kuhn's wcwidth
This package includes Markus Kuhn's wcwidth(mk_wcwidth)

```
Markus Kuhn -- 2007-05-26 (Unicode 5.0)

Permission to use, copy, modify, and distribute this software
for any purpose and without fee is hereby granted. The author
disclaims all warranties with regard to this software.

Latest version: http://www.cl.cam.ac.uk/~mgk25/ucs/wcwidth.c
```

References
----------

### ttyrec

a tty recorder

    http://0xcc.net/ttyrec/index.html.en

### yaft

Yet another framebuffer terminal

    http://uobikiemukot.github.io/yaft/


License
-------

![GPLv3](https://raw.githubusercontent.com/saitoha/seq2gif/master/images/gplv3.png)

