# ChesROMS-ubuntu
https://docs.microsoft.com/en-us/windows/wsl/install-win10
Install the Windows Subsystem for Linux
Enable the "Windows Subsystem for Linux" optional feature and reboot.

Open PowerShell as Administrator and run:

PowerShell

Copy
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
Restart your computer when prompted.

Install vcXsrv
create shortcut to vcXsrv into shell:startup
export DISPLAY=localhost:0.0 (add to bashrc)

start bash
type FROM http://madiris.altervista.org/?p=248, with edits.

Install subversion
       sudo apt-get install subversion
Install make
       sudo apt-get install make
Install netcdf
       sudo apt-get update
       sudo apt-get install libnetcdf-dev netcdf-bin libnetcdff-dev
Install compilers:
       sudo apt-get install cpp g++ gfortran
install mpi
       sudo apt-get install libopenmpi-dev openmpi-bin


mkdir romsdir
svn checkout --username pradal https://www.myroms.org/svn/src/trunk romsdir

(remember password...)

in compiler script, set export USE_NETCDF4 ON
export NF_CONFIG=/usr/bin/nf-config
export NETCDF_INCDIR=/usr/include
check paths to netcdf /usr/include, /usr/bin/, /usr/lib



HOW TO BUILD
     in roms, or romsdir, or roms_ubuntu, edit chesapeake.build.bash (or test2mpi.build.bash) 
     with ROMS_APPLICATION set to new test name
     MY_ROOT_DIR set to new testdir name
          
     execute  ./chesapeake.build.bash or ./test2mpi.build.bash
     





