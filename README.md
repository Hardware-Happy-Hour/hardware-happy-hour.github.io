# Hardware Happy Hour website

[hardwarehappyhour.com](https://hardwarehappyhour.com/) &nbsp; | &nbsp;
[Jekyll documentation](https://jekyllrb.com/) &nbsp; | &nbsp;

## General idea behind running the site using Jekyll and Github pages

For a somewhat loosely structured community based project like this, running and maintaining a website can easily end up being only one or two people doing both the management, maintenance and content, often resulting in one or more of these suffering due to ressource constraints.

Setting up the site like this is an attempt at opening up for contributions from a much wider group, and still keeping a little bit of control and possibility to eg. roll back easily if something goes wrong.

Below you will find a simple guide on how to get going, if you would like to add or modify anything on the [hardwarehappyhour.com](https://hardwarehappyhour.com/) website.

## What you need

First of, you will need a Github user, so that you can fork the project into your own account and later on make a pull request with your changes.

Even though it is possible to simply edit the files, add new files or delete files and commit the changes, it is recommended that you [install Jekyll](https://jekyllrb.com/) so that you can run the site locally and test that your changes behave as expected, especially if you want to help with more alaborate changes like the theme or structure.

Again not strictly necesary, but generally nice to have is a git client and a text editor.

## Changing or adding content

### Fork and clone this reepository

1. In the top-right corner of this page, click **Fork**.

2. Clone a copy of your fork on your local machine, replacing *YOUR-USERNAME* with your Github username.

   `$ git clone https://github.com/YOUR-USERNAME/hardware-happy-hour.github.io.git`

### Running the Jekyll development server

If you have Jekyll installed, you can now start the development server by:

   `$ cd hardware-happy-hour.github.io`

   `$ bundle exec jekyll serve`

This will start a small web server on your local machine, and serve the site on: [http://127.0.0.1:4000](http://127.0.0.1:4000) where you can then surf the site and browse around.

### Add or change content

While the development server is running, you can now change content in eg. group descriptions or posts and when you save a file, the development server automatically picks up the changes and rebuilds the site, all you have to do is change to your browser and refresh the page and you changes should appear.

There are a few different folders in this project and they all have a specific purpose:

- `_groups` is the folder that holds markdown files with 3H group descriptions
- `_includes` are helper snippets for sidebars, menu, etc. (part of template)
- `_layouts` are the layouts currently defined (also part of template)
- `_pages` is where structural things like group list, category list and global content like contact page, etc. is kept
- `_posts` are the collection of news, events, tutorials and other content that will be part of the overall conteent stream. This is most likely the most used and again using markdown files
- `assets/images` is where image files goes - both for group pages and for regular posts. (There are also a few other subfolders in `assets` for stylesheets and javascript files)

#### Change/add group description

To change the description, website link or twitter handle, simply open and edit the `_groups/GROUPNAME.md` and save it. To add a new group, you just make a new file following the naming scheme and with a similar preamble and description as the others and you will have a new group on the site.

#### Add a new event

Event invites are simply posts that have the `event` category. When you make a new post, the naming of the file is important, since the first part is the publish date (in the format YYYY-MM-DD) and the second part will become part of the path in the URL for that event post and then the file extension `.md` for markdown. You should not use fancy characters, only a-z, 0-9 and - (dash) in the filename. Even though you can make posts with a date in the future, which will not be included in the build, your post will still be public, when it is pushed and later merged into the repository, so this is not a place for secrets.

If you need a new image for your post, you can add it to the `assets/images` folder and refer to it in your post.

### Commit and push

When you are done with your changes, all files saved and you have checked that it looked correct, it's time to commit your changes and push them to your own fork at Github.

First you add all the changed/new files

   `git add .`

Then you commit with a message to help others understand what you did.

   `git commit -m "Added new event for 3H xxx on yyy"`

And to move the changes up to Github, you push your repository changes

   `git push`

### Make pull request

The last thing to do is creating a pull request on Github to let the maintainers know that you have made some changes that you would like to have applied to the running website.

If you go to [https://github.com/Hardware-Happy-Hour/hardware-happy-hour.github.io](https://github.com/Hardware-Happy-Hour/hardware-happy-hour.github.io) right after you pushed your changes to your fork, there usually is a yellow box with a button to initiate the pull request process. If you have made something complicated, you can write in a short description, but by default it will find your commmit messages and include those.

### Changes being merged into the main repository

We will try to handle pull request as quick as possible and if you have any questions with this process, feel free to drop by the #web channel on our [Discord server](https://discordapp.com/invite/ckFFN8B)

### Copyright

Copyright (C) 2019 WowThemes.net.

Copyright (C) 2020 Hardware Happy Hour

Theme designed and developed by [Sal](https://www.wowthemes.net/) and modified by [Thomas Flummer](https://thomasflummer.com/), *free* under MIT license.
