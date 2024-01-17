# jekyll-v4-build-pages

A simple GitHub Action for producing Jekyll build artifacts compatible with GitHub Pages.

**This action is not the official action used for GitHub Pages.** This is a fork of the original `jekyll-build-pages` that I have modified to support Jekyll v4. This action will work mostly the same as the original, with the main difference being it will build a Jekyll site with Jekyll v4.x. To see a list of the dependencies that this action uses, checkout out [georgeh2os.com/pages-gem/versions](https://www.georgeh2os.com/pages-gem/versions/).

While you could use this action directly to build a Jekyll site with GitHub Actions, it would be easier to use [jekyll-v4-gh-pages](https://github.com/dunkmann00/jekyll-v4-gh-pages) if you are looking to build **and** deploy a Jekyll site with GitHub Actions.

# Scope

This is used along with [`actions/deploy-pages`](https://github.com/actions/deploy-pages) as part of the official support for building Pages with Actions (currently in public beta for public repositories).

# Usage

See [action.yml](action.yml)

# Release instructions

In order to release a new version of this Action:

1. Locate the semantic version of the [upcoming release][release-list] (a draft is maintained by the [`draft-release` workflow][draft-release]).

2. Prepare a pull request to update [`action.yml`][action.yml] to reference the incoming version

3. Publish the draft release from the `main` branch with semantic version as the tag name, _with_ the checkbox to publish to the GitHub Marketplace checked. :ballot_box_with_check:

4. After publishing the release, the [`release` workflow][release] will automatically run to create/update the corresponding the major version tag such as `v1`.

   ⚠️ Environment approval is required. Check the [Release workflow run list][release-workflow-runs].

## License

The scripts and documentation in this project are released under the [MIT License](LICENSE).

<!-- references -->
[release-list]: https://github.com/dunkmann00/jekyll-v4-build-pages/releases
[draft-release]: .github/workflows/release.yml
[release]: .github/workflows/release.yml
[release-workflow-runs]: https://github.com/dunkmann00/jekyll-v4-build-pages/actions/workflows/release.yml
[action.yml]: https://github.com/dunkmann00/jekyll-v4-build-pages/blob/649f5d3c2b2462620c8945f034200e431ceddd29/action.yml#LL31C55-L31C61
