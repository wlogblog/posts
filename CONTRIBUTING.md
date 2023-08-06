
# Post Submissions

All posts are stored in `/submissions`; so to contribute a new post, just create a new `.md` file (reference an existing post if it helps) and PR this repo.


- PRs should only contain the `.md` file that defines the post that you want to contribute.
- Your PR must pass the blog's `CI/CD` tests (which will automatically run when a PR is raised).
- All blog posts are written in [hugo](https://gohugo.io/)'s markdown convention. The simplest way to preview it is with a [live markdown testing tool](https://spec.commonmark.org/dingus/).  


## when will my post be visible on the site?

If your PR is merged into the `main` branch by `@the.editor`, it means that the submission is accepted and should be visible within at most 24 hours.


# Local Rendering

If you want to see how your post would look on the site; you can locally render a simplified copy of the site with `hugo` inside of the `.pr_tests` directory.

### 1.make sure you have [hugo](https://gohugo.io/) installed

```bash 
brew install hugo
```

### 2. initialise the hugo theme `PaperMod`
make sure you are in the root of repo
```bash
git clone https://github.com/adityatelange/hugo-PaperMod .pr_tests/themes/PaperMod --depth=1 --branch v7.0
```

### 3. initialise the existing content contained within `./submissions` directory
```bash
cp -r submissions .pr_tests/content/posts
```
If your new post is already in "submissions" directory, it will show up as well.

### 4. serve the site locally

```bash
hugo server
```

Navigate to http://localhost:1313 in any browser.


## More Info about `hugo`
https://gohugo.io/getting-started/quick-start/