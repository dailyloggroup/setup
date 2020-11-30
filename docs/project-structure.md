---
layout: default
title: Project Structure
nav_order: 2
---

# Project Structure
{: .fs-9  }


Daily log is powered by Jekyll, which is a static site generator. Jekyll comes with a basic file structure. 
{: .fs-6 .fw-300 }

## Directory Structure
- Go to the project root directory, and run the following command on the terminal.

  ```bash
  # daily_log/
  tree -L 2
  ```

- A formatted directory structure will be printed out to the console. Note that Jekyll has a special feature that ignores underscore-started directories. All the blog posts are going to be inside the `_posts` directory.

  ```
  .
  ├── 404.md
  ├── Gemfile
  ├── Gemfile.lock
  ├── LICENSE
  ├── README.md
  ├── _authors
  ├── _config.yml
  ├── _data
  ├── _includes
  ├── _layouts
  ├── _months
  ├── _posts
  │   ├── 2020-01-01-how-daily-log-works.md
  │   ├── 2020-01-02-daily-practice.md
  │   ├── 2020-01-03-weekly-review-meeting.md
  │   └── 2020-01-05-test.md
  ├── _sass
  ├── _site
  ├── about.md
  ├── assets
  ├── authors.html
  ├── css
  ├── deploy.sh
  ├── feed.xml
  ├── index.html
  ├── js
  ├── s3_website.yml
  ├── script
  ├── search.md
  └── urban.gemspec
  ```
