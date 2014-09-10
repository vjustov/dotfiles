dotfiles
========

###Install

Start by cloning down the repo:

$ git clone https://github.com/vjustov/dotfiles.git

afterwards cd into the directory and then run this script:

$ bin/install

This script symlinks all dotfiles into your home directory.

Please note: This will only install files that do not already exist in your $HOME directory. If you have, e.g. your own .bashrc file, you can move it to ~/.bashrc.local, and dotmatrix will source it for you.

###Vim bundles

For Vim users, there's another script you might want to run, after you've run bin/install:

$ bin/vimbundles.sh

This will install the set of Vim bundles we use.

After you've done ./bin/install, you'll have a .vimbundle file and this is a manifest of sorts that the vimbundles.sh script will use to install various vim plugins. If you have other plugins that you like that aren't on this list, you can put them in a ~/.vimbundle.local and that will be installed secondarily.

The ~/.vimbundle.local file should include one plugin per line, each having the following format:

github-user/repo-name

You need not include a trailing .git.
