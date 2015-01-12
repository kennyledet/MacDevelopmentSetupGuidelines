Actions
======

<h2>Initial Sensible (for software developers) Mac Defaults</h2>

*[Make an obligatory code path]*

	mkdir ~/code

*[Show all hidden files]*

	defaults write com.apple.finder AppleShowAllFiles YES 

*[Enable key press repetition]*

	defaults write -g ApplePressAndHoldEnabled -bool false

*Organize Finder favorites sidebar according to current personal tastes* (preferably sorted in descending order based on most frequently accessed)

<h4>Setting zsh as your default shell (or, The Beginnings of a Highly Superior shell Experience)</h4>
* [It’s actually quite simple to join the master race! Visit this nice Github repo to see!](https://github.com/robbyrussell/oh-my-zsh)



SSH Keys
-
	mkdir ~/.ssh
	cd ~/.ssh

*[ Create a default local public SSH key pair ]*

	ssh-keygen -t rsa


Git setup
-
*[Init your Git configuration with some sensibile open source defaults]*
	curl -O https://raw.githubusercontent.com/nicolashery/mac-dev-setup/master/.gitconfig 

*[Setup personal Git configuration]*
	git config --global user.name “Your Name”

	git config --global user.email “youremail@domain.com”

	git config --global credential.helper osxkeychain

Vim Setup
-
* Defer to [the Vim section in nicolashery’s mac-dev-setup repo](https://github.com/nicolashery/mac-dev-setup#vim) for now*

Python Setup
-

*[Install the recommended package manager]*

	sudo easy_install pip

	sudo pip install --upgrade distribute

	sudo pip install --upgrade pip

*[Install a better interactive Python interpreter console]*

	sudo pip install ipython[zmq,qtconsole,notebook,test]

Heroku Setup
-
*[Install the Heroku Toolbelt]*

[Found here!!](https://toolbelt.heroku.com/)

*[Setup SSH Keys support]*
	heroku keys:add


<hr>
Applications
=
Development
-

* iTerm 2 [lightyears ahead of the default Mac Terminal]

* Xcode [the industry standard IDE for native iOS and Mac software development]
	* Also install the Command Line Tools



* Sublime Text [code editor for pretty much everything else]
	* It’s free to use, it just bugs you to purchase a full license (gives you access to development versions, but they aren’t released that often) after each certain set amount of saves

* Homebrew
	* Also install Brew Cask to use Brew to manage native Mac apps in addition to UNIX ports


* Firefox Developer Edition [Beta Firefox geared specifically toward web developers]
	* Or Chrome Canary if that’s your style, smh

* VirtualBox [run GNU/Linux distributions in virtualized containers within OS X, without rebooting]

* Sequel Pro [for SQL database management]

General Helpers
-
* Caffeine [keeps your Mac awake]
* Flux [changes screen warmth based on the time of day, [helps you sleep by making your screen *not* mimick the sun](https://justgetflux.com/research.html) ]

Productivity
-
* Alfred [misc Mac productivity beast, though I mainly just use it for quickly emptying the Trash since Yosemite brought a Spotlight pop-up that can search files and the web in much the same way Alfred does, but natively]

* Mailbox [awesomely productive Gmail management]

* Markdown [free Markdown editor with live preview pane]

* SleepPillow [ ambient noise (nice presets) ]

* Relax Melodies [ ambient noise (more customizable) ]

* CheatSheet [quick shortcut to pull up guide of all shortcuts and their keyboard combinations for the current app]
* 1Password [beautiful and functional cross-platform password management (including iOS), if you’re into that sort of thing]

Entertainment and Media Content
-
* Spotify [awesome streaming music player with huge catalog, radio, playlists and plugins (+ download capabilties for Premium users)]

* MplayerX [faster and more aesthetically pleasing than VLC]

Connectivity
-
* Transmission [for downloading torrents]

* Colloquy [for using IRC]

Maintenence Tools
-
* Appcleaner [remove ALL(well, usually it’s most) files related to an Application, not just the .app file]
* Onyx [Mac maintenance power house]
	* It seriously kicks extensive ass, get it
* The Unarchiver [unarchive compressed files with support for more extensions than the native OS X solution]

[Office / Home] Content Production
-
* Keynote [better than Microsoft’s PowerPoint for making presentations]
* Pages [better than Microsoft’s Word for some word processing (like flyers)]

* Microsoft Word [better than Apple’s Pages for most word processing]
* Microsoft Excel [better than Apple’s Numbers for processing spreadsheets]

* Logic Pro X / Garageband [professional and amateur tools, respectably, for producing music]
* Ableton Studio [professional music production tool with features for live performances, loved by a lot of Electronic producers]

<h4>Design Specific</h4>

* Sketch [hot new vector tool]
* Photoshop CC [industry standard bitmap-based design & editing tool]
* Pixelmator [cheaper version of Photoshop]
* Paintbrush [MS Paint Mac equivalent]
* Paintcode [for designing graphic elements for Apple frameworks] 

Misc
-
* Mactracker [for die-hard Apple fanboys like me]

<hr>

Essential Software Development Tools [may be considered Applications OR Scripts]
=


Homebrew Packages
-

<h4>Core</h4>

* git [industry-standard versional control system right now, used across the field and on Github]

* wget [download files from terminal]

* tmux [manage terminal sessions (multiplexer)]

* cask [terminal-based native Mac app management using Homebrew]

* vim --override-system-vi [fresher vim release +override]

<h4>Python</h4>


* python3 [it’s newer than Python 2]

* pyenv-virtualenv [for initializing standalone self-managed virtual Python environments]

* pyqt [GUI toolkit]

<h4>Javascript/NodeJS</h4>

* node [ Node.js: ( asynchronous, event-driven Javascript platform based on Google’s V8 engine [[Chrome’s runtime]] ) ]
	* Installing this package also installs npm, Node’s default package manager
* nvm [ Node.js version management script ]

<h4>Ruby</h4>

* rbenv [virtualenv, but for Ruby]
	* [Add ```ruby-build``` as a plugin for compiling/installing different Ruby versions](https://github.com/sstephenson/ruby-build)
* bundler [gem manager for ruby]

<h4>Misc</h4>

* zeromq [distributed message queue platform]

* the_silver_searcher [ like ack, but faster (search files in terminal) ]

* xquartz [open-source Mac port of X.Org X Window System found on GNU/Linux]


Databases
=
* MongoDB [open-source document-based database, the leading [NoSQL](http://www.mongodb.com/nosql-explained) db]

* Redis [open-source key-value cache and store (or data structure server)]

* postgres [SQL db superior to *MySQL*]

* MySQL [inferior SQL db that’s **still** used more than *postgres* for some reason (I blame PHP development)]

<hr>

Games
=
* Steam [ like the App Store for Mac games, plus social/community features and achievements (ok, so it’s more like Xbox Live for Mac) ]

* League of Legends [most popular MOBA out, native Mac client]

	* **Add me:** KennyTheHitman93
	* Extremely fun, rewarding and addicting time-waster

* Hearthstone
	* I’ve downloaded it, and plan on playing it, but I’m much too busy right now to give my actual opinion. Everyone says it is a must-have so I’m still listing it here

* OpenEmu [bomb ass, open source, extensive collection of emulators for every *relevant* gaming platform, wrapped up in one nice Mac application]

	 * I’ve been supporting them since near day one, and the initial devs are a great group of engineers. [Check out the Github repo!](https://github.com/OpenEmu/OpenEmu)

<hr>

Browser Plugins
=
* Silverlight [for watching Netflix]

* Flash [if absolutely necessary..ugh]
