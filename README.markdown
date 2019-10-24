# Source for the MWorks Project Website #

This repository contains the source for the [MWorks project website](https://mworks.github.io/), which is automatically converted by GitHub into a static site via [Jekyll](https://jekyllrb.com/).

## Local testing ##

To test changes to the MWorks website locally, you must first install the [github-pages gem](https://jekyllrb.com/docs/github-pages/).  To do this on macOS Catalina (10.15), `cd` to the top level of this repository, then run the following command:

    bundle install --path vendor/bundle
    
If you've installed github-pages previously, you can upgrade to the latest version by running

    bundle update
    
Once github-pages is installed, the following command will generate the website and start a local web server:

    bundle exec jekyll serve

You can then [visit the test site](http://localhost:4000/) to verify your changes before publishing.
