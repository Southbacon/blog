# Southbacon Blog!

## Creating new Blog Entries
1. Create a new branch with the title of your new entry.
2. Create your new entry inside of the `src/pages/` directory. (New name of post should probably be formatted like this: `YYYY-MM-DD-post-title`.)
3. At the top of the entry, use the following metadata template:
```
---
title: Hello World
date: "2018-06-29T13:12:03.284Z"
author: your-username
---
```
4. Write and commit your entry.
5. Create a new pull request against the master branch.

Once 2 other people in the community have reviewed your entry, it will be merged in and then someone who has permission to publish the new entry to the gh-pages branch can then build and deploy the new entry.

## Developing locally and to review how your new blog entry looks on the rendered site:
1. Clone this repository, cd into the new site directory and and run `npm install`.
2. Run `gatsby develop` or `npm run develop`.
