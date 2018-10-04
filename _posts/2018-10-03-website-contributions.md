---
layout: post
title: "Website contribution quick-guide"
date: 2018-10-03
---

There has been interest in contributing to the website, but not everyone knows how to go about that.  I'm going to outline some basic steps below.  If you're already familiar with git and github hosted webpages then this will be a lot of review.


At a high level we want to do the following:
1. Have a fork of the source code associated with our user on github
2. Clone our repository to get access to the source code
3. Create or modify files as needed
4. Add the new/modified files to staging
5. Create a commit (with useful message)
6. Push the changes to the remote repository
7. Create a pull request explaining your changes


__Step 0__
Before we can begin step one, we need a github account.  If you don't already have one, head on over to [github](https://github.com/join). Otherwise sign in and proceed.

__Step 1__
Head to the [repository](https://github.com/ColaMakerspace/ColaMakerspace.github.io) and click the `fork` button. This creates a copy of the repository under your user account which you can experiment with until you are happy with the final result.

__Step 2__
From your forked repository page on github, you will be able to get a checkout link from the green `clone or download` button. If you are using a command line git client you can then use the following command to check out a local copy where [yourUsername] is replaced with the username you created/signed into in step 0:
```
git clone https://github.com/[yourUsername]/ColaMakerspace.github.io.git
```

__Step 3__
If you are creating a post, you can go ahead and create a new file in the `_posts` directory.  All files in that directory are organized by date and are written in markdown. I found the following very useful while writing this post in markdown: [markdown cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

__Step 4__
With the amazing changes now complete, run the following command to stage the changes you want to commit:
```
git add [filename]
```

This can be done for each file you want to add.
To view which files you have currently staged you can run the following:
```
git status
```

__Step 5__
After all desired files are staged, use the following command to commit them:
```
git commit -a "your amazingly descriptive message explaining how great your changes are"
```

__Step 6__
Next, push the changes to the remote server with:
```
git push origin [nameOfBranch]
```

If you are not sure what your branch name is, run:
```
git branch
```

If your changes are a markdown file, they can be easily previewed by opening them in the github repository source code browser. This is a good way to validate that markdown formatting is working as intended.  If your changes are more structural to the website, more thorough testing should be done.

__Step 7__
Finally, with all the changes back on github under your account you must create a pull request.  To do so, go to your forked repository and click the `New pull request` button.  This prompts you for a description and/or comments which may be help the admin understand your changes.  Once the pull request has been accepted, the admin will merge it into the production repository.  From there it will be automatically deployed to [the website](http://colamakerspace.com).
