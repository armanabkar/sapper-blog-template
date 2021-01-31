# Sapper Blog

A starter template for building markdown-powered blogs with [Sapper](https://github.com/sveltejs/sapper) and [Svelte](https://github.com/sveltejs/svelte).

### 👉 [Live Demo](https://armanabkar.ir/)

<h2 align="center">
  <img src="./screenshot.png" alt="sapper-blog" width="600px" />
  <br>
</h2>

## ✨ Getting started

```bash
git clone https://github.com/armanabkar/sapper-blog-template.git
cd sapper-blog-template
npm install # or yarn!
npm run dev
```

Open up [localhost:3000](http://localhost:3000) and start clicking around.

## Test
```bash
# Run all Cypress e2e tests
npm test
```

Consult [sapper.svelte.dev](https://sapper.svelte.dev) for help getting started.

## ⚡ Features

- [x] Responsive & Lightweight
- [x] Markdown-based Personal Blog 
- [x] Portfolio
- [x] Personal Projects Page
- [x] Pagination for blog and projects
- [x] Highly Customizable
- [x] Dark Mode (Still in Development)
- [x] Animations & Transition
- [ ] Contact Form

## 🖌 Styles

You can modify styles in static/global.css file:

```css
:root {
  --primary: #2196f3;
  --secondary: #3b3936;
  --grey: #aaa;
  --white: #fafafa;
}
```

## 🏗 Structure

The base structure of this template is the same as Sapper's [default template](https://github.com/sveltejs/sapper-template/). These are some of the new things you'll find here:

### src/routes/blog

This is the home of your blog. The most important files in here are:

- `_posts.js`: this module contains the logic for loading and parsing your markdown posts.
- `[slug].svelte`: this is the template of your blog post page.
- `index.svelte`: this is the template of your article list page.

### src/routes/blog/posts

This is where your markdown posts live in. All `.md` files in this directory are treated as blog posts and parsed automatically by the `_posts.js` module.

- The markdown file name becomes the post slug. For example `hello-world.md` becomes `http://localhost:3000/blog/hello-world`.
- Everything between the start of the post and the `<!-- more -->` tag becomes the article's "excerpt".
- Frontmatter properties supported are `title` and `date`.

### src/routes/projects

This is your projects page. You can add your projects info to Projects array in projects.js file:

```
export const Projects = [
  {
    name: "project_name",
    description: "project_description",
    imageUrl: "project_image_url",
    code: "project_source_code",
  },
]  
```

## 🐛 Bugs and feedback

Sapper is in early development, and may have the odd rough edge here and there. Please be vocal over on the [Sapper issue tracker](https://github.com/sveltejs/sapper/issues).
