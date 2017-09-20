# NorthInvent-Wave-bsp-platform
NorthInvent Wave Evolution Roj Smarc Quad and Solo bsp platform

To get the BSP you need to have repo installed and use it as:

Install the repo utility:

$: mkdir ~/bin
$: curl http://commondatastorage.googleapis.com/git-repo-downloads/repo > ~/bin/repo
$: chmod a+x ~/bin/repo

Download the BSP source:

$: PATH=${PATH}:~/bin
$: mkdir NIwave-bsp
$: cd NIwave-bsp
$: repo init -u https://github.com/ipTronix/NorthInvent-Wave-bsp-platform -b dizzy
$: repo sync

At the end of the commands you have every metadata you need to start work with.

To start a simple image build for Roj smarc with imx6 quad:

$: MACHINE=waveq source ./setup-environment build
$: bitbake core-image-minimal

To start a simple image build for Roj smarc with imx6 solo:

$: MACHINE=waves source ./setup-environment build
$: bitbake core-image-minimal

You can use any directory to host your build.

The source code is checked out at "NIwave-bsp/sources".
