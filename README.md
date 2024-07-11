MAKE SCRIPTS
============

Some scripts to be run from makefiles.

## Help

copy-script

    Usage: copy-script [-fc] -d DIRECTORY FROM...
    
    Copy script adding "%copy%" to it's "#tags: " section. If
    it doesn't contain it prints a warning, can be skipped with "-f".
    
    If you specify "-c" then the copy will be done if the specified
    paths do exist.

make-h

    Usage: make-h ...
    
    ... init|i [c]    : Initialize/update Makefile.
    
    ... add BLKS...   : Add "go" block. (go, sh, license, man)
    ... update        : Update blocks.
    
    ... get VARIABLE : Get variable.
    ... chk TARGET   : Check the target is available.
    
    ... project      : Get PROJECT.
    ... version      : Get VERSION.

runit-h

    Usage: runit-h [-v][-D DESTDIR] ...
    
      -a NAME PROGRAM ARGS... : Create a normal waiting service.
    
    Create and manage services using runit.
    
    Platforms: Linux

systemd-h

    Usage: systemd-h [-v][-D DESTDIR][-d DESC] ...
    
      -a NAME PROGRAM ARGS... : Create a normal waiting service.
    
    Create and manage services using runit.
    
    Platforms: Linux

## Collaborating

For making bug reports, feature requests and donations visit
one of the following links:

1. [gemini://harkadev.com/oss/](gemini://harkadev.com/oss/)
2. [https://harkadev.com/oss/](https://harkadev.com/oss/)
