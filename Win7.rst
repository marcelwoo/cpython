============
Python 3.9.4 fork for Windows 7 support
============

A lot of people still use Windows 7. End date of ESU support - 2023-01-10.

***************
Build instructions:
***************

You need Visual Studio 2017 and Python 3.8. Switch off vcpkg if it's installed
(vcpkg integrate remove). Install everything related to Python in Visual Studio Installer.

 1.  Start your "x64 Native Tools Command Prompt for VS 2017"
 2.  Change current directory to the place with enough free space.
 3.  pip install -U sphinx
 4.  set PYTHON="C:\\Program Files\\Python38\\python.exe"
 5.  set SPHINXBUILD="C:\\Program Files\\Python38\\Scripts\\sphinx-build.exe"
 6.  git clone https://github.com/NulAsh/cpython.git
 7.  cd cpython\\Tools\\msi
 8.  buildrelease.bat -x64
 9.  cd ..\\..\\PCbuild\\amd64\\en-us

And in this folder we can see installer python-3.9.4-amd64.exe, install it as usual.

If you need debugging symbols and/or debug binaries, you need to use python-3.9.4-amd64-full.exe

Usually Python is distributed in two forms:
- web-based installer (internally called "releaseweb") - very small executable that downloads everything before installation, will not work if you have no internet connection
- executable installer (internally called "releaselocal") - have standard Python distribution inside, but without debugging symbols (*.pdb) and debug binaries,
so if you need them, you still have to download them separately (installer will do this for you if you select appropriate checkboxes)

But in case of my fork, if you need them, you have to download full release, it have them inside
