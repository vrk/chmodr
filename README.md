# chmodr

Source code for [https://chmodr.dev/](https://chmodr.dev/).

Created from the [eleventy-base-blog](https://github.com/11ty/eleventy-base-blog) template.

## Build & run locally

### 1. Clone this Repository

```
git clone git@github.com:vrk/chmodr.git
```

### 2. Navigate to the directory

```
cd chmodr
```

### 3. Install dependencies

```
npm install
```

### 4. Run Eleventy

```
npm start
```

## Add new posts

- `posts/` has the blog posts. Add a new file in this directory to create a new post. Follow the existing files as an example of what frontmatter to include.
- Posts and other content in this repository are typically written in [Markdown](https://www.markdownguide.org/), but they can be any template format (blog posts needn’t be markdown, for example). Configure the supported templates in `.eleventy.js` -> `templateFormats`.
- Use the `eleventyNavigation` key in your front matter to add a template to the top level site navigation. For example, this is in use on `index.njk` and `about/index.md`.
- The `css` and `img` directories in the input directory will be copied to the output folder (via `addPassthroughCopy()` in the `.eleventy.js` file).
- The blog post feed template is in `feed/feed.njk`.
- This site uses three layouts:
  - `_includes/layouts/base.njk`: the top level HTML structure
  - `_includes/layouts/home.njk`: the home page template (wrapped into `base.njk`)
  - `_includes/layouts/post.njk`: the blog post template (wrapped into `base.njk`)
- `_includes/postlist.njk` is a Nunjucks include and is a reusable component used to display a list of all the posts. `index.njk` has an example of how to use it.

