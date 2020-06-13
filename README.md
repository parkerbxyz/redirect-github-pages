# redirect-github-pages

This template repository allows you to quickly and easily redirect GitHub Pages sites when their repositories are renamed or transferred from one user or organization to another.

## Using this template

To create a redirect, you must first create a repository from this template:

1. Above the file list, click **Use this template**.
1. Use the **Owner** drop-down menu, and select the account you want to own the repository.
1. Name the repository `username.github.io`, where `username` is your username (or organization name) on GitHub.
1. Click **Create repository from template**.

## Creating a redirect

To create a redirect from one GitHub Pages URL to another:

1. Create a new markdown file with the same name as old Pages repository.

1. Add the following to the top of the new markdown file:

   ```markdown
   ---
   redirect_to: <redirect-url>
   ---
   ```

### Example

You renamed your Pages repository from `foo` to `bar` and need to redirect `username.github.io/foo` to `username.github.io/bar`.

Create a new markdown file named [`foo.md`](foo.md) with the following contents:

   ```markdown
   ---
   redirect_to: username.github.io/bar
   ---
   ```

## Running locally

Install dependencies and run the server locally:

```sh
script/server
```
