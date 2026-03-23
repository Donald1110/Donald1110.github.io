---
title: Deploying to GitHub
date: 1969-10-29 00:00:00
category: guides
aside: true
copyright: false
archives: false
tags:
---
# Deploying Changes to GitHub
This project uses Git to deploy the site. hexo-deployer-git should already be installed in the folder.

<strong>For collaborators, create a GitHub account if you haven't already and send me the email associated it so I can add you as a collaborator.</strong>

Once that is done, you will gain access to the original repository and the forked repository within the CSC Computing Society organization.

After deploying to the original repository, remember to sync the changes in the fork in the Computing Society organization for them to take effect on the official site.

(Deploying directly to the fork is not possible at the moment because of restrictions set by the admins making it unable to generate deploy keys.)

Before you deploy the website, make sure you have reloaded algolia with:
`hexo algolia`.
as to add the new files to its searching database.

To deploy, do:
`hexo clean`
and
`hexo generate`
Then:
`hexo deploy`.

You do not need to authenticate when running `hexo clean && hexo deploy` because the repo link in the \_config.yml contains a personal token, so no need to change that (a security hazard, but makes things way easier).

One deploying is done, you should see: 
`INFO  Deploy done: git`
and the new webpages or changes should have been added to the repo.