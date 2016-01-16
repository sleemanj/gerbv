This is a "fork" of gerbv ( http://gerbv.geda-project.org/ )

"Fork" is in quotes because the only change is currently to one solitary define, and it allows it to work with more complex merged (panelized) gerber files.   Forking just makes it easier to keep track of with future gerbv updates.

To build:
----------------------------------------
These are the brief instructions for Linux building, see gerbv's instructions for building under Windows.  I use gnu stow for local packages (apt-get install stow; man stow)

    git clone https://github.com/sleemanj/gerbv.git
    cd gerbv
    sh autogen.sh
    ./configure --prefix=/usr/local/stow/gerbv [other switches]
    make && sudo make install
    cd /usr/local/stow
    sudo stow gerbv
   
then run it (make sure you run the one you installed, ie, /usr/local/bin/gerbv )

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


