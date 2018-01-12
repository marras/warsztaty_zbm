# [10th Biophysical Workshops](http://www.staff.amu.edu.pl/~zbm/xzwbiofiz/)

This page is built using `staticmatic`, a Ruby-based tool for creating website
using [HAML syntax](http://haml.info/) - basically it's HTML, just nicer. The
stylesheets use [SASS](http://sass-lang.com/) but also compile to plain CSS in
the end.

## Install prerequisites

This assumes you are using a UNIX-style operating system (e.g. Linux / Mac OS X)

#### 1. Install Ruby programming language:
  - Most systems have it installed by default, check by running `ruby -v`
  - If Ruby isn't present, we'll need to install it. The simplest way is to just use the version bundled with your operating
    system (`sudo apt-get install ruby`) and follow the instructions.

*If the default Ruby isn't available on your system, try [Ruby Version Manager](http://rvm.io/)*
If you chose RVM, install it:
  - `gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB`
  - `\curl -sSL https://get.rvm.io | bash -s stable`

  Then install Ruby by following the instructions on [RVM page](http://rvm.io/rubies/installing).

  There are a few commands listed on the RVM website but you can give it a shot and just try
  `rvm install 2.3.0` for a start. It should work, just make sure you read the
  output carefully.

#### 2. Install Git client (`sudo apt-get install git`)

#### 3. Clone the repository to your computer: `git clone git@github.com:marras/warsztaty_zbm.git`

If this step fails, it might be because you don't have
a [GitHub](http://github.com) account, or you weren't given access to this
repository.

#### 4. Enter the website folder and install remaining dependencies
  - `cd warsztaty_zbm`
  - `bundle install`

If The last step fails, please make sure the Ruby Bundler is installed:
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
  - The final *.html files will reside in the `site/` folder. Its contents can now to be uploaded to the actual server (e.g. main3.amu.edu.pl /public_html/xzwbiofiz)