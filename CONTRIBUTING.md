# Contributing

We welcome contributions! Please follow these guidelines.

## Development

Install dependencies:
```bash
npm install
```

Build the server:
```bash
npm run build
```

For development with auto-rebuild:
```bash
npm run watch
```

## Releasing

This project uses [standard-version](https://github.com/conventional-changelog/standard-version) combined with [Conventional Commits](https://www.conventionalcommits.org/) for automated versioning, changelog generation, and tagging.

To create a new release:

1.  Ensure your Git working directory is clean.
2.  Make sure your commit messages follow the Conventional Commits format (e.g., `feat: ...`, `fix: ...`, `BREAKING CHANGE: ...`).
3.  Run the release script:
    ```bash
    npm run release
    ```
    This will bump the version in `package.json`, update `CHANGELOG.md`, commit the changes, and create a Git tag.
4.  Push the commit and tag to the remote repository:
    ```bash
    git push --follow-tags origin main # Or your default branch
    ```
5.  (Optional) Publish the new version to npm:
    ```bash
    npm publish
    ```


## Debugging

Since MCP servers communicate over stdio, debugging can be challenging. We recommend using the [MCP Inspector](https://github.com/modelcontextprotocol/inspector), which is available as a package script:

```bash
npm run inspector
```

The Inspector will provide a URL to access debugging tools in your browser.