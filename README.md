# utl-transpose-more-than-one-variable
Transpose more than one variable
    Transpose more than one variable

    Art's utl_transpose is faster and more flexible that 'proc transpose'.

    github
    https://tinyurl.com/thrxtbt
    https://github.com/rogerjdeangelis/utl-transpose-more-than-one-variable

    macros
    https://tinyurl.com/y9nfugth
    https://github.com/rogerjdeangelis/utl-macros-used-in-many-of-rogerjdeangelis-repositories


    other transpose repos
    https://tinyurl.com/rkypv24
    https://github.com/rogerjdeangelis?utf8=%E2%9C%93&tab=repositories&q=+transpose+in%3Amname&type=&language=


    SAS Forum
    https://tinyurl.com/rmc4oot
    https://communities.sas.com/t5/SAS-Programming/transpose-data-more-than-one-variable/m-p/615152


    *_                   _
    (_)_ __  _ __  _   _| |_
    | | '_ \| '_ \| | | | __|
    | | | | | |_) | |_| | |_
    |_|_| |_| .__/ \__,_|\__|
            |_|
    ;

    data have;
          input facility mortgage $ id $ name $;
    cards4;
    1 A 001 Jhon
    1 A 003 Frank
    2 C 004 Tom
    ;;;;
    run;quit;

    *            _               _
      ___  _   _| |_ _ __  _   _| |_
     / _ \| | | | __| '_ \| | | | __|
    | (_) | |_| | |_| |_) | |_| | |_
     \___/ \__,_|\__| .__/ \__,_|\__|
                    |_|
    ;

     WORK.WANT total obs=2

      FACILITY    MORTGAGE1    ID1    NAME1    MORTGAGE2    ID2    NAME2

          1           A        001    Jhon         A        003    Frank
          2           C        004    Tom

    *          _       _   _
     ___  ___ | |_   _| |_(_) ___  _ __
    / __|/ _ \| | | | | __| |/ _ \| '_ \
    \__ \ (_) | | |_| | |_| | (_) | | | |
    |___/\___/|_|\__,_|\__|_|\___/|_| |_|

    ;

    %utl_transpose(data=have,out=want,by=facility,var=mortgage id name);


