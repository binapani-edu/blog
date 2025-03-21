# Writing Blogs for Binapani: A Complete Guide

## Introduction

Hello there, fellow writer! 👋

Welcome to the comprehensive guide for creating and sharing blog posts for Binapani. Whether you're a seasoned blogger or completely new to writing technical content, this guide will walk you through every step of the process with plenty of helpful tips along the way.

Don't worry if you're unfamiliar with Git or Markdown - we've got you covered!
By following these steps, you will easily convert your brilliant ideas into a blog post or an article, and it will be published on the [Binapani Blogs page](https://binapani.com/blog) for the community to enjoy and learn from.

## Getting Started

Let's begin with the basics of setting up your writing environment:

1. **Fork the Repository**: Think of this as making your personal copy of the Binapani [blog repository](https://github.com/binapani-edu/blog) on GitHub. This gives you a safe space to experiment without affecting the original repository.
  
2. **Clone It Locally**: Bring your forked repository to your computer so you can work on it comfortably with your favorite editor. This step allows you to make changes offline.
  
3. **Create a Branch**: Give your writing space a name that follows the format `YourName/blog-title` (for example, `alice/my-first-blog`). This helps keep everything organized and makes it clear who's working on what.

## Choosing Your Blog Slug

> **Friendly Tip:**
> The "slug" is essentially the URL-friendly identifier for your blog post - it's more important than it might seem at first!

Before diving into writing, take a moment to think about your blog's slug. This should be:
- **Short and sweet**: Keep it concise for easier sharing
- **Descriptive**: Give readers a hint about your content
- **Unique**: Make sure it hasn't been used before
- **Kebab-cased**: Use lowercase-with-hyphens format (like `my-awesome-blog-post`)

Why does this matter? Your slug will:
- Become the folder name for your blog post
- Form part of the URL when published (e.g. binapani.com/blog/your-blog-slug)
- Help with search engine optimization
- Make your content easier to find and share

Choose wisely - a good slug is both informative and memorable!

## Repository Structure

Now let's set up your blog's home within the repository:

- **Blog Folder**: Create a new folder inside the `/blogs/` directory named after the slug you just brainstormed.

- **Content File**: Inside your new folder, create a `content.md` file. This is where all your brilliant writing will live!

- **Asset Management**: Create an `/assets/` subfolder to store all your images, diagrams, gifs or any other visual elements that will make your blog shine.

Your blog's structure should look something like this:
```shell
/
├── README.md
├── _blog.yml
└── blogs/
    └── your-blog-slug/
        ├── content.md
        └── assets/
            ├── thumbnail.jpg
            ├── helpful-diagram.svg
            └── other-images.png
```

## Crafting Your Blog Post

### Writing Style

Remember, you're writing for humans! Keep your content:
- **Clear and conversational**: Write as if you're explaining to a friend
- **Well-structured**: Use headers to organize your thoughts logically
- **Engaging**: Break up long paragraphs and vary sentence length
- **Accessible**: Explain complex concepts simply without talking down to your readers

### Markdown Essentials

Markdown makes formatting easy while keeping your content clean:

- **Headers**: Use `#` for titles, `##` for sections, and `###` for subsections
- **Emphasis**: Use *italics* with `*asterisks*` or **bold** with `**double asterisks**`
- **Lists**: Create bulleted lists with `-` or numbered lists with `1.`, `2.`, etc.
- **Links**: Format links as `[link text](https://example.com)`
- For more details on markdown, you can refer to the [Markdown Guide](https://www.markdownguide.org/)

### Working with Images

Images can transform your blog from good to great:

- **Store all images** in your `assets` folder to keep everything organized
- **Reference them** using relative paths: `![Alt text describing the image](./assets/image.jpg)`
- **Optimize before uploading** to keep the repository lightweight:
  - Use tools like [TinyPNG](https://tinypng.com/) or [ILoveIMG](https://www.iloveimg.com/compress-image)
  - Aim for a maximum file size of 300KB per image when possible
  - Create thumbnails with consistent dimensions (1300x650, or roughly 20:9 ratio is recommended)

- **Add helpful captions** to provide context for your images:
  ```markdown
  | ![Diagram showing the workflow](./assets/workflow.jpg) |
  |:--:|
  | *Figure 1: Step-by-step workflow for implementing the technique* |
  ```

### Code Snippets

For tutorials or technical blogs, proper code formatting is crucial:

Use three backticks followed by the language name to enable syntax highlighting:

<pre>
```python
def greet_reader():
    return "Thank you for reading my Binapani blog post!"
```
</pre>
This makes your code more readable and professional-looking.

### LaTeX for Mathematical Formulas

Teaching a concept that requires math? Binapani supports LaTeX notation:

```markdown
\\( E = mc^2 \\)
```

This renders as a beautifully formatted equation on the published blog.
For more details on writing LaTeX in Markdown, you can refer to the [GitHub LaTeX Guide](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions).

### Citations and References

It's always a good practice to cite your sources at the end of your blog post. This helps in providing the original source of the information, helps improve the credibility, and also gives the reader a way to explore more.

There are various ways to add citations to your blog post.
You can look up the best practices for your preferred citation style.

## Registering Your Blog in _blog.yml

This step is **absolutely crucial** - your blog won't appear on the website without it!

Add your blog's information to the `_blog.yml` file with these details:

```yaml
- slug: your-blog-slug
  title: Your Compelling Blog Title
  thumbnail: /blogs/your-blog-slug/assets/thumbnail.jpg
  description: "A concise, enticing description that makes readers want to click (aim for 150-200 characters)"
  authors:
    - name: full name or username
      profile: https://github.com/yourgithubusername
      avatar: https://avatars.githubusercontent.com/u/youruserid?v=4
  created: Month DD, YYYY
  updated: Month DD, YYYY
  tags:
    - relevant-tag
    - another-tag
```

Here are the detailed explanations for the fields:

- `slug`: Unique identifier for your blog post (use kebab-case, lowercase with hyphens)
- `title`: Display title of your blog post
- `thumbnail`: Path to the featured image (must be placed in your blog's assets folder)
- `description`: Brief summary of your post (recommended: 150-200 characters)
- `authors`: List of contributors (include name or username, GitHub or any other profile URL, and avatar URL)
- `created`: Original publication date
- `updated`: Last modification date (same as created for new blog, different for PRs editing an existing blog)
- `tags`: Relevant categories for your post (helps with discoverability)

This information helps categorize your blog, makes it discoverable, and provides attribution for your hard work.

## Submitting Your Masterpiece

Ready to share your knowledge with the world? Here's how:

1. **Commit Your Changes**: Write meaningful commit messages that explain what you've done. If possible, follow [conventional commits](https://www.conventionalcommits.org/en/v1.0.0/) format (like `feat: add new blog on machine learning basics`).

2. **Push to Your Fork**: Send your local changes to your GitHub repository.

3. **Open a Pull Request (PR)**: Submit your work to the main Binapani repository with a title like "`[new blog] Your Blog Title`" or "`[edit blog] Your Blog Title`" for PRs editing an existing blog.

4. **Describe Your Contribution**: In your PR description, include:
   - A brief summary of what readers will learn from your blog
   - A checklist confirming you've:
     - [ ] Added your complete blog content
     - [ ] Optimized all images for web
     - [ ] Updated the `_blog.yml` file properly
     - [ ] Reviewed for spelling and grammar

5. **Review Process**: The Binapani team will review your submission, possibly suggesting edits or improvements. Don't be discouraged by feedback - it's all part of creating the best possible content!

## Final Polish

Before submitting, consider these quality checks:

- **Read aloud**: Does your writing flow naturally?
- **Check images**: Are they informative and properly formatted?
- **Verify links**: Make sure all links work correctly
- **Test code**: If you included code snippets, double-check they run as expected
- **Get feedback**: Consider asking a friend to review your post and re-ask your co-authors to review it.

## Conclusion

Congratulations! By following this guide, you're well on your way to sharing your knowledge and insights with the world!
Remember, the best blogs combine technical accuracy with engaging, human writing and creativity - don't be afraid to let your personality shine through!

Writing and publishing your first blog might seem daunting, but we're here to support you every step of the way. Once approved, you'll see your creation live at [https://binapani.com/blog](https://binapani.com/blog), ready to help and inspire readers worldwide.

## Need a Helping Hand?

Stuck on something? Have questions? The Binapani community is friendly and helpful!
Simply open an issue in the repository with the "question" label, and someone will be happy to guide you. Happy writing!
