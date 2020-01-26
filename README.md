# Git-Demo-for-Students

Hello Second Years. This is your homework :-)

Please do the following steps:

* Step 0. Create an account on Github. I strongly advise you to sign up to the [Github Student Developer Package](https://education.github.com/pack) and receive some goodies from Amazon Web Services (AWS), namecheap among others. There also exists Gitlab and Bitbucket which are nice, but the majority of your friends are likely to be using Github so you may as well be on the same platform. Once you have made your account, please send onto me your github username so I can authenticate you. You will not be able to complete Step N without doing that, but you will be able to complete steps 1 through N-1.

* Step 1. Verify that Git is installed on your system. Git is preinstalled on Mac OSX and some [*nix](https://en.wikipedia.org/wiki/Unix-like) systems, however most Linux Distributions require you to install git manually. Open up a terminal and type ```git --version```. If all is well, you should see something similiar to the following.

If you are on Windows (gasp! :O) you will have to manually install git. There are a number of ways you could do this, and I'll outline a few options here.
- **I.(Recommended):** Use a program apart of the Windows System called Windows Powershell. I usually avoid using Windows Powershell as its commands are different to Unix. There is enough common functionality to work with. Install [Chocolately](https://chocolatey.org/) by following the installation instructions on their website. Chocolately is a package manager for Windows. Once installed, install git via Powershell by typing the following ```chocolately install git```.
- **II.(For the Linux Enthusiast stuck on Windows):** Enable the *Linux Subsystem for Windows* in the System Settings [(Follow this guide)](https://docs.microsoft.com/en-us/windows/wsl/install-win10), install a Linux Distribution to the *Linux Subsystem for Windows* via the *Windows Store* application - Ubuntu, Fedora, Debian, OpenSUSE are all good choices. If you don't have a preference or aren't familiar with Linux, then I would suggest Ubuntu as it is the most user friendly (and would likewise discourage Debian). Once installed you should be able to launch an Ubuntu Session. Next, install git using the following command. ```sudo apt-get install git```. If you are unfamiliar with Linux, sudo means that you are requesting [Root User Priveleges](https://en.wikipedia.org/wiki/Superuser#Unix_and_Unix-like) (this is not too disimiliar to Adminstrator in Windows), apt is the package manager for Debian based Linux Distributions like Ubuntu.
- **III.(Most straightforward):** Install [Cygwin](https://cygwin.com/). Cygwin is an interface to Windows which adds some Linux Tools and as familiar Unix-like shell environment. It does not mean you can run Linux applications natively on Windows using Cygwin, but it does mean that via Cygwin you can use your Windows machine in a manner more familiar to Unix shells. Unlike the Linux distributions for the *Linux Subsystem for Windows** git will come preinstalled here.

What's the difference between these approaches? So with **I.** you will get a means of installing Native Windows applications to your system via a package manager at the expense of having to use Powershell which is not Unix-like. With **II.** you get to install native linux applications to a Linux layer running within Windows - a little bit more awkward to work with in my experience. With **III.** you get a Windows x86 application which allows you to interface to Windows in a manner you would be used to on Linux/Unix.

If you are on Linux, you can install git using your distribution's package manager. In Ubuntu/Debian, this is ```sudo apt-get install git```.

* Step 2.
With your terminal, navigate to a directory of your choosing e.g. ```mkdir ~/software-engineering-projct/ && cd ~/software-engineering-project/```. Clone this repository by typing in the git command ```git clone https://github.com/avieor/Git-Demo-for-Students.git```. You should now have a local copy of this repository. You can use ```ls -al``` on *nix to view all files (including hidden directories). Alternatively, you can use tree if you have it installed to show files as a Tree ```tree -a .``` :-)

* Step 3.
Make a branch. A branch create a snapshot of the codebase and work on it independently without having to worry about other people's work conflicting with your code. The idea of a branch is to allow teams of developers to work on implementing seperate features without having to worry about the state of the code being changed. A working state of the code always available. To create branch ```git branch ```
