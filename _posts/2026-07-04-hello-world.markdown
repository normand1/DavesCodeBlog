---
layout: post
title:  "Hello, World"
date:   2026-07-04 09:00:00 -0700
categories: meta
---

Welcome to the blog. This first post does double duty: it says hello, and it
shows you exactly how every future post gets published.

## How to add a new post

1. Create a file in the `_posts/` directory named
   `YYYY-MM-DD-a-short-slug.markdown` — for example
   `2026-07-11-debugging-a-race-condition.markdown`. The date and slug in the
   filename become part of the post's URL, so pick them deliberately.
2. Start the file with **front matter** — the block fenced by `---` lines at
   the top of this very file. At minimum set `layout: post`, a `title`, and a
   `date`. `categories` is optional.
3. Write the body in Markdown below the front matter.
4. Commit and push to the `master` branch. GitHub Pages rebuilds the site
   automatically, and the post is live in a minute or two. That's the whole
   workflow — no build step to run yourself.

## Previewing locally (optional)

If you want to see changes before pushing, run the local server:

```bash
bundle exec jekyll serve
```

Then open <http://localhost:4000/DavesCodeBlog/>. The server rebuilds on every
save, so you get a live preview as you write.

## Markdown, including code

Standard Markdown works — **bold**, _italics_, [links](https://github.com/normand1),
lists, blockquotes, and fenced code blocks with syntax highlighting:

```ruby
def greet(name)
  puts "Hi, #{name}!"
end

greet("world")
```

That's it. Delete this post whenever you like — it's just here to get you
started.
