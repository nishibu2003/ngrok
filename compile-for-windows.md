# How to compile ngrok for Windows

## Get tools.
### Go(https://golang.org/dl/)
[go1.17.2.windows-amd64.zip]https://golang.org/dl/go1.17.2.windows-amd64.zip  
Unzip the file. For example `G:\ngrok\go`.


1. ### Git(https://git-scm.com/download/win)
[64-bit Git for Windows Portable]https://github.com/git-for-windows/git/releases/download/v2.33.1.windows.1/PortableGit-2.33.1-64-bit.7z.exe  
Unzip the file. For example `G:\ngrok\PortableGit`.


1. ### Make for Windowws(http://gnuwin32.sourceforge.net/packages/make.htm)
[Make for Windows 3.81]http://gnuwin32.sourceforge.net/downlinks/make-bin-zip.php  
[LibIntl for Windows]http://gnuwin32.sourceforge.net/downlinks/libintl-bin-zip.php  
[LibIconv for Windows]http://gnuwin32.sourceforge.net/downlinks/libiconv-bin-zip.php  
Unzip the files. For example `G:\ngrok\make-3.81-bin`.  
Copy 2 dll files (ibiconv2.dll and libintl3.dll) to the same folder as make.exe. 


## Get ngrok sources.
Create a Git clone or download a zip from a github repository to your local drive. https://github.com/nishibu2003/ngrok  
For example `G:\ngrok\ngrok-1.7.1`.


## Compile.
Open a command prompt and type:
```
set goroot=G:\ngrok\go
set path=G:\ngrok\PortableGit\bin;%goroot%\bin;G:\ngrok\make-3.81-bin\bin;%path%
set gopath=G:\ngrok\ngrok-1.7.1
set GO111MODULE=off
cd /d G:\ngrok\ngrok-1.7.1
make
```

