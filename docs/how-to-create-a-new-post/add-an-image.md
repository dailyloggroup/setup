---
layout: default
title: Add an image
parent: How to create a new post
nav_order: 1
---

# Add an image

Make your content more exciting with images? Here's how.
{: .fs-6 .fw-300 }

## Source image files
- Add image file(s) under `assets/img` directory.

  ```
  tree -L 2 assets/img/
  
  assets/img/
  ├── test1.jpg
  ├── test2.jpg
  ```


## Update the post

- Add a new variable called `images` to the frontmatter of the post. You can add more than one image to the current post. In the example below, two images have been added.

  ```yaml
    layout: post
    title: "My new post"
    date: 2020-11-30 09:20 +0900
    module: 2021-01
    author:
    images:
      - url: test1.jpg
        alt: test 1
        title: test 1
      - url: test2.jpg
        alt: test 2
        title: test 2
  ```

- Assign the first image to a new variable, i.e., `image`. Then in the post body, add an `include` tag, denoted by curly braces and percent signs: {-% and %}, with the pre-formatted `post_image.html` page. Details regarding the image tag, including the boostrap modal that pops up upon clicking an image, have been abstracted out in a separate file as a template. It is stored under `_includes` folder.

  ```
  {% raw %}
    {% assign image = page.images[0] %}
    {% include post_image.html image=image %}
  {% endraw %}
  ```

- In the current project, `jekyll_picture_tag` gem is used to accommodate various image size that fit the given screen size. The below line also works to add an image to the post; however, the image may not be responsive to multiple screen sizes.

  ```md
    ![My image Name](/assets/images/test.jpg)
  ```


- Refer to this page for more information about [Liquid tags](https://shopify.github.io/liquid/basics/introduction/).