# CI setup for Feed me up, Scotty!

You can fork this repository and edit `feeds.toml` to start generating your own
RSS feeds.

# Automatically generate feeds

## On GitHub

To automatically generate feeds twice a day on GitHub:

1. Fork this repository and edit `feeds.toml`.
2. Create a branch called `gh-pages`.
3. Visit the _Actions_ tab for your fork, then enable workflows for your fork.
4. Make sure the Publishing Source for your GitHub Pages site is set to the
   `gh-pages` branch.
   [Instructions here.](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)

GitHub Actions will then automatically run twice a day to check for updates,
and publish your feeds at `https://<username>.github.io/feeds/`.

## On GitLab

To automatically generate feeds on GitLab:

1. Fork this repository and edit `feeds.toml`.
2. [Create a new pipeline schedule](./-/pipeline_schedules/new) (CI/CD ˃
   Schedules).
3. Set it to your desired interval (e.g. `30 5,17 * * *` to run at 5:30 and
   17:30).
4. Hit "Save pipeline schedule".

GitLab CI/CD will then automatically run at your selected interval to check for
updates, and publish your feeds at `https://<username>.gitlab.io/feeds/`.
