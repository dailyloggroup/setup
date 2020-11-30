---
layout: default
title: How to create a pull request
nav_order: 4
permalink: /docs/how-to-create-a-pull-request
---

# How to create a pull request

## Commit and push

- Assuming that you're working on your branch, `john-doe#2021-01-w1`, and have created a new post under `_posts` directory, run the following git commands:

  ```
  # To see any changes made in the working directory
  git status

  # To add a change in the working directory to the staging area
  git add .

  # To create a commit with a concise message
  git commit -m"Add a new post"

  # To review a recently added commit
  git log --pretty=oneline
  ```


- When you're ready to share your draft with the team, push your branch to the remote repository. The following command updates the remote repository with the local commit created in the previous step.

  ```
  git push origin <your_branch_name>

  # for instance
  git push origin john-doe#2021-01-w1
  ```

## Open a pull request

- Go to the shared project repository on GitHub, and you’ll see a button "Compare & pull request. Click it to open a new pull request. 

- Provide a brief description of your post. Now submit the pull request by clicking the green button on the bottom of the request form.


## Respond to feedback

- Fellow members can add comments on a pull request. They can leave a comment on particular lines in the code, which can be found under `Files Changed` tab. You can reply to their comments, make further changes as necessary and push them again by following the previous git commands.

## Merge the pull request

- Once you're happy with the revised version of your post, click `Merge pull request` to merge the changes back to main. Or put it simply, to add your post.

## Update locally

- Now, the remote repo has been updated while the local repo hasn't. So, go back to the terminal and run the following git commands:

  ```
  # To switch to main branch
  git checkout main

  # To fetch and download content from a remote repository
  git pull
  ```

- And you're done! By the end of each week, the organizer will review the newly added posts and publish them on the official website.