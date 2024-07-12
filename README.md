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

json-cfg

    Usage: json-cfg ...
    
    Mechanism for forming configuration json files out of your local
    settings stored in "json-cfg__NAME" scripts.
    
    ## Defining settings:
    
      1. Write a script named "json-cfg__NAME".
      2. Add "--help" support to this script.
      3. Without arguments it should print testing settings.
    
    ## Searching settings.
    
      json-cfg -l      : List defined configuration script names.
      json-cfg -h NAME : Print configuration help.
    
    ## Writting makefiles that create settings.
    
      assemble:
          json-cfg -e CONFIG_FILE -i NAME[,ARGS...] -i EXAMPLE_FILE
    
    The makefiles should have a configuration file (EXAMPLE_FILE). When
    executed "make assemble" then a configuration file is created which
    it is packed with "make install".

make-h

    Usage: make-h ...
    
    ... init|i [c]    : Initialize/update Makefile.
    
    ... add BLKS...   : Add "go" block. (go, sh, license, man)
    ... update        : Update blocks.
    
    ... get VARIABLE : Get variable.
    ... chk TARGET   : Check the target is available.
    
    ... project      : Get PROJECT.
    ... version      : Get VERSION.

release-mode

    Usage: release-mode [-a] [COMMAND...]
    
    Execute a command or open a shell with "RELEASE_MODE=rel"
    environment variable set.

runit-h

    Usage: runit-h [-v][-D DESTDIR] ...
    
      -a NAME PROGRAM ARGS... : Create a normal waiting service.
    
    Create and manage services using runit.
    
    Platforms: Linux

script-h

    Usage: script-h [-r|p : Record/play keystrokes] COMMAND
    
    Helper script around script(1), scriptreplay(1), ttyrec(1), xterm(1)
    and ttyrec2gif(go) to record terminal session gifs.
    
    The gif is generated in "rec/tty.gif", keystrokes in "rec/script.{i,t}"
    and ttyrec file in "rec/ttyrecord".

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
