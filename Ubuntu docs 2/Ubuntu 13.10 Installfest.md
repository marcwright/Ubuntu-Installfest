#Setting up an Ubuntu Dev environment
#### for [@ga_la](https://twitter.com/ga_la)'s Web Development Immersive

---

Ubuntu set-up for our Linux-friendly students, courtesy of LA WDI-2 student Evan Pavlica

--
##Step one: (re)install Ubuntu


If you've never installed Ubuntu /Linux on your machine before, you've got a little work to do. If you want to keep whatever existing system you have, you'll likely have to re-partition your drive to have room for the linux install. This is dangerous for your existing filesystem, so make a backup to an external drive before starting.

**Get the Ubuntu install image**


I really can't compete with the Ubuntu documentation for installing... it's clear, and has instructions for all the little problems you may encounter along the way. Visit [their website](http://ubuntu.com) and get yourself set up with a fresh installation.

*If you are going to be installing with a USB drive, check out [UNetBootin](http://unetbootin.sourceforge.net/) as they make creating a USB install tool really simple.*


##Step Two: Installfest

**__Disclaimer: Our pre-work said not to install anything but Sublime and Chrome before class... If that's the case for you, save the instructions for Ruby, Postgres, etc for the in-class installfest.__**


You probably have a list of things you need for WDI already (and since one class is different from another, I'm sure my list will vary). Be that as it may, let's get installin'.

- **Chrome** - Google Chrome is awesome. This should be the first thing you download. Once you're all set up and logged into you Ubuntu system for the first time, open up Firefox (the default browser for Ubuntu) and point it to the [Google Chrome site](http://chrome.google.com). Download the appropriate file for your system (most likely the *.deb 64-bit) and let it auto-open in Ubuntu Software Center. Once Software Center loads, hit install, enter your password, and wait for the package to get itself setup. 

- **Sublime Text** - There's a couple of ways to get sublime, for me the easiest is to use the PPA (personal package archive)... this way, it's easy to remove if need be, and it'll get update though the package manager. Follow the instructions for either [Sublime Text 2](http://www.webupd8.org/2011/03/sublime-text-2-ubuntu-ppa.html) or [Sublime Text 3](http://www.webupd8.org/2013/07/sublime-text-3-ubuntu-ppa-now-available.html) depending on your needs (2 is older and better supported... 3 is up and coming. Both have similar functionality.) If the PPA isn't for you, hit up the [Sublime Text](http://www.sublimetext.com/) site to get the manual-install package.
  - I highly recommend you get [Package Control](https://sublime.wbond.net/) installed for Sublime... there's so many handy features I don't know why you'd use sublime without them.

- **Ubuntu build packages** - These are things that get installed with XCode or Brew on Mac OS... on Ubuntu we use the *build-essential* package. There's also a few others in the terminal command below that will be needed later on for compiling ruby; it's best just to get them now:
   
  - open the terminal ( **Ctrl + Alt + T** works for this) and type `sudo apt-get update` then 

```
sudo apt-get install \
build-essential curl autoconf libssl-dev libyaml-dev \
libreadline6 libreadline6-dev zlib1g zlib1g-dev \
sqlite3 libsqlite3-dev
```

- Install **Git**. You'll really need this. In the terminal: `sudo apt-get install git`

  - Follow github's instructions to [set up git](https://help.github.com/articles/set-up-git)

  - Also follow their instructions on [generating SSH keys](https://help.github.com/articles/generating-ssh-keys)


- Install ruby using **rbenv** by following the installation instructions [here](https://github.com/sstephenson/rbenv#installation). 

  - be sure to also install *ruby-build* -- the link is at the end of the installation section
  
  - once rbenv & ruby-build are installed: `rbenv install 2.1.2` 

- Install **Rails** : `gem install rails --version=4.0.4 --no-ri --no-rdoc`



## Set up BASH (optional)


Customize your BASH (terminal session) by editing the .bashrc file... in terminal, you can type `gedit ~/.bashrc` to start this process. There's a lot of different things you can do here that could be helpful, for example:

  - Setting up aliases (you can also parse these out into a separate file, ~/.bash_aliases) -- there are a couple of these already specified in your bashrc by default. Check out [this site](http://www.cyberciti.biz/tips/bash-aliases-mac-centos-linux-unix.html) for some good ideas about what you can do with aliases

  - Enabling color in terminal -- not for everyone (color is apparently distracting??), but if you want a little more color in the terminal, uncomment (remove the #) from `force_color_prompt=yes`

  - Change the prompt -- Ubuntu's BASH defaults to `[username]@[computer name]:[working directory]$` for brevity, I like to make mine shorter... but there are many different ways to modify this. Check out [the community documentation](https://help.ubuntu.com/community/CustomizingBashPrompt) for customizing BASH.
