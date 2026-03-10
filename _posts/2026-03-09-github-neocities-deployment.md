---
layout: post
title: "How to deploy Github into Neocities (+ with Jekyll)"
date: 2026-03-09
tags: [guide, github, jekyll, neocities]
category: guide
---

There are guides on how to deploy Github into Neocities, but I also have an extra layer of Jekyll, which took me a while to figure out.

Prerequisites: Have a Neocities and Github account, have Jekyll and Git installed

### 1. Setting up your repository
Your repository is kind of like your overarching project folder. First, name it whatever you like. I usually just make mine the name of my Neocities website (e.g. whatdidgiudo).

In your command prompt, type in `cd (your folder location)` to go into that folder. For instance, I would type in `cd whatdidgiudo`.

Once in, type `git init` to initialise some github files into your folder. You should then type `git remote add origin https://github.com/user/repo-name`. This connects your local folder with the repository on Github. To check if it works, you can try `git status` and see if your terminal displays the files in your folder.

### 2. API Key
Go into Neocities > Settings > API. Generate your API key (make sure not to send it to anyone!)

In Github, go to your repository settings > secrets > actions. Create a repository secret. You should name it `NEOCITIES_API_TOKEN` (just for convenience sake). In the details, you should paste in your API key. Don't worry, after you finish editing, you won't be able to see the key again.

### 3. Committing
In your local folder, make a new folder named `.github`. Inside that folder, add another folder named workflows. Inside that folder, add a file named `neocities.yml` (the name of the `.yml` file does not matter either, it's just more convenience).

Inside `neocities.yml`, paste this in:

```
name: Deploy to Neocities

on:
  push:
    branches: [main]

jobs:
  deploy:
    runs-on: ubuntu-latest
    
    steps:
      - uses: actions/checkout@v3
      
      - name: Set up Ruby
        uses: ruby/setup-ruby@v1
        with:
          ruby-version: 3.2
          bundler-cache: true
      
      - name: Build with Jekyll
        run: bundle exec jekyll build
      
      - name: Deploy to Neocities
        uses: bcomnes/deploy-to-neocities@v1
        with:
          api_token: ${{ secrets.NEOCITIES_API_TOKEN }}
          cleanup: true
          dist_dir: _site
```

Just replace `ruby-version: 3.2` with whatever version of Ruby you're on, which you can check by typing in `ruby --version` in your terminal.

Afterwards, back in your terminal, you should type `git status` again to check that nothing weird is going on.

After that, you should add `git add .` to add all of your new files.

Then, type in `git commit -m "Your message here"`. You can type in anything you want, but in this case I typed "Initial commit".

Finally, type in `git push origin main`-- wait a bit, and then reload your github repository to see your files on Github and Neocities!

### Other notes
As a beginner, your usual flow should be:

1. `cd your-project-folder`: go into your project folder
2. `git status`: check the files that have been edited, uploaded, and deleted
3. `git commit -m "Your message here"`: commit your changes and attach a message on it. The message isn't necessary, but it's good practice, especially since 99% of computer science jobs rely on Github, and you'll probably work with a team, who'll appreciate the documentation.
4. `git push origin main`: push your changes onto github and neocities

This isn't even Neocities exclusive, it's what you'd be doing with Github 99% of the time.

### Troubleshooting
#### Problem: Help! Why can't I push my new files?
For whatever reason, you're probably on a `master` branch. In the main repo page, check that your branch is `main`, not `master`. If it is, go to branch > all branches > rename your `master` branch to `main`. Try pushing your files again.

Another method you could do is go into your terminal and type `git branch`, which will show you what branch you're on. If it happens to be `master`, `git branch -m master main`.

*If you have any questions, don't hesitate to reach out. I'll try my best to help you.*