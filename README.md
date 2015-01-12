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

<h4>**Setting zsh as your default shell (or, The Beginnings of a Highly Superior shell Experience)**</h4>

* [It’s actually quite simple to join the master race! Visit this nice Github repo to see!](https://github.com/robbyrussell/oh-my-zsh)
* [Useful site for getting explanations of command-line arguments for various UNIX shell programs ](http://explainshell.com/)
* [Slide presentation on the benefits of using zsh over other options](http://www.slideshare.net/jaguardesignstudio/why-zsh-is-cooler-than-your-shell-16194692)


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

<h2>Development</h2>

<br/>

<h4>Main</h4>
————

<h5>Terminal</h5>

* iTerm 2 [lightyears ahead of the default Mac Terminal]
	* [Bonus points: The awesome and easy-on-the-eyes Solarized color schemes](http://ethanschoonover.com/solarized)
	* [Old but still relevant OS X terminal customization thread on Arstechnica](http://arstechnica.com/civis/viewtopic.php?t=1215355)

<br/>

* Homebrew [install tailored Mac ports of UNIX software]
	* Also install Brew Cask to use Brew to manage native Mac apps in addition to UNIX ports



* Firefox Developer Edition [Beta Firefox geared specifically toward web developers]
	* Or Chrome Canary if that’s your style, smh

* VirtualBox [run GNU/Linux distributions in virtualized containers within OS X, without rebooting]

* Sequel Pro [for SQL database management]

<br/>

<h5>IDEs</h5>

* Xcode [the industry standard IDE for native **iOS** and **Mac** software development]
	* Main languages are **Objective-C** and **Swift**
	* Also install the Command Line Tools for extra brownie points
		* You’ll need them to compile many Homebrew ports anyways
	* Apple provides Beta releases for registered developers 
		* $99 yearly fee gets you these + OS X betas too
<br>

* Android Studio [open-source **Android** **Java** IDE]
	* Haven’t hacked Android in a bit, but even when I was using Android Studio in pre-release it absolutely crapped all over Eclipse.
	* Also, Google themselves recommend using Android Studio for all _modern_ Android development

* Sublime Text [code editor for pretty much everything else]
	* It’s free to use, it just bugs you to purchase a full license (gives you access to development versions, but they aren’t released that often) after each certain set amount of saves
	* Technically a text editor, **but the massive amount of plugins available for it allow you to easily transform it into a fully-functional custom-tailored IDE**
		* *Can code your own plugins in Python*
		* Install [Package Control](https://packagecontrol.io/) for plugin discovery and management

<br/>

<h4>Homebrew Packages</h4>
—————————————

<h5>Core [or, The Programs Named with 3-4 Letters]</h5>

* ```git``` [ industry-standard version control system right now, used across the field and is the underlying driving force behind Github *(which you’re probably reading this on right now)* ]
	* [Git gud.](http://www.git-scm.com/book/en/v2)

<br/>

* ``wget`` [ download files from terminal ]
	* [Noob’z Guide](http://www.regravity.com/documents/Wget%20%96%20A%20Noob%92s%20guide%20-%20Regravity.com.pdf)
	* [Examples](http://ssh-commands.blogspot.com/2013/01/the-ultimate-wget-download-guide-with.html)
	* [Manual](http://www.gnu.org/software/wget/manual/wget.html)


* ``tmux``[ manage terminal sessions ( *a.k.a. [multiplexer](http://linuxcommand.org/lc3_adv_termmux.php) )* ]
	* [Quick Start](https://myhumblecorner.wordpress.com/2011/08/30/screen-to-tmux-a-humble-quick-start-guide/)
	* [Crash Course](http://robots.thoughtbot.com/a-tmux-crash-course)
	- [Noob’z Guide](http://blog.hawkhost.com/2010/06/28/tmux-the-terminal-multiplexer/)
	* [Manual](http://www.openbsd.org/cgi-bin/man.cgi/OpenBSD-current/man1/tmux.1?query=tmux&sec=1)

<br/>

* ``cask`` [ manage native Mac app installations/removals in the terminal, through a Homebrew extension ]
	* [Homepage](http://caskroom.io/)

* ``vim`` --override-system-vi [ fresher vim release +override’s the out of date default Apple-provided Vim distribution ]

<h5>Python</h5>

* Python Distributions

	* ```python3``` [it’s newer than Python 2]
	* ```pypy``` [it’s faster than Python 3]

<br/>

* Essential Tooling
	* ```pyenv-virtualenv``` [for initializing standalone self-managed virtual Python environments]


* Essential Frameworks   ````TODO: Move the recommended frameworks/libs to more sensible sections; they don’t belong here! (holy shit I’m tired)````
	* Web Development
		* [Django, a powerhouse web framework](https://www.djangoproject.com/)
			* Provides most the bells and whistles and has its own set of rules and ways it thinks things should be done
			* Better for fuller feature-set for content-based websites
			* More jobs available for it
			* Disclaimer: This is the first web framework I truly learned and became proficient in
				* *Tons* of freelance projects completed and delivered on time [or, if not, close enough at the very least] using it and, thus, *tons* of money made with it
				* Also see my [**old** [ remember this key fact before you laugh at any line of code or bad decision in it; I was like 15 years old and my skillset, practices and general proficiencies as a good engineer have since grown much, much higher in quality ! ] open-source media platform (began as Youtube clone) hosted right here on Github](https://github.com/kennyledet/emp) . It was *my first relatively sizable Django project*, **and** *my first web application project that was more complex than the usual traditionally beginner-friendly blogs, todo lists, one-off script wrappers and Twitter clone implementations in general.* It taught me TONS about web development, and I have the utmost respect for its developers and everyone in the community contributing plugins and learning resources. **HOWEVER**: These days I prefer to use Flask for most tasks.

		* [Flask, a minimalist web framework](http://flask.pocoo.org/docs/0.10/api/)
			* My go-to web framework when a specific language isn’t a requirement
				* Not even just because Python is my favorite lang *[and even then, Swift is swiftly becoming my new favorite!]*
				* Because it objectively sets the bar of how a modern minimalist web framework should look and act
			* Provides a nice core API along with an easily extensible architecture;
				* [*Many* plugins](https://github.com/humiaozuzu/awesome-flask) that solve most common web development problems are now available for you to pick, choose and freely combine in your application’s architecture, interchangeably *[dat decoupling]*
				* Along with [Blueprints](http://flask.pocoo.org/docs/0.10/blueprints/), the extensibility of the plug-in system essentially allows you to ultimately form your own specialized, domain-specific web frameworks, optimized for each of your projects’ specific intents and purposes. <br/>
	**This is a bit more difficult to pull off in Django (at least at the core level)**
			* Better-suited and much quicker for developing APIs and web services
			* Easier to deploy

	* GUI Toolkits
		* [PyQt](https://wiki.python.org/moin/PyQt)
			* Homebrew package: ```pyqt```
			* Necessary for building some other Homebrew packages
		* [Pyside](http://qt-project.org/wiki/PySide_Binaries_MacOSX)
			* I **highly** prefer using Pyside over the original PyQt module for developing GUIs in Python
				* More lenient licensing than PyQt policy, **especially important for commercial applications** [ [See comparison](http://www.devilsan.com/blog/choosing-between-pyside-or-pyqt-license-consideration) ]
				* They’re mostly interchangeable other than that; [here is a list of more differences](http://qt-project.org/wiki/Differences_Between_PySide_and_PyQt) *(note that PySide is limited to PyQt API 2, if that matters for you)*

	* Automation
		* [selenium](http://docs.seleniumhq.org/) [ web testing *(see: automation, scraping)* ]
		* If I can get away with only using Python, I love and highly prefer to use [splinter](http://splinter.cobrateam.info/en/latest/) a lot more — especially in my own projects
			* Cross-platform, higher-level wrapper around selenium’s core functionality
				* It’s lesser-known and, by extension, used less and has much less documentation and online support available for it, **buttttt—**
					* It benefits from a *much more respectably Pythonic interface* which helps in making it **simpler to use, more comfortable to learn for experienced Python developers and ``MUCH`` quicker for development** *(think C relative to Python, C being selenium and Python being splinter)*
				* selenium and its multi-platform library distributions are still used more often across the industry *(since more people know it, of course)* — *so if you want better chance at jobs involving web testing and/or automation, you’ll still be learning selenium*

<h5>Node.js</h5>

* Node.js Distributions
	* ```node``` — [ [node.js, the exponentially popular, asynchronous, event-driven Javascript platform based on Google’s V8 engine *(which is Chrome’s runtime)*](http://nodejs.org/) ]

		* Installing the core ```node``` package also installs [ ```npm```, the default package manager for Node.js](https://www.npmjs.com/)

* Essential Tooling
	* ```nvm``` — [ [Node.js version management script ](https://github.com/creationix/nvm) ]

<br/>

* Essential Frameworks  ````TODO: Move the recommended frameworks/libs to more sensible sections; they don’t belong here!````

	* Web Development
		* [Meteor](https://www.meteor.com/)
			* I used this when it first came out, before it was the *hot new Javascript framework of the month(s)*, and while it was nice back then too it really has grown up into quite the powerhouse node.js based web framework
			* Geared towards real-time web applications
		* [Derby](http://derbyjs.com/)
			* Similar to Meteor in that it’s meant for real-time apps, but I like Meteor much better ;)
		* [Express](http://expressjs.com/)
			* Minimalist node.js framework — gets out your way but provides the basics necessary for modern most web applications
			* Still in heavy use in the industry

<h5>Ruby</h5>

* Tooling
	* ```rbenv``` [virtualenv, but for Ruby]
		* [Add ```ruby-build``` as a plugin for compiling/installing different Ruby versions](https://github.com/sstephenson/ruby-build)

	* ```bundler``` [gem manager for ruby]

* Web Development
	* [Ruby on Rails [ industry-standard Ruby webdev powerhouse ] ](http://rubyonrails.org/)
	* [Sinatra [ for smaller web apps ] ](http://www.sinatrarb.com/)

<h5>Databases</h5>

* [```mongo``` [ MongoDB: open-source document-based database, the leading [NoSQL](http://www.mongodb.com/nosql-explained) db ] ](http://www.mongodb.org/)

* [```redis``` [ open-source key-value cache and store (or data structure server) ] ](http://redis.io/)

* [```postgres``` [ SQL db superior to *MySQL* ] ](http://www.postgresql.org/)

* [```mysql``` [ inferior SQL db that’s **still** used more than *postgres* for *some* reason *(I blame PHP development)* ] ](http://www.mysql.com/)


<h5>Misc</h5>

* [```xquartz``` [ open-source Mac port of X.Org X Window System *found on GNU/Linux* ] ](http://xquartz.macosforge.org/landing/)

* [```zeromq``` [ distributed message queue platform ] ](http://zeromq.org/)

* [```the_silver_searcher``` [ search files on your drive in the terminal, like ack, but *faster*  ] ](https://github.com/ggreer/the_silver_searcher)


<hr/>

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
* Spotify [awesome streaming music player with huge catalog, radio, playlists and plugins (Save feature for basically organizing a cloud-based iTunes library free for all users; *+ download feature available to Premium subscribers*)]

* MplayerX [faster and more aesthetically pleasing than VLC]

Connectivity
-
* Transmission [for downloading torrents]

* Colloquy [for using IRC]

Maintenence Tools
-
* Appcleaner [ remove *ALL* **(well, usually it’s *most*)** core files associated with a Mac Application, not just the .app file]
* Onyx [ Mac maintenance power house ]
	* It seriously kicks extensive ass, get it
* The Unarchiver [unarchive compressed files + support for tons more extensions than the native OS X solution]

[Office / Home] Content Production
-
<h5>Apple</h4>

* Keynote [better than *Microsoft’s PowerPoint* for making presentations]
* Pages [better than *Microsoft’s Word* for **some** word processing *(like cool and stylish flyers and resumes)*]

* Logic Pro X / Garageband [professional and amateur tools, respectably, for producing music]

<h5>Microsoft</h4>

* Microsoft Word [better than *Apple’s Pages* for **most** word processing]
* Microsoft Excel [better than *Apple’s Numbers* for processing spreadsheets]

<h5>Other Companies (yes, they’re still relevant in this space)</h5>

* Ableton Studio [professional music production tool with features for live performances, loved by a lot of Electronic producers]

<h4>Design-Specific</h4>

* Sketch [hot new vector tool]
* Photoshop CC [industry standard bitmap-based design & editing tool]
* Pixelmator [cheaper version of Photoshop]
* Paintbrush [MS Paint Mac equivalent]
* Paintcode [for designing graphic elements for Apple frameworks] 

Misc
-
* Mactracker [ a neat library for exploring the entire catalog of Apple product releases throughout history up to the current iterations]
	* *Very nice to have for die-hard Apple fanboys(or girls!) such as myself :)*

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
