# Instructions to modify website content

These are instructions on modifying content for the Data Help Desk website
hosted on GitHub through GitHub pages. The website is running on Jekyll which
takes markdown content pages and turns them into a static site with html
formatted content pages. The repo is set up with a GitHub action that will
update the Jekyll website when new content (either updated or new) is pushed to
the repo.

**Website:**
[https://ESIPFed.github.io/data-help-desk/](https://ESIPFed.github.io/data-help-desk/)

# To clone the GitHub repo and make edits

To clone the GitHub repository and have access to both the main and gh-pages
branches, follow these steps:

This workflow will allow you to maintain and update both branches independently
on your local machine and push changes to the appropriate branch on GitHub.

You must be on the branch _gh-pages_ in order for your content changes to update
the website.

1.  First, clone the repository normally:

        git clone https://github.com/ESIPFed/data-help-desk.git

        cd data-help-desk

2.  By default, this will check out the default branch (usually main) and create
    remote tracking branches for all branches on the remote, but only the
    default branch will be available locally.

3.  To see all branches (including remote ones):

        git branch -a

4.  Create a local gh-pages branch that tracks the remote gh-pages branch:

        git checkout -b gh-pages origin/gh-pages

5.  The website content is on the gh-pages branch

    Switch to gh-pages

        git checkout gh-pages

    You can confirm which branch you're currently on using:

        git branch

6.  When you're on the gh-pages branch and want to make changes:

    Pull down the existing repo content

        git pull

    Make your changes...

    Add the changes

        git add .

    Commit the changes

        git commit -m "Your commit message"

    Push changes to the gh-pages branch

        git push origin gh-pages

    If you get an error saying you can’t push the content because it doesn’t
    match the current state of the repo, make sure to do a git pull first. You
    may need to resolve conflicts first.

# To view content updates locally

You can either edit the pages using Visual Studio Code or a similar text editor
(not WORD) and then push them to GitHub to see the updates, or you can install
Jekyll on your computer and see the changes on a locally served website, and
then push the docs to GitHub to see the updates. Without Jekyll on your
computer, you can still preview what the markdown text will look like on GitHub
pages using the preview option in Visual Studio Code.

To view content updates on a website served on your computer, see the following
instructions for installation and commands needed.

**For a mac:** Instructions to use Jekyll on a mac

[instructions_use_Jekyll_mac.md](link)

**For a PC:** Instructions to use Jekyll on Windows

[instructions_use_Jekyll_windows.md](link)

# To view content updates online

The content changes will take some time to reflect on the website because GitHub
is compiling them behind the scenes to become a Jekyll website displayed using
GitHub pages. The GitHub action is stored in

[https://github.com/ESIPFed/data-help-desk/blob/gh-pages/.github/workflows/jekyll.yml](https://github.com/ESIPFed/data-help-desk/blob/gh-pages/.github/workflows/jekyll.yml)

To see the progress of the Jekyll action and whether there are any problems,
click on the commit link displayed at the top of the repo page on GitHub. This
link will be displayed after the content is pushed to the repo.

# To make edits to the markdown content pages

Use Visual Studio Code (VS Code) to edit or create markdown files ending in the
extension “.md”. Do not use Word. In VS Code, you will be able to see a preview
of the markdown file.

## Install VS Code

[https://code.visualstudio.com/download](https://code.visualstudio.com/download)

## Open the website folder on computer to make edits

In VS Code, there will be a Welcome page with a link on it called “Open”. Click
on this and choose the website folder. This will contain all the website
markdown files and other files related to Jekyll.

## Preview a markdown file

Preview a markdown file by right clicking on the open file tab in VS Code, and
then choosing the option “Open Preview”. This will not look exactly like the
website because there are CSS styles used for the website to modify how content
is displayed.

## Location of website content markdown files

Home page: index.md

Example of a main link with no children: faq.md

Example of a main link with children: docs/how_to_overview.md

Example of the child of a main parent link: docs/how_to/create_a_survey_form.md

Location of parent links with sub-links: The parent pages are inside the docs
folder and not within a sub-folder.

Location of sub-links: The pages inside the docs folder contained in a
sub-folder.

## Menu creation

Any files in the website folder ending with “.md” will display as links in the
website sidebar menu as long as they have “top matter”. This is the text at the
top of each page surrounded by three dases “---”.

**Home page front matter**

\--- layout: home title: Home permalink: / nav_order: 1 has_toc: false \---

layout: Defines the layout the page will take. There will only be one ‘home’
layout.

**Main link without a child link content page front matter**

\--- layout: page title: FAQ permalink: /faq/ nav_order: 9 has_toc: false \---

**Main link with a child link content page front matter**

\--- layout: page title: How to permalink: /docs/how_to/ nav_order: 6 has_toc:
false \---

**Child link content page front matter**

\--- layout: page title: Create a survey form parent: How to nav_order: 5
has_toc: false \---

Notice the parent entry “How to” has to be the title of the parent page.

## Setting the order of the menu links

The nav_order entry sets the order for main links, and if it is a child page,
the nav_order entry sets the order of the child links.

**Be careful** using the same title for multiple pages in the front matter
section. Depending on the menu order, it can create a link in the wrong menu
section.

## If modifying menu order and document naming

**Be careful**: If you change the name of a document or move their order, you’ll
need to make corresponding changes in the web pages for links that reference
that page. To find these links in the content, do a search for the original doc
name.

# To customize the theme "just-the-docs"

Documentation for the theme is at
[https://just-the-docs.com/](https://just-the-docs.com/)

## Layout

[https://just-the-docs.com/docs/layout/layout/](https://just-the-docs.com/docs/layout/layout/)

## Navigation

[https://just-the-docs.com/docs/navigation/](https://just-the-docs.com/docs/navigation/)
