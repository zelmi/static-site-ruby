# Static Web Site Design
This project redesigns an existing website from from the CSE department's directory. The webpage that was redesigned is former Prof. Dey's website which can be found [here](http://web.cse.ohio-state.edu/~dey.8/)
## Installation

Installing Ruby and the Middleman gem is required to run this project. Enter the following commands into your terminal to install Ruby.

```bash
$sudo apt install zlib1g-dev build-essential libssl-dev libreadline-dev
libyaml-dev libsqlite3-dev sqlite3 libxml2-dev libxslt1-dev  libcurl4-openssl-dev
software-properties-common libffi-dev

$rbenv install 2.6.6 # this step takes several minutes

$rbenv global 2.6.6  # set default ruby version

$ruby -v # confirm it works
```
Afterwards, to install Middleman,
```bash
$gem install middleman
```
## Requires
Ruby gem Middleman

## Design
This webpage is statically generated using the ruby gem Middleman. The ruby file config.rb contains all of the Middleman configuration settings used to build this website. The source folder holds all of the html embedded ruby files and other files that contain all of the necessary parts to create the website. In order to build the website, the source folder's contents are compiled into the build folder using "bundle exec middleman build" command, and the site can then be viewed using the command "bundle exec middleman server" and visiting the link the command provides. Each html file reads from yaml files which contain the specified information to display on the respective page. The data folder contains all of the yaml files to be read from. Each category folder in data is broken down into subcategory folders that contain the specific yaml files holding the pertaining information. index.html is the home page, i.e. the first page the user sees when visiting the website, and displays the professor's name, contact information, and the information regarding books stored in books.yml. books.yml holds the values for the title, author, publisher, and sample characters for each book. academics.html is the academcis page which displays information retrieved from education.yml in a list format, which contains the degree, location, and years for each degree. activities.html is the activies page which goes through the values of the keys inside the profAct folder's yaml files and displays them accordingly. research.html displays data from the yaml files inside the research folder in a list format as well. The images folder contains tamal.png which is displayed on the homepage. The stylesheets folder contains site.css.scss which dictates how the site should look, such as the border width and colors to display on each page. In the layout folder, layout.erb instructs Middleman on how the site should be displayed using the given html and css files.
  
## How to use this program

To run the program, enter the directory for lab4, then input:

```
$bundle exec middleman server
```

The terminal will then provide you a link to visit the webpage, and upon inputting that link into your web browser you should be able to access the generated webpage.

## Markdown File

### VSCode

To view the formatted markdown file in VSCode, use VSCode code editor. Download here: https://code.visualstudio.com
Open the generated markdown file after running program and select open preview (Ctrl+Shift+V or Command+Shift+V).

### RubyMine

To view the formatted markdown file in RubyMine, navigate to the project tab, and then double click the README.md file in the project folder.

### Terminal

To view the formatted markdown file in the Ubuntu terminal, issue the following command to install the mdless gem:
```
$ gem install mdless
```
To open the generated markdown file, navigate to the lib folder of the project in the terminal, then issue the following command:
```
$ mdless article.md
```
The generated markdown file will open in the terminal. To quit mdless and return to the terminal, at anytime press 'q'.

## Contributors

### Team: //Todo: Make team name

Esther Hu

Evan Hubert

Zehur Elmi

Nick Springer
