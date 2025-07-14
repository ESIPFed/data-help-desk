# Instructions to use Jekyll on a mac

# Install jekyll

The next commands use 'sudo' which requires your mac password

    sudo gem update –system

    sudo gem install bundler

If you get an error, rerun the command with the version suggested, for example

    sudo gem install bundler \-v 2.4.22

Install Jekyll

    gem install bundler jekyll

# Create a website using Jekyll

Create a website called "my-website" inside the folder "parent-folder" From a
terminal, cd to the path of the parent-folder

    cd path-to-parent-folder

    jekyll new my-website

    cd my-website

# To serve the website locally and view it in a browser

In a terminal, make sure you are in the website folder and then type

    bundle exec jekyll serve

You will see warnings in the terminal, but you can ignore these

Type the local web server address
"[http://127.0.0.1:4000/](http://127.0.0.1:4000/)" into the search bar of your
browser

You can also type in "[http://localhost:4000](http://localhost:4000)" if that's
easier to remember. They both work

**To stop the server**

Hold down the control and c keys at the same time

# Change the website theme

The free theme just-the-docs can be modified later and is a good starting point.

GitHub:
[https://github.com/just-the-docs/just-the-docs](https://github.com/just-the-docs/just-the-docs)

Demo & documentation: [https://just-the-docs.com/](https://just-the-docs.com/)

To add this theme, add this text to the bottom of the file "Gemfile" \#
just-the-docs theme

gem "just-the-docs"

Set the theme in your project's Jekyll \_config.yml file by replacing the
current theme

Look for the section: \# Build settings in \_config.yml and then replace the
theme text to be

theme: just-the-docs

To fetch required files, in a terminal within the website folder type bundle

To suppress warnings that are not errors (because one group made updates that
another group didn't use yet), add this to the bottom of the \_config.yml file

\# Suppress warnings sass: quiet_deps: true

You'll still see some warnings, but not as many, and you can ignore these.

To see the updated theme, serve it to the browser

    bundle exec jekyll serve

And type in [http://localhost:4000](http://localhost:4000) in the browser search
bar

And to stop it, hold down the control and c keys at the same time

## Use watch to continuously see updates on the browser

    jekyll serve \--watch

# To customize the theme "just-the-docs"

Documentation for the theme is at
[https://just-the-docs.com/](https://just-the-docs.com/)

## Layout

[https://just-the-docs.com/docs/layout/layout/](https://just-the-docs.com/docs/layout/layout/)

## Navigation

[https://just-the-docs.com/docs/navigation/](https://just-the-docs.com/docs/navigation/)

Put pages in the docs folder and you can order into subfolders.
