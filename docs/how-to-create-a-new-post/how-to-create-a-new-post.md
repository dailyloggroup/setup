---
layout: default
title: How to create a new post
nav_order: 3
has_children: true
permalink: /docs/how-to-create-a-new-post
---

# How to create a new blog post

## Working directory

- Create a new git branch following the naming convention:
  - Branch name: `<writer name>#<module>-<week number>`
  - ex. `john-doe#2021-01-w1`

  ```
  git checkout -b john-doe#2021-01-w1
  ```

- Display a list of all branches in the project repo. The `*` symbol indicates the branch that you're currently working on.
  
  ```
  git branch
  main
  * john-doe#2021-01-w1
  ```

## Jekyll post

- To write a post in Jekyll, run the jekyll compose command, followed by the title of a new post wrapped in double quotes.

  ```
  jekyll post "My new post"
  ```

- Whenever a new post is created, Jekyll automatically prepends a date in front of a post title, followed by an extension. If you'd like to change the default date to the latest date after revision, you can rename the file with a new date.

  ```
  _posts/2020-11-30-my-new-post.md
  ```

- The new post comes with a frontmatter containing default variables. Fill in the missing variable `author` with your own name.

  ```yaml
    layout: post
    title: "My new post"
    date: 2020-11-30 09:20 +0900
    module: 2021-01
    author:
  ```

- Make sure that your name matches the one registered under `_authors` directory. Also, the `module` variable should match the current month, so that the posts will be categorized under the correct month.
