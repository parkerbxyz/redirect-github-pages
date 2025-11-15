# redirect-github-pages

This template repository allows you to quickly and easily redirect GitHub Pages sites when their repositories are renamed or transferred from one user or organization to another.

## Using this template

To create a redirect, you must first create a user or organization GitHub Pages site from this template:

1. Click [**Use this template**](https://github.com/parkerbxyz/redirect-github-pages/generate).
1. Use the **Owner** drop-down menu, and select the account you want to own the repository.
1. Name the repository `username.github.io`, where `username` is your username (or organization name) on GitHub.
1. Click **Create repository from template**.

## Creating a redirect

To create a redirect from one GitHub Pages URL to another:

1. Create a new markdown file with the same name as the old Pages repository you'd like to redirect _from_ (e.g., `foo.md`).

1. Add the following to the top of the new markdown file:

   ```markdown
   ---
   redirect_to: https://username.github.io/new-repo
   ---
   ```

   Replace `https://username.github.io/new-repo` with your new GitHub Pages site URL.

### Example

You renamed your Pages repository from `foo` to `bar` and need to redirect `username.github.io/foo` to `username.github.io/bar`.

From your account Pages site repository (`github.com/username/username.github.io`), create a new markdown file named `foo.md` and add the following to the top of the file:

   ```markdown
   ---
   redirect_to: https://username.github.io/bar
   ---
   ```

## How it works

- Uses the `jekyll-redirect-from` plugin (built into GitHub Pages).
- GitHub automatically builds Jekyll sites when you push.
- No Gemfile or local Ruby installation needed.
- Simple frontmatter syntax for easy configuration.
- Generates HTML meta refresh redirects with SEO-friendly canonical links.

## Running locally (optional)

If you want to test locally, you'll need Ruby and Bundler installed. Then run:

```sh
script/server
```

This will automatically create a Gemfile, install dependencies, and start the Jekyll server with live reload.

However, for this simple use case, you can just push to GitHub and let GitHub Pages build it automatically.
