This is a "fork" of gerbv ( http://gerbv.geda-project.org/ )

"Fork" is in quotes because the only change is currently to one solitary define, and it allows it to work with more complex merged (panelized) gerber files.   Forking just makes it easier to keep track of with future gerbv updates.

To build:
----------------------------------------
    git clone [this repository]
    cd [repo]
    sh autogen.sh
    ./configure [switches (see below)]
    make && sudo make install
   
then run it (make sure you run the one you installed if you didn't put it in /usr/bin or whatever)


The following (gerbv) switches are available to configure:
--help: Lists all configure options.
--enable-debug: Program will output lots of debug spew while running. (default = no -> no debug output by default.)
--enable-unit-mm: Set default unit for coordinates in status bar to mm (default = no -> units = inches by default.)
--enable-efence: Link with ElectricFence for malloc debugging (default = no -> efence off by default.)
--disable-update-desktop-database: Update desktop icon database after installation (default = no -> desktop icon installed by default.)


To bring in future changes from the offical gerbv:
----------------------------------------

    git clone [this repository]
    git add remote geda git://git.geda-project.org/gerbv.git
    git pull geda master
    [resolve conflicts if any]
    [build and test, see above]
    [git push if appropriate]


