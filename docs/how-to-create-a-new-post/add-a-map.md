---
layout: default
title: Add a map
parent: How to create a new post
nav_order: 3
---

# Add a map

Fancy adding a map to geography-heavy posts? Embed google maps with the help of jekyll-maps plugin.
{: .fs-6 .fw-300 }

## Update the post

- Add location information to your posts YAML front-matter, with the `location` variable:

  ```yaml
    layout: post
    title: "My new post"
    date: 2020-11-30 09:20 +0900
    module: 2021-01
    author:
    location:
      latitude: 37.558318
      longitude: 126.925889
  ```

- Then, simply add a map tag in the body of your post.

  ```md
  {% raw %}
    {% google_map %}
  {% endraw %}
  ```

- For more information about the map plugin, refer to the github [repo](https://github.com/ayastreb/jekyll-maps).