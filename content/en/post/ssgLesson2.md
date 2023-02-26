---
date: 2023-02-24
description: "Another lesson on Static Site Generators and Hugo"
featured_image: "http://localhost:1313/images/postBG8.jpg"
tags: ["webdev"]
title: "How did we make this site? pt 2"
disable_share: false
---

## What does a page look like?

A page is made up of a few different parts. The first part is the front matter. The comes the content

### What is the front matter?

The front matter is a set of key value pairs that define the page. The front matter is surrounded by `---` on the top and bottom. The front matter is written in [TOML](https://toml.io/en/). The front matter is used to define the page's title, description, featured image, tags, etc. An example of the front matter is shown below:

```toml
---
date: 2023-02-24
description: "A lesson on Static Site Generators and Hugo"
featured_image: "http://localhost:1313/images/postBG9.jpg"
tags: ["webdev"]
title: "How did we make this site? pt 1"
disable_share: false
---
```

### What is the content?

The content is the main body of the page. The content is written in [Markdown](https://www.markdownguide.org/). The content is what is displayed on the page. An example of some content is shown below:

```markdown
# Heading 1 (H1)

This is a paragraph. It can be as long as you want. It can also contain **bold** and *italics*.

## Heading 2 (H2)

This is another paragraph.

This is another paragraph under the same heading.

### Heading 3 (H3)

This is another paragraph under a different heading.

![Image](/images/postBG9.jpg "Image Title")
this is an image and its caption.

#### Heading 4 (H4)

This is a paragraph with a [link](https://www.google.com/).

This is a table:

| Header 1 | Header 2 | Header 3 |
| -------- | -------- | -------- |
| Row 1    | Row 1    | Row 1    |
| Row 2    | Row 2    | Row 2    |
| Row 3    | Row 3    | Row 3    |

##### Heading 5 (H5)

This is a paragraph with a list:

- Item 1
- Item 2
- Item 3

This is a paragraph with a numbered list:

1. Item 1
2. Item 2
3. Item 3

###### Heading 6 (H6)

This is a paragraph with a block quote:

> This is a block quote.

This is a paragraph with a horizontal rule:

--- 

```

### What would that markdown look like rendered?

Below is what the markdown above would look like rendered:

# Heading 1 (H1)

This is a paragraph. It can be as long as you want. It can also contain **bold** and *italics*.

## Heading 2 (H2)

This is another paragraph.

This is another paragraph under the same heading.

### Heading 3 (H3)

This is another paragraph under a different heading.

![Image](/images/postBG9.jpg "Image Title")
this is an image and its caption.

#### Heading 4 (H4)

This is a paragraph with a [link](https://www.google.com/).

This is a table:

| Header 1 | Header 2 | Header 3 |
| -------- | -------- | -------- |
| Row 1    | Row 1    | Row 1    |
| Row 2    | Row 2    | Row 2    |
| Row 3    | Row 3    | Row 3    |

##### Heading 5 (H5)

This is a paragraph with a list:

- Item 1
- Item 2
- Item 3

This is a paragraph with a numbered list:

1. Item 1
2. Item 2
3. Item 3

###### Heading 6 (H6)

This is a paragraph with a block quote:

> This is a block quote.

This is a paragraph with a horizontal rule:

--- 
