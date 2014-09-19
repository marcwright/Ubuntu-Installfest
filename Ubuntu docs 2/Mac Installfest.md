#WDI Installfest (Mac)

**Version note:** Ruby 2.1.2 and Rails 4.0.4 are the standard for our class. If you already have another version installed, we'll either be advancing or rolling you back for consistency.

---

Most students will be on Macs (for Windows/Ubuntu, see the appropriate Readmes!). This set of instructions is meant to guide the Installfest process.

Please check your OS X version before beginning. (Click the Apple menu and choose *About this Mac*.) This set of steps should work for 10.7 - 10.9; if you're on another version, let an instructor know.

##XCode Command Line Tools

In Terminal:

`xcode-select --install`

Find an instructor for support if you have any errors!

##Homebrew

###Install Homebrew

In Terminal:

`ruby -e "$(curl -fsSL https://raw.github.com/Homebrew/homebrew/go/install)"`


###Brew Doctor
`brew doctor`

- See what the Doctor says.  You may need to edit your ~/.bash_profile or make other adjustments. If you're not sure how to handle the output, flag down an instructor!

**Rule of thumb:** Don't type any commands starting with 'sudo' unless an instructor okays it :)


##rbenv & Ruby

###Install RBENV

In Terminal:

`brew update`

then, we'll use brew to install rbenv:

`brew install rbenv rbenv-gem-rehash ruby-build`

then, we'll enable shims and autocompletion:

`echo 'eval "$(rbenv init -)"' >> ~/.bash_profile`

then, we'll make sure your $PATH has access to the rbenv command-line utility:

`echo 'export PATH="$HOME/.rbenv/shims:$PATH"' >> ~/.bash_profile`

then, reload your bash profile:

`source ~/.bash_profile`



###Install Ruby 2.1.2

Curious whether you've got Ruby installed already? Type `ruby -v` in Terminal to find out.


In Terminal:

`rbenv install 2.1.2`

This will take a while. Don't panic if it's more than 5 minutes and it looks like nothing has happened.

###Set Ruby 2.1.2 as the Default

In Terminal:

`rbenv global 2.1.2`


###Rehash to install shims

In Terminal:

`rbenv rehash`


##Rails

###Install Rails 4.0.4 & rehash

In Terminal: 

`gem install rails --version=4.0.4 --no-ri --no-rdoc`

###Double-check your Ruby & Rails versions

In Terminal:

`ruby -v`

then 

`rails -v`

You should have Ruby 2.1.2 and Rails 4.0.4. 

If you don't, please find an instructor!


##Git

###Install git

In Terminal:

`brew install git`


###Update git config information

In Terminal:

`git config --global user.name "YOUR-USERNAME"`

then

`git config --global user.email YOUR-EMAIL-ADDRESS`

then

`git config --global credential.helper cache`



