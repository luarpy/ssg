# ssg
Custom static site generator based on the work of [romanzolotarev](https://www.romanzolotarev.com/ssg.html) and modified by [NotTheBee](https://www.youtube.com/watch?v=N_ttw2Dihn8).

## Dependencies
- lowdown or Markdown.pl
- [pup](https://github.com/EricChiang/pup)

###### Debian based
```sh
sudo apt install lowdown pup
```
## Installation
```sh
git clone https://github.com/luarpy/ssg.git
cd ssg
chmod +x ssg
```
And place it in your PATH variable if you want to use it as a system binary:
```sh
export PATH="$PATH:$PWD"
```

## Usage
Follow this [example](https://www.romanzolotarev.com/ssg.html#:~:text=bin/Markdown.pl%0A%24-,usage,-make%20sure%20ssg6)

### Configuration file
It will be used if it exist under ```src/.config``` directory. Otherwise it will use the default values.
Configuration file example:
```txt
STYLESHEET="../path/to/stylesheet.css"
MAINPAGE="mainpagename.html" # or "mainpage.md"
DOMAIN="domain.example.com"
SCRIPT="../path/to/script.js" # or "../path/to/scripts_dir"
```
I ended up needing a configuration file because I only use one CSS style sheet and I did not wanted to copy it to every subdirectory inside the main path. This way the script manages the relative path to this files.



## TODO
- [ ] Remove space between tags so the file characters are less, this way I could reduce file's size 
- [ ] Darkmode button does not work
- [ ] Add favicon support
- [ ] Generate and search for a PAGE_TITLE_PATTERN in the file, so it gets replaces with page's name
- [ ] Add support in the CSS file for the navigation bar
