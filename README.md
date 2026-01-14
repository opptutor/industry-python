# Industry Python Blog

[Free Python Course](https://industry-python.thinkific.com/products/courses/industry-projects-with-python)

A Quarto-based blog for Industry Python content.

## Adding a New Blog Post

To add a new blog post, follow these steps:

### 1. Create a New Post Directory

Create a new directory in the `posts/` folder with a descriptive name (use kebab-case):

```bash
mkdir posts/your-post-name
```

### 2. Create the Post File

Create an `index.qmd` file in your new directory:

```bash
touch posts/your-post-name/index.qmd
```

### 3. Add Post Content

Open `posts/your-post-name/index.qmd` and add your content with the required YAML frontmatter:

```yaml
---
title: "Your Post Title"
author: "Your Name"
date: "YYYY-MM-DD"
categories: [category1, category2]
---

Your post content goes here. You can use:

- **Markdown** for formatting
- Code blocks for examples
- Images (see below)
- Any Quarto features
```

### 4. Add Images and Assets (Optional)

If your post includes images or other assets, place them in the same directory as your `index.qmd` file:

```
posts/your-post-name/
  ├── index.qmd
  ├── image1.png
  └── thumbnail.jpg
```

Reference images in your post using relative paths:

```markdown
![](image1.png)
```

### 5. Preview Locally

To preview your blog locally, run:

```bash
quarto preview
```

This will start a local server where you can view your blog and see your new post.

### 6. Build and Deploy

When you're ready to publish:

1. **Commit your changes:**

```bash
git add posts/your-post-name/
git commit -m "Add new post: Your Post Title"
```

2. **Push to GitHub:**

```bash
git push
```

3. **Automatic Deployment:**

The GitHub Action will automatically build and deploy your site to GitHub Pages. You can check the deployment status in the Actions tab of your GitHub repository.

## Post Frontmatter Options

The YAML frontmatter supports these fields:

- `title` (required): The title of your blog post
- `author` (required): The author's name
- `date` (required): Publication date in `YYYY-MM-DD` format
- `categories`: Array of category names (e.g., `[news, tutorial, python]`)

## Project Structure

```
industry-python-blog/
├── posts/
│   ├── _metadata.yml          # Settings applied to all posts
│   ├── welcome/
│   │   ├── index.qmd          # Post content
│   │   └── images/            # Post assets
│   └── your-post-name/
│       └── index.qmd
├── _quarto.yml                # Quarto configuration
├── index.qmd                  # Blog homepage
└── about.qmd                  # About page
```

## Development

### Local Development

1. Install Quarto: <https://quarto.org/docs/get-started/>

2. Preview the site:

```bash
quarto preview
```

3. Build the site:

```bash
quarto render
```

The built site will be in the `_site/` directory (ignored by git).

### GitHub Pages

The site is automatically built and deployed via GitHub Actions when you push to the `main` or `master` branch. The workflow:

1. Builds the Quarto site
2. Deploys it to GitHub Pages

No manual deployment needed!

## Resources

- [Quarto Documentation](https://quarto.org/)
- [Quarto Blog Format](https://quarto.org/docs/websites/website-blog.html)
