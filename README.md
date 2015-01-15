Actions
======

<h2>Initial Sensible [well, for software developers] Mac Defaults</h2>

*[ Make an obligatory code path ]*

	mkdir ~/code

*[ Show all hidden files ]*

	defaults write com.apple.finder AppleShowAllFiles YES 

*[ Enable key press repetition ]*

	defaults write -g ApplePressAndHoldEnabled -bool false

*Organize Finder favorites sidebar according to current personal tastes* (preferably sorted in descending order based on most frequently accessed)

<h4>**Setting zsh as your default shell [or, The Beginnings of a Highly Superior shell Experience]**</h4>

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
*[ Init your Git configuration with some sensibile open source defaults ]*

	curl -O https://raw.githubusercontent.com/nicolashery/mac-dev-setup/master/.gitconfig 

*[ Setup personal Git configuration ]*

	git config --global user.name “Your Name”

	git config --global user.email “youremail@domain.com”

	git config --global credential.helper osxkeychain

Vim Setup
-
* Defer to [the Vim section in nicolashery’s mac-dev-setup repo](https://github.com/nicolashery/mac-dev-setup#vim) for now*

Python Setup
-

*[ Install the recommended package manager ]*

	sudo easy_install pip

	sudo pip install --upgrade distribute

	sudo pip install --upgrade pip

*[ Install a better interactive Python interpreter console ]*

	sudo pip install ipython[zmq,qtconsole,notebook,test]

*[ Make path to store virtual environments in ]*
	mkdir ~/envs

*[ Install virtuenv module globally to create virtual Python environments ]*
	sudo pip install virtualenv

Heroku Setup
-
*[ Install the Heroku Toolbelt ]*

[Found here!!](https://toolbelt.heroku.com/)

*[ Setup SSH Keys support ]*

	heroku keys:add


<hr/>
Applications
=

<h2>Security</h2>
* [ Hands Off - Free version works fully for a set time period, can re-enable](https://www.oneperiodic.com/products/handsoff/) — [ protect your Mac’s internet and disk access ]
	* I prefer this over the more popular and well-known *Little Snitch*, because *Hands Off* also helps protect against file tampering.

<h2>Development</h2>

<br/>

<h4>Core</h4>
————

<h5>Terminal</h5>

* [ iTerm 2 ](http://iterm2.com/) — [ lightyears ahead of the default Mac Terminal ]
	* [Bonus points: The awesome and easy-on-the-eyes Solarized color schemes](http://ethanschoonover.com/solarized)
	* [Old but still relevant OS X terminal customization thread on Arstechnica](http://arstechnica.com/civis/viewtopic.php?t=1215355)

* [ Homebrew ](http://brew.sh/) —  [ install tailored Mac ports of UNIX software ]
	* Also install Homebrew Cask to use Homebrew to manage native Mac apps in addition to UNIX ports
		* Install with ```brew cask install google-chrome```
		* [ Homepage ](http://caskroom.io/)

<br/>


<h5>Browsers</h5>

* [Firefox Developer Edition [ Beta Firefox geared specifically toward web developers ] ](https://www.mozilla.org/en-US/firefox/developer/)
	* Or Chrome Canary, if that’s your style, smh

<h5>Virtualization [or, How to Disgrace Your Mac and Shame Your Family and Friends by Running Operating Systems That <em>Aren’t</em> the OS X Master Race</h5>

* Bootcamp [ for Windows ]
	* [Support](http://www.apple.com/support/bootcamp/)
	* [Guide](http://manuals.info.apple.com/MANUALS/1000/MA1519/en_US/Boot_Camp_Install-Setup_10.6.pdf)

* VirtualBox [ for everything else, including GNU/Linux distributions ]
	* [Homepage](https://www.virtualbox.org/)
	* [Lifehacker Guide: Installing Ubuntu](http://lifehacker.com/5938332/how-to-run-mac-os-x-on-any-windows-pc-using-virtualbox)

<h5>Database Management</h5>

* [ Sequel Pro ](http://www.sequelpro.com/) — [ for SQL, freely available ]

<br/>

<h5>IDEs</h5>

* [ Xcode ](https://developer.apple.com/xcode/) — [ the industry standard IDE for native **iOS** and **Mac** software development ]
	* Main languages are **Objective-C** and [ **Swift** ](https://developer.apple.com/swift/)
	* Also [ install the Command Line Tools for extra brownie points ](http://railsapps.github.io/xcode-command-line-tools.html)
		* You’ll need them to compile many Homebrew ports anyways
	* [ Apple provides Beta releases for registered developers ](https://developer.apple.com/news/?id=07112014a)
		* [ Registering as an iOS or Mac developer (pay $99 yearly fee) gets you these + OS X betas too ](https://developer.apple.com/register/index.action)
	* Add the [ Alcatraz extension ](http://alcatraz.io/) for built-in plugin/theme management

<br/>

* [ Android Studio ](http://developer.android.com/sdk/index.html) — [ open-source **Android** **Java** IDE ]
	* Haven’t hacked Android in a bit, but even when I was using Android Studio in pre-release it absolutely crapped all over Eclipse.
	* Also, Google themselves recommend using Android Studio for all _modern_ Android development

<br/>

* [ Sublime Text ](http://www.sublimetext.com/) —  [ code editor for pretty much everything else ]
	* It’s free to use, it just bugs you to purchase a full license (gives you access to development versions, but they aren’t released that often) after each certain set amount of saves
	* Technically, mainly a code editor, **but the massive amount of plugins available for it allow you to easily transform it into a fully-functional custom-tailored IDE**
		* *Can code your own plugins in Python*
		* Install [Package Control](https://packagecontrol.io/) for plugin discovery and management
	* Create a symbolic link to the automatically installed supplementary shell program ```subl``` ….
		* ….*which can be used to quickly open Sublime sessions with a folder you’re in inside a terminal*
		* ```ln -s "/Applications/Sublime Text.app/Contents/SharedSupport/bin/subl" /usr/local/bin/sublime```
			* This creates the link to be called from your command line with ```sublime``` … <br/> 
				….Rename this word [at the end in the ```ln``` call]  to whatever you’d like in order to customize this. <br/> ****Subjective Opinion:*** It may be longer, but I prefer to type 					```sublime``` instead of ```subl``` purely for the sake of explicitness.
		* <h5>Quick directions:</h5>
			* [ Open current directory in Sublime Text ] —  ```sublime .```
			* [ *Stupid Example:* Opening my code folder in Sublime Text ] — ```subl ~/code```
<br/>

<h4>Homebrew Packages</h4>
—————————————

<h5>Core [or, The Programs Usually Named with 3-4 Letters for some reason]</h5>

* ```git``` [ industry-standard version control system right now, used across the field and is the underlying driving force behind Github *(which you’re probably reading this on right now)* ]
	* [Git gud.](http://www.git-scm.com/book/en/v2)

* ``vim --override-system-vi`` [ fresher vim release +override’s the out of date default Apple-provided Vim distribution ]

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

* ``ffmpeg`` [ video processing power house ]
	* to add libfaac support, run ``brew reinstall ffmpeg --with-faac``
* ``gifsicle`` [ gif processing power house ]


<br/>

* ``cask`` [ manage native Mac app installations/removals in the terminal, through a Homebrew extension ]
	* [Homepage](http://caskroom.io/)


<h5>Python</h5>

* Python Distributions

	* ```python3``` [it’s newer than Python 2]
	* ```pypy``` [it’s faster than Python 3]

<br/>

* Essential Frameworks   ````TODO: Move the recommended frameworks/libs to more sensible sections; they don’t belong here! (holy shit I’m tired) — or develop a visual indicator for Homebrew packages so they can be under any heading````
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

<br/><br/><br/><br/>

General Helpers
-

* [ ClipMenu 1.0.0a1 alpha - Free ](http://www.clipmenu.com/blog/2014/11/11/clipmenu-1-0-0a1-released/) — [ awesome clipboard management tool ]
	* Access extensive clipboard history
	* Image and code previews ( *code previews have syntax highlighting* )
* [ Caffeine - Free ](https://itunes.apple.com/us/app/caffeine/id411246225) — [ keeps your Mac awake ]
	* Unobtrusive; simply sits in menubar
* [ Flux - Free ](https://justgetflux.com/) — [ changes screen warmth based on the time of day ]
	* [Helps you sleep by making your screen *not* mimick the sun](https://justgetflux.com/research.html)
* [ Bartender - Paid w/ free trial ](http://www.macbartender.com/) — [ Organizes menubar app icons (*can hide them for cleaner look*) ]

Productivity
-

* **General**
	* [ Alfred - Free w/ paid upgrade ](http://www.alfredapp.com/) — [ swiss army knife style Mac productivity beast ]
		* [ Paid “Powerpack” upgrade ](http://www.alfredapp.com/powerpack/) supports more features and extensions named “Workflows”
		* ****Subjective Note***: I mainly just use it for quickly emptying the Trash since Yosemite brought a Spotlight pop-up that can search files and the web in much the same way Alfred does, but natively*


* **Mail**
	* [ Mailbox - Free ](http://www.mailboxapp.com/) —  [ awesomely productive Gmail management ]
		* Can sort your mail for you in smart and actually useful ways
		* ****Subjective Opinion***: Could really use support for more than just Gmail*

<br/>


* **Cloud Notes**
	* [ Simplenote - Free](https://itunes.apple.com/us/app/simplenote/id692867256?mt=12) — [ Like the name says, it’s simple (much more-so than Evernote) ]
	* [ Evernote - Free w/ premium subscription ](https://evernote.com/) — Cloud notes powerhouse
		* Supports tons of media options and scanning from app
		* More widely supported and integrated into 3rd party applications, if that matters to you

<br/>


* **Markdown Editors**
	* [ Markdown - Free ](https://itunes.apple.com/us/app/id727484953) — [ free Markdown editor with live preview pane ]
	* [ Mou Beta - Free ](http://25.io/mou/) — [ like above, is a bit better *when it actually works and isn’t crashing* ]

<br/>


* **Password Managers**

	* [ 1Password - Free w/ paid desktop licenses](https://agilebits.com/onepassword) —  [ beautiful and functional cross-platform password management (including iOS), if you’re into that sort of thing ]
	* [ Lastpass ](https://lastpass.com/misc_download2.php) — [ it works, but less attractively than 1Password ]
		* I’m still using it alongside 1Password for purely legacy reasons, though I do plan on transferring all my logins to *1Password*
		* Also has mobile apps, *but you gotta pay for a premium subscription ($11.99 / year) to use them*

<br/>


* **Ambient Noise** *[ for when you want to listen to something other than music while programming ]*
	* [ Sleep Pillow - Free ](https://itunes.apple.com/us/app/sleep-pillow/id597419160?mt=12) — [ nice presets ]
	* [ Relax Melodies - Free w/ IAP](http://www.ipnossoft.com/app/relax-melodies/) — [ more customizable ]

<br/>


* **Misc**
	* CheatSheet [quick shortcut to pull up guide of all shortcuts and their keyboard combinations for the current app]

<br/>
<br/>


Entertainment and Media Content
-

* **Music**
	* [ Spotify - Free w/ premium subscriptions ](https://www.spotify.com/us/) — [ awesome streaming music player with huge catalog, radio, playlists and plugins
		* “Save” feature can technically be used to organize a cloud-based iTunes-like library *[ free for all users ]*
		* Download feature for actually saving songs to local drive *[ available to Premium subscribers ($9.99 / month) ]*

* **Videos**
	* [ MplayerX - Free ](http://mplayerx.org/) — [ top-notch video player ]
		* Can play most any type of video file you can throw at it
		* Faster and more aesthetically pleasing than *VLC*

<br/>
<br/>


Connectivity
-

* [ Transmission - Free (just asks for donations) ](https://www.transmissionbt.com/) — [ top-notch torrent downloader ]
* [ Colloquy -  Free ](http://colloquy.info/) — [ for chatting on IRC ]
* [ Cyberduck - Free ](https://cyberduck.io/) — [ connectivity powerhouse for *everything else* ]
	* Supports *FTP/SFTP, WebDAV, Amazon S3, Google Cloud Storage and Rackspace Cloud Files*

<br/>


Maintenence Tools
-

* [ Appcleaner - Free ](http://www.freemacsoft.net/appcleaner/) —  [ remove *ALL* **(well, usually it’s *most*)** core files associated with a Mac Application, not just the .app file ]
* [ Onyx - Free ](http://www.titanium.free.fr/onyx.html) — [ Mac maintenance power house ]
	* It seriously kicks extensive ass, get it
* [ The Unarchiver - Free ](http://wakaba.c3.cx/s/apps/unarchiver.html) — [ unarchives compressed files + support for tons more extensions than the native OS X solution ]
* [ Disk Inventory X - Free ](http://www.derlien.com/) — [ nice tool to visualize how your Mac’s storage is being used, file by file ]

<br/>


*[ Office / Home ]* Content Production
-

<h5>Apple</h5>

* [ Keynote - $19.99 ](https://itunes.apple.com/us/app/keynote/id409183694?mt=12) — [ better than *Microsoft’s PowerPoint* for making presentations ]
* [ Pages - $19.99 ](http://www.apple.com/mac/pages/) — [ better than *Microsoft’s Word* for **some** word processing *(like cool and stylish flyers and resumes)* ]

* [ Logic Pro X / Garageband - $199.99 ](https://itunes.apple.com/us/app/logic-pro-x/id634148309?mt%3D12) — [ professional and amateur *DAWS(Digital Audio Workstations)*, respectably, for producing music on Apple platforms ]

<br/>


<a href=“www.microsoftstore.com/store/msusa/en_US/pdp/productID.286395000”><h5>Microsoft - $99.99</h5></a>

* Word [ better than *Apple’s Pages* for **most** word processing ]
* Excel [ better than *Apple’s Numbers* for processing spreadsheets ]

<br/>


<h5>Other Companies (yes, they’re still relevant in this space)</h5>

* [ Ableton Live - $79.99 - $599 ](https://www.ableton.com/en/shop/) — [ professional music production tool with features for live performances, loved by a lot of Electronic producers ]
	* [ Extension Packs ](https://www.ableton.com/en/packs/)

<br/>


<h4>Design-Specific</h4>

* [ Sketch - $99.99 w/ free trial ](http://bohemiancoding.com/sketch/) — [ hot new vector tool ]
	* Heavily used in the *iOS and Android app design communities* nowadays
* [ Photoshop CC - Fucking Subscriptions ](http://www.adobe.com/products/photoshop.html) — [ industry standard bitmap-based design & editing tool ]
* [ Pixelmator - $29.99 ](http://www.pixelmator.com/) — [ cheaper version of *Photoshop*, **with a one-time payment..** ]
* [ Paintbrush - Free](http://paintbrush.sourceforge.net/) — [ Mac equivalent  for *Microsoft Paint* and spiritual successor to *Apple’s own MacPaint* ]
* [ Paintcode 2 - $99.99 ](http://www.paintcodeapp.com/) — [ for designing graphic elements translatable into **code for Apple’s platforms** ] 

<hr/>


Browser Plugins
=
* [ Microsoft Silverlight - Free ](http://www.microsoft.com/silverlight/) — [ used for watching Netflix ]

* [ Adobe Flash - Free, at the cost of hogging your processor and battery power](http://get.adobe.com/flashplayer/) — [ if absolutely necessary..ugh ]

<hr/>


Misc
=
* [ Mactracker - Free ](https://itunes.apple.com/us/app/mactracker/id311421597?mt=8) — [ a neat library-like application for exploring the entire catalog of Apple product releases throughout history up to the current iterations ]
	* ***Very** nice to have for die-hard Apple fanboys(or girls!) such as myself :)*

<hr/>


Gaming [Or, SHIT I really should get back to work!!]
=

* **Bookmark [the Humble Bundle homepage](https://www.humblebundle.com/) and check back frequently**
	* [ They regularly add great new deals on games to their Store ](https://www.humblebundle.com/store) — *for [Windows, Mac, and Mobile]*
	* They also release a [ **weekly** bundle ](https://www.humblebundle.com/weekly), as well as a *less frequent, but usually better bundle [ The “Main” Humble Bundle ] on the homepage*
		* Proceeds go to different charities!
		* **Choose what you want to pay; *but you have to pay a minimum of $1 to receive Steam keys* **

<h4>Platforms</h4>

* [ Steam - Free platform, Free and Paid games ](http://store.steampowered.com/) — [ like the App Store for Mac games, plus social/community features and achievements (ok, ok, *so it’s more like Xbox Live for Mac*) ]

* [ OpenEmu - Free ](http://openemu.org/) — [ bomb ass, open source, extensive collection of emulators for every *relevant* past-gen gaming platform, wrapped up in one nice Mac application ]

	 * **I’ve been supporting them since near day one, and the initial devs are a great group of engineers. [ Check out the Github repo! ](https://github.com/OpenEmu/OpenEmu)**

<br>

<h4>Games</h4>

* [ League of Legends - Free to play w/ IAP ](http://na.leagueoflegends.com/) — [ most popular MOBA out, [ now has native Mac client ](https://signup.leagueoflegends.com/en/signup/redownload) ]
	* Extremely fun, rewarding and addicting time-waster
	* **Add me:** KennyTheHitman93

* [ Hearthstone - Free to play w/ IAP ](http://us.battle.net/hearthstone/en/) — [ popular trading card game based in Warcraft universe ]
	* I’ve downloaded it, and plan on playing it, but I’m much too busy right now to give my actual opinion. Everyone says it is a must-have so I’m still listing it here


