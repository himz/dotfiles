dotfiles: Configuration files for my working set
========

I manage my vim/bash configs in separate directory ~/dotfiles.

bash directory contains my my .bashrc, .bash_aliases etc. bin - not same as ~/bin, contains scripts I use on day to day basis. desktop contains contains configurations exported from my Ubuntu desktop apps(e.g. my compiz-unity profile).

Everything needs to be soft linked to the relevant locations from here as shown by following commands:

rm-rf ~/.vim
ln -s ~/dotfiles/vim ~/.vim           

rm-rf ~/.vimrc
ln -s ~/dotfiles/vim/vimrc ~/.vimrc

rm -rf ~/.bashrc
ln -s ~/dotfiles/bash/bashrc ~/.bashrc

rm -rf ~/.bash_aliases
ln -s ~/dotfiles/bash/aliases ~/.bash_aliases

After this, goto dotfiles folder and run following command 
git submodule init && git submodule update

The above command will update all the vim plugins and use them .


PS: Most of this is taken from the following post:
http://mirnazim.org/writings/vim-plugins-i-use/