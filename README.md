# 10th Biophysical Workshops

This page is built using `staticmatic`, a Ruby-based tool for creating website
using [HAML syntax](http://haml.info/) - basically it's HTML, just nicer. The
stylesheets use [SASS](http://sass-lang.com/) but also compile to plain CSS in
the end.

## Install prerequisites

This assumes you are using a UNIX-style operating system (e.g. Linux / Mac OS X)

1. Install Ruby programming language:
  - Most systems have it installed by default, check by running `ruby -v`
  - If Ruby isn't present, install the [Ruby Version Manager](http://rvm.io/) or just use the version bundled with your operating
    system (`sudo apt-get install ruby`) and follow the instructions.
  - If you chose RVM, follow the instructions on its [homepage](http://rvm.io/rubies/installing). This mostly boils down to running
  `rvm install 2.3.0`

2. Install Git client (`sudo apt-get install git`)

3. Clone the repository to your computer: `git clone git@github.com:marras/warsztaty_zbm.git`

4. Enter the website folder and install remaining dependencies
  - `cd warsztaty_zbm`
  - `bundle install`

If The second step fails, please make sure the Ruby Bundler is installed:
`gem install bundler`

## How to build the website:

4. [Optional] Preview the website on your computer
  - `staticmatic preview .` (This command launches a local server).
  - Open [http://localhost:3000](http://localhost:3000) on your computer and
    navigate around the website. You can now make changes in your local `src/`
    folder and see the effects in your browser.

5. Compile (build) the website
  - If step 4 was followed: close the _staticmatic_ server
  - Compile the HAML templates into HTML: `staticmatic build .`
  - The final *.html files will reside in the `site/` folder. Its contents need to be uploaded to the actual server (e.g. main3.amu.edu.pl)