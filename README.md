# Dave's Code Blog

A [Jekyll](https://jekyllrb.com/) blog published with **GitHub Pages** at
**https://normand1.github.io/DavesCodeBlog/**.

GitHub builds and deploys the site automatically — there is no build step to run
yourself. Just add Markdown and push.

## Adding a new post

1. Create a file in [`_posts/`](_posts/) named `YYYY-MM-DD-a-short-slug.markdown`
   (e.g. `2026-07-11-debugging-a-race-condition.markdown`).
2. Add front matter at the top, then write the body in Markdown:

   ```markdown
   ---
   layout: post
   title:  "Your Title Here"
   date:   2026-07-11 09:00:00 -0700
   categories: notes
   ---

   Your content...
   ```

3. Commit and push to the `master` branch. The post is live in a minute or two.

See [`_posts/2026-07-04-hello-world.markdown`](_posts/2026-07-04-hello-world.markdown)
for a fuller example.

## Previewing locally (optional)

The first time, install the toolchain (Ruby + Bundler required):

```bash
bundle install
```

On macOS, if `eventmachine` fails to compile with an OpenSSL error, point it at
Homebrew's OpenSSL first, then re-run `bundle install`:

```bash
bundle config set --local build.eventmachine "--with-openssl-dir=$(brew --prefix openssl@3)"
```

Then serve the site and open <http://localhost:4000/DavesCodeBlog/>:

```bash
bundle exec jekyll serve
```

The preview rebuilds automatically as you edit (except `_config.yml`, which
needs a server restart).

## Configuration

Site-wide settings (title, description, social links) live in
[`_config.yml`](_config.yml). To move the blog to the site root
(`https://normand1.github.io/`) or a custom domain, set `baseurl: ""` and update
`url` accordingly.
