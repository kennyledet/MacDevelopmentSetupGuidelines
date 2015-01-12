Actions
======
Make a ~/code directory

defaults write com.apple.finder AppleShowAllFiles YES [show hidden]

defaults write -g ApplePressAndHoldEnabled -bool false [enable key press repetition]

Organize Finder favorites

Add ruby-build plugin to rbenv [git clone https://github.com/sstephenson/ruby-build.git ~/.rbenv/plugins/ruby-build] 

Git setup
-
curl -O https://raw.githubusercontent.com/nicolashery/mac-dev-setup/master/.gitconfig (sensible defaults)

git config --global user.name "Kendrick Ledet"

git config --global user.email "kendrickledet@gmail.com"

git config --global credential.helper osxkeychain

Vim Setup
-
https://github.com/nicolashery/mac-dev-setup#vim

Python Setup
-
sudo easy_install pip

sudo pip install --upgrade distribute

sudo pip install --upgrade pip

sudo pip install ipython[zmq,qtconsole,notebook,test]

SSH Keys
-
mkdir ~/.ssh

ssh-keygen -t rsa

Heroku
-
heroku keys:add


Applications
=
iTerm 2

Xcode [+ command line tools]

Sublime Text

Firefox Developer Edition

VirtualBox

Sequel Pro

Heroku Toolbelt

Mailbox

Markdown

Spotify

Transmission

MplayerX

SleepPillow

Relax Melodies

Appcleaner

The Unarchiver

Keynote

Mactracker


Tools
=
Homebrew [+ cask]

Alfred

Onyx

Caffeine

Flux

zsh [oh-my-zsh]

1Password

CheatSheet


Brew Packages
=
git

wget

vim --override-system-vi

tmux

python3

pyenv-virtualenv

zeromq

pyqt

node

nvm

rbenv

bundler [gem manager for ruby]

the_silver_searcher

cask

xquartz

Databases
=
MongoDB

Redis

postgres

MySQL


Games
=
League of Legends

Steam

OpenEmu

Hearthstone


Extensions
=
Silverlight [for Netflix]

Flash [if necessary..ugh]
