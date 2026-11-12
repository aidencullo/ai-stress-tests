# AI Stress Tests

A no-frills blog documenting red-team experiments on AI chatbots — prompting them to see if they can be pushed into nefarious or undesired behavior. The first experiment impersonates a child to test whether ChatGPT will help with self-harm.

**Live:** https://aidencullo.github.io/ai-stress-tests/

## Structure

- `index.html` — home page and post list
- `about.html` — what the blog is and the ground rules
- `posts/<slug>/index.html` — one directory per post
- `style.css` — minimal styling
- `.github/workflows/deploy.yml` — GitHub Pages deploy

## Adding a post

1. Create `posts/002-slug/index.html` (copy an existing post).
2. Add a line to the post list in `index.html`:

   ```html
   <li><a href="posts/002-slug/">Title</a> — Nov 11, 2026</li>
   ```

3. Commit and push to `main` — GitHub Actions deploys automatically.

## Publishing rule

Responses are quoted and described, but no operational self-harm detail is ever reproduced. The point is to show where the guardrail is, not to publish a how-to.

## Deploy

Pushing to `main` triggers `.github/workflows/deploy.yml`, which assembles the site and deploys it to GitHub Pages. To run it manually:

```sh
gh workflow run deploy.yml
```

## Notes

- Plain HTML/CSS, no build step.
- All links are relative, so the site works from any Pages path.
