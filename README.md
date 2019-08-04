# processing-export
ُA Java processing library to Export your artwork as PNG, SVG or PDF files with unique filenames (based on a prefix/sketch_name and current time). Heavily inspired from [fn](https://github.com/inconvergent/fn) library by Anders Hoff, and based on processing core [PDF](https://github.com/processing/processing/tree/master/java/libraries/pdf) and [SVG](https://github.com/processing/processing/tree/master/java/libraries/svg) libraries. 

ُThis library is handy for people who find it repetitive and annoying to name single file seperatly. At the end, it's all computer-generated, so why not computer-named too?

It will give you unique file names based on current git commit, as well as the
time and date. You can also set your own prefix and/or postfix.

It will generate unique filenames based on two components: either a chosen filename or sketch_name if not supplied with a filename and a time-date postfix: 

    {prefix} or {sketch-name}-yyyymmdd-hhmmss

For Example: 

    beginRecord(PNG, "filename") \\ filename-20190126-142138
    beginRecord(PNG)             \\ sketch_name-20190126-142138
    


## Install

The easiest is to install with:

    ./setup.py [install | develop] --user

Unfortunately the command line support relies on `entry_points`, which is
rather slow. To make it run faster you can (for instance) add a symlink in your
local `bin` folder to `./run.py` in this package.

