ns3 website: https://www.nsnam.org/

ns3 docs: https://www.nsnam.org/docs/release/3.37/tutorial/ns-3-tutorial.pdf


Installation Instructions:

$ cd

$ mkdir workspace

$ cd workspace

$ wget https://www.nsnam.org/release/ns-allinone-3.37.tar.bz2

$ tar xjf ns-allinone-3.37.tar.bz2


Notice the use above of the wget utility, which is a command-line tool to fetch objects from the web; if you do not
have this installed, you can use a browser for this step.
Following these steps, if you change into the directory ns-allinone-3.37, you should see a number of files and
directories


$ cd ns-allinone-3.37

$ ls

bake build.py constants.py netanim-3.108 ns-3.37 README.md util.py


Building with build.py

Note: This build step is only available from a source archive release described above; not from downloading via git or
bake.

When working from a released tarball, a convenience script available as part of ns-3-allinone can orchestrate a
simple build of components. This program is called build.py. 

This program will get the project configured for you
in the most commonly useful way. However, please note that more advanced configuration and work with ns-3 will
typically involve using the native ns-3 build system, CMake, to be introduced later in this tutorial.

If you downloaded using a tarball you should have a directory called something like ns-allinone-3.37 under your
~/workspace directory. Type the following:

$ ./build.py --enable-examples --enable-tests

Because we are working with examples and tests in this tutorial, and because they are not built by default in ns-3, the
arguments for build.py tells it to build them for us. The program also defaults to building all available modules. Later,
you can build ns-3 without examples and tests, or eliminate the modules that are not necessary for your work, if you
wish.
You will see lots of compiler output messages displayed as the build script builds the various pieces you downloaded.
First, the script will attempt to build the netanim animator, and then ns-3.