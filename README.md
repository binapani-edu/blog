# Blog

repo for Binapani blog posts

## Contribution Guidelines

### Getting Started

1. **Fork the repository**: Create your own copy of the repo to work on.
2. **Clone the repository**: Clone your fork to your local machine.
3. **Create a branch**: Create a new branch for your contribution.

### Writing Blog Posts

1. **Format**: Write posts in Markdown format.
2. **Structure**: Include a title, date, author, and tags at the top of your post.
3. **Images**: Store images in the `assets` folder and reference them with relative paths.
4. **Code snippets**: Use proper Markdown code blocks with language specification.

### Blog Configuration (REQUIRED)

All blog posts **must** be registered in the `_blog.yml` file to be displayed on the website.
Your PR might be rejected if this step is missing.

1. **Add your blog entry** at the end of the `_blog.yml` file with the following fields:
   ```yaml
   - slug: your-blog-slug
     title: Your Blog Title
     thumbnail: /blogs/your-blog-slug/assets/thumbnail.jpg
     description: "A brief description of your blog post"
     authors:
       - name: yourgithubusername
         profile: https://github.com/yourgithubusername
         avatar: https://avatars.githubusercontent.com/u/youruserid?v=4
     created: Month DD, YYYY
     updated: Month DD, YYYY
     tags:
       - relevant-tag
       - another-tag
   ```

2. **Field explanations**:
   - `slug`: Unique identifier for your blog post (use kebab-case, lowercase with hyphens)
   - `title`: Display title of your blog post
   - `thumbnail`: Path to the featured image (must be placed in your blog's assets folder)
   - `description`: Brief summary of your post (recommended: 150-200 characters)
   - `authors`: List of contributors (include GitHub username, profile URL, and avatar URL)
   - `created`: Original publication date
   - `updated`: Last modification date (same as created for new blog, different for PRs editing an existing blog)
   - `tags`: Relevant categories for your post (helps with discoverability)

3. **Example structure**:
   ```
   /blogs/your-blog-slug/
     content.md
     /assets/
       thumbnail.jpg
       other-images.png
   ```

### Submitting Changes

1. **Commit your changes**: Make meaningful commit messages.
2. **Push to your fork**: Upload your changes to your GitHub repository.
3. **Submit a Pull Request**: Create a PR against the main repository.
4. **Code review**: Wait for a review from the maintainers.

### Style Guide

- Use clear, concise language
- Include relevant images and diagrams where helpful
- Properly format code examples
- Ensure proper citation for any external resources

### Need Help?

If you have questions or need assistance, please open an issue with the "question" label.

Thank you for contributing to the Binapani blog!
