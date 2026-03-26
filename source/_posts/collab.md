---
title: Online Collaboration
date: 1969-10-29 00:00:00
category: guides
aside: true
copyright: false
archives: false
tags:
---
# Github!
You can collaborate with the source files shared on GitHub. Remember to create a GitHub account and send the username to me so I can add you as a collaborator.

# Folder Layout
The project layout is as following:

```
Project/
└── FFA-Source-Files/
    ├── source/
        ├── <strong>_posts/</strong>
            ├── activity-guide.md
            ├── charity-market.md
            ├── ...
            └── wrapping-boxes.md
        └── categories/
            └── index.md
    ├── themes/
        ├── butterfly/
            ├── .github/
                └── ...
            ├── languages/
                └── ...
            ├── layout/
                └── ...
            ├── scripts/
                └── ...
            ├── source/
                └── ...
            ├── .gitignore
            ├── LICENSE
            ├── README.md
            ├── README_CN.md
            ├── <strong>_config.yml</strong>
            ├── package.json
            └── plugins.yml
        └── .gitkeep
    ├── .gitignore
    ├── _config.landscape.yml
    ├── <strong>_config.yml</strong>
    ├── package-lock.json
    └── package.json
```

Files and folders with a preceding dot will not appear when you clone or extract the zip when you download this repo. If you need to use them (for whatever reason), press ⇧⌘. to reveal them as hidden files/folders.

Embolded items are extremely important and will be used very often.

The _config.yml files are briefly explained in the Markdown tab. Visit the documentation provided on that page to learn more about Hexo and Butterfly's configurations.

All of the markdown files used to generate your posts are located in the _posts/ folder.

If you want to add a new page, simply use GitHub's repository file viewer and add a new file. Make sure the front matter is included for the correct configurations for your page.

# Testing a Page
Since all the project files are stored online, you will need to clone or download the project into your local device.

Either download the repository as a .zip file or run `git clone <repo link>`. If you use git to clone the repository, make sure you have done `cd <desired directory>` so the files are downloaded in the corect place.

After you do so, run:
`cd <repo name>`(FFA-Source-Files for this repo)`.

Then, install the required node-modules:
`npm install`

Finally, run:
`npx hexo s`
To test the page.
