# **Instructions to use Jekyll on Windows**

## **Install Jekyll**

### **Prerequisites**

First, you need to install Ruby and the Ruby DevKit on Windows. The easiest way
is to use RubyInstaller:

1. Download and install Ruby+Devkit from
   [https://rubyinstaller.org/downloads/](https://rubyinstaller.org/downloads/)
2. Choose the version with Devkit (recommended: Ruby+Devkit 3.0.X or newer)
3. During installation, make sure to check "Run 'ridk install'" at the final
   step
4. In the command prompt that opens, press Enter to install MSYS2 base
   installation
5. When prompted, press Enter again to complete the installation

### **Install Bundler and Jekyll**

Open Command Prompt or PowerShell as Administrator and run:

    gem update --system

    gem install bundler

If you get an error, rerun the command with the version suggested, for example:

    gem install bundler -v 2.4.22

**Install Jekyll**

    gem install bundler jekyll

## **Create a website using Jekyll**

Create a website called "my-website" inside a folder

From Command Prompt or PowerShell, navigate to your desired parent folder:

    cd C:\\path\\to\\your\\parent-folder

    jekyll new my-website

    cd my-website

## **To serve the website locally and view it in a browser**

In Command Prompt or PowerShell, make sure you are in the website folder and
then type:

    bundle exec jekyll serve

You will see warnings in the terminal, but you can ignore these

Type the local web server address
"[http://127.0.0.1:4000/](http://127.0.0.1:4000/)" into the address bar of your
browser

You can also type in "[http://localhost:4000](http://localhost:4000)" if that's
easier to remember. They both work

**To stop the server** Hold down the Ctrl and C keys at the same time

## **Change the website theme**

The free theme just-the-docs can be modified later and is a good starting point.

GitHub:
[https://github.com/just-the-docs/just-the-docs](https://github.com/just-the-docs/just-the-docs)
Demo & documentation: [https://just-the-docs.com/](https://just-the-docs.com/)

To add this theme, add this text to the bottom of the file "Gemfile":

\# just-the-docs theme

gem "just-the-docs"

Set the theme in your project's Jekyll \_config.yml file by replacing the
current theme

Look for the section: `# Build settings` in \_config.yml and then replace the
theme text to be:

theme: just-the-docs

To fetch required files, in Command Prompt or PowerShell within the website
folder type:

    bundle

To suppress warnings that are not errors (because one group made updates that
another group didn't use yet), add this to the bottom of the \_config.yml file:

yaml _\# Suppress warnings_ sass:

quiet_deps: true

You'll still see some warnings, but not as many, and you can ignore these.

To see the updated theme, serve it to the browser:

    bundle exec jekyll serve

And type in [http://localhost:4000](http://localhost:4000) in the browser
address bar

And to stop it, hold down the Ctrl and C keys at the same time

## **Use watch to continuously see updates in the browser**

    jekyll serve --watch

## **To customize the theme "just-the-docs"**

Documentation for the theme is at
[https://just-the-docs.com/](https://just-the-docs.com/)

**Layout**
[https://just-the-docs.com/docs/layout/layout/](https://just-the-docs.com/docs/layout/layout/)

**Navigation**
[https://just-the-docs.com/docs/navigation/](https://just-the-docs.com/docs/navigation/)

Put pages in the docs folder and you can order into subfolders.
