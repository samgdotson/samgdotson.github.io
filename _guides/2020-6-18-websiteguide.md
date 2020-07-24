---
layout: post
title: How to Build a Website with GitHub Pages
---

### Step 0: Make a GitHub account

### Step 1: Create a new repository on GitHub

- Call it [username].github.io
- Initialize with ``README.md``

### Step 2: Choose a theme

Since this is a beginner tutorial, we can choose a simple theme supported
by GitHub pages. My go-to is ``cayman`` but you can pick any one you'd like.

![select-theme](../../assets/images/website-guide/select-a-theme.png)

Once you hit "Select Theme" GitHub will automatically create a ``_config.yml``
file and update your ``README.md``. To continue, hit "Commit Changes".

After a few minutes, GitHub will publish your website.


### (Optional) Building Your Website Locally

This is an optional step because you can preview Markdown files in
the GitHub file editor.

![preview1](../../assets/images/website-guide/preview-changes.png) | ![preview1](../../assets/images/website-guide/preview-changes2.png)

However, it can be beneficial to check the changes you're going to make before
publishing them. Check [here](../localbuild.html) for instructions
on how to build your website locally with ``jekyll``.


### Step 4: Create a Home page

You can do this from GitHub directly or from terminal. Here, I will show you
how to do it from GitHub.

- Navigate to your repository and select "Create New File"
- Add the following code:

```
---
layout: default
title: Home
---

# Hi my name is Sam

```

- Add a small commit message (e.g. "updates the home page")
- Select "commit changes"


### Step 5: Add other pages, like a CV or Resume!

- Create a new file, as in **Step 4**.
- Call it ``mynewpage.md``
- Add the header info

```markdown
---
layout: default
title: Home
---
```

- Add some information:

```markdown
### Personal Info

- Name: Sam Dotson
- Email: sgd2@illinois.edu

### About

I am a 400 foot tall purple platypus-bear with pink horns and silver wings.
```
- "Commit changes" to save

### Step 6: Add links between pages

- Navigate to your repository and open ``index.md``.
- Select "edit file".
- Add the line

``[Here's a link to my new page!](./mynewpage.html)``

- Commit changes
- Check your website in a few minutes to see the updates!

Note you probably want to add a link back to your main page! This is pretty
easy, just adjust the link code to your new page and add it to ``mynewpage.md``.


### That's All, Folks!

You now have the tools you need to make basic changes to your website.

There are some slightly more advanced things you can do with your website:
- [Add a fancier theme](../2020-6-19-fancythemes.md)
- Add a custom domain name to your website
