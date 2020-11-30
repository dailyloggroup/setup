---
layout: default
title: Add a carousel
parent: How to create a new post
nav_order: 2
---

# Add a carousel

Want to display multiple images in one frame? Add a slideshow for cycling through a series of content, with the support for previous/next buttons and indicators showing image captions.
{: .fs-6 .fw-300 }

## Source image files
- Add image file(s) under `assets/img` directory.

  ```
  tree -L 2 assets/img/
  
  assets/img/
  ├── test1.jpg
  ├── test2.jpg
  ```

- Add a new yaml file (i.e., `carousel.yml`) under `_data` directory in the following format:

  ```yaml
  # _data/carousel.yml
  - title: "An image"
    caption: "Test 1"
    url: "test1.jpg"

  - title: "Another image"
    caption: "Test 2"
    url: "test2.jpg"
  ```

## Update the post

- Adding a carousel is slightly different than adding an image to the post. Add an include tag with `carousel.html` page, followed by `name` and `data` key-value pairs. Note that there are no commas in between.

- The `name` key must be given, as it is used to identify the boostrap carousel element; otherwise, it won't work. The `data` variable refers to the `carousel.yml` file created in the previous step.

  ```md
  {% raw %}
    {% include carousel.html name="Example" data=site.data.carousel %}
  {% endraw %}
  ```

- If you want to add more than one carousel element to the post, you can simply add another include tag, with a different name and a new yaml file containing a series of images.