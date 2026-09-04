---
layout: post
title: "How I Made This Blog with Jekyll"
date: 2026-09-04 20:00:00 +0700
excerpt: "Why I started blogging and how I shipped this site with Jekyll, Tailwind, and GitHub Pages."
tags: [jekyll, blogging, personal]
---

Hi! Welcome to my blog. If you're reading this, it means I actually shipped it.

My first post here was just a markdown test — `Markdown Goes Brrrrr` — to make sure headings, code blocks, and tables render correctly. This is my first *real* post: why I made this blog and how.

<!-- break -->

## Why I wanted a blog

I love writing, so I wanted a personal space to talk about anything, from tech to personal life. No algorithm, no likes, just my own little corner on the internet.

I also wanted a place where I can write badly at first and get better over time.

## Why Jekyll?

I picked Jekyll because:

1. **It's just markdown.** I write in `_posts/`, push, and done.
2. **It's free.** Hosted on GitHub Pages with a custom domain.
3. **No database, no CMS.** Just static files I fully control.

My stack is pretty simple:

- `jekyll` for the site
- `jekyll-tailwindcss` for styling
- `jekyll-seo-tag` and `jekyll-paginate` for SEO and pagination

## How I built it in an afternoon

1. Created a new Jekyll site and added the Gemfile dependencies:

```bash
bundle install
bundle exec jekyll serve
```

2. Set up `_config.yml` with my title, pagination, and permalinks:

```yaml
title: cyrls's blog
paginate: 10
permalink: /:title/
show_excerpts: true
```

3. Made custom layouts in `_layouts/` — `default`, `home`, `post`, and `profile` for my about page.
4. Added posts in `_posts/` using the format `YYYY-MM-DD-title.md`.
5. Deployed to GitHub Pages and pointed my custom domain to it with a `CNAME` file:

```
blog.gemasatriatama.web.id
```

That was it. Visit, refresh, blog online.

## One problem I hit

Ruby dependencies. Classic.

My fix was boring but works: delete `Gemfile.lock`, run `bundle install` again, and make sure I'm using the same Ruby version locally and in GitHub Actions. If `jekyll serve` fails, 90% of the time it's a gem version issue.

## What's next?

Honestly, just writing more. I want to post about:

- my dev setup and tools I actually use
- small things I'm learning
- personal life stuff

No strict schedule. Just write when I have something to say.

Thanks for stopping by.

Love, Peace, and Gawl  
【=◈◡◈=】
