![Image of organon](https://i.imgur.com/VvoUkMP.jpg)

This program focuses on automating the download, installation and compilation of pentest tools from source

# ATTENTION!

## ** This tool is no longer working! Server is down ** .

Tool developed for Linux systems (APT and Pacman)

Authors:
--------
* [Franco Colombino (Fnkoc)](https://github.com/fnk0c)
* [Ygor Máximo (Maximoz)](https://github.com/maximozsec)

Requirements
-------------
1. Python >=2.7 or >=3.4    
2. python-pymysql
3. python-BeautifulSoup
4. python-html5lib
5. python-wget
6. GNU/Linux system based on Debian and Arch

Install
-------
	git clone https://github.com/fnk0c/organon.git
	cd organon
	python setup.py install

[With screenshot](http://organon.ddns.net/install)

Tested on:
----------
* Ubuntu 14.04  
* Ubuntu 14.10  
* Ubuntu 15.04  
* Debian 7.8 Wheezy
* Debian 8 Jessie
* Elementary OS Luna
* Linux Mint 17.1
* Manjaro (Unstable)

Screenshot
----------
![Screenshot](https://i.imgur.com/mAKhkRC.png)

Help
----
	usage: organon.py [-h] [-a] [-v] [-i I [I ...]] [-r R [R ...]]
                  [--dependencies] [--config] [-u] [-s S] [-l] [--clean]

	Package manager that focus on Pentest tools

	optional arguments:
	  -h, --help      show this help message and exit
	  -a, --about     About this tool
	  -v, --version   Show version and exit
	  -i I [I ...]    Install packages
	  -r R [R ...]    Remove packages
	  --dependencies  Remove dependencies (use with -r)
	  --config        Remove configuration files (use with -r)
	  -u              Update Organon
	  -s S            Search for package
	  -l              List all packages available
	  --clean         Clean Organon's cache

	* Listing available tools  
	        organon -l  
	* Searching for tools  
	        organon -s <package>
	* Installing tool  
	        organon -i <package> <package>
	* Update Organon  
	        organon -u
	* Remove tool
	        organon -r <package> <package>  
	* Remove tool and its dependencies and configuration files
	        organon -r <package> <package> --dependencies --config  
	* Clean .cache directory
	        organon --clean 
	* Current Version
	        organon -v

BUGS
----
Since it's still on development phase bugs are expected. Please, **report to us!** or open an **Issue**
* fb.com/franco.colombino
* fb.com/cienciahacker

Be Part of development
----------------------
Send us a message on facebook

About current version
---------------------
#### `v0.2.1`
- All features from previous versions + review of the code  
 - Installation script re-wrote and optimized  
 - Remove ruby  
 - All scripts are made in python  

About previous version
---------------------
#### `v0.2.0`
- **Goal**
 - Install tools and its dependences from a MySQL database

- **MySQL**
 - Server version: 5.5.41-0+wheezy1 (Debian)

 - Ruby code to connect to the database (depreciated)

 - Python script to execute the SQL commands and run the program

- **PKGCONFIG**
 - The installation scripts were replaced by pkgconfig files, similar to pacman pkgbuild. These files are hosted on the organon server.

- **Arch Linux support**
 - Organon now supports Arch and Debian linux  

- **Improvements on Install and Remove functions**
 - * Check if already installed
 - * When uninstalling, Organon check for the tool and diferent directorys (/usr/share || /usr/local/share || /opt)
