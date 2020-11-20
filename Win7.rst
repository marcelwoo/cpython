============
Python 3.9.0 fork for Windows 7 support
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
 
 And in this folder we can see installer python-3.9.0-amd64.exe, install it as usual.
