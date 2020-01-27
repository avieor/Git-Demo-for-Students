# Git-Demo-for-Students

Hello Second Years. This is your homework :-)

Please do the following steps:

* Step 0. Create an account on Github. I strongly advise you to sign up to the [Github Student Developer Package](https://education.github.com/pack) and receive some goodies from Amazon Web Services (AWS), namecheap among others. There also exists Gitlab and Bitbucket which are nice, but the majority of your friends are likely to be using Github so you may as well be on the same platform. Once you have made your account, please send onto me your github username so I can authenticate you. You will not be able to complete Step 8 without doing that, but you will be able to complete steps 1 through 7.

* Step 1.
Verify that Git is installed on your system. Git is preinstalled on Mac OSX and some [*nix](https://en.wikipedia.org/wiki/Unix-like) systems, however most Linux Distributions require you to install git manually. Open up a terminal and type ```git --version```. If all is well, you should see something similiar to the following.

If you are on Windows (gasp! :O) you will have to manually install git. There are a number of ways you could do this, and I'll outline a few options here.

- **I.(Recommended):** Use a program apart of the Windows System called Windows Powershell. I usually avoid using Windows Powershell as its commands are different to Unix. There is enough common functionality to work with. Install [Chocolately](https://chocolatey.org/) by following the installation instructions on their website. Chocolately is a package manager for Windows. Once installed, install git via Powershell by typing the following ```chocolately install git```.

- **II.(For the Linux Enthusiast stuck on Windows):** Enable the *Linux Subsystem for Windows* in the System Settings [(Follow this guide)](https://docs.microsoft.com/en-us/windows/wsl/install-win10), install a Linux Distribution to the *Linux Subsystem for Windows* via the *Windows Store* application - Ubuntu, Fedora, Debian, OpenSUSE are all good choices. If you don't have a preference or aren't familiar with Linux, then I would suggest Ubuntu as it is the most user friendly (and would likewise discourage Debian). Once installed you should be able to launch an Ubuntu Session. Next, install git using the following command. ```sudo apt-get install git```. If you are unfamiliar with Linux, sudo means that you are requesting [Root User Priveleges](https://en.wikipedia.org/wiki/Superuser#Unix_and_Unix-like) (this is not too disimiliar to Adminstrator in Windows), apt is the package manager for Debian based Linux Distributions like Ubuntu.

- **III.(Most straightforward):** Install [Cygwin](https://cygwin.com/). Cygwin is an interface to Windows which adds some Linux Tools and as familiar Unix-like shell environment. It does not mean you can run Linux applications natively on Windows using Cygwin, but it does mean that via Cygwin you can use your Windows machine in a manner more familiar to Unix shells. Unlike the Linux distributions for the *Linux Subsystem for Windows** git will come preinstalled here.

What's the difference between these approaches? So with **I.** you will get a means of installing Native Windows applications to your system via a package manager at the expense of having to use Powershell which is not Unix-like. With **II.** you get to install native linux applications to a Linux layer running within Windows - a little bit more awkward to work with in my experience. With **III.** you get a Windows x86 application which allows you to interface to Windows in a manner you would be used to on Linux/Unix.

If you are on Linux, you can install git using your distribution's package manager. In Ubuntu/Debian, this is ```sudo apt-get install git```.

* Step 2.
With your terminal, navigate to a directory of your choosing e.g. ```mkdir ~/software-engineering-projct/ && cd ~/software-engineering-project/```. Clone this repository by typing in the git command ```git clone https://github.com/avieor/Git-Demo-for-Students.git```. You should now have a local copy of this repository. You can use ```ls -al``` on *nix to view all files (including hidden directories**. Alternatively, you can use tree if you have it installed to show files as a Tree ```tree -a .``` :-)

* Step 3. 
Open README.md with your favourite text editor (brownie points if you can do this via the command line). If you don't already have a favourite text editor, or aren't use what a text editor is, then you should spend some time exploring various options. A text editor is a computer program used to edit computer files and write computer code. Some popular text editors include:
- [Atom](https://atom.io/)
- [Sublime Text 3](https://www.sublimetext.com/)
- [Visual Studio Code](https://code.visualstudio.com/)
- [Emacs](https://www.gnu.org/software/emacs/) - See also [Spacemacs](https://www.spacemacs.org/), which is a better out-of-the-box Emacs configuration aimed at former Vim users.
- [Vim](https://www.vim.org/)

If you aren't familiar with either Vim or Emacs, they have a steeper learning curve. I do recommend playing around with them and learning how to use Spacemacs eventually, but we will need to get work done quickly so I would recommend your preferred among {Atom, Sublime, VS Code} for this task.

Anyways, let's say you've got README.md open. This is what that homework webpage looks like in the flesh! Quite the stark change right? Do not make any changes to the README.md file just yet. Close your text editor and switch back to the terminal. 

* Step 4.
Make a branch. A branch create a snapshot of the codebase and work on it independently without having to worry about other people's work conflicting with your code. The idea of a branch is to allow teams of developers to work on implementing seperate features without having to worry about the state of the code being changed. A working state of the code always available. To create branch ```git branch nameofmybranch```, replacing _nameofmybranch_ with whatever you want to call your branch. Names such as eoinsbranch are good in so far as it lets us know that the branch is being worked on by Eoin. In a Software Engineering Process, you might name the branch after a feature that is being implemented via that branch.

* Step 5.
Checkout (which is the strange git terminology for "Switch to this other branch") to your newly created branch. ```git checkout nameofmybranch```. You can confirm what branch you are working on if you use ```git remote -v```. Now I want you to create a file called e.g. "eoinsfile.md". In a *nix system, this is straight forward from the terminal ```touch eoinsfile.md``` or ```echo "Hello World" > `/eoinsfile.md``` will both work. On Windows Powershell, you'll have to look up how to achieve this from the terminal. You can also opt to launch your favourite editor and create a new file via a GUI. Switching back and forth between the master branch and eoinsbranch branch will reveal that this file will only exist within eoinsbranch. Pretty cool right?

* Step 6.
Edit your new file and populate it will something of your chosing. Maybe you really like poetry and you will put your favourite poem in, or you will just pop in "Hello World, homework is complete". I am less interested in what you put in here than I am interested in knowing that you're able to **a)** use git **b)** use a text editor to edit files. The .md file extension signifies that the file is a Markdown file which is a markup language used for documentation on Github repos and is easily rendered into HTML. It's easy to write and looks pretty. [There is an overview on the syntax here.](https://en.wikipedia.org/wiki/Markdown)

* Step 7.
So now you've got a new file complete. Well done. Here's the important part - Versioning the software you have written. There's 3 steps to this.
- *Adding Changed files*: In this step, we add any files we've changed before we create a commit. In our case, ```git add eoinsfile.md``` will do the trick.
- *Creating a Git Commit*: So, we're ready to create a git commit. I usually do this and write the associated message in the same command. ```git commit -m "Adding eoinsfile.md to the repository"```. Now your branch has been successfully versioned via a commit.

* Step 8. 
This step covers pushing to the repo found on Github.com, which is an important part of the homework. To complete this step, you must have first sent on your Github account username to me (Eoin) via Email / Whatsapp etc. I also have to have added you as a contributor to the repository. Once that's out of the way, you can push your commits to Github via the push command, and you must specify your targert branch. This may look like ```git push origin eoinsbranch```.

* Step 9.
Next we can cover how to merge two branches together. When you're doing using git in a production environment one needs to be conscious about when its appropriate to make changes to the master branch. In most circumstances, you will require approval to make changes to master and will have to alert the other developers that this . This is the mindset I want you guys to have. We will be doing [scrum](https://en.wikipedia.org/wiki/Scrum)-like meetings as often as we can (depending on how often we can meet considering how varied timetables) during each week of the Project.

To do this, we need to do this in two steps. ```git checkout master``` will take us back to the master branch. ```git merge eoinsbranch``` will merge the two branches together. No conflicts should occur as we've only merged seperate files.


## Final Comments
If you've managed to do all of this, well done! If you don't immediately see the benefit of using git and Github right now, don't worry but I emphasise that these tools are a crucial part of any Software Engineering Process, and have been for the last 20 years. In fact, they are so important that if you're a prospective Software Engineer who does not know how to use these tools you wouldn't be taken seriously. I recommend getting very familiar and comfortable with using Git and Github/Gitlab/Bitbucket from here onwards. Use git for your homework assignments, just be sure to set your repos to private! Imagine you are due to present your work to a TA / Demonstrator for grading, but you decided to tweak your homework perhaps trying to improve it, and you find that you've added a new bug and you can't remember how to fix it. I've seen this happen before!
