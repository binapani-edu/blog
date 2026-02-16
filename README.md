# Blog

repo for [Binapani blog posts](https://binapani.com/blog)

## Contribution Guidelines

### Getting Started

1. **Fork the repository**: Create your own copy of the repo to work on.
2. **Clone the repository**: Clone your fork to your local machine.
3. **Create a branch**: Create a branch with the format `YourName/BlogTitle` (e.g., `john/my-awesome-blog`).

### Blog Structure

1. **Create a folder**: Create a folder for your blog post with the format `/blogs/your-blog-slug/`.
   - Use short, descriptive slugs in kebab-case (lowercase with hyphens)
   - This slug will become part of the blog's URL on the website (so keep it short, unique and descriptive)

2. **Add content file**: Create a `content.md` file inside your blog folder.

3. **Add assets**: Create an `/assets/` subfolder for all images.

4. **Final structure**: Your blog folder should look something like this:
   ```
   /blogs/your-blog-slug/
     content.md
     /assets/
       thumbnail.jpg
       other-images.png
   ```

### Writing Blog Posts

1. **Format**: Write posts in Markdown format.

2. **Blog Header**: Start your `content.md` with a descriptive title:
   ```markdown
   # Your Blog Title

   Your content here...
   ```

3. **Images**: 
   - Store all images in the `assets` folder 
   - Reference them with relative paths: `![Alt text](./assets/image.jpg)`
   - **Optimize your images** before adding them to keep the repository lightweight:
     - Use compression tools like [TinyPNG](https://tinypng.com/) or [ILoveIMG](https://www.iloveimg.com/compress-image)
     - Aim for a maximum file size of 300KB per image when possible
     - Create thumbnails with dimensions 1200x630 (1.91:1 ratio, the [Open Graph standard](https://ogp.me/) for best social media previews)
     - Supported thumbnail formats: JPG and PNG
     - Keep thumbnail file size **under 600KB** for overall best link preview compatibility

4. **Code snippets**: Use proper Markdown code blocks with language specification:
   
   To create a code block with syntax highlighting,
   use three backticks followed by the language name, then your code, and close with three backticks:

   <pre>
   ```python
   def example():
       return "Hello World"
   ```
   </pre>

   This will render as:

   ```python
   def example():
       return "Hello World"
   ```

5. **Captioning Figures**: You can add captions to images using HTML or tables:
   ```markdown
   | ![Description](./assets/image.jpg) |
   |:--:|
   | *Figure 1: Description of the figure* |
   ```

6. **LaTeX Support**: For mathematical formulas, use LaTeX notation:
   ```markdown
   \\( E = mc^2 \\)
   ```

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

### Important Disclaimer for Contributors

**✋ Please Note:** When submitting a PR, ensure you had only modified:

1. Files within your own blog slug folder (`/blogs/your-blog-slug/*`)
2. The specific section in `_blog.yml` that corresponds to your blog

For **new blog posts**, add your entry at the **end** of the `_blog.yml` file unless specifically instructed otherwise by maintainers.

For **existing blog edits**, only modify the specific `_blog.yml` entry for your blog slug.

PRs that modify other blogs' content or unrelated parts of the configuration may be rejected.

### Submitting Changes

1. **Commit your changes**: Make meaningful commit messages that describe your changes. (use [conventional commits](https://www.conventionalcommits.org/en/v1.0.0/))
2. **Push to your fork**: Upload your changes to your GitHub repository.
3. **Submit a Pull Request**: Create a PR against the main repository with the title format "`[new blog] Your Blog Title`". (or "`[edit blog] Your Blog Title`" for PRs editing an existing blog)
4. **PR Description**: In your PR description, include:
   - A brief summary of your blog post
   - A checklist confirming you've:
     - [ ] Added your blog post content
     - [ ] Optimized all images
     - [ ] Updated the `_blog.yml` file
5. **Code review**: Wait for a review from the maintainers.

### Style Guide

- Use clear, concise language
- Include relevant images and diagrams where helpful
- Properly format code examples with syntax highlighting
- Ensure proper citation for any external resources
- Break up long paragraphs for better readability
- Use headers to organize your content logically

### Need Help?

If you have questions or need assistance, please open an issue with the "question" label.

Thank you for contributing to the Binapani blog!

## 

On successful submission of your blog post, your blog post/article will be published on the website: [https://binapani.com/blog](https://binapani.com/blog).
