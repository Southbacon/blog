# Southbacon Blog!

[![Current Version](https://img.shields.io/badge/Southbacon%20Blog%20Version-0.0.0-brightgreen.svg?style=for-the-badge)](https://github.com/Southbacon/blog)

## Getting Up and Running
1. [Log into the official repository](https://github.com/Southbacon/blog), (repo), in GitHub and select the fork option towards the top right corner of the page.

2. Once forked, copy the `ssh` URL of your fork into your clipboard, (GitHub provides a button to the right of the ssh URL for our convenience).

3. In your preferred Terminal application, navigate to the folder in which you keep your applications/projects.

4. In that folder, clone your fork of the repo - this will be your `origin`:
  ```shell
  git clone git@github.com:<USERNAME>/blog.git
  ```
5. Move into that directory and check that your origin points to your fork of the project:
  ```shell
  cd blog
  git remote -v
  ```

6. Add a remote to reference `upstream` - this is the project's official repository:
  ```shell
  git remote add upstream git@github.com:Southbacon/blog.git
  ```
7. Install packages:
  ```shell
  npm install
  ```

8. Run `gatsby develop` or `npm run develop`.

9. #Profit


## Creating new Blog Entries
1. Keep conflicts at bay; before creating a new topic:
  ```shell
  git checkout master
  git fetch upstream
  git reset --hard upstream/master
  ```

2. Create a new branch with the title of your new entry:
  ```shell
  git checkout -b <TOPIC-BRANCH-NAME>
  ```

3. Create your new entry inside of the `src/pages/` directory.
  **New name of your post should be formatted like: `YYYY-MM-DD-post-title`.**

4. At the top of the entry, use the following metadata template:
  ```
  ---
  title: Hello World
  date: "2018-06-29T13:12:03.284Z"
  author: your-username
  ---
  ```

5. Write your awesome blog post.

6. Commit your entry like a baws.
  ```shell
  git add YYYY-MM-DD-post-title
  git commit -m "YYYY-MM-DD-post-title - This is mah stuffs, y0. FAWTH FLAW FO LYF!"
  ```

7. Create a new pull request against the main repository's master branch.

Once 2 other people in the community have reviewed your entry, it will be merged in and then someone who has permission to publish the new entry to the gh-pages branch can then build and deploy the new entry.
