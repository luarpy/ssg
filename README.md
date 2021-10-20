# ssg
Custom static site generator based on the work of [romanzolotarev](https://www.romanzolotarev.com/ssg.html) and modified by [NotTheBee](https://www.youtube.com/watch?v=N_ttw2Dihn8).

## Dependencies
- lowdown or Markdown.pl

###### Debian based
```sh
sudo apt install lowdown
```

## Usage
Follow this [example](https://www.romanzolotarev.com/ssg.html#:~:text=bin/Markdown.pl%0A%24-,usage,-make%20sure%20ssg6)

### Configuration file
It will be used if it exist under ```src/``` directory. Otherwise it will use the default values.
Configuration file example:
```txt
STYLESHEET="../path/to/stylesheet.css"
MAINPAGE="mainpagename.html" # or "mainpage.md"
DOMAIN="domain.example.com"
SCRIPT="../path/to/script.js" # or "../path/to/scripts_dir"
```
I ended up needing a configuration file because I only use one CSS style sheet and I did not wanted to copy it to every subdirectory inside the main path. This way the script manages the relative path to this files.

## TODO
- [ ] Add option to generate table of contents
- [ ] Add support for configuration file
- [ ] Change ```render_html_file()``. I need something more flexible and readable than _awk_ syntax for replacing characters
