## @changesets/cli Github action.

### Standard public package template.

#### @see [Publish](https://github.com/9a8ri3L/changeset-tests/blob/main/.github/workflows/publish.yml)

- Make sure that the [NPM_TOKEN](https://docs.npmjs.com/creating-and-viewing-access-tokens) is not expired.
- Make sure that "Allow GitHub Actions to create and approve pull requests" is checked.
- Make sure that [package.json](https://github.com/9a8ri3L/changeset-tests/blob/main/package.json) file has `"publishConfig": {
  "access": "public"
}`, and remove `"private": "false"` if present.
- Make sure that [.changeset/config.json](https://github.com/9a8ri3L/changeset-tests/blob/main/.changeset/config.json) file has `"access": "public"`
- Make sure that the installed version of your package manager is the same in [.github/workflows YML files](https://github.com/9a8ri3L/changeset-tests/tree/main/.github/workflows) with the used version in your local.
- Run `pnpm changeset` every time you need to update your package version, before commiting and pushing to Github repository and [changesets/action](https://github.com/changesets/action) will handle version.
- Every PR is opened by `Chengesets release Github action` will create a head branch `changeset-release/main`, which can be deleted automatically after merge by activate "Automatically delete head branches" in the repo general settings.
- Every mergrd PR has been opened by `Changesets release Github action` will create a tag/release/publish to [NPM registry](https://www.npmjs.com/)

@see [changeset-tests NPM package](https://www.npmjs.com/package/@g-tests/changeset-tests)

That's a standard configuration.
For more information, visit [Changesets](https://github.com/changesets/changesets)
