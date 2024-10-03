---
title: First Post
date: 2024-10-01 24:00:00 +0000
categories: [blog]
tags: [blog, website, hosting, mazepin]     # TAG names should always be lowercase
---

## Frist Post

# Migrating mazepin.ch from Static HTML/CSS to Jekyll on GitHub Pages

## Introduction

For years, mazepin.ch was built on a foundation of static HTML and CSS files. It worked well for simple tasks, but as the site grew and I wanted to introduce more features, manage content easily, and improve scalability, it became clear that a more modern solution was needed.

In this post, I’ll walk through my journey migrating mazepin.ch to Jekyll, a static site generator, hosted on GitHub Pages. This transition not only simplified the management of the website but also improved performance and workflow efficiency.

## The Old Setup: Static HTML & CSS

Before the migration, mazepin.ch consisted of a handful of HTML and CSS files. It was simple, but every change required manual updates across multiple files, and there was no easy way to introduce dynamic content or layouts.

Here’s how the website looked in its early years:
 
<img src="/assets/img/01/mazepin.ch_2022.png" alt="old Version" width="250">

## Why Jekyll and GitHub Pages?

After researching various options, Jekyll stood out due to its simplicity and seamless integration with GitHub Pages. Here are a few reasons why I chose Jekyll:

- **Markdown Support:** Writing blog posts and content in Markdown is significantly faster than in HTML.
- **Version Control with GitHub:** GitHub Pages allows automatic deployment from a repository, which means I can push changes quickly and easily.
- **Themes & Layouts:** Jekyll’s support for layouts and templates makes managing consistent designs across pages effortless.
- **No Server Management:** With GitHub Pages, there’s no need to worry about server maintenance or hosting fees.

This transition greatly improved how I manage and update content.

## The Migration Process

1. **Setting Up Jekyll:** 
   I started by installing Jekyll and setting up a basic site structure. Jekyll’s folder structure was easy to understand, with `_posts`, `_layouts`, and `_includes` directories for organizing content and templates.

2. **Converting Static Files:** 
   All the old static HTML files were converted into Jekyll templates and layouts. Content that was previously hardcoded into individual HTML files was now transformed into modular, reusable components.

3. **Hosting on GitHub Pages:** 
   Finally, I hosted the site on GitHub Pages by creating a new repository, pushing the code, and configuring GitHub to serve the site from the `gh-pages` branch.

The new setup looks cleaner and allows for faster updates:

## Challenges Faced

During the migration, there were a few challenges I encountered:

- **Learning Curve:** Jekyll has a learning curve, especially when dealing with Liquid templates, but once I got the hang of it, everything became more intuitive.
- **URL Structure:** Migrating the existing URLs to match Jekyll’s structure required some tweaks to ensure SEO rankings and old links didn’t break.

## The Final Result

With the migration complete, mazepin.ch is now fully powered by Jekyll and hosted on GitHub Pages. The site is faster, easier to update, and more flexible for future content additions.

<img src="/assets/img/01/SCR-20241003-segj(1).png" alt="new Version" width="250">

## Conclusion

Migrating from static HTML and CSS to Jekyll and GitHub Pages has been a game-changer for mazepin.ch. It has reduced the time I spend managing content, and the integration with GitHub Pages has simplified deployment. 

If you're maintaining a static site and looking for a modern solution, Jekyll and GitHub Pages are worth considering.

Stay tuned for more updates!

---

*Want to know more about the tools I used or have questions? Feel free to reach out at [noah@mazepin.ch](mailto:noah@mazepin.ch).*

