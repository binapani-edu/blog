# Writing Blogs for Binapani: A Complete Guide

## Introduction

Welcome! This guide will help you create and share blog posts for Binapani.
If you're new to blogging or Git, don't worry! just follow these steps.

On successful submission, your blog or article will be published on the Binapani website > [Blogs page](https://binapani.com/blog).

## Getting Started

1. **Fork the Repository**: Make your own copy of the Binapani [blog repository](https://github.com/binapani-edu/blog) on GitHub.  
2. **Clone It Locally**: Clone your forked version so you can edit files on your computer.  
3. **Create a Branch**: Name it with your username and the blog title (format: `YourName/blog-title`). For example, `alice/my-first-blog`.

## Repository structure

> **Note:**
> - Firstly, decide a slug for your blog post.
> - It should be short, descriptive, unique and in kebab-case (lowercase with hyphens).
> - It should be representative of the content of your blog post.
> - This is important because it will be used to identify your blog post in the repository, it will also be the folder name of your blog post and this becomes the unique url of your blog post.

To create a new blog post or article, you need to adhere to the following folder structure in the blog repository:

- **Blog Folder**: In the `/blogs/` directory, make a new folder named after your blog topic. It should be same as the slug you decided earlier.
- **content.md**: Add this file inside your slug folder to hold your writing.  
- **Assets**: Create an `/assets/` subfolder for any images or diagrams you plan to include in your blog.

Note: Your blog folder should look like this:
```shell
/
├── README.md
├── _blog.yml
└── blogs/
    └── your-blog-slug/
        ├── content.md
        └── assets/
            ├── thumbnail.jpg
            ├── other-images.png
            └── other-diagrams.svg
```


## Writing Blog Posts
- **Markdown Format**: Keep your text clear and easy to read.  
- **Images**: Store images in your `assets` folder and reference them with relative paths like `![alt text](./assets/image.jpg)`.  
- **Code Snippets**: Use fenced code blocks with a specified language. example:
   <pre>
   ```python
   def example():
       return "Hello World"
   ```
   </pre>
- **Figure Captions**: Use tables or HTML for captions, if needed.  

## Blog Configuration
Don't forget to register your post in `_blog.yml`. Include details like `slug`, `title`, `description`, and `authors` so your blog will appear correctly on the website.

## Submitting Changes
1. **Commit**: Write clear commit messages.  
2. **Push**: Send your changes to GitHub.  
3. **Open a Pull Request**: Describe your blog and confirm you've followed all guidelines (including optimized images and `_blog.yml` updates).

## Conclusion
Writing a Binapani blog post is simple once you know the basics. Following this guide ensures your blog is clear, organized, and ready to share.

## Need Help?
Open an issue with the "question" label if you have any problems or need guidance.
